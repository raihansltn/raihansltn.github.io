---
title: Cryptography CTF - Power Prime
summary: Writeup for CTF in Cryptography
date: 2024-08-26
type: docs
tags:
  - Python
image:
  caption: 'Power Prime challenge as seen on COMPFEST 16 Hacker Class'
---
Back with me, with another Cryptography challenge on CTF. This time, we'll be figuring out a simple challenge of RSA Algorithm. We will talk a little about the challenge, algorithm used to encrypt and decrypt the message, and detail about how I obtained the flag. Without further ado, lettuce begin 🥬.

So, to begin with, hacker class is an initial series of CTF competition event by COMPFEST, this one challenge (Power Prime), is a part of the second wave of this hacker class series. It's classified as a Cryptography challenge.

Power Primer Challenge as seen on ctf.compfest websiteRSA warmup, eh… I guess we are expecting an easy challenge here (I don't know what I'm doing). This challenge is not hosted anywhere, there's only a source code called chall.py , looks like everything is inside there. Let's take a peek on it.

```
from Crypto.Util.number import getPrime, bytes_to_long
from secret import message, x, y

p = getPrime(y)
n = p ** x
e = 0x10001
c = pow(bytes_to_long(message), e, n)

print(f"n = {n}")
print(f"e = {e}")
print(f"c = {c}")

# output
# n = 174398141961264126560505296048651397103940625972358808906187816452656090815275082092703206639204234732453380366400438429846076789218559828669690390572528240520254507036152659026582129125892087219537071916257813880120391483891236016422449795410600212796367274254070440928882993348666993424943717023976062255483456283318813107003678274274454583252439764631805477342477492425052659593801
# e = 65537
# c = 38415069832658278102412940476349224522223117826717864236716063942465292251639452037471899276433883280487660575851320701796429668476551053062015248611453285019543570394965516221325993414456754832832080360042304547277452474428650298929639938371072386565545457564351801474854761480051602266412901190322297685878637385354294132832534425751762322767659303351614194618177802401960510283943
```

That's everything, solid enough, seems like we got everything needed to decrypt this message. Before I get into it, I wanna explain a brief explanation about RSA Algorithm.

RSA (Rivest-Shamir-Adleman) is a widely-used public key cryptosystem that allows for secure data transmission. Basically, just like the other encryption thingy, it's based on the mathematical difficulty of factoring large composite numbers, that's the thing that makes this algorithm can be hard. The bigger the value we have to factorize, the harder it is to decrypt (manually) without using the key.

The key components used in this algorithm:
- Two Prime Numbers (usually large numbers), the two distinct large prime numbers will be called as p and q
- then modulus (n), this variable can be obtained by multiply the value of p and q
n=p×q
- euler's totient function: ϕ(n)=(p−1)×(q−1)
- public exponent (e): this should be a small integer that is coprime with ϕ(n), in RSA, the commonly used public exponent is 65537
- private exponent (d): d=e−1modϕ(n) , where d is the modular inverse of e modulo ϕ(n).
- public key: consisted of (n, e)
- private key: consisted of (n, d)

The rest of methodes about encryption and decryption with this algorithm, I suggest you to read this.
I guess that's for the brief lecture about RSA, let's analyze to code to figure things out. From my short analyze, the source code is a basic code of RSA encryption, where a plaintext message is encrypted using a public key. Let's try to break it down, and discuss about how we might obtain the flag.

Prime generation:
p = getPrime(y) 
A prime number 'p' is generated with a bit length of 'y'.

The calculation of the modulus:
n = p ** x 

The modulus 'n' is calculated as 'p' raised to the power of 'x'.

Public exponent:
e = 0x10001 

Public exponent 'e' is set to '10001' (in hex) or '65537', which is (as I said before) commonly used in RSA.

Encryption:
c = pow(bytes_to_long(message), e, n) 
The message here is converted to a long integer and then encrypted using RSA by raising the message to the power of 'e' modulo 'n', resulting in the ciphertext 'c'.

```
Output:
print(f"n = {n}") print(f"e = {e}") print(f"c = {c}")
the value will be printed as values of 'n', 'e', and the ciphertext 'c'.
```

Oh yeah, almost forgot, the variable 'c' is used as the encrypted message variable, a.k.a. ciphertext.
Well, something off about this encryption scrypt is/are: the message encrypted here using an RSA encryption scheme where the modulus 'n' is unusually constructed as n=p^x , instead of the typical n = p x q (where p and q are two large prime numbers).

So… how do we obtain the flag? To retrieve the message or original flag encrypted as ciphertext 'c' here, we need to perform the usual RSA decryption operation. However, because of that unusual structure of 'n', the standard RSA decryption won't work directly.

