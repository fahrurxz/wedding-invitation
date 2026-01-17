# Website Undangan Pernikahan - undanganresmi.my.id

Website undangan pernikahan digital yang dikonversi dari WordPress ke static site untuk deployment di GitHub Pages.

## 📋 Struktur Folder

```
undanganresmi.my.id/
├── index.html                 # Halaman utama (dari motion-02/index.html)
├── CNAME                      # Konfigurasi domain custom
├── assets/                    # Folder untuk semua aset
│   ├── css/                  # File CSS
│   ├── js/                   # File JavaScript
│   ├── images/               # Gambar dan foto
│   └── fonts/                # Custom fonts
├── wp-content/               # Aset WordPress (CSS, JS, images)
│   ├── plugins/              # CSS & JS dari plugin
│   ├── themes/               # CSS & JS dari tema
│   └── uploads/              # Upload files (gambar, dll)
└── README.md                 # Dokumentasi ini
```

## 🚀 Deployment ke GitHub Pages

### 1. Persiapan Repository
```bash
git init
git add .
git commit -m "Initial commit: Wedding invitation website"
```

### 2. Buat Repository di GitHub
- Buka GitHub dan buat repository baru
- Nama repository bisa apa saja (misalnya: `wedding-invitation`)
- Jangan centang "Initialize this repository with a README"

### 3. Push ke GitHub
```bash
git remote add origin https://github.com/username/wedding-invitation.git
git branch -M main
git push -u origin main
```

### 4. Aktifkan GitHub Pages
1. Buka repository di GitHub
2. Klik **Settings** > **Pages**
3. Di bagian **Source**, pilih branch `main` dan folder `/ (root)`
4. Klik **Save**
5. Website akan tersedia di: `https://username.github.io/wedding-invitation/`

## 🌐 Setup Custom Domain (undanganresmi.my.id)

### Di GitHub:
1. Buka **Settings** > **Pages**
2. Di bagian **Custom domain**, masukkan: `undanganresmi.my.id`
3. Klik **Save**
4. Centang **Enforce HTTPS** (tunggu beberapa menit setelah DNS aktif)

### Di Domain Provider:
Tambahkan DNS records berikut:

**A Records** (untuk root domain):
```
@   A   185.199.108.153
@   A   185.199.109.153
@   A   185.199.110.153
@   A   185.199.111.153
```

**CNAME Record** (untuk www):
```
www   CNAME   username.github.io.
```

Ganti `username` dengan username GitHub Anda.

## 📝 Catatan Penting

1. **File index.html**: File utama berada di root folder (dipindahkan dari motion-02/)
2. **Aset WordPress**: Folder wp-content/ berisi semua CSS, JS, dan images dari WordPress
3. **No Backend**: Website ini sepenuhnya static, tidak ada database atau server-side processing
4. **Manajemen Tamu & Link Personal**: Lihat file **`GUEST-MANAGEMENT.md`** untuk sistem:
   - ✅ Tambah/edit data tamu di Google Sheets
   - ✅ Generate link personal: `https://undanganresmi.my.id/?to=Nama%20Tamu`
   - ✅ Nama tamu otomatis muncul di undangan
   - ✅ Tracking siapa yang sudah buka
5. **Form Ucapan/Wishes**: Lihat file `FORM-SOLUTIONS.md` untuk 4 cara mengatasi form:
   - ✅ Google Forms (PALING MUDAH & GRATIS)
   - ✅ Formspree (Design Custom)
   - ✅ Google Sheets API (Advanced)
   - ✅ Firebase (Real-time)

## 🔧 Maintenance

### Update Konten
Untuk mengubah konten:
1. Edit file `index.html`
2. Commit changes: `git commit -am "Update content"`
3. Push ke GitHub: `git push`
4. Website akan otomatis terupdate dalam beberapa menit

### Optimasi
- Compress gambar sebelum upload (gunakan TinyPNG atau ImageOptim)
- Minify CSS dan JS untuk performa lebih baik
- Gunakan CDN untuk jQuery dan library lainnya

## 📱 Fitur Website

- ✅ Responsive design (Mobile & Desktop)
- ✅ Gallery foto
- ✅ Countdown timer
- ✅ Google Maps integration
- ✅ Background music
- ✅ Animasi smooth scroll
- ⚠️ Form wishes (perlu konfigurasi backend)

## 🎨 Kustomisasi

File yang sering diubah:
- `index.html` - Konten teks, nama, tanggal, dll
- `assets/css/` - Style dan warna tema
- `assets/images/` - Foto couple dan dekorasi

## 📞 Support

Untuk pertanyaan atau bantuan, hubungi:
- Website: https://alfatihdigital.id/
- WhatsApp: 08131415215
- Instagram: @alfattih.id

---

**Made with 💗 by Alfatih Digital**
