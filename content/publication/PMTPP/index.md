---
title: "Prediksi Pengaruh Merokok Secara Aktif dan Pasif Terhadap Risiko Terjangkit Penyakit Paru-Paru Menggunakan RapidMiner dan Algoritma Naïve Bayes"
authors:
- admin
date: "2024-09-11T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2024-09-11T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: Merokok merupakan sebuah kegiatan yang dirasa sudah lumrah di Indonesia, hampir dimanapun dan kapanpun, kita dapat melihat seorang perokok yang sedang menghisap batang rokoknya di negara Indonesia ini. 39% dari penduduk Indonesia merupakan perokok aktif, atau sekitar 70 juta jiwa dari penduduk Indonesia yang berjumlah 275 juta jiwa. Merokok juga memiliki bahaya laten yang masih banyak diabaikan oleh orang-orang di sekitar kita, belum lagi penyakit yang dapat mengiringi dan berpotensi lebih besar untuk menyerang apabila seseorang itu sering menghisap ataupun terpapar asap rokok. Penelitian ini mengklasifikasikan individu berdasarkan status merokok dan memprediksi kemungkinan terkena penyakit paru-paru menggunakan model Naïve Bayes. Analisis menunjukkan bahwa 42% perokok pasif dari total keseluruhan data berpotensi terkena penyakit paru-paru, dibandingkan dengan 45% dari total keseluruhan data yang merupakan perokok aktif. Temuan ini menyoroti bahaya tersembunyi paparan asap rokok pasif dan menekankan perlunya langkah-langkah kesehatan masyarakat untuk melindungi individu dan mempromosikan lingkungan bebas asap rokok.

# Summary. An optional shortened abstract.
summary: Analisis klasifikasi menggunakan model Naïve Bayes menunjukkan bahwa perokok pasif, yang tidak merokok secara aktif, memiliki persentase dan jumlah kasus potensial penyakit paru-paru yang jauh lebih tinggi dibandingkan dengan perokok aktif. Hal ini bertentangan dengan persepsi umum bahwa perokok aktif lebih berisiko terkena penyakit paru-paru. Temuan ini menyoroti bahaya tersembunyi dari paparan asap rokok pasif. Perokok pasif menghirup sejumlah besar bahan kimia berbahaya dari rokok, meskipun mereka tidak merokok secara langsung. Bahan kimia ini dapat menyebabkan berbagai masalah kesehatan, termasuk penyakit paru-paru. Ironisnya, perokok pasif yang tidak merokok sendiri mungkin menghadapi risiko penyakit paru-paru yang lebih tinggi karena tindakan orang lain. Hal ini menunjukkan pentingnya langkah-langkah kesehatan masyarakat untuk melindungi individu dari paparan asap rokok pasif dan mempromosikan lingkungan bebas asap rokok. Analisis ini menekankan perlunya kampanye kesadaran publik dan peraturan yang lebih ketat untuk membatasi paparan asap rokok pasif. Melindungi individu dari paparan asap rokok pasif dapat secara signifikan mengurangi beban penyakit paru-paru dan meningkatkan kesehatan masyarakat secara keseluruhan.

tags:
- AI
- Klasifikasi
- Naive Bayes

featured: true