Ok, then we gotta make our own path to decrypt this RSA.

First thing to do, we gotta factorize n
Since n = p^x and p is a prime, we can factor 'n' to find 'p' and 'x'. And how do we obtain these? By taking the 'x'-th root of 'n', giving us the value of 'p'.

After that, we can find the private key. Once we obtained the value of 'p' and 'x', we can calculate the private key 'd' using the formula:
d=e−^1modϕ(n)

Here, the euler's totient function will be: ϕ(n)=p^x−1 × (p−1).

Lastly, we can decrypt the ciphertext 'c' using the private key 'd':
m = c^d mod n, then we convert the result back from a long integer to bytes to get the original message/flag using the library.

How did I finish this challenge? I ain't doing allat LMAO.

Since we're in CTF, beg your pardon, we don't have time to wait our own script to calculate these things (atleast the first and second steps). Thanks to some intelligence people on this project, called RsaCtfTool by RsaCtfTool on github (you guys can use that), it's very easy (atleast for our case) to obtain some elements needed to obtain the flag.

First, we will generate a public key first using n and e. Using the argument - createpub -n -e, the tool will generate us the publickey.


Generate publickey using RsaCtfTool./RsaCtfTool.py 
```
--createpub -n 174398141961264126560505296048651397103940625972358808906187816452656090815275082092703206639204234732453380366400438429846076789218559828669690390572528240520254507036152659026582129125892087219537071916257813880120391483891236016422449795410600212796367274254070440928882993348666993424943717023976062255483456283318813107003678274274454583252439764631805477342477492425052659593801 -e 65537
```
We obtained the public key there, let's write it in the .pub format file. I echo-ed it into key.pub

Publickey as key.pubAfter that, let's obtain the private key using the argument - private with the same tool. We gotta use the public key in .pub format we made before.
```
./RsaCtfTool.py --publickey ./key.pub --private
```
Private key generated using RsaCtfToolThat's it, we got the value of 'd' a.k.a. private key, now we have collected all the ingredients to decrypt our message. I think I will make a short python script to reverse the ciphertext so we can obtain the message 'm'

Oh yea.. almost forgot again, in cryptography, the original message/input message, usually called as variable 'm'
```
from Crypto.Util.number import long_to_bytes

d = 0x1420461fc3402c3f76ab08b54474b21600c5f7702c232cf05a37bcdb0792246dce4a5e2e246826e569a36554be98042d1026ce628cd6447927758a80514a88e5a030f819c004fd556ee87b16b59301afb102f7fa98fcdf1e24bf17c0ef38e3756ca85fbc00036de812538d84dd1d8f6fe2b91b3a93ef3af6ec38c7b97e8dfeacbaa74c4750c6c910f45ed8e7a3ca0d15df87227740ef37c1f8a16364d773b99
c = 38415069832658278102412940476349224522223117826717864236716063942465292251639452037471899276433883280487660575851320701796429668476551053062015248611453285019543570394965516221325993414456754832832080360042304547277452474428650298929639938371072386565545457564351801474854761480051602266412901190322297685878637385354294132832534425751762322767659303351614194618177802401960510283943
n = 174398141961264126560505296048651397103940625972358808906187816452656090815275082092703206639204234732453380366400438429846076789218559828669690390572528240520254507036152659026582129125892087219537071916257813880120391483891236016422449795410600212796367274254070440928882993348666993424943717023976062255483456283318813107003678274274454583252439764631805477342477492425052659593801
e = 65537

m = pow(c, d, n)
flag = long_to_bytes(m)
print(flag)
```

'c' is the ciphertext we want to decrypt, 'd' is the private key we obtained before, 'n' is the modulus used in this RSA encryption.

To obtain m we will use:
```
pow(c, d, n)
```

this func will perform modular exponentiation. In our context, it's used to compute m = c^d mod n, where 'm' (as I said before) is the decrypted message a.k.a. plaintext.

then the pow function is a built-in python func that can efficiently compute c^d mod n using modular exponentiation, which is… yeah, essential for RSA decryption.

then the converting the decrypted message here, we use variable flag as the decrypted message

```
flag = long_to_bytes(m)
```

where long_to_bytes(m) func will convert the decrypted integer m into a byte string. Then that's it, we will just print the flag.

flag obtained

Thanks for reading this far. Until we meet again.
Sources:
https://www.geeksforgeeks.org/rsa-algorithm-cryptography/
https://www.simplilearn.com/tutorials/cryptography-tutorial/rsa-algorithm#:~:text=When%20using%20RSA%20for%20encryption,any%20keys%20in%20this%20scenario.
https://baptistout.net/posts/convert-jwks-modulus-exponent-to-pem-or-ssh-public-key/
https://github.com/RsaCtfTool/RsaCtfTool