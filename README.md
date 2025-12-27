📰 BBC News Topic Modeling with LDA & NMF

Bu proje, BBC News veri seti üzerinde Konu Modellemesi (Topic Modeling) yapmak amacıyla geliştirilmiştir.
Projede iki farklı yaklaşım kullanılmıştır:

Latent Dirichlet Allocation (LDA)

Non-negative Matrix Factorization (NMF)

Modelleme süreci; veri temizleme, metin ön işleme, vektörleştirme, model eğitimi, görselleştirme ve yeni metinler üzerinde test adımlarını kapsamaktadır.

🚀 Projenin Amacı

Haber metinlerinden otomatik konu çıkarımı yapmak

LDA ve NMF algoritmalarını karşılaştırmalı olarak kullanmak

Eğitilen modellerle yeni haber metinlerinin konusunu tahmin etmek

Sonuçları kelime bulutları ve pyLDAvis ile görselleştirmek

📂 Kullanılan Veri Seti

Kaynak: BBC News Dataset

Platform: Kaggle

İndirme: kagglehub kullanılarak otomatik indirilir

Veri seti; başlık, açıklama ve kategori bilgilerini içeren haber metinlerinden oluşmaktadır.

🧱 Proje Akışı

Gerekli Kütüphanelerin Yüklenmesi

Veri Setinin İndirilmesi

Metin Birleştirme ve Temizlik

Metin Ön İşleme

HTML temizleme

URL kaldırma

Tokenization

Stopword temizliği

Lemmatization (WordNet)

Vektörleştirme

LDA → CountVectorizer

NMF → TfidfVectorizer

Model Eğitimi

20 konu (topic) olacak şekilde

Konu Analizi ve Etiketleme

Görselleştirme

pyLDAvis (interaktif)

WordCloud çıktıları

Yeni Metin Üzerinde Test

Modellerin Kaydedilmesi

🛠️ Kullanılan Teknolojiler ve Kütüphaneler

Python

NumPy, Pandas

NLTK

Scikit-learn

BeautifulSoup

Matplotlib, Seaborn

WordCloud

pyLDAvis

Joblib

📊 Modelleme Detayları
🔹 LDA Pipeline

CountVectorizer

LatentDirichletAllocation

🔹 NMF Pipeline

TfidfVectorizer

NMF

Her iki model de 20 konu olacak şekilde eğitilmiştir.

🖼️ Görselleştirmeler

pyLDAvis ile interaktif konu dağılımları

Her konu için otomatik oluşturulan WordCloud görselleri

lda_word_cloud_topic_X.png

nmf_word_cloud_topic_X.png

🧪 Yeni Metin Testi

Proje, kullanıcıdan alınan haber metinlerini analiz ederek:

LDA konu tahmini

NMF konu tahmini

LDA için güven oranı (%)

bilgilerini terminal üzerinden sunar.

Çıkmak için:

q

💾 Model Kaydetme

Eğitilen modeller aşağıdaki dosyalar halinde kaydedilir:

lda_pipeline.joblib
nmf_pipeline.joblib


Bu dosyalar daha sonra yeniden yüklenerek inference (tahmin) amacıyla kullanılabilir.

▶️ Çalıştırma
pip install -r requirements.txt


Ardından Python dosyasını veya notebook’u çalıştırmanız yeterlidir.

Not: İlk çalıştırmada NLTK paketleri otomatik olarak indirilecektir.

📌 Notlar

Proje Google Colab ortamında geliştirilmiştir.

kagglehub kullanımı için Kaggle API yapılandırması gereklidir.

Büyük veri setlerinde ön işleme adımı zaman alabilir.

👤 Geliştirici

Bu proje, Doğal Dil İşleme (NLP) ve Konu Modellemesi pratikleri amacıyla geliştirilmiştir.
