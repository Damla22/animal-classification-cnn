# animal-classification-cnn
Bu proje, 10 farklı hayvan türünü sınıflandırmak amacıyla CNN modelleri kullanılarak gerçekleştirilmiştir. 

# **Hayvan Sınıflandırma Projesi**
## 📌 **Proje Hakkında**
Bu proje, Convolutional Neural Network (CNN) kullanarak 10 farklı hayvan sınıfını sınıflandırmayı amaçlamaktadır. Model, eğitim sırasında veri manipülasyonlarının etkilerini analiz etmek ve sonuçları iyileştirmek için geliştirilmiştir.
[Kaggle Projesine buradan ulaşabilirsiniz.](https://www.kaggle.com/code/damlagkta/goruntuisleme)


## 📂 **Veri Seti**
Bu projede kullanılan veri setine şu bağlantıdan ulaşabilirsiniz:  
[Animals with Attributes 2 - Kaggle](https://www.kaggle.com/datasets/rrebirrth/animals-with-attributes-2)

### Özellikler:
* Toplam 50 hayvan sınıfı içerir.
* Her sınıf, farklı sayıda görüntü barındırır.
* Projede 10 sınıf kullanılmıştır:
* Collie, Dolphin, Elephant, Fox, Moose, Rabbit, Sheep, Squirrel, Giant Panda, Polar Bear.
* Kullanılan her sınıf için 650 görüntü seçilmiştir.
  
### Veri İşleme:
* Görüntüler, model girişi için 128x128 piksel boyutuna küçültülmüş ve normalize edilmiştir.
* Veri seti %70 eğitim ve %30 test olarak ayrılmıştır.

## **🛠️ Kullanılan Kütüphaneler**
Proje kapsamında aşağıdaki kütüphaneler kullanılmıştır:
* NumPy: Veri manipülasyonu ve diziler için.
* OpenCV: Görüntü işleme ve boyutlandırma için.
* Matplotlib: Veri görselleştirme için.
* Scikit-learn: Veri seti ayrımı için.
* TensorFlow/Keras: Derin öğrenme modeli oluşturmak ve eğitmek için.
---

## **📊 Yapılan Analizler ve İşlemler**
### **1️⃣ Veri Hazırlığı**
* Görüntüler yeniden boyutlandırılmış ve normalize edilmiştir.
* Veri seti, eğitim ve test olarak ayrılmıştır.
* Veri artırma (data augmentation) teknikleri uygulanmıştır:
    * Döndürme
    * Yakınlaştırma
    * Kaydırma
    * Yatay çevirme
      
### **2️⃣ CNN Modelinin Tasarlanması**
**Model Yapısı:**
* Konvolüsyon katmanları (Conv2D)
* Havuzlama katmanları (MaxPooling2D)
* Dropout (Overfitting’i önlemek için)
* Fully Connected (Dense) katmanlar
* Kayıp Fonksiyonu: Categorical Crossentropy
* Optimizasyon Algoritması: Adam

### **3️⃣ Model Eğitimi ve Performans Değerlendirme**
* Model, eğitim sırasında doğruluk (accuracy) ve kayıp (loss) grafiklerinde analiz edilmiştir.
* Eğitim ve doğrulama verileri arasındaki fark incelenmiştir.

### **4️⃣ Manipüle Edilmiş Testler**
* Farklı ışık manipülasyonlarına maruz kalan test setleri değerlendirilmiştir.
* Manipüle edilmiş görüntülere renk sabitliği (Gray World algoritması) uygulanarak testler tekrarlanmıştır.

### **5️⃣ Sonuçların Karşılaştırılması**
* Standart test seti, manipüle edilmiş test seti ve renk sabitliği uygulanmış test seti başarı oranları karşılaştırılmıştır.
* Manipülasyonların model üzerindeki etkileri tartışılmıştır.
