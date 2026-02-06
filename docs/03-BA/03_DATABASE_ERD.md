# ENTITY RELATIONSHIP DIAGRAM (ERD)

**Project**: Management Event Kolam Renang  
**Status**: DRAFT (Bahan Coding Minggu 1)

Berikut adalah struktur database yang **HARUS** diimplementasikan Junior Dev.

```mermaid
erDiagram

    USERS ||--o{ REGISTRATIONS : "melakukan"
    USERS ||--o{ NOTIFICATIONS : "menerima"
    EVENTS ||--o{ REGISTRATIONS : "memiliki"

    USERS {
        int id PK
        string email UK "Login"
        string password "Hashed"
        string role "ENUM('guest', 'user', 'admin', 'pelatih')"
        string full_name
        string phone
        date birth_date
        string club_name
        text address
        string ktp_photo "Path file"
        timestamp created_at
    }

    EVENTS {
        int id PK
        string title
        text description
        datetime event_date
        string location
        decimal price
        string status "ENUM('upcoming', 'open', 'closed', 'completed')"
        string banner_photo "Path file"
        timestamp created_at
    }

    REGISTRATIONS {
        int id PK
        int user_id FK
        int event_id FK
        string payment_status "ENUM('pending', 'waiting_confirmation', 'paid', 'rejected')"
        string payment_proof "Path file bukti bayar"
        decimal amount_paid
        text admin_notes "Alasan reject jika ada"
        timestamp created_at
    }

    NOTIFICATIONS {
        int id PK
        int user_id FK
        string title
        text message
        boolean is_read
        timestamp created_at
    }

```

## Catatan Implementasi (Untuk Junior)

1.  **Users Table**: Simpan password wajib pakai `password_hash()` (Bcrypt/Argon2). Jangan Plain text!
2.  **Registrations**: Tabel ini adalah 'Transaksi'. Satu user bisa daftar banyak event.
3.  **Roles**: Simpan sebagai String/Enum di database agar mudah dibaca.
