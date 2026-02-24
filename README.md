## E-Ticaret Dönüşüm Hunisi ve Pazarlama Kanalları Performans Analizi (BigQuery - SQL)
## Proje Özeti
Bu proje, bir e-ticaret platformunun ham kullanıcı verilerini (user events) kullanarak müşteri yolculuğunu optimize etmeyi ve pazarlama bütçesi verimliliğini artırmayı hedefleyen uçtan uca bir veri analizi çalışmasıdır. Projenin temel odak noktası, kullanıcıların web sitesine giriş anından satın alma aşamasına kadar geçen süreci (Sales Funnel) dijital izler üzerinden takip ederek, sistemdeki darboğazları ve yüksek performanslı trafik kaynaklarını tespit etmektir.
## Veri Seti İçeriği
File: user_events.csv
-	Etkinlik İzleri: Kullanıcıların user_id bazlı tüm dijital ayak izleri.
-	Huni Basamakları: page_view, add_to_cart ve purchase gibi kritik dönüşüm adımları.
-	Trafik Kaynakları: Kullanıcının siteye geldiği kanal bilgisi (Email, Social, Organic).
-	Zaman ve Değer: İşlem tarihleri ve satın alma tutarları (amount).
## Temel Performans Göstergeleri 
-	Dönüşüm Oranı: Kullanıcıların görüntülemeden satın almaya geçiş yüzdesi hesaplanarak genel satış başarısı ölçülmüştür.
-	Huni Kayıp Oranı: Her bir aşama (sepet, ödeme vb.) arasındaki kullanıcı kaybı tespit edilerek iyileştirilmesi gereken "darboğaz" noktaları belirlenmiştir.
-	Kanal Başına Dönüşüm: E-posta, sosyal medya ve organik trafik kaynaklarının satışa dönüşme verimliliği karşılaştırılmıştır.
-	Dönüşüm Süresi: Bir kullanıcının ilk etkileşiminden satın almaya kadar geçen ortalama süre (dakika bazında) analiz edilmiştir.
-	Ortalama Sipariş Değeri: Toplam gelirin toplam sipariş sayısına bölünmesiyle, müşteri başına elde edilen ortalama kazanç hesaplanmıştır.
## Analitik Odak Noktaları
-	 Huni Optimizasyonu: Kullanıcı yolculuğundaki sızıntı noktalarını ve müşteri kaybının ana nedenlerini tespit etmek.
-	 Kanal Verimliliği: Trafik kaynaklarının (E-posta, Sosyal Medya vb.) satışa dönüşme kalitesini ve verimliliğini karşılaştırmak.
-	 Davranışsal Zaman Analizi: İlk etkileşimden satın almaya kadar geçen süreyi ölçerek kullanıcı karar verme hızını analiz etmek.
-	Gelir ve Sepet Analizi: Toplam gelir ve ortalama sipariş değeri (AOV) üzerinden pazarlama harcamalarının geri dönüşünü değerlendirmek.
-	Veri Temelli Karar Destek: Teknik sonuçları; UX, Pazarlama ve Finans ekipleri için uygulanabilir stratejik önerilere dönüştürmek.
## İş Akışı
1.	Veri Hazırlama ve Yükleme
2.	SQL ile Veri İşleme ve Modelleme
3.	Görselleştirme (Tableau)
4.	Raporlama ve Stratejik Karar Desteği
## BigQuery SQL Sorgu Çıktıları
**1. Satış Hunisini ve Bu Huninin Farklı Aşamalarını Tanımlamak**

<img width="538" height="53" alt="Ekran Resmi 2026-02-23 08 20 57" src="https://github.com/user-attachments/assets/bfde9a71-8583-4347-92a9-3b0267e6343b" />


**2. Huni Boyunca Dönüşüm Oranları ve Kullanıcı Kayıp Analizi**

<img width="875" height="36" alt="Ekran Resmi 2026-02-23 08 23 32" src="https://github.com/user-attachments/assets/18519624-ab4c-4688-80eb-401902858f83" />


**3. Kaynağa Göre Satış Hunisi**

<img width="775" height="127" alt="Ekran Resmi 2026-02-23 08 26 44" src="https://github.com/user-attachments/assets/0967bd47-97b4-4031-b9b0-7ed3070adbbe" />


**4. Kullanıcının İlk Etkileşiminden Satın Almaya Kadar Geçen Sürenin Analizi**

<img width="646" height="52" alt="Ekran Resmi 2026-02-23 08 27 59" src="https://github.com/user-attachments/assets/5029fb13-c6ff-4f8d-a9fc-43141e8d9d45" />


