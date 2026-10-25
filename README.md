# Website PT. Sasana Bersaudara Indonesia — sasanabersaudaraind.id

Website statis (HTML/CSS/JS murni, tanpa perlu build). Siap di-host di GitHub Pages.

## Cara pasang di GitHub Pages

1. Buat repository baru di GitHub, misalnya `sasanabersaudaraind.id` (atau nama lain).
2. Upload semua isi folder ini ke repository:
   - `index.html`
   - `manifest.webmanifest`, `sw.js`, `robots.txt`, `sitemap.xml`
   - folder `assets/` (beserta seluruh isinya, termasuk `assets/icons/`)
3. Di repository, buka **Settings → Pages**.
4. Pada bagian **Build and deployment**, pilih Source: **Deploy from a branch**, Branch: `main`, folder `/ (root)`, lalu **Save**.
5. Tunggu 1–2 menit, website akan online di `https://<username>.github.io/<nama-repo>/`.
6. (Opsional) Untuk domain sendiri `sasanabersaudaraind.id`: di Settings → Pages isi **Custom domain** dengan `sasanabersaudaraind.id`, lalu di penyedia DNS domain tambahkan record yang diarahkan GitHub (A record ke IP GitHub Pages / CNAME ke `<username>.github.io`).

## Yang masih perlu dilengkapi

- Nomor telepon/WhatsApp resmi perusahaan (di bagian Kontak footer masih tertulis "(akan dilengkapi)").
- Alamat kantor lengkap bila ingin ditampilkan.
- Alamat email `info@sasanabersaudaraind.id` — sesuaikan bila berbeda.

## Struktur

- `index.html` — seluruh halaman (Beranda, Tentang, Layanan, Keunggulan, Profil/Visi-Misi/Nilai PRIMA, Klien & Proyek, Galeri, Kontak)
- `assets/` — logo SBI, logo klien, dan foto galeri
- `assets/icons/` — ikon aplikasi (favicon & PWA) dari simbol logo SBI

## SEO & PWA

- SEO: meta description & keywords, canonical ke `https://sasanabersaudaraind.id/`, Open Graph/Twitter Card, data terstruktur JSON-LD (ProfessionalService), `robots.txt`, dan `sitemap.xml`. Setelah domain aktif, daftarkan ke Google Search Console dan kirim sitemap-nya.
- PWA: website dapat di-"install" sebagai aplikasi di HP/desktop (manifest + service worker) dan tetap bisa dibuka saat offline setelah kunjungan pertama. PWA membutuhkan HTTPS — GitHub Pages sudah menyediakannya.
- Catatan: bila nanti mengedit `index.html`, naikkan versi cache di `sw.js` (mis. `sbi-cache-v2`) agar pengunjung menerima versi terbaru.
