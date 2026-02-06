# SYSTEM FLOWCHART (Activity Diagram)

**Project**: Management Event Kolam Renang  
**Status**: Draft

Berikut adalah alur logika utama yang harus di-coding.

## 1. Flow Pendaftaran Lomba (User Side)

```mermaid
flowchart TD
    Start([Mulai]) --> Login{Sudah Login?}
    Login -- Tidak --> PageLogin[Halaman Login/Register]
    PageLogin --> Login
    Login -- Ya --> PilihEvent[Pilih Event Lomba]
    PilihEvent --> CekKuota{Kuota Masih Ada?}

    CekKuota -- Habis --> TampilPenuh[Tampilkan Full Booked]
    TampilPenuh --> Stop([Selesai])

    CekKuota -- Ada --> FormIsi[Isi Form Peserta & Upload KTP]
    FormIsi --> Submit[Klik Daftar]
    Submit --> SaveDB[(Simpan ke DB Pending)]
    SaveDB --> PageBayar[Halaman Info Pembayaran]

    PageBayar --> UserBayar[User Transfer]
    UserBayar --> UploadBukti[User Upload Bukti Bayar]
    UploadBukti --> UpdateStatus[(Update Status Waiting)]
    UpdateStatus --> WaitAdmin[Tunggu Verifikasi Admin]
    WaitAdmin --> Stop
```

## 2. Flow Verifikasi Pembayaran (Admin Side)

```mermaid
flowchart TD
    StartAdmin([Mulai Admin]) --> ListTrx[Lihat Daftar Transaksi Waiting]
    ListTrx --> CekBukti[Cek Foto Bukti Transfer]
    CekBukti --> Valid{Valid?}

    Valid -- Ya Uang Masuk --> KlikApprove[Klik Terima]
    KlikApprove --> UpdateLunas[(Status = PAID)]
    UpdateLunas --> KirimNotif[Kirim Notif Sukses ke User]

    Valid -- Tidak Fake --> KlikReject[Klik Tolak]
    KlikReject --> InputAlasan[Input Alasan Penolakan]
    InputAlasan --> UpdateReject[(Status = REJECTED)]
    UpdateReject --> KirimNotifGagal[Kirim Notif Gagal ke User]

    KirimNotif --> Selesai([Selesai])
    KirimNotifGagal --> Selesai
```
