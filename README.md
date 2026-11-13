# ✍️ TintaKertas — Text to Handwriting Generator

**TintaKertas** adalah aplikasi web interaktif berbasis *client-side* untuk mengubah teks digital menjadi gambar tulisan tangan yang tampak realistis di atas kertas. Dirancang dengan kontrol tata letak presisi, dukungan unggah font dan latar kertas kustom, serta simulasi ketidakrapian alami tulisan tangan dan aliran tinta bolpoin.

---

## ✨ Fitur Utama

- **Simulasi Tulisan Tangan Organik (Natural Jitter)**:
  - Variasi kemiringan (*skew*), rotasi, skala huruf (*scale bounce*), dan kerapatan spasi antar karakter/kata.
  - Kontrol **Kemiringan Baris (`Line Slant`)** untuk efek tulisan yang perlahan melorot ke bawah atau menanjak.
  - Kontrol **Tembus Batas Garis & Margin** agar tulisan dapat melampaui garis buku maupun margin kanan secara alami.
  - **5 Preset Gaya Tulisan**: *Rapi Pelajar*, *Normal Santai*, *Ngebut / Buru-buru*, *Miring Melorot*, dan *Berantakan Bebas*.
- **Fluktuasi Tinta Bolpoin Realistis**:
  - Simulasi kepekatan tinta yang tidak konsisten (kadang pekat tebal, kadang sedikit memudar) seperti aliran bola tinta pulpen asli.
  - Pilihan warna tinta pulpen standar (Biru, Hitam, Merah, Hijau, Ungu) maupun pemilih warna kustom (*color picker*).
- **Koleksi Font & Unggah Font Sendiri**:
  - Tersedia 8 font tulisan tangan bawaan (*Caveat, Kalam, Patrick Hand, Indie Flower, Shadows Into Light, Architects Daughter, Dancing Script, Homemade Apple*).
  - Mendukung unggah file font pribadi berformat **`.ttf`, `.otf`, `.woff`, atau `.woff2`**.
- **Kertas Bawaan & Latar Belakang Kustom**:
  - Preset kertas **Bergaris (Buku Tulis)** yang otomatis menyesuaikan jarak garis dengan *line-height*, **Polos HVS**, **Kotak-kotak (Grid)**, **Titik-titik (Dotted)**, dan **Vintage**.
  - Unggah gambar latar kertas sendiri (**`.jpg`, `.png`, `.webp`**) dengan 4 mode penyesuaian (*Cover*, *Stretch*, *Contain*, *Repeat*).
- **Kontrol Layout Presisi & Ekspor**:
  - Pengaturan ukuran huruf, tinggi baris, posisi vertikal awal teks (*offset*), jarak huruf/kata, margin keempat sisi, serta rasio halaman (**A4, US Letter, F4/Folio, Persegi 1:1**).
  - Ekspor langsung ke **PNG resolusi tinggi (2x scale)** atau **Cetak (`Ctrl+P`)**.
- **100% Privasi (Client-Side)**:
  - Seluruh proses rendering, font unggahan, dan gambar kertas diproses langsung di browser pengguna tanpa dikirim ke server mana pun.

---

## 🚀 Cara Hosting di GitHub Pages (`username.github.io`)

1. **Buat Repositori Baru** di GitHub (misalnya bernama `tintakertas` atau `USERNAME.github.io`).
2. **File Repositori**:
   - `index.html` (Aplikasi utama + Konten SEO & FAQ)
   - `robots.txt` (Instruksi crawler mesin pencari Google/Bing)
   - `sitemap.xml` (Peta situs XML untuk indeks pencarian)
   - `README.md` (Dokumentasi proyek)
3. **Konfigurasi URL SEO (Opsional namun Disarankan)**:
   - Buka `robots.txt` dan `sitemap.xml`, ganti `https://username.github.io/` dengan alamat repositori aktif Anda (misal `https://username.github.io/tintakertas/`).
4. **Upload File ke Repositori**:
   - Unggah semua file melalui antarmuka web GitHub atau Git CLI:
     ```bash
     git init
     git add index.html robots.txt sitemap.xml README.md
     git commit -m "feat: TintaKertas generator dengan optimasi SEO & robots.txt"
     git branch -M main
     git remote add origin https://github.com/USERNAME/NAMA-REPO.git
     git push -u origin main
     ```
5. **Aktifkan GitHub Pages**:
   - Buka tab **Settings** → **Pages** di repositori GitHub Anda.
   - Pada bagian **Build and deployment** → **Source**, pilih **Deploy from a branch**.
   - Pilih branch **`main`** dan folder **`/ (root)`**, lalu klik **Save**.
   - Tunggu 1–2 menit hingga situs Anda aktif di `https://USERNAME.github.io/NAMA-REPO/`.

---

## 🔍 Optimasi Mesin Pencari (SEO) & Kata Kunci

Aplikasi ini telah dioptimalkan secara teknis dan semantik untuk meranking berbagai variasi kata kunci penelusuran (termasuk kata kunci tidak baku/panjang) di Google:
- **Kata Kunci Utama & Variasi Long-Tail**:
  - *"font tulistangan generator"*
  - *"mengetik tulisan"*
  - *"menulis dengan mengetik"*
  - *"ngetik tulisan tangan"*
  - *"bot nulis tangan"*
  - *"ubah ketikan jadi tulisan tangan"*
  - *"generator tulisan tangan di kertas bergaris"*
  - *"salin ketikan ke buku tulis"*
- **Teknis SEO yang Disertakan**:
  - `robots.txt` ramah crawler dengan tautan ke `sitemap.xml`.
  - `sitemap.xml` standar Schema.org / Sitemaps Protocol.
  - JSON-LD Structured Data Schema (`WebApplication` & `FAQPage`) untuk mengaktifkan Rich Snippets di Google SERP.
  - Bagian konten panduan & FAQ interaktif native HTML (`<details>`) di halaman utama tanpa memberatkan performa rendering.

---

## 🛠️ Teknologi yang Digunakan

- **HTML5 & Vanilla JavaScript (ES6+)** — Tanpa dependensi *build tool* atau framework berat, siap dijalankan langsung sebagai file statis.
- **Tailwind CSS (CDN)** — Tata letak responsif untuk perangkat desktop maupun mobile.
- **html2canvas** — Rendering kanvas kertas dan tulisan tangan menjadi berkas PNG siap unduh.
- **CSS Font Loading API (`FontFace`)** — Memuat file font lokal pengguna secara dinamis di browser.

---

## 📄 Lisensi

Proyek ini bersifat terbuka (*open-source*) dan bebas digunakan maupun dimodifikasi untuk keperluan pribadi maupun pendidikan.