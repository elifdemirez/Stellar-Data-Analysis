# Stellar-Data-Analysis

## Proje Özeti
Bu proje, **Stellar Classification Dataset SDSS17** veri setini kullanarak, yıldızların sınıflandırılmasını gerçekleştirmeyi amaçlamaktadır. Veri seti, yıldızların çeşitli özelliklerini içeren veriler sunmaktadır.

## Proje Hedefi ve Yaklaşımı

Projemin amacı, **Stellar Classification Dataset SDSS17** veri setindeki yıldızların sınıflandırılmasını doğru bir şekilde yapabilmek. Bu hedef doğrultusunda:

- Veri setini keşfetmek,
- Temizlemek,
- Anlamlı özellikler çıkarmak (feature engineering),
- En önemli özellikleri seçmek (feature selection),
- Yıldızların sınıflandırılmasında kullanılabilecek makine öğrenmesi modellerine hazırlamak.

## Veri Seti

Veri seti, yıldızların çeşitli spektral özelliklerine dair bilgileri içeren bir dizi sayı ve sınıf etiketinden oluşmaktadır. Ana hedef, sınıflandırma yaparak hangi yıldızların hangi sınıfa ait olduğunu belirlemektir.

### Veri Seti Özellikleri

- **Class**: Yıldız türü. (`GALAXY`, `STAR`, `QSO`)
- **z**: Kızılötesi kayma.
- **redshift**: Redshift değeri.
- **log_redshift**: Redshift'in logaritmik değeri.

## Veri Temizleme ve Keşifsel Veri Analizi (EDA)

İlk adımda, veri setindeki eksik, hatalı veya tutarsız veriler temizlendi ve ardından keşifsel veri analizi (EDA) yapıldı. EDA, verinin genel yapısını anlamak için aşağıdaki adımları içerdi:

1. **Veri Temizleme**: Eksik veya hatalı verilerin silinmesi.
2. **İstatistiksel Özellikler**: Veri setinin temel istatistiksel özetleri (`mean`, `std`, `min`, `max`, `median` vb.) çıkarıldı.
3. **Veri Dağılımı**: Özelliklerin dağılımları histogramlarla analiz edildi.

### Elde Edilen Sonuçlar

- **Eksik Veri**: Veri setinde eksik değer bulunmamaktadır.
- **İstatistiksel Özet**: Özelliklerin genel dağılımları ve merkezi eğilimleri gözlemlendi.

## Feature Engineering ve Feature Selection

Veri mühendisliği adımında, yeni özellikler oluşturulmuş ve gereksiz özellikler elenmiştir. Feature Selection sürecinde ise, modelin başarısını artıracak ve modelin eğitim süresini azaltacak önemli özellikler seçilmiştir.

### Feature Engineering
- **log_redshift**: Redshift'in logaritmik dönüşümü yapılmıştır, bu sayede özelliklerin daha dengeli bir dağılım göstermesi sağlanmıştır.

### Feature Selection
Feature selection adımında **z**, **redshift** ve **log_redshift** özelliklerinin sınıflandırma için en önemli olanlar olduğu belirlenmiştir. Bu özellikler, hedef değişkeni ile güçlü bir korelasyona sahip çıkmıştır.

## Veri Görselleştirme

Veri görselleştirme adımında, farklı görsel araçlar kullanılarak değişkenler arasındaki ilişkiler analiz edilmiştir. Aşağıdaki grafikler ve görselleştirmeler bu adımda kullanılmıştır:

1. **Histogramlar**: Her bir özelliğin dağılımını incelemek için histogramlar oluşturulmuştur.
2. **Korelasyon Matrisi**: Özellikler arasındaki ilişkileri görsel olarak incelemek amacıyla korelasyon matrisine bakılmıştır.
3. **Scatter Plotlar**: Özellikler arasındaki doğrusal ilişkileri görmek için scatter plotlar oluşturulmuştur.


### Sonuç ve Öneriler

#### Elde Edilen Analizler Işığında Veri Seti ve Çözüm Önerisi
Bu projede, **yıldız sınıflandırma** problemi üzerine çalıştık. Veri seti, yıldız türlerini sınıflandırmak için kullanılan astronomik gözlem verilerini içermektedir. Bu model, **yıldızların türlerini tahmin etmek** için kullanılabilir ve astronomi araştırmalarında daha hızlı ve doğru sonuçlar elde edilmesine yardımcı olabilir.

#### Şirket İçerisinde Kullanım Senaryosu
Bu model, **gökbilim araştırma şirketlerinde** veya **astronomik gözlem enstitülerinde** yıldız türlerini sınıflandırmak amacıyla kullanılabilir. Özellikle yeni teleskoplarla yapılan gözlemlerden elde edilen verilerle, model daha hızlı ve doğru sınıflandırmalar yaparak araştırmalara yön verebilir.

#### Hangi Algoritma ve Model Seçilmeli?
- **XGBoost**: Yüksek doğruluk ve hızlı eğitim süreleri ile sınıflandırma problemleri için uygun.
- **Random Forest**: Özelliklerin önemini belirleyerek overfitting'i engeller ve genelleme sağlar.

#### Öneriler
1. **Daha Fazla Özellik Eklenmesi**: Gökbilimsel verilerle daha kapsamlı bir model oluşturulabilir.
2. **Veri Kümesinin Genişletilmesi**: Farklı bölgelerden gelen gözlemlerle modelin doğruluğu artırılabilir.
3. **Modelin İzlenmesi ve Güncellenmesi**: Modelin performansı sürekli izlenmeli ve gerektiğinde güncellenmelidir.

