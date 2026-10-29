# P3K-finall-243026037
PROJEK: Aplikasi Panduan Pertolongan Pertama (P3K) Offline

Link deployment: https://ephemeral-sprinkles-f38c53.netlify.app

Arsitekturnya: 
  1. HTML5 : buat kerangka programnya (di projek ini pakai single page application)
  2. CSS3 : untuk tampilan UI mobile first dan responsif
  3. Vanilla.js : logika aplikasi, manipulasi DOM, dan pencarian data
  4. Firebase : untuk simpan data bagian record medis, secara otomatis menyimpan data saat terhubung internet
  5. Manifest.json dan sw.js : setup buat install ke layar hp ataupun perangkat mobile lainnya, saat offline memunculkan data                   chache yang udah disimpan sw.js saat online
  6. Netlify : buat deploy sistem nya biar bisa dibuka di browser hp dan diinstall dengan bantuan manifest.json
 
 Fitur Utama Sistem:
   1. Panduan pertolongan pertama (data ditanam langsung dalam js menggunakan array sehingga bisa diakses secara offline)
   2. Fitur pencarian cepat (memfilter data secara cepat berdasarkan gejala atau judul saat user mengetik)
   3. Catatan medis (user bisa menyimpan panduan pertolongan penting terutama kalau memiliki anggota keluarga dengan riwayat                     penyakit tertentu, saat offline disimpan secara localstorage sebagai fallback dan disinkronkan dengan firebase jika ada                    internet)
   4. Button darurat SOS (integrasi protokol "tel:" untuk memanggil ambulance)
   5. Progresive Web App (PWA) (membuat apk ini bisa diinstall di home screen hp dan dijalankan secara standalone (full layarr tanpa             adress bar browser)
   6. Service worker chaching (menchache data gambar saat online biar bisa tetep muncul waktu offline)

Struktur Proyek: 
```text
p3k-offline-app/
├── index.html          # File utama aplikasi (berisi HTML, CSS, dan JS)
├── manifest.json       # Konfigurasi metadata PWA
├── sw.js               # Service Worker untuk fitur offline & caching
├── image/              # Folder aset gambar ilustrasi medis
── screenshots/        # Dokumentasi tangkapan layar aplikasi

Cara jalanin APK:
1. download atau clone repo ini
2. buka file index.html lewat browser
3. untuk pengalaman yang lebih baik, buka pakai VS code dan jalankan lewat live server atauu deploy menggunakan netlify atau vercel
4. jika di deploy nanti akan muncul pop up untuk install ke home screen
5. setelah install berhasil, akses langsung di home screen perangkat
6. untuk penggunaan pertama, bukaa saat ada internet agar service worker bisa melakukan chaching atau menyimpan gambar untuk digunakan saat offline
