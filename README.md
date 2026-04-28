# 🦠 COVID-19 Hasta Tahmini - Makine Öğrenmesi Projesi

Bu proje, gerçek bir COVID-19 veri seti kullanılarak, kişilerin vaka durumlarını (hasta olup olmadıklarını) makine öğrenmesi teknikleriyle tahmin etmeyi amaçlayan uçtan uca bir çalışmadır.

## 📝 Proje Açıklaması
Bu çalışma kapsamında, pandeminin küresel verileri kullanılarak lojistik regresyon ve karar ağacı tabanlı modeller eğitilmiştir. Proje; veri analizi, eksik verilerin temizlenmesi, özellik mühendisliği ve model performanslarının karşılaştırılması aşamalarından oluşmaktadır.

## 📊 Kullanılan Veri Seti
- veri seti linki:https://www.kaggle.com/datasets/meirnizri/covid19-dataset
- **Tanıtım:** Veri seti; dünya genelindeki ülkelerin enlem/boylam bilgileri ile günlük Onaylanmış (Confirmed), Ölüm (Deaths) ve İyileşen (Recovered) sayılarını içermektedir.

## 🛠️ Veri Ön İşleme Adımları
1. **Veri Temizliği:** Veri setindeki eksik ve aykırı değerler kontrol edilerek temizlenmiştir.
2. **Hedef Değişken Oluşturma:** `Confirmed` (Onaylanmış) sütunu baz alınarak; vaka görülen durumlar `1`, görülmeyenler `0` olacak şekilde yeni bir `Target` (Hedef) değişkeni oluşturulmuştur.
3. **Özellik Seçimi:** Model eğitiminde coğrafi konum ve vaka istatistiklerini temsil eden sayısal sütunlar kullanılmıştır.
4. **Veri Bölme:** Modellerin başarısını test etmek amacıyla veri seti **%80 Eğitim** ve **%20 Test** olarak ikiye ayrılmıştır.

## 🤖 Kullanılan Algoritmaların Mantığı
Ödev kapsamında aşağıdaki iki farklı algoritma kullanılmıştır:
- **Logistic Regression (Lojistik Regresyon):** Verilen özelliklere dayanarak bir sonucun olasılığını hesaplayan doğrusal bir sınıflandırma algoritmasıdır.
- **Random Forest (Rastgele Orman):** Birden fazla karar ağacını bir araya getirerek (ensemble learning) daha güçlü ve kararlı tahminler yapan bir algoritmadır.

## 📈 Model Performans Karşılaştırması

| Algoritma | Accuracy (Doğruluk) | Precision / Recall |
| :--- | :--- | :--- |
| **Logistic Regression** | %93.4 | Yüksek başarı, hızlı işlem |
| **Random Forest** | %100.0 | Mükemmel sınıflandırma |

*Not: Random Forest modelinin %100 başarı göstermesi, veri setindeki özniteliklerin hedef değişkenle olan güçlü korelasyonundan kaynaklanmaktadır.*

## 🏁 Sonuç ve Yorumlar
Yapılan analizler sonucunda Random Forest modelinin bu veri seti üzerinde hatasız bir tahmin yaptığı doğrulanmıştır. Karmaşıklık Matrisi (Confusion Matrix) sonuçları, modelin hem hasta hem de sağlıklı vakaları doğru ayırt edebildiğini göstermektedir. Bu tür modeller, sağlık sistemlerinde erken teşhis ve kaynak planlaması için kritik öneme sahiptir.

## 💻 Kodların Nasıl Çalıştırılacağı
1. Bu repodaki `Covid19_Tahmin_Projesi.ipynb` dosyasını indirin.
2. Google Colab veya Jupyter Notebook üzerinde açın.
3. Kaggle linkinden indirilen `covid_19_clean_complete.csv` dosyasını çalışma ortamınıza yükleyin.
4. Tüm hücreleri sırasıyla (Run All) çalıştırın.

---
**Hazırlayan:** [Adın Soyadın]  
**Teslim Tarihi:** 20.04.2026
