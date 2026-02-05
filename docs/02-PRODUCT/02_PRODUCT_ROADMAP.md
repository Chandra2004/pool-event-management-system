# PRODUCT ROADMAP

**Project**: Management Event Kolam Renang  
**Phase**: MVP (Minimum Viable Product)  
**Start Date**: 05 Februari 2026
**Deadline**: 20 Februari 2026 (Hard Deadline)

---

## 📅 Timeline Eksekusi (Sprint Cepat)

Mengingat durasi hanya **15 Hari**, kita akan menggunakan metode _Sprint_ cepat per 3-4 hari.

### 🏁 Phase 1: Foundation & Database (5 - 8 Feb)

**Target**: Sistem login jalan & Database siap.

- [ ] **05 Feb**: Setup Project, Repo, & Environment.
- [ ] **06 Feb**: Finalisasi ERD & Create Database Tables.
- [ ] **07 Feb**: Slicing UI Login/Register & Halaman Dashboard Kerangka.
- [ ] **08 Feb**: Implementasi Auth (Login/Register) Backend.

### ⚙️ Phase 2: Core Event Management (9 - 12 Feb)

**Target**: Data Lomba sudah bisa diinput Admin & Dilihat User.

- [ ] **09 Feb**: CRUD Master Event (Admin bisa tambah jadwal lomba).
- [ ] **10 Feb**: Public View (Halaman Home & List Lomba).
- [ ] **11 Feb**: Halaman Detail Event (Info lengkap lomba).
- [ ] **12 Feb**: Integrasi tampilan public dengan database real.

### 📝 Phase 3: Registration & Transaction (13 - 17 Feb)

**Target**: User bisa daftar & Bayar (Fitur Paling Krusial).

- [ ] **13 Feb**: Form Pendaftaran Peserta (Input & Upload KTP).
- [ ] **14 Feb**: Fitur Upload Bukti Pembayaran.
- [ ] **15 Feb**: Dashboard Admin: Verifikasi Pembayaran (Approve/Reject).
- [ ] **16 Feb**: Testing alur pendaftaran dari awal sampai akhir.
- [ ] **17 Feb**: Perbaikan bug transaksi (Handling error upload, dll).

### 🚀 Phase 4: Finishing & Deploy (18 - 20 Feb)

**Target**: Data bisa ditarik & Website Live.

- [ ] **18 Feb**: Fitur Export Excel (Rekap Peserta).
- [ ] **19 Feb**: Final UI Polishing (Rapikan CSS, Cek Mobile Responsiveness).
- [ ] **20 Feb**: **DEPLOYMENT** & Serah Terima.

---

## ⚠️ Critical Path (Jangan Sampai Telat)

1.  **Database Lomba & Peserta**: Kalau ini salah desain di tanggal 6 Feb, ke belakang akan berantakan.
2.  **Form Upload**: Sering bermasalah di permission folder/size limit. Tes lebih awal.
