
# FLOWCHART PIPELINE CI/CD APLIKASI DIGITAL KAMPUS

Diagram berikut menjelaskan proses pengembangan dan deployment aplikasi digital kampus menggunakan CI/CD.

```mermaid
flowchart TD
    A([Mulai]) --> B[Developer Membuat Kode]
    B --> C[Git Commit]
    C --> D[Push Code ke GitHub]
    D --> E[GitHub Actions]
    E --> F[Build Aplikasi]
    F --> G[Automated Testing]

    G --> H{Testing Berhasil?}

    H -->|Tidak| I[Perbaikan Kode]
    I --> B

    H -->|Ya| J[Code Review]
    J --> K{Disetujui?}

    K -->|Tidak| I
    K -->|Ya| L[Build Docker Image]
    L --> M[Deploy ke Cloud]
    M --> N[Aplikasi Digunakan]
    N --> O[Monitoring Sistem]

    O --> P{Ada Masalah?}
    P -->|Ya| I
    P -->|Tidak| Q([Selesai])

    style A fill:#d1fae5,stroke:#059669
    style Q fill:#d1fae5,stroke:#059669
    style H fill:#fef3c7,stroke:#d97706
    style K fill:#fef3c7,stroke:#d97706
    style P fill:#fef3c7,stroke:#d97706
    style M fill:#dbeafe,stroke:#2563eb
