# 🏠 House Price Prediction (Ev Fiyat Tahmini)

![Project Status](https://img.shields.io/badge/status-completed-green) ![Language](https://img.shields.io/badge/language-Python-blue) ![Library](https://img.shields.io/badge/library-Scikit--Learn-orange)

Bu proje, makine öğrenmesi algoritmalarını kullanarak ev fiyatlarını tahmin etmeyi amaçlayan kapsamlı bir veri bilimi çalışmasıdır. Veri seti üzerinde detaylı Keşifsel Veri Analizi (EDA), veri ön işleme ve çeşitli regresyon modellerinin performans karşılaştırmaları yapılmıştır.

## 📊 Proje Hakkında

Emlak piyasasındaki fiyatlandırma dinamiklerini anlamak ve belirli özelliklere (alan, oda sayısı, konum vb.) dayanarak bir evin piyasa değerini tahmin etmek hedeflenmiştir. Proje kapsamında hem doğrusal (Linear) hem de topluluk (Ensemble) öğrenme yöntemleri kullanılmıştır.

**Temel Hedef:** `Housing.csv` veri setindeki özellikleri kullanarak `price` (fiyat) değişkenini en yüksek doğrulukla tahmin etmek.

## 📂 Veri Seti Özellikleri

Kullanılan veri seti (`Housing.csv`), evlerin fiziksel özelliklerini ve fiyat bilgilerini içerir.

| Özellik | Açıklama |
| :--- | :--- |
| **price** | Hedef değişken (Evin fiyatı) |
| **area** | Evin metrekaresi |
| **bedrooms** | Yatak odası sayısı |
| **bathrooms** | Banyo sayısı |
| **stories** | Kat sayısı |
| **mainroad** | Ana yola bağlantısı var mı? |
| **guestroom** | Misafir odası var mı? |
| **basement** | Bodrum katı var mı? |
| **airconditioning** | Klima var mı? |
| **furnishingstatus** | Eşya durumu (Mobilyalı, Yarı Mobilyalı, Boş) |

*(Diğer özellikler: hotwaterheating, parking, prefarea vb.)*

## 🛠️ Uygulanan Yöntemler

Proje sürecinde aşağıdaki adımlar izlenmiştir:

1.  **Keşifsel Veri Analizi (EDA):**
    * Eksik ve yinelenen verilerin temizlenmesi.
    * Dağılım grafikleri (Distplot) ve Kutu grafikleri (Boxplot) ile aykırı değer analizi.
    * Korelasyon matrisi (Heatmap) ile özellikler arasındaki ilişkilerin incelenmesi.
2.  **Veri Ön İşleme:**
    * Kategorik değişkenler için **One-Hot Encoding**.
    * Özelliklerin ölçeklendirilmesi (**StandardScaler** / **MinMaxScaler**).
    * Verinin Eğitim ve Test seti olarak ayrılması.
3.  **Modelleme:**
    * Linear Regression (Çoklu Doğrusal Regresyon)
    * Ridge & Lasso & Elastic-Net Regression (Düzenlileştirme)
    * Polynomial Regression
    * Random Forest Regressor
    * Gradient Boosting & XGBoost & CatBoost
    * Support Vector Regressor (SVR)

## 📈 Model Performansları

Yapılan testler sonucunda modellerin **R² (Belirlilik Katsayısı)** skorlarına göre başarı durumu:

| Model | Başarı Durumu | Notlar |
| :--- | :--- | :--- |
| **Lasso Regression** | **Yüksek (~%64.6)** | En iyi genelleme performanslarından biri. |
| **Ridge Regression** | **Yüksek (~%64.5)** | Lasso ile benzer, kararlı sonuçlar. |
| **CatBoost** | **Yüksek (~%64.4)** | Topluluk modelleri arasında öne çıktı. |
| **Gradient Boosting** | İyi (~%63.1) | Güçlü bir tahmin yeteneği sergiledi. |
| **XGBoost** | Orta (~%61.5) | Hiperparametre optimizasyonu ile artırılabilir. |
| **SVR** | Düşük (< 0) | Bu veri seti dağılımı için uygun olmadığı görüldü. |

> **Sonuç:** Lasso ve Ridge regresyon modelleri, veri setindeki gürültüyü iyi yöneterek en dengeli sonuçları vermiştir.

## 🧰 Kullanılan Teknolojiler

* **Python** (3.x)
* **Pandas & NumPy** (Veri Manipülasyonu)
* **Matplotlib & Seaborn** (Veri Görselleştirme)
* **Scikit-Learn** (Makine Öğrenmesi Modelleri)
* **XGBoost / CatBoost** (Gelişmiş Algoritmalar)
* **Statsmodels** (İstatistiksel Analiz)

## 🚀 Kurulum

1.  Projeyi klonlayın:
    ```bash
    git clone [https://github.com/kullaniciadi/ev-fiyat-tahmini.git](https://github.com/kullaniciadi/ev-fiyat-tahmini.git)
    ```
2.  Gerekli kütüphaneleri yükleyin:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn xgboost catboost statsmodels
    ```
3.  Jupyter Notebook'u çalıştırın:
    ```bash
    jupyter notebook ev_fiyat_tahmini.ipynb
    ```

## 👨‍💻 Yazar

**Furkan Öztürk**

---
*Bu proje Veri Bilimi ve Makine Öğrenmesi çalışmaları kapsamında geliştirilmiştir.*
