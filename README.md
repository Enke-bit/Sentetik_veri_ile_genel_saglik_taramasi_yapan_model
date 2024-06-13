# Genel Muayene Modeli ve Sentetik Veri Üretimi

Bu çalışma, sağlık alanında genel muayene için bir makine öğrenimi modeli geliştirme sürecini kapsamaktadır. Amaç, sentetik veri oluşturarak ve bu veri üzerinde bir sınıflandırma modeli eğiterek genel sağlık durumunu tahmin etmektir.

## Kullanılan Teknolojiler ve Kütüphaneler
- Python
- Pandas
- NumPy
- Faker
- Scikit-learn

## Veri Oluşturma
Sentetik veri, Faker kütüphanesi kullanılarak üretildi. Oluşturulan özellikler şunlardır:
- Age (Yaş)
- Gender (Cinsiyet)
- Weight (Kilo)
- Height (Boy)
- Known Conditions (Bilinen Hastalıklar)
- Health Status (Sağlık Durumu)

## Veri İşleme
Veri oluşturulduktan sonra, cinsiyet bilgisini sayısal verilere dönüştürüldü (Male -> 0, Female -> 1).

## Model Seçimi ve Eğitim
Eğitim için kullanılan model: **Logistic Regression (Lojistik Regresyon)**

## Model Değerlendirme
Eğitim setinin %80'inden faydalanılarak model eğitildi ve geri kalan %20'lik test seti üzerinde değerlendirildi.

### Model Başarımı
- **Accuracy:** 46.00%
- **Classification Report:**

            precision    recall  f1-score   support

       0       0.45      0.54      0.49        96
       1       0.48      0.38      0.43       104

accuracy                           0.46       200



## Veri ve Tahminlerin Kaydedilmesi
Model, eğitildiği veriyi ve tahminleri CSV formatında kaydetti. Dosya adı: **13-06-2024_health_predictions.csv**

---
