## Kapasitif Dokunma Sensörü ve Uygulamaları

### İçerik:

* Projenin adı ve kısaca amacı: “İnsan dokunuşunu algılayarak makineyi durdurmak veya güvenlik sağlamak.”
* Kapasitif sensörlerin genel tanımı: “Parmağımızın dokunduğu yüzeydeki kapasite değişimini ölçen sistem.”

### Endüstriyel Makine Güvenliği İhtiyacı:

*   Dikiş makineleri, testere sistemleri, budama makasları gibi hızlı kesici veya dikiş yapan aletlerde güvenlik gereksinimi.
*   İnsan eli dokunduğunda (farkında olmadan yaklaştığında değil, gerçekten temas ettiğinde) makineyi durdurmak.

### Neden Kapasitif Algılama?

*   Mekanik sensörlere göre daha az aşınma ve daha hassas tespit.
*   Üretim maliyeti görece düşük; ufak modifikasyonlarla uygulanabilir.


## Kapasitif Dokunma Nedir?

* 1) Kapasite Kavramı:
    * İki yüzey (sensör elektrodu + insan vücudu) arasında oluşan küçük bir elektriksel yük depolama yeteneği.
    * İnsan vücudu toprak gibi davranarak küçük de olsa bir kapasite oluşturur.

* 2) İnsan Eli Dokununca Ne Olur?
    * Metal yüzeye parmak değdiğinde, o noktada kapasite artar.
    * Devre bu kapasite artışını tespit eder ve “dokunuldu” şeklinde sinyal üretir.

* 3) Yaklaşma vs Temas:
    * Bazı kapasitif sensörler parmak yaklaşınca dahi algılar (yakınlık sensörü).
    * Bu projede hedef: Sadece temas anında algılama.


## OPAMP Rolü ve Çalışma Prensibi

* 1) Op Amp (Operation Amplifier) Nedir?
    * Çok küçük gerilim farklarını büyültmeye yarayan elektronik devre bloğu.

* 2) Kapasitif Ölçümde Nasıl Kullanılıyor?
    * Elektrotu yüksek empedanslı bir girişten izleyerek, dokunma anındaki kapasite/gerilim değişimini algılar.
    * Devrenin geri beslemesi ve ayarlanan eşik dirençleri sayesinde “dokunuldu” sinyalini üretir.

## Dikiş Makinesinde Güvenlik

* 1) Makine Yüzeyine Elektrot Yerleştirme:
    * Makine ayağının üstüne ve altına iki ayrı bobin/kablo çekiliyor.
    * Koruyucu dış yüzey (yalıtım) kaldırılarak metal kısım insan eliyle doğrudan temas edebilecek hale geliyor.

* 2) Dokunma Algılandığında Ne Oluyor?
    * Devre anında çıkışını aktif hâle getirerek makineyi durdurur (örneğin motoru keser).

* 3) Endüstriyel Sorunlar ve Çözüm:
    * Birçok makine aynı anda açılınca, hatta besleme hattında parazit oluşuyor.
    * Bu parazitler bazen sanki “dokunulmuş” gibi yanlış tetikleme yaratabiliyor.
    * Çözüm Önerileri: Pil veya izole güç kaynağı ile besleme, filtre devreleri, kablolama düzeni, daha düşük gürültülü op amp/komparatör kullanımı.

## Avantajlar ve Dezavantajlar

### Avantajlar;
* 4 mikrosaniye algılama, 4 milisaniye(Role) tepki süresi.
* Temassız switch’lere kıyasla daha hassas ve daha az aşınma.
* Farklı yüzeylere uygulanabilme (metal, bobin sargısı).
* Görece basit devrelerle gerçekleştirilebilme.

### Dezavantajlar;
* Endüstriyel ortamlarda gürültü/parazit hassasiyeti.
* Farklı kumaş tiplerinde değişken iletkenlikten dolayı hatalı tetiklenme.
* Kumaşta oluşan statik elektrikten dolayı hatalı tetiklenme