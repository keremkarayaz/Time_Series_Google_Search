# 📈 Google Trends Zaman Serisi Analizi: Depresyon Arama Hacmi

Bu proje, Google Trends üzerinden alınan "Depresyon" kelimesinin Türkiye'deki arama hacmini analiz etmek ve Prophet modeli ile geleceğe yönelik tahminlerde bulunmak amacıyla hazırlanmıştır.

---

## 🔍 Projenin Amacı

- **Veri Kaynağı:** Google Trends (CSV formatında dışa aktarıldı)
- **Anahtar Kelime:** Depresyon
- **Bölge:** Türkiye
- **Analiz Türü:** Zaman serisi analizi ve tahminleme
- **Model:** Meta tarafından geliştirilen Prophet zaman serisi modeli

---

## 📁 Dosyalar

- `Times_Series_Google_Trends.ipynb` : Tüm adımların yer aldığı Jupyter notebook dosyası.
- `multiTimeline.csv` : Google Trends'ten indirilen ham veri dosyası (çalıştırma için gerekli).
- `README.md` : Proje hakkında açıklamalar ve kurulum bilgileri.

---

## ⚙️ Kullanılan Kütüphaneler

- `pandas`
- `matplotlib`
- `prophet` (eski adıyla `fbprophet`)

---

## 🧪 Uygulanan Adımlar

### 1️⃣ Veri Yükleme ve Temizlik
- Google Trends verisi okunur, kolon isimleri sadeleştirilir.
- Tarih sütunu `datetime` formatına çevrilir ve index yapılır.

### 2️⃣ Veri Görselleştirme
- Trend skorları çizgi grafikle görselleştirilir.
- 4 haftalık hareketli ortalama hesaplanarak dalgalanmalar yumuşatılır.

### 3️⃣ Prophet Modeli Eğitimi
- Prophet modeline uygun format (`ds`, `y`) hazırlanır.
- Model eğitilir ve 12 haftalık ileriye dönük tahmin yapılır.

### 4️⃣ Tahmin Sonuçlarının Analizi
- Prophet modelinin bileşenleri (trend, haftalık, yıllık etkiler) incelenir.
- 2025 yılı özelinde aylık ortalama tahminler bar grafikle sunulur.
  
  ---

## 📊 Çıktılar

### ✅ 12 Haftalık Tahmin
Model, 12 hafta sonrası için arama hacmi tahminleri üretir.

### ✅ 2025 Yılı Aylık Ortalama Grafik
2025 yılı boyunca ay ay depresyon aramalarındaki tahmini değişimler gösterilir.

---

## 📌 Lisans

Bu proje [MIT Lisansı](https://opensource.org/licenses/MIT) ile lisanslanmıştır.


Tüm detaylar için: [LICENSE](https://opensource.org/licenses/MIT)
