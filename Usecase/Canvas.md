```mermaid

graph LR
    Admin{{Admin}}
    Student{{Student}}
    Teacher{{Teacher}}

    subgraph Web Pendaftaran Ekstrakulikuler
        SignUp(Registrasi)
        SignIn(Login)
        PembuatanProfil(Pembuatan Profil)
        Dashboard(Dashboard)
        EditProfil(Edit Profil)
        Notifikasi(Lihat Notifikasi)
        Jadwal(Lihat / Pengelola Jadwal)
        Ekstrakulikuler(Lihat / Pengelola Ekstrakulikuler)
        PendaftaranEkstrakulikuler(Daftar Ekstrakulikuler)
        
        StudentPeng(Pengelola Siswa)
        TeacherPeng(Pengelola Guru)
        
        PenerimaanAnggota(Penerimaan Anggota Baru)
        PengelolaAnggota(Pengelola Anggota)

        SignUp -.->|include| PembuatanProfil

        Dashboard -.->|include| SignIn
        EditProfil -.->|include| SignIn
        Notifikasi -.->|include| SignIn
        Jadwal -.->|include| SignIn
        Ekstrakulikuler -.->|include| SignIn
        
        StudentMgmt -.->|include| SignIn
        TeacherMgmt -.->|include| SignIn
        PenerimaanAnggota -.->|include| SignIn
        PengelolaAnggota -.->|include| SignIn
        PendaftaranEkstrakulikuler -.->|include| SignIn

        PendaftaranEkstrakulikuler -.->|extend| Ekstrakulikuler
    end

    Admin --> StudentPeng
    Admin --> TeacherPeng
    Admin --> Ekstrakulikuler

    Student --> SignUp
    Student --> Dashboard
    Student --> EditProfil
    Student --> Notifikasi
    Student --> Jadwal
    Student --> Ekstrakulikuler
    Student --> PendaftaranEkstrakulikuler

    Teacher --> Dashboard
    Teacher --> EditProfil
    Teacher --> Notifikasi
    Teacher --> Jadwal
    Teacher --> Ekstrakulikuler
    Teacher --> PenerimaanAnggota
    Teacher --> PengelolaAnggota

```
