# Dewiii Bukett — MyBuqeet

Satu halaman statis untuk daftar harga dan pemesanan buket uang.

## Struktur

- `index.html` — seluruh aplikasi (HTML + Tailwind CSS + vanilla JS)
- `images/` — foto produk (5 file jpg)
- Tanpa build system, package manager, test, atau CI

## Development

- **Tidak perlu build.** Buka `index.html` langsung di browser.
- Tailwind CSS dan Lucide icons via CDN — butuh koneksi internet.
- Gunakan lokal dev server (misal `python -m http.server` atau Live Server) untuk hindari CORS pada gambar.

## Integrasi WhatsApp

- Nomor: `6289528332956` — dipakai di semua tautan WhatsApp di halaman.
- Alur checkout: item keranjang disimpan di `localStorage` key `bukettCart` → pesan diformat → redirect ke `wa.me`.
- Array `products` inline di `index.html` (`index.html:497`) adalah sumber utama data produk.

## Konvensi

- Harga disimpan sebagai string seperti `"45K"` — `getPriceValue()` menghapus karakter non-angka.
- Semua gambar (hero + produk) ada di `images/` dengan nama deskriptif (`hero.jpg`, `buket-45k.jpg`, dll).
- Semuanya (style, JS, data) ada di satu file — edit `index.html` saja.
