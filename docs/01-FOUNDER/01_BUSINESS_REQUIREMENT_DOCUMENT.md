# BUSINESS REQUIREMENT DOCUMENT (BRD)

**Project**: Management Event Kolam Renang
**Client**: Khafid Swimming Club
**Date**: 05 Februari 2026

---

## 1. Executive Summary

Dokumen ini menjelaskan kebutuhan bisnis tingkat tinggi untuk sistem manajemen event. Fokus utamanya adalah efisiensi operasional dan akurasi data keuangan & peserta.

## 2. Analisis Masalah (Current Pain Points)

| Proses                | Masalah Saat Ini (Manual/Google Form)                                     | Dampak Bisnis                                                   |
| :-------------------- | :------------------------------------------------------------------------ | :-------------------------------------------------------------- |
| **Pendaftaran** | Peserta isi GForm, kadang salah input, butuh login akun Google.           | **Konversi pendaftar rendah, data sering duplikat.**           |
| **Pembayaran**  | Transfer ke rek pribadi, konfirmasi via Chat WA. Admin cek mutasi manual. | Risiko_Human Error_ tinggi, konfirmasi lambat, potensi fraud. |
| **Rekap Data**  | Admin copy-paste dari Spreadsheet ke Excel format lomba.                  | Memakan waktu 3-4 hari kerja hanya untuk rekap sebelum lomba.   |
| **Informasi**   | Peserta tanya hal sama berulang-ulang di WA (Jadwal, Lokasi, dll).        | Waktu admin habis untuk balas chat, bukan kerja strategis.      |

## 3. Solusi yang Diusulkan (Proposed Solution)

Membangun platform "One-Stop Solution" berbasis Web.

### Keuntungan Bisnis (Business Benefits):

1. **Efisiensi Waktu**: Memotong waktu rekap data dari 3 hari menjadi < 5 menit (Download Excel).
2. **Akurasi Keuangan**: Sistem status pembayaran (Pending/Lunas) meminimalisir peserta yang belum bayar tapi ikut lomba.
3. **Database Aset**: Klub memiliki database atlet/member yang bisa dimonétisasi di masa depan (misal: penawaran merchandise).

## 4. Kebutuhan Fungsional Tingkat Tinggi

- Sistem Pendaftaran Event Online 24/7.
- Sistem Manajemen Pembayaran & Verifikasi.
- Sistem Pengumuman & Informasi Terpusat.
- Sistem Pelaporan Otomatis (Export Data).

## 5. Batasan (Constraints)

- **Budget**: Efisiensi biaya server (menggunakan Hosting Shared/VPS kecil di awal).
- **Teknologi**: Menggunakan PHP Native/Framework ringan agar mudah dimaintain oleh tim internal nanti.
- **Waktu**: Harus siap sebelum event besar pertama pasca-Lebaran.