links:
# - name: Custom Link
#   url: http://example.org
url_pdf: https://drive.google.com/file/d/1lgUuqnOQIuuwgmF8D7OueXPKZSskiCsz/view?usp=sharing
# url_code: '#'
# url_dataset: '#'
# url_poster: '#'
# url_project: '#'
url_slides: https://drive.google.com/file/d/1wnMRiwwFwxYO9Xt7rcRU1xyEWBo972rd/view?usp=sharing
# url_source: '#'
# url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Shutterstock via kompas.com**](https://asset.kompas.com/crops/aogevpDJHEMCX0m0VrPvU1gYYlw=/0x4:795x534/750x500/data/photo/2019/02/05/2731882312.jpg)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---
### Pendahuluan
Paru-paru memiliki peranan penting bagi tubuh, yakni sebagai sistem pernapasan yang memenuhi kebutuhan oksigen dalam tubuh. Paru-paru memiliki fungsi sebagai tempat bertukarnya oksigen dan karbondioksida dari darah. Jika paru-paru tidak berfungsi dengan baik, maka sistem pernapasan akan terganggu, yang mana dapat menyebabkan gangguan kesehatan dan timbulnya suatu penyakit. Salah satu penyebab gangguan kesehatan pada paru-paru adalah kebiasaan merokok.
Merokok memiliki dampak yang bahaya bagi tubuh. Merokok dikenal sebagai penyebab utama berbagai penyakit paru-paru. Rokok mengandung 7 ribu bahan kimia, dan beberapa diantaranya dapat memicu kanker. Merokok menyebabkan kerusakan pada paru-paru dan berbagai masalah paru-paru yang serius, seperti: kanker paru-paru, pneumonia, penyakit paru-paru obstruktif kronis (PPOK) yakni kesulitan bernapas yang biasanya terjadi setelah bertahun-tahun merokok, dan berbagai penyakit paru lainnya.
Tidak hanya perokok aktif, mereka yang terkena asap rokok dari perokok lain atau biasa disebut perokok pasif, juga berisiko mengalami gangguan kesehatan pada paru-paru, termasuk penyakit paru-paru dan kanker paru-paru. Melansir dari World Health Organization (WHO), pada Pernyataan: Hari Tanpa Tembakau Sedunia 2020 menyatakan, setiap tahun sekitar 225.700 orang di Indonesia meninggal akibat merokok atau penyakit lain yang berkaitan dengan tembakau.
Oleh sebab itu, perlu kiranya suatu pengklasifikasian pengaruh merokok secara aktif dan pasif terhadap risiko terjangkit penyakit paru-paru. Pada penelitian ini digunakan algoritma Naïve Bayes, karena telah terbukti sebagai salah satu pendekatan yang efektif dalam memodelkan hubungan antara variabel paparan rokok dan risiko terkena penyakit paru-paru. Jumlah dataset yang digunakan berjumlah 30.000 data dengan tingkat akurasi mencapai 93,40%. Dengan pengklasifikasian ini, diharapkan mampu membantu mengedukasi perokok aktif akan bahaya merokok untuk keseharan paru-paru dan segera berhenti merokok.

### Landasan Teori
Algoritma adalah metode atau langkah yang direncanakan secara tersusun dan berurutan untuk menyelesaikan atau memecahkan permasalahan dengan sebuah instruksi atau kegiatan.
Dalam statistika, Naïve Bayes classifiers adalah bagian linier dari “klasifikasi probabilistik” yang mengasumsikan bahwa fitur-fitur tersebut saling independen secara bersyarat, dengan asumsi kelas target. Keuntungan penggunaannya adalah bahwa metode ini hanya membutuhkan jumlah data training yang sedikit untuk menentukan estimasi parameter yang diperlukan dalam proses pengklasifikasian. Karena yang diasumsikan sebagai variable independent, maka hanya varians dari suatu variable dalam sebuah kelas yang dibutuhkan untuk menentukan klasifikasi, bukan keseluruhan dari matriks kovarians.
Accuracy adalah metrik yang mengukur seberapa sering sebuah model machine learning memprediksi hasil dengan benar. Akurasi dapat dihitung dengan membagi jumlah prediksi yang benar dengan total jumlah prediksi.
Precision adalah metrik yang mengukur seberapa sering sebuah model machine learning memprediksi kelas positif dengan benar. Precision dapat dihitung dengan membagi jumlah prediksi positif yang benar (true positives) dengan total jumlah contoh yang diprediksi model sebagai positif (baik yang benar maupun yang salah).
Recall adalah metrik yang mengukur seberapa sering sebuah model machine learning mengidentifikasi contoh positif dengan benar (true positives) dari semua sampel positif sebenarnya dalam dataset. Recall dapat dihitung dengan membagi jumlah true positives dengan jumlah contoh positif.