# Authentication Flow ERD

```mermaid
erDiagram
    ROLE ||--o{ USERS : "memiliki"
    USERS ||--o{ LOGINS : "memulai"

    USERS {
        int id_user PK "Auto Increment"
        int id_role FK "Relasi ke tabel Role"
        string nama_user "Unique"
        string email "Unique"
        string kata_sandi 
    }
    
    ROLE {
        int id_role PK "Auto Increment"
        string nama_role "Unique (Contoh: Admin, User)"
    }

    LOGINS {
        int id_login PK "Auto Increment"
        int id_user FK "Relasi ke tabel Pengguna"
    }

```
