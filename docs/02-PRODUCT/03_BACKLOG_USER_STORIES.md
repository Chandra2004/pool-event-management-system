# USER STORIES & BACKLOG

**Project**: Management Event Kolam Renang  
**Reference**: PRD v1.0

---

## 📌 Epics: Authentication (Auth)

### [US-AUTH-01] Register sebagai Peserta

**As a** Calon Peserta  
**I want to** membuat akun dengan email dan password  
**So that** data saya tersimpan dan tidak perlu isi ulang saat daftar event berikutnya.  
_Acceptance Criteria:_

1.  Validasi format email.
2.  Password minimal 8 karakter.
3.  Email verifikasi dikirim (Opsional MVP).

### [US-AUTH-02] Login Admin

**As a** Admin Klub  
**I want to** login ke halaman khusus admin  
**So that** saya bisa mengelola event tanpa dilihat publik.  
_Acceptance Criteria:_

1.  Halaman login terpisah (misal: `/admin/login`).
2.  Session timeout setelah 2 jam (Security).

---

## 📌 Epics: Event Transaction (Trx)

### [US-TRX-01] Daftar Event

**As a** Peserta Logged-in  
**I want to** klik tombol "Daftar" di detail event  
**So that** saya bisa masuk ke form pengisian data lomba.

### [US-TRX-02] Upload Bukti Bayar

**As a** Peserta  
**I want to** upload foto bukti transfer (JPG/PNG)  
**So that** pendaftaran saya bisa diproses admin.  
_Acceptance Criteria:_

1.  Maksimal file size 2MB.
2.  Hanya menerima gambar (bukan .exe/.zip).
3.  Status transaksi berubah jadi "Waiting Confirmation".

### [US-TRX-03] Verifikasi Pembayaran

**As a** Admin  
**I want to** melihat list pendaftar status "Waiting" dan tombol Approve/Reject  
**So that** saya bisa memvalidasi uang yang masuk.  
_Acceptance Criteria:_

1.  Jika klik Approve, status jadi "Lunas", User dapat notif.
2.  Jika klik Reject, Admin wajib isi "Alasan Penolakan".

---

## 📌 Epics: Reporting (Rep)

### [US-REP-01] Export Excel

**As a** Admin  
**I want to** download data peserta per event  
**So that** saya bisa print untuk daftar hadir lomba offline.  
_Acceptance Criteria:_

1.  Format file .xlsx.
2.  Kolom berisi: Nama, Kategori, Klub, Status Bayar.
