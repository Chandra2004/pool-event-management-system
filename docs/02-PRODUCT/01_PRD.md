# PRODUCT REQUIREMENTS DOCUMENT (PRD)

**Project**: Management Event Kolam Renang  
**Referenced Charter**: `docs/01-FOUNDER/PROJECT_CHARTER.md`  
**Version**: 1.0  
**Status**: Draft

---

## 1. Executive Summary

Sistem berbasis web untuk mengelola pendaftaran lomba renang secara end-to-end, menggantikan sistem manual/Google Form untuk meningkatkan akurasi data dan profesionalitas klub.

## 2. User Personas

| Role               | Deskripsi        | Kebutuhan Utama                                                    |
| :----------------- | :--------------- | :----------------------------------------------------------------- |
| **Guest**          | Pengunjung umum  | Melihat jadwal lomba, info klub, dan galeri.                       |
| **Peserta (User)** | Atlet/Ortu atlet | Mendaftar lomba, bayar tiket, cek status pendaftaran.              |
| **Admin**          | Pengelola KSC    | Membuat event, verifikasi pembayaran, download rekap data (Excel). |
| **Pelatih**        | Staff internal   | Melihat daftar atlet (View Only).                                  |

## 3. Functional Requirements (Fitur)

### 3.1. Modul Event (Core)

- **[REQ-EVT-01] View Event List**: Menampilkan daftar event (Coming Soon, Ongoing, Completed).
- **[REQ-EVT-02] Event Details**: Halaman detail event berisi Deskripsi, Tanggal, Harga, Kategori, & Prize Pool.
- **[REQ-EVT-03] Manage Event (Admin Only)**: CRUD Event (Create, Read, Update, Delete/Close).
  - _Constraint_: Admin bisa "Tutup Pendaftaran" secara manual.

### 3.2. Modul Registrasi & Peserta

- **[REQ-REG-01] User Registration/Login**: Register via Email, Password, Nama Lengkap.
- **[REQ-REG-02] Event Registration Form**:
  - Input: Nama, Umur, Kategori Lomba, Nama Klub (Asal).
  - Upload: Scan KTP/Kartu Pelajar.
- **[REQ-REG-03] Dashboard Peserta**:
  - List event yang diikuti.
  - Status pendaftaran per event (Pending/Lunas/Ditolak).

### 3.3. Modul Pembayaran

- **[REQ-PAY-01] Payment Info**: Menampilkan metode bayar (QRIS, Transfer, E-Wallet) di detail event/checkout.
- **[REQ-PAY-02] Upload Bukti**: User harus upload bukti transfer agar status berubah jadi "Waiting Confirmation".
- **[REQ-PAY-03] Payment Verification (Admin Only)**: Admin mengecek bukti bayar & mengubah status jadi "Diterima" atau "Ditolak".

### 3.4. Modul Laporan & Admin

- **[REQ-ADM-01] Export Data**: Download data peserta per event dalam format **Excel (.xlsx)**.
- **[REQ-ADM-02] Dashboard Summary**: Counter jumlah pendaftar per event.

## 4. Non-Functional Requirements

- **[NFR-01] Design**: Style "Modern, Sporty, Formal". Warna dominan sesuai logo (jika ada) atau tema air.
- **[NFR-02] Device**: Responsive Web (Optimal di HP & Laptop).
- **[NFR-03] Security**: Password user terenkripsi, Upload file dibatasi (jpg/png/pdf max 2MB).

## 5. Roadmap / User Flow

1.  **Guest** buka web -> Lihat Jadwal Event.
2.  **Guest** Register akun -> Jadi **Peserta**.
3.  **Peserta** pilih Event -> Isi Form & Upload Dokumen -> Transfer -> Upload Bukti.
4.  **Admin** terima notif -> Cek Bukti -> Klik "Approve".
5.  **Peserta** dapat notifikasi "Diterima" di Dashboard -> Siap lomba.

---

**Success Metrics:**

- Pendaftaran 100% via Web (No more WA manual).
- Rekap data Excel tersedia dalam < 1 menit.
