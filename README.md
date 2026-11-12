# Lentera Belajar AI — PWA (GitHub Pages)

Versi 1.0.0. Klien web yang dapat dipasang (PWA) dan berjalan luring untuk backend Google Apps Script + Google Sheets.

## Isi repositori (5 berkas)

| Berkas | Fungsi |
| --- | --- |
| `index.html` | Seluruh aplikasi (HTML + CSS + JS dalam satu berkas, tanpa CDN) |
| `manifest.json` | Manifest PWA (nama, warna, ikon) |
| `sw.js` | Service worker — cache shell untuk mode luring |
| `icon-512.png` | Ikon aplikasi |
| `README.md` | Berkas ini |

## Cara memasang

1. Buat repositori GitHub baru (boleh privat bila akun Anda mendukung Pages privat), unggah kelima berkas ke *root* cabang `main`.
2. **Settings → Pages → Build and deployment → Source: Deploy from a branch → `main` / `(root)` → Save.**
3. Tunggu ±1 menit, buka `https://<nama-akun>.github.io/<nama-repo>/`.
4. Pada layar pertama, tempel **URL Web App Apps Script** (berakhiran `/exec`).
   Agar pengguna tidak perlu mengetiknya, buka `index.html`, cari `const DEFAULT_GAS_URL = '';` lalu isi URL di antara tanda kutip.

## Memperbarui

Setiap kali `index.html` diganti, naikkan nilai `CACHE` di `sw.js` (mis. `lentera-v1.0.0-2`) agar perangkat pengguna mengambil versi baru.

## Yang bekerja saat luring

Membuka aplikasi, membaca kursus yang sudah pernah dibuka, kartu ingatan, catatan, timer fokus, rencana belajar, dan riwayat tutor yang tersimpan. Perubahan (centang pelajaran, kartu, catatan) masuk antrean dan dikirim otomatis saat daring.
Tutor AI, kuis, pembayaran, dan login pertama memerlukan internet.

## Lisensi

Perangkat lunak berlisensi komersial — lihat `LISENSI.txt` pada paket penyedia. Memuat `qrcode-generator` © Kazuhiko Arase (MIT).
