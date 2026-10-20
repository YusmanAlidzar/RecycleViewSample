# RecycleViewSample

Tugas PAM (Pengembangan Aplikasi Mobile) - Modul 1 Praktikum 07.

## Deskripsi

Proyek ini merupakan aplikasi Android sederhana yang mempraktikkan penggunaan
`RecyclerView` untuk menampilkan daftar data secara efisien. Aplikasi membuat
20 data item secara dinamis, kemudian menampilkannya dalam bentuk daftar
vertikal menggunakan `LinearLayoutManager` dan `CustomAdapter`.

## Fitur

- Menampilkan daftar 20 item (`Item 1` sampai `Item 20`).
- Menggunakan `RecyclerView` untuk menampilkan daftar.
- Menggunakan `CardView` sebagai tampilan setiap item.
- Menggunakan adapter dan `ViewHolder` untuk menghubungkan data dengan layout.
- Mencatat jumlah data ke Logcat dengan tag `test string`.

## Teknologi

- Kotlin
- Android SDK
- AndroidX RecyclerView
- AndroidX ConstraintLayout
- Material Components
- Gradle Kotlin DSL

## Struktur Utama

```text
.
├── app/
│   └── src/
│       └── main/
│           ├── java/lat/pam/
│           │   ├── recycleviewsample/
│           │   │   ├── CustomAdapter.kt
│           │   │   └── MainActivity.kt
│           │   └── samplerecyclerview/
│           │       └── ItemsViewModel.kt
│           └── res/
│               └── layout/
│                   ├── activity_main.xml
│                   └── card_view_design.xml
├── build.gradle.kts
├── gradle/
│   └── libs.versions.toml
└── settings.gradle.kts
```

## Alur Kerja `RecyclerView`

1. `MainActivity` membuat `ArrayList<ItemsViewModel>` berisi 20 item.
2. `LinearLayoutManager` mengatur daftar secara vertikal.
3. `CustomAdapter` menerima data dan membuat `ViewHolder`.
4. `onBindViewHolder` mengisi teks item ke `TextView`.
5. `RecyclerView` menampilkan item menggunakan layout `card_view_design.xml`.