```mermaid

graph LR
    Admin{{Admin}}

    subgraph Web Pendaftaran Ekstrakulikuler
        SignIn(Login)
        Student(Pengelola Siswa)
        Teacher(Pengelola Guru)
        Ekstrakulikuler(Pengelola Ekstrakulikuler)

        Student -.->|include| SignIn
        Teacher -.->|include| SignIn
        Ekstrakulikuler -.->|include| SignIn
    end

    Admin --> Student
    Admin --> Teacher
    Admin --> Ekstrakulikuler

```
