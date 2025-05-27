# VeriBilimiProje
Proje Başlığı:
IMDb Top 250 Filmleri Üzerine Veri Analizi ve IMDb Puan Tahmin Modeli

Proje Açıklaması:
Bu projede, IMDb’nin Top 250 listesindeki filmler üzerinden veri analizi gerçekleştirilmiş ve film puanlarını etkileyen faktörler incelenmiştir. Film türü, yönetmen, vizyon yılı ve süresi gibi değişkenler kullanılarak doğrusal regresyon modeli ile IMDb puanı tahmin edilmeye çalışılmıştır. Ayrıca görsel analizlerle film türleri, yıllar ve yönetmenler bazında IMDb eğilimleri ortaya konmuştur.

Kullanılan Yöntemler:

1. Veri Toplama ve Temizleme:

IMDb Top 250 listesindeki filmler web scraping yoluyla çekilmiş ve pandas kütüphanesiyle işlenmiştir.

Süre (Runtime) sütunu metinsel ifadelerden arındırılarak sayısal forma çevrilmiştir.

Kategorik değişkenler (tür, yönetmen) sayısallaştırılmıştır (LabelEncoder).

2. Veri Görselleştirme:

Türlere göre IMDb puanı dağılımı (boxplot)

Korelasyon matrisi (heatmap)

Yıllara göre IMDb puanı değişimi (lineplot)

Yönetmen–tür bazlı IMDb ortalaması (pivot heatmap)

Gerçek vs. tahmin IMDb puanı (scatter plot)

3. İstatistiksel Test:

ANOVA testi ile film türlerinin IMDb puanı üzerindeki etkisi analiz edilmiştir.

4. Makine Öğrenmesi – Doğrusal Regresyon:

Bağımsız değişkenler: Tür, yönetmen, süre, yıl

Bağımlı değişken: IMDb puanı

Modelin başarısı R² ve RMSE değerleriyle ölçülmüştür.

Özet Sonuçlar:

ANOVA testi sonucuna göre film türü IMDb puanını istatistiksel olarak anlamlı biçimde etkilemektedir.

Özellikle Frank Darabont, Christopher Nolan ve Quentin Tarantino gibi yönetmenler yüksek ortalama puanlara sahiptir.

Yıllar bazında analizde, 1970–1990 arası filmlerin genel olarak daha yüksek puanlandığı, 2000 sonrası dönemde ise puanların sabitlenme eğiliminde olduğu gözlemlenmiştir.

Regresyon modelinin performansı düşüktür:
  R² = 0.0211 → Model IMDb puanlarındaki değişkenliğin yalnızca %2’sini açıklayabilmiştir.
  RMSE = 0.3423 → Ortalama tahmin hatası yaklaşık 0.34 puandır.

Tahmin-gözlem karşılaştırma grafiğinde modelin çoğu filmi ortalama değerde tahmin ettiği, dolayısıyla varyasyonu yakalayamadığı görülmüştür.

İyileştirme Önerileri:

Oyuncular, ödüller, metascore gibi yeni nitelikler eklenerek model zenginleştirilebilir.

One-hot encoding gibi daha uygun veri temsil yöntemleri tercih edilebilir.

XGBoost gibi daha güçlü regresyon algoritmaları denenebilir.

IMDb Top 250 dışında daha geniş veri kümeleriyle (örneğin 1000+ film) model eğitimi yapılabilir.

Genel Değerlendirme:
Doğrusal regresyon modeli IMDb puanlarını başarılı bir şekilde tahmin edememiştir. Ancak yapılan analizler, film türü ve yönetmen gibi özelliklerin puanlar üzerinde etkili olduğunu göstermiştir. Modelin geliştirilmesi için daha geniş veri, daha zengin özellikler ve gelişmiş algoritmalar önerilmektedir.