**5. Satış Sürecinin Her Aşamasında Oluşan Gelir Analizi**

<img width="707" height="53" alt="Ekran Resmi 2026-02-23 08 29 13" src="https://github.com/user-attachments/assets/e4f2ad63-de9a-4083-bfc0-05335b9ae5d7" />


## Dasboard
https://public.tableau.com/app/profile/selin.serra.usta/viz/E-commerceConversionFunnelandMarketingChannelPerformanceAnalysis/Dashboard1

<img width="1799" height="1049" alt="Dashboard 1" src="https://github.com/user-attachments/assets/713d2ccc-5706-4a92-bbe2-4b091c99d2c7" />


## Önemli Bulgular
- **En Büyük Kayıp Noktası:** Kullanıcıların yaklaşık %70'inin "Sayfa Görüntüleme" ile "Sepete Ekleme" arasında kaybedildiği tespit edilmiştir. Bu, huninin en zayıf halkasıdır.
- **Teknik Akış Başarısı:** "Ödeme Bilgisi" aşamasından "Satın Alma" aşamasına geçiş oranı %92 gibi oldukça yüksek bir seviyededir. Bu durum, ödeme sisteminde teknik bir engel olmadığını gösterir.
- **Kanal Verimliliği:** Sosyal medya en yüksek trafik hacmini sağlarken, e-posta kanalı en yüksek satın alma dönüşüm oranına sahiptir.
- **Dönüşüm Hızı:** Satın alma işlemini tamamlayan kullanıcıların büyük bir çoğunluğunun ilk etkileşimden sonraki ilk 24 dakika içinde karar verdiği görülmüştür.
- **Sipariş Değeri ve Kanal İlişkisi:** Sadece dönüşüm oranı değil, Ortalama Sipariş Değeri bakımından da e-posta kanalının ücretli reklamlara göre daha yüksek hacimli sepetler oluşturduğu tespit edilmiştir.
- **Ödeme Adımı Sadakati:** Ödeme sayfasına gelen her 10 kullanıcıdan 9'u işlemi başarıyla tamamlamaktadır. Bu, ödeme güvenliği ve kullanıcı arayüzünün bu aşamada oldukça güven verici olduğunu gösterir.
## Derinlemesine İçgörüler
- **Harekete Geçirici Mesaj Eksikliği:** "Sayfa Görüntüleme" ile "Sepete Ekleme" arasındaki devasa fark, ürün detay sayfalarının kullanıcıyı ikna etmekte zorlandığını gösterir. 
- **Kanal Karakteristiği:** Sosyal medya trafiği "keşif" odaklıdır ve genellikle düşük bağlılık gösterir. Buna karşın e-posta trafiği, markaya daha önceden aşina olan "sadık kitle"den oluştuğu için yatırım getirisi (ROI) en yüksek kanaldır.
- **Kayıp Analizi:** "Sepet" ile "Ödeme Başlangıcı" arasındaki kayıplar, kullanıcıların sepete ürün ekledikten sonra kargo ücreti veya ek maliyetler gibi sürprizlerle karşılaşıp vazgeçmiş olabileceğine işaret eder.
## Aksiyon Planı
- **E-posta Listesini Büyütme:** Dönüşümü en yüksek kanal olduğu için, web sitesinde "e-posta bültenine kayıt olana indirim" gibi kurgularla bu listenin büyütülmesi önerilir.
- **Sepet Hatırlatma Senaryoları:** Sepete ürün ekleyip ödeme yapmayan kullanıcılar için otomatik "sepetinizde ürün kaldı" hatırlatmaları kurulmalıdır.
- **Hızlandırma:** Kullanıcıların çoğu 24 dakika içinde satın alma yaptığı için, bu süre zarfında kullanıcılara "sınırlı süreli teklifler" sunulabilir.
- **Bütçe Optimizasyonu:** Sosyal medya bütçesinin bir kısmının, dönüşüm oranı çok daha güçlü olan e-posta pazarlamasına aktarılması yatırım getirisini (ROI) artıracaktır.
## Sonuç
BigQuery ile gerçekleştirilen bu analiz, satış hunisindeki %70’lik kaybı ve e-posta kanalının yüksek ROI potansiyelini kanıtlamıştır. Çalışma; ham veriyi stratejik içgörüye dönüştürerek, pazarlama bütçesinin optimizasyonu ve satış verimliliğinin artırılması için somut bir rehber sunmaktadır.


