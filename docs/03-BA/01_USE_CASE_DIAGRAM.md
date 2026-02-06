# USE CASE DIAGRAM

**Project**: Management Event Kolam Renang  
**Status**: Draft (Updated for Stability)

Siapa bisa melakukan apa? (Format Flowchart untuk kompatibilitas maksimal)

```mermaid
flowchart LR
    %% Actors
    subgraph Actors
        Guest((Guest))
        User((Peserta))
        Admin((Admin))
    end

    %% System Boundary
    subgraph Website_Event [Sistem Website Event]
        UC1([Lihat Jadwal Lomba])
        UC2([Login / Register])
        UC3([Daftar Lomba])
        UC4([Upload Bukti Bayar])
        UC5([Dashboard Peserta])
        UC6([Kelola Master Event])
        UC7([Verifikasi Pembayaran])
        UC8([Download Laporan Excel])
    end

    %% Relationships
    Guest --- UC1
    Guest --- UC2

    User --- UC1
    User --- UC2
    User --- UC3
    User --- UC4
    User --- UC5

    Admin --- UC2
    Admin --- UC6
    Admin --- UC7
    Admin --- UC8

    %% Styling for Use Case circles
    style UC1 rx:20,ry:20
    style UC2 rx:20,ry:20
    style UC3 rx:20,ry:20
    style UC4 rx:20,ry:20
    style UC5 rx:20,ry:20
    style UC6 rx:20,ry:20
    style UC7 rx:20,ry:20
    style UC8 rx:20,ry:20
```

## Detail Use Case (Singkat)

1.  **Lihat Jadwal Lomba**: Semua orang bisa lihat.
2.  **Daftar Lomba**: Hanya User yang sudah login.
3.  **Verifikasi**: Hanya Admin. Peserta tidak boleh verifikasi sendiri.
