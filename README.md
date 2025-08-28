BlazeDemo JMeter Test Plan 🚀

Bu proje, BlazeDemo
 sitesi üzerinde JMeter kullanılarak yük testi gerçekleştirmek için hazırlanmış bir test planını içerir.

🎯 Senaryo

Thread Group → 100 kullanıcı

Constant Timer → Her istek arası 5 saniye bekleme

Loop Controller (2x) → URL1 / ve URL5 /vacation.html iki tur çalıştırılır

Assertion → URL3 /password/reset için yanıt doğrulama

Dinamik Label → URL2 /login label’ı içinde gün- ay- yıl gösterilir (dd-MM-YYYY)

Listeners (3 adet) → Summary Report, View Results Tree, Graph Results

📂 Test Plan Yapısı

### Thread Group (100 Users)
- **Constant Timer (5s)**
- **Loop Controller (2 Loops)**
  - URL1 → /
  - URL5 → /vacation.html
- URL2 → /login (Label: dd-MM-YYYY)
- URL3 → /password/reset (+ Assertion)
- URL4 → /register

### Listener’lar
- Summary Report
- View Results Tree
- Graph Results
<img width="1919" height="988" alt="image" src="https://github.com/user-attachments/assets/e7531490-05f9-4cc1-99e8-a94f6ac9d510" />


⚙️ Kurulum

Apache JMeter
 indirip kurun.

Repo’yu klonlayın:

git clone https://github.com/kullanici/blazedemo-jmeter.git
cd blazedemo-jmeter


blazedemo_test_plan.jmx dosyasını JMeter ile açın.

🧪 Çalıştırma

GUI ile test ettikten sonra Non-GUI modda koşup HTML raporu almak için:

# Testi çalıştır
jmeter -n -t blazedemo_test_plan.jmx -l results.jtl

# HTML raporu oluştur
jmeter -g results.jtl -o html-report


📊 Sonuçları görmek için: html-report/index.html dosyasını tarayıcıda açın.

📸 Örnek Çıktılar
Graph Results

HTML Rapor

 .\jmeter.bat -g C:\Users\aksoy\OneDrive\Masaüstü\apache-jmeter-5.6.3\apache-jmeter-5.6.3\bin\results\result.jtl -o C:\Users\aksoy\OneDrive\Masaüstü\apache-jmeter-5.6.3\apache-jmeter-5.6.3\bin\results\html_report

<img width="1919" height="874" alt="image" src="https://github.com/user-attachments/assets/5aac442f-e21c-4ca1-9679-a039ae797e9a" />

<img width="1919" height="870" alt="image" src="https://github.com/user-attachments/assets/fdcc8cbf-8c11-45de-8144-31675acec650" />

 <img width="1919" height="869" alt="image" src="https://github.com/user-attachments/assets/5c7200d1-e3d6-4a4f-917d-738cc93dcba4" />


✅ Bu test planı ile BlazeDemo üzerinde yük testi yapılabilir, grafiksel sonuçlar elde edilebilir ve HTML rapor üretilebilir.
