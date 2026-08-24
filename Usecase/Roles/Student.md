```mermaid

graph LR
    Student{{Student}}

    subgraph Web Pendaftaran Ekstrakulikuler
        SignUp(Registrasi)
        SignIn(Login)
        PembuatanProfil(Pembuatan Profil)
        Dashboard(Dashboard)
        EditProfil(Edit Profil)
        Notifikasi(Lihat Notifikasi)
        Jadwal(Lihat Jadwal Ekstrakulikuler)
        Ekstrakulikuler(Lihat Ekstrakulikuler)
        PendaftaranEkstrakulikuler(Daftar Ekstrakulikuler)

        SignUp -.->|include| PembuatanProfil

        Dashboard -.->|include| SignIn
        EditProfil -.->|include| SignIn
        Notifikasi -.->|include| SignIn
        PendaftaranEkstrakulikuler -.->|include| SignIn
        
        PendaftaranEkstrakulikuler -.->|extend| Ekstrakulikuler
    end

    Student --> SignUp
    Student --> Ekstrakulikuler
    Student --> Dashboard
    Student --> EditProfil
    Student --> PendaftaranEkstrakulikuler
    Student --> Jadwal
    Student --> Notifikasi

```
