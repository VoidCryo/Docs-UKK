```mermaid

graph TB
    Student{{Student}}

    subgraph "Pendaftaran Ekstrakulikuler"
        SignUp(Registrasi)
        SignIn(Login)
        PembuatanProfil(Pembuatan Profil)
        Dashboard(Dashboard)
        Notifikasi(Notifikasi)
        Jadwal(Jadwal Ekstrakulikuler)
        Ekstrakulikuler(Ekstrakulikuler)
        PendaftaranEkstrakulikuler(Pendaftaran Ekstrakulikuler)
        ProfilPembina(Profil Pembina)
        VerifikasiPassword(Verifikasi Password)

        SignIn -.->|include| VerifikasiPassword
        SignUp -.->|include| PembuatanProfil
        Dashboard -.->|include| SignIn
        Dashboard -.->|include| Notifikasi
        Dashboard -.->|include| Jadwal
        Jadwal -.->|include| Ekstrakulikuler
        Ekstrakulikuler -.->|include| ProfilPembina
        Ekstrakulikuler -.->|extend| PendaftaranEkstrakulikuler
    end

    Student --> SignUp
    Student --> SignIn
    Student --> Ekstrakulikuler

```
