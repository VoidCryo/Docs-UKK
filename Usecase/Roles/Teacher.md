```mermaid

graph LR
    Teacher{{Teacher}}

    subgraph Web Pendaftaran Ekstrakulikuler
        SignIn(Login)
        Dashboard(Dashboard)
        Notifikasi(Lihat Notifikasi)
        Jadwal(Pembuatan Jadwal)
        PenerimaanAnggota(Penerimaan Anggota Baru)
        PengelolaAnggota(Pengelola Anggota)
        PengelolaEkstrakulikuler(Pengelola Ekstrakulikuler)
        EditProfil(Edit Profil)

        Dashboard -.->|include| SignIn
        PengelolaAnggota -.->|include| SignIn
        PengelolaEkstrakulikuler -.->|include| SignIn
        Jadwal -.->|include| SignIn
        PenerimaanAnggota -.->|include| SignIn
        EditProfil -.->|include| SignIn
    end

    Teacher --> Dashboard
    Teacher --> EditProfil
    Teacher --> Jadwal
    Teacher --> PenerimaanAnggota
    Teacher --> PengelolaAnggota
    Teacher --> PengelolaEkstrakulikuler
    Teacher --> Notifikasi

```
