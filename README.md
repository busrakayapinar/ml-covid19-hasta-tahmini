# ml-covid19-hasta-tahmini
Bu proje, Kaggle üzerinden alınan gerçek bir COVID-19 veri seti kullanılarak, bir kişinin vaka durumunu tahmin eden uçtan uca bir makine öğrenmesi sürecini içermektedir.
veri seti linki:https://www.kaggle.com/datasets/meirnizri/covid19-dataset
Proje Özeti
Bu çalışmada, COVID-19 verileri kullanılarak lojistik regresyon ve karar ağacı tabanlı modeller eğitilmiştir. Amaç, veri setindeki diğer değişkenleri kullanarak vaka olup olmadığını en yüksek doğrulukla tahmin etmektir.
Veri Seti Analizi (EDA)
Veri Kaynağı: COVID-19 Clean Complete (Kaggle)

İnceleme: Veri setinde lokasyon verileri (Enlem/Boylam) ve vaka istatistikleri (Onaylanmış, Ölüm, İyileşen) incelenmiştir.

Görselleştirme: Vaka sayılarının dağılımı Seaborn kütüphanesi ile görselleştirilerek veri setinin dengesi kontrol edilmiştir.
Confirmed sütunu kullanılarak, vaka olan durumlar 1, olmayanlar 0 olarak işaretlenip Target değişkeni oluşturulmuştur.

Veri seti, modellerin başarısını tarafsız ölçebilmek adına %80 Eğitim ve %20 Test verisi olarak bölünmüştür.
Proje kapsamında iki farklı algoritma karşılaştırılmıştır:
Algoritma,Accuracy (Doğruluk)
Logistic Regression,%93.4
Random Forest,%100.0
Sonuç ve Değerlendirme
Logistic Regression: %93.4 gibi yüksek bir başarı göstermiştir ancak bazı vakaları kaçırabildiği gözlemlenmiştir.

Random Forest: %100 doğruluk oranı ile en iyi sonucu vermiştir. Bu durum, modelin veri setindeki parametreler arasındaki ilişkiyi mükemmel şekilde öğrendiğini göstermektedir.

Karmaşıklık Matrisi: Random Forest modelinin hata yapmadan tüm sınıfları doğru tahmin ettiği matris üzerinde doğrulanmıştır.
Gereksinimler
Kodların çalışması için aşağıdaki Python kütüphaneleri gereklidir:

pandas, numpy, matplotlib, seaborn, scikit-learn
