# BUSINESS PROCESS FLOW (AS-IS vs TO-BE)

## 1. Alur Pendaftaran Lomba (Main Flow)

### AS-IS (Cara Lama)

1.  Admin share poster lomba di IG/WA.
2.  Peserta chat WA admin minta link form / info.
3.  Peserta isi Google Form (Sering typo / salah input).
4.  Peserta transfer manual ke rekening Owner.
5.  Peserta kirim bukti transfer ke WA Admin.
6.  Admin buka M-Banking cek mutasi satu-satu.
7.  Admin balas WA "Oke lunas".
8.  Admin buka Google Sheet, rapikan data manual satu-satu.

**Masalah:** Bottleneck parah di Admin (Poin 5, 6, 7). Rawan chat tenggelam.

---

### TO-BE (Sistem Baru)

1.  Admin buat Event di Web -> Share Link Web.
2.  Peserta buka Web -> Baca Info lengkap.
3.  Peserta **Register/Login** (Data tersimpan, gak perlu isi ulang next event).
4.  Peserta pilih Event -> Klik "Daftar" -> Upload Dokumen (KTP dll).
5.  Sistem tampilkan Info Bayar & Instruksi.
6.  Peserta Transfer -> **Upload Bukti di Web**.
7.  Admin lihat notif di **Dashboard Admin** -> Klik "Verifikasi".
8.  Sistem otomatis kirim notif "Lunas" ke Dashboard Peserta & Email.
9.  Data otomatis masuk database -> Siap download Excel kapanpun.

**Perbaikan:** Admin tidak perlu chat satu-satu. Cek mutasi & verifikasi terpusat di satu dashboard.
