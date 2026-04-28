# 🦠 COVID-19 Hasta Tahmini - Makine Öğrenmesi Projesi

Bu proje, gerçek bir COVID-19 veri seti kullanılarak, kişilerin vaka durumlarını (hasta olup olmadıklarını) makine öğrenmesi teknikleriyle tahmin etmeyi amaçlayan uçtan uca bir çalışmadır.

 📝 Proje Açıklaması
Bu çalışma kapsamında, pandeminin küresel verileri kullanılarak lojistik regresyon ve karar ağacı tabanlı modeller eğitilmiştir. Proje; veri analizi, eksik verilerin temizlenmesi, özellik mühendisliği ve model performanslarının karşılaştırılması aşamalarından oluşmaktadır.

 📊 Kullanılan Veri Seti
- veri seti linki:https://www.kaggle.com/datasets/meirnizri/covid19-dataset
- **Tanıtım:** Veri seti; dünya genelindeki ülkelerin enlem/boylam bilgileri ile günlük Onaylanmış (Confirmed), Ölüm (Deaths) ve İyileşen (Recovered) sayılarını içermektedir.

 🛠️ Veri Ön İşleme Adımları
1. **Veri Temizliği:** Veri setindeki eksik ve aykırı değerler kontrol edilerek temizlenmiştir.
2. **Hedef Değişken Oluşturma:** `Confirmed` (Onaylanmış) sütunu baz alınarak; vaka görülen durumlar `1`, görülmeyenler `0` olacak şekilde yeni bir `Target` (Hedef) değişkeni oluşturulmuştur.
3. **Özellik Seçimi:** Model eğitiminde coğrafi konum ve vaka istatistiklerini temsil eden sayısal sütunlar kullanılmıştır.
4. **Veri Bölme:** Modellerin başarısını test etmek amacıyla veri seti **%80 Eğitim** ve **%20 Test** olarak ikiye ayrılmıştır.

 🤖 Kullanılan Algoritmaların Mantığı
Ödev kapsamında aşağıdaki iki farklı algoritma kullanılmıştır:
- **Logistic Regression:** Verilen özelliklere dayanarak bir sonucun olasılığını hesaplayan doğrusal bir sınıflandırma algoritmasıdır.
- **Random Forest:** Birden fazla karar ağacını bir araya getirerek (ensemble learning) daha güçlü ve kararlı tahminler yapan bir algoritmadır.

 📈 Model Performans Karşılaştırması

| Algoritma | Accuracy (Doğruluk) | Precision / Recall |
| :--- | :--- | :--- |
| **Logistic Regression** | %93.4 | Yüksek başarı, hızlı işlem |
| **Random Forest** | %100.0 | Mükemmel sınıflandırma |

Not: Random Forest modelinin %100 başarı göstermesi, veri setindeki özniteliklerin hedef değişkenle olan güçlü korelasyonundan kaynaklanmaktadır.*

 🏁 Sonuç ve Yorumlar
Bu projede elde edilen sonuçlar, makine öğrenmesi modellerinin pandemi yönetimi ve sağlık teşhis süreçlerindeki potansiyelini açıkça ortaya koymaktadır. Yapılan analizler sonucunda şu çıkarımlara varılmıştır:

Model Başarısı: * Logistic Regression, doğrusal bir model olmasına rağmen %93.4 gibi oldukça yüksek bir doğruluk oranına ulaşmıştır. Bu durum, veri setindeki temel özelliklerin (enlem, boylam, vaka sayıları) hedef değişkenle güçlü bir korelasyona sahip olduğunu kanıtlamaktadır.

Random Forest modeli ise %100 doğruluk (Accuracy) ile kusursuz bir sınıflandırma yapmıştır. Bu başarının temel sebebi, Random Forest'ın karar ağaçları topluluğu kullanarak verideki karmaşık ve doğrusal olmayan ilişkileri çok daha iyi yakalayabilmesidir.

Vaka Tahmini ve Sağlık Sektöründeki Önemi: * Confusion Matrix (Karmaşıklık Matrisi) sonuçlarına göre, modeller "hasta" ve "sağlıklı" sınıflarını birbirinden keskin bir şekilde ayırabilmektedir. Sağlık sektöründe özellikle False Negative (hasta olan birine sağlıklı denmesi) riskinin düşük olması hayati önem taşır. Bu modeller, kısıtlı kaynakların (hastane yatağı, test kitleri vb.) doğru yönlendirilmesinde karar destek mekanizması olarak kullanılabilir.

Teknik Değerlendirme: * Random Forest'ın %100 başarı göstermesi, veri setinin model tarafından tamamen öğrenildiğini gösterir. Ancak gerçek dünya senaryolarında, modelin daha önce hiç görmediği (farklı varyantlar veya farklı demografik veriler gibi) verilerle de beslenerek "overfitting" (aşırı öğrenme) riskine karşı düzenli olarak test edilmesi önerilir.

Gelecek Çalışmalar: * Modelin başarısını daha da artırmak ve genelleştirmek adına; yaş, cinsiyet ve kronik hastalık geçmişi gibi daha spesifik hasta semptomlarını içeren veri setleri üzerinde de benzer çalışmalar yürütülebilir.

 💻 Kodların Nasıl Çalıştırılacağı
1. Bu repodaki `Covid19_Tahmin_Projesi.ipynb` dosyasını indirin.
2. Google Colab veya Jupyter Notebook üzerinde açın.
3. Kaggle linkinden indirilen dosyayı çalışma ortamınıza yükleyin.
4. Tüm hücreleri sırasıyla (Run All) çalıştırın.

Hazırlayan:Büşra Kayapınar 
