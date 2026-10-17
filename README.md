# Toples untuk Tofles

Sebuah toples kaca di tengah salju. Ketuk, dan ada surat di dalamnya.

Halaman statis satu file. Tidak ada build, tidak ada dependency, tidak ada backend. Buka `index.html` di browser dan semuanya jalan.

---

## Isi

- `index.html` — seluruh halaman: HTML, CSS, JavaScript, dan dua stiker (base64) dalam satu file.

Tidak ada aset eksternal selain Google Fonts (Fraunces, Karla, Caveat).

---

## Alur

1. **Toples** — ketuk untuk membuka. Tutup terangkat, percikan cahaya keluar, salju melambat.
2. **Gulungan** — muncul kertas tergulung berpita merah. Ketuk lagi.
3. **Surat** — kertas terkuak dari atas ke bawah, surat terbaca.

Setiap kali toples dibuka, satu bintang baru muncul di dalamnya dan tidak pernah hilang.

---

## Mengubah isi surat

Panel penulis disembunyikan supaya penerima tidak melihatnya. Tiga cara membukanya:

| Cara | Keterangan |
|---|---|
| Tahan toples 0,9 detik | Ada getar halus sebagai konfirmasi |
| `Ctrl + E` | Desktop |
| Tambahkan `?tulis=1` di URL | Cara paling pasti |

Yang bisa diubah: sapaan, isi surat, kalimat puncak, penutup, dan tanggal.

Semua tersimpan di `localStorage` perangkat itu saja — tidak dikirim ke mana-mana.

---

## Mencetak

`Ctrl + P`. Semua elemen antarmuka hilang, yang tersisa hanya surat di kertas putih.

---

## Catatan teknis

- **Tanpa JavaScript** — surat tetap terbaca lengkap lewat `<noscript>`.
- **Tanpa internet** — layout tetap utuh, hanya font jatuh ke serif/sans sistem.
- **`prefers-reduced-motion`** — semua animasi berhenti, salju digambar sekali tanpa bergerak.
- **Aksesibilitas** — semua tap target ≥44px, fokus keyboard terkunci di dalam dialog, `Esc` menutup, `aria-hidden` dikelola saat fase berganti.
- **Suara** — mati secara bawaan. Bisa dinyalakan dari panel penulis.

---

## Menjalankan secara lokal

Cukup buka filenya:

```
start index.html
```

Atau lewat server kalau perlu:

```
python -m http.server 8000
```

Lalu buka `http://localhost:8000`.
