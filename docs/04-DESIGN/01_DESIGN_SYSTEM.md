# DESIGN SYSTEM GUIDELINES (MODERN STACK)

**Role**: UI/UX Designer  
**Framework**: Laravel Blade + Tailwind CSS + Flowbite + Lucide Icons

---

## 1. Core Technology Stack

- **Templating**: Laravel Blade (Komponen reusable via `@include` atau `<x-component>`).
- **Styling**: Tailwind CSS (Utility-first framework).
- **UI Kit**: Flowbite (Komponen siap pakai: Modal, Navbar, Dropdown, Table).
- **Icons**: Lucide Icons (Ringan, Outline style, Modern).

## 2. Color Palette (Tailwind Configuration)

Gunakan palette warna berikut di `tailwind.config.js` agar konsisten:

- **Primary (Blue Ocean)**:
  - `primary-500`: `#0ea5e9`
  - `primary-600`: `#0284c7` (Main Brand Color)
  - `primary-700`: `#0369a1`
- **Secondary (Navy Deep)**:
  - `secondary-900`: `#0c4a6e` (Footers, Headings)
- **Background**:
  - `bg-main`: `#f8fafc` (Slightly greyish blue, clean feel).
- **Status Colors**:
  - `success`: `#10b981` (Diterima/Lunas)
  - `warning`: `#f59e0b` (Pending)
  - `danger`: `#ef4444` (Ditolak/Dibatalkan)

## 3. Typography

- **Primary Font**: `Poppins` atau `Inter`.
- **Setup**: Import via Google Fonts di `app.blade.php`.
- **Usage**:
  - Heading: `font-bold text-slate-900`
  - Body: `font-normal text-slate-700 leading-relaxed`

## 4. Components Strategy (Flowbite)

Junior wajib menggunakan komponen dari **Flowbite** untuk kecepatan dan standarisasi:

- **Navigation**: Sidebar/Navbar harus tetap nampak di mobile (Responsive).
- **Forms**: Gunakan input Flowbite dengan focus ring Ocean Blue.
- **Tables**: Gunakan table Flowbite untuk list pendaftar (zebra stripe style).
- **Modals**: Untuk konfirmasi hapus data atau verifikasi pembayaran.

## 5. Iconography (Lucide)

Gunakan icon yang deskriptif dan konsisten:

- `user`: Profil peserta.
- `calendar`: Jadwal lomba.
- `credit-card`: Pembayaran.
- `check-circle`: Validasi admin.
- `alert-triangle`: Peringatan/Reject.

---

## 💡 Instruksi untuk Junior (Farrel & Mada):

1. **Setup Tailwind**: Pastikan `tailwind.config.js` sudah memiliki konfigurasi warna di atas.
2. **Master Layout**: Buat satu file `layouts/app.blade.php` sebagai kerangka utama.
3. **Flowbite**: Gunakan CDN atau NPM untuk Flowbite JS agar interaksi (modal/dropdown) berfungsi.
4. **Consistency**: Jangan mencampur warna custom di luar palette yang sudah ditentukan.
