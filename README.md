# 🖼️ Amazon Ürün Görsel Sınıflandırma (ResNet-50)

## 📌 Proje Özeti
Bu proje, **ResNet-50 (PyTorch)** kullanarak Amazon ürün görsellerini üç sınıfa ayırmayı amaçlamaktadır:

- **All_Beauty (Kozmetik & Güzellik)**
- **Digital_Music (Dijital Müzik)**
- **Health_and_Personal_Care (Sağlık & Kişisel Bakım)**

Çalışma, **transfer öğrenmenin güçlü yönlerini ve sınırlamalarını** özellikle küçük ve dengesiz veri kümeleri üzerinde göstermektedir.

---

## 🚀 Teknik Yaklaşım
- **Model Mimarisi:** ResNet-50 ile Transfer Learning (ImageNet üzerinde önceden eğitilmiş)  
- **Veri Ön İşleme:**  
  - Görsellerin yeniden boyutlandırılması  
  - Veri artırma (döndürme, çevirme, normalizasyon)  
- **Eğitim Detayları:**  
  - Kayıp Fonksiyonu: CrossEntropy  
  - Optimizasyon: Adam  
  - Öğrenme oranı planlaması  
- **Değerlendirme Metrikleri:** Doğruluk (Accuracy) ve sınıf bazlı performans analizi  

---

## 📊 Sonuçlar
- **Eğitim Doğruluğu:** `91.67%`  
- **Test Doğruluğu:** `41.67%`  
- **Önemli Gözlem:**  
  - Eğitim setinde yüksek başarı → **Aşırı uyum (Overfitting) tespit edildi**  
  - **Digital_Music** sınıfında sınıflandırma tamamen başarısız oldu  

| Sınıf                      | Performans |
|-----------------------------|-------------|
| All_Beauty                 | İyi         |
| Health_and_Personal_Care   | Orta        |
| Digital_Music              | Zayıf (başarısız) |

---

## ⚠️ Belirlenen Sorunlar
- Belirgin **aşırı uyum (overfitting)** (yüksek eğitim doğruluğu, düşük test doğruluğu)  
- **Genelleme başarısızlığı** (yeni verilerde düşük performans)  
- **Sınıf dengesizliği** problemi  
- **Digital_Music** kategorisinde tamamen başarısız sınıflandırma  

---

## 💡 Önerilen İyileştirmeler
- **Veri Kümesini Genişletme**: Daha dengeli eğitim örnekleri toplamak  
- **Gelişmiş Veri Artırma**: Daha güçlü düzenlileştirme teknikleri uygulamak  
- **Model Optimizasyonu**: ResNet-101, EfficientNet veya Vision Transformers denemek  
- **Sınıf Dengesizliği Çözümü**: Oversampling, undersampling veya ağırlıklı kayıp fonksiyonu kullanmak  
- **Çapraz Doğrulama**: Daha iyi model doğrulama stratejileri geliştirmek  

---

## 📚 Temel Çıkarımlar
Bu proje göstermektedir ki:  
- **Transfer öğrenme**, sınırlı veri kümelerinde zorluklar barındırır  
- **Veri kalitesi ve dengesi**, başarı için kritik öneme sahiptir  
- Sadece **doğruluk (accuracy)** yerine **sınıf bazlı değerlendirme** de önemlidir  

---

## 🛠️ Kullanılan Teknolojiler
- **Python 3.x**
- **PyTorch**
- **Torchvision**
- **Matplotlib / Seaborn** (görselleştirme için)
- **NumPy, Pandas** (veri işleme için)

---

## 📌 Gelecek Çalışmalar
- **Daha büyük mimariler** (ResNet-101, EfficientNet) veya **Vision Transformers (ViT)** denemek  
- **Yarı denetimli / kendi kendine öğrenme yöntemleri** uygulamak  
- **Hiperparametre optimizasyonu** (Optuna gibi araçlarla)  
- Modeli **Flask/FastAPI + Docker** ile dağıtmak  

---

## 👤 FURKAN DEMİR 
Geliştiren: **[FURKAN DEMİR ]**  



