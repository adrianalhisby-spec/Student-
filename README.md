# ITS NU Sriwijaya — Student Life Portal
### Versi Web + Android (PWA)

Portal modern & interaktif **Kehidupan Mahasiswa** ITS NU Sriwijaya Sumsel.

---

## 1. Versi WEB

### Cara Jalankan Lokal
```bash
cd its-nu-student-life
python3 -m http.server 8080
# buka http://localhost:8080
```

Atau klik dua kali `index.html`.

### Deploy Online (Gratis)
- **Netlify**: Drag & drop folder ke netlify.com
- **Vercel**: Import project
- **GitHub Pages**: Push lalu aktifkan Pages

---

## 2. Versi ANDROID (PWA - Install seperti Aplikasi)

Website ini sudah menjadi **Progressive Web App (PWA)**.

### Cara Install di Android:
1. Buka website di **Google Chrome** (Android)
2. Tunggu beberapa detik → muncul banner "Add to Home screen" / "Install app"
3. Atau klik tombol **"📲 Install Aplikasi"** di pojok kanan bawah
4. Atau: Menu Chrome (⋮) → **Install app** / **Add to Home screen**

Setelah di-install:
- Muncul icon di home screen seperti aplikasi biasa
- Buka full-screen (tanpa address bar)
- Bisa dipakai offline (halaman utama tersimpan)

### Fitur Android-ready:
- Manifest.json
- Service Worker (offline support)
- Theme color hijau NU
- App icon 192px & 512px
- Install prompt otomatis
- Standalone display mode

---

## 3. Buat APK Native (Opsional - Capacitor)

Kalau ingin file `.apk` yang bisa di-upload ke Play Store:

```bash
# 1. Install Capacitor
npm init -y
npm install @capacitor/core @capacitor/cli @capacitor/android
npx cap init "ITS NU Student Life" "ac.id.itsnusriwijaya.studentlife"

# 2. Copy web files ke folder www
mkdir www
cp -r *.html css js icons manifest.json sw.js www/

# 3. Add Android platform
npx cap add android
npx cap sync

# 4. Buka di Android Studio
npx cap open android
```

Lalu di Android Studio → Build → Build Bundle(s) / APK(s).

---

## Struktur Project

```
its-nu-student-life/
├── index.html
├── kehidupan-mahasiswa.html
├── ... (halaman lain)
├── css/style.css
├── js/main.js
├── icons/
│   ├── icon-192.png
│   ├── icon-512.png
│   └── icon.svg
├── manifest.json          ← PWA config
├── sw.js                  ← Service Worker
├── package.json
├── netlify.toml
└── README.md
```

---

## Fitur Utama
- Loading screen + animasi smooth
- Dark / Light mode
- Sticky nav + mobile menu
- Typing effect, counter animasi, scroll reveal
- Timeline "Sehari di ITS NU"
- Filter gallery, testimoni slider
- Form kontak
- **Bisa di-install sebagai aplikasi Android**

---

**Identitas**: Institut Teknologi dan Sains Nahdlatul Ulama Sriwijaya Sumatera Selatan  
Alamat: Jl. Talang Kerangga No.411, Palembang 30129  
Rektor: Prof. Dr. Zainal Effendi, SH., MM., DBA
