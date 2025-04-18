---
title: "Pembangunan Model Prediksi Depresi Pelajar Berdasarkan Faktor Lingkungan dan Akademis"
authors:
- admin
date: "2025-01-03T00:00:00Z"
doi: 

# Schedule page publish date (NOT publication's date).
publishDate: "2025-04-18T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: Depresi merupakan salah satu masalah kesehatan mental yang membutuhkan perhatian serius karena dampaknya yang signifikan terhadap kehidupan individu. Dalam artikel ini, kami mengembangkan model prediksi depresi menggunakan algoritma Logistic Regression yang dioptimalkan dengan metode hyperparameter tuning berbasis GridSearchCV. Penelitian ini memanfaatkan dataset dengan berbagai fitur seperti tekanan akademik, durasi tidur, kebiasaan makan, dan tingkat kepuasan belajar. Data terlebih dahulu dinormalisasi menggunakan StandardScaler untuk meningkatkan performa model, karena Logistic Regression sensitif terhadap skala data. Hasil evaluasi menunjukkan bahwa model mencapai akurasi sebesar 84,206%, dengan nilai precision, recall, dan F1-score yang konsisten untuk kedua kelas (Not-Depressed dan Depressed). Optimasi parameter, seperti penalti regulasi dan nilai regularisasi, berhasil meningkatkan akurasi dibandingkan model baseline tanpa tuning. Studi ini menunjukkan bahwa Logistic Regression, meskipun sederhana, dapat menjadi alat yang efektif untuk mendeteksi risiko depresi jika dioptimalkan dengan teknik yang tepat. Selain itu, penggunaan GridSearchCV memungkinkan pencarian parameter yang lebih optimal, meningkatkan kemampuan model untuk generalisasi. Model ini memiliki potensi untuk digunakan dalam sistem deteksi dini, khususnya di lingkungan pendidikan atau pekerjaan, guna mendukung intervensi dini terhadap individu yang berisiko. Penelitian ini membuka peluang untuk eksplorasi lebih lanjut, seperti penambahan fitur lain, penggunaan algoritma pembelajaran mesin yang lebih kompleks, dan integrasi dengan sistem kesehatan mental untuk meningkatkan akurasi dan memberikan hasil yang lebih dapat diandalkan.

# Summary. An optional shortened abstract.
summary: Dalam penelitian ini, kami berhasil membangun model prediksi depresi menggunakan algoritma Logistic Regression yang dioptimalkan dengan metode GridSearchCV. Pendekatan ini memungkinkan kami untuk menemukan kombinasi parameter terbaik, seperti penalti, regularisasi, dan jumlah iterasi maksimum, yang memberikan performa model paling optimal. Berdasarkan evaluasi, model ini mencapai akurasi sebesar 84,206% pada data uji, dengan nilai precision, recall, dan F1-score yang seimbang, terutama untuk kelas Depressed yang menjadi fokus utama. Hal ini menunjukkan bahwa model dapat mengenali individu yang berisiko depresi dengan cukup baik, sekaligus meminimalkan kesalahan prediksi. Adapun proses normalisasi data menggunakan StandardScaler juga berperan penting dalam meningkatkan performa Logistic Regression, terutama karena fitur-fitur yang digunakan memiliki skala yang berbeda. Dengan optimasi melalui GridSearchCV, kami mampu meningkatkan akurasi model dibandingkan baseline Logistic Regression tanpa tuning parameter. Saran yang diajukan oleh kami antara lain adalah integrasi fitur tambahan seperti faktor lingkungan atau data psikologis, untuk meningkatkan akurasi prediksi. Lalu eksperimen dengan algoritma lain yang lebih kompleks untuk membandingkan performa. Serta validasi yang lebih luas guna memastikan model dapat diaplikasikan secara general.

tags:
- AI
- Klasifikasi
- Logistic Regression
- Prediction
- Depression

featured: true

# - name: Custom Link
#   url: http://example.org
url_pdf: https://drive.google.com/file/d/1Uxwt_-na1tQLcXgAd26lbDazAwWqiAWZ/view?usp=drive_link 
url_code: 'https://colab.research.google.com/drive/1nig-k6GaFxZmZ3z5H3TMQUYVHHabmo2t?usp=sharing'
url_dataset: 'https://www.kaggle.com/datasets/hopesb/student-depression-dataset'
url_poster: 'https://drive.google.com/file/d/1cLbrZFJsvsupWercSvp-MP1q5Mo8P1Wl/view?usp=drive_link'
url_project: 'https://colab.research.google.com/drive/1nig-k6GaFxZmZ3z5H3TMQUYVHHabmo2t?usp=sharing'
url_slides: 'https://drive.google.com/file/d/1uXSLeFz0ETw_PUS0df8mu978OAnPyWwK/view?usp=drive_link'
# url_source: '#'
# url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Our Notebook'
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
