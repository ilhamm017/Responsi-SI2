# Tugas Praktikum Docker: Website Data Diri 

## Website Anda
Bangun website data diri sederhana yang terdiri dari **dua halaman** di Killercoda Ubuntu Playground (**Tidak usah terlalu memikirkan soal desain websitenya, yang terpenting dapat menampilkan konten dengan jelas**). Gunakan Docker untuk mengelola container, image, network, dan (opsional) volume.
Website data diri Anda akan terdiri dari dua halaman sederhana yang di-hosting di container terpisah:

**1. Halaman Utama**

Menampilkan:

* **Nama Lengkap**
* **NIM**
* **Program Studi**
* **Hobi**
* **Link** ke halaman profil (`/profil`)

**2. Halaman Profil )**

* Menampilkan **foto profil** Anda.

## Tantangan! 🚀

**Selesaikan langkah-langkah berikut untuk membangun website Anda:**

### 1. Persiapan

1. Buat dua direktori: `website-utama` dan `website-profil`.
2. Di dalam `website-utama`:
   *  Buat file `index.html` (sesuai deskripsi halaman utama).
   * Pastikan link "profil" mengarah ke `/profil`.
3. Di dalam `website-profil`, letakkan file gambar profil Anda (`foto.jpg`).

### 2. Docker Network (Modul 13)

* Buat jaringan Docker dengan nama my-**nama-mahasiswa**-network

### 3. Dockerfile dan Image (Modul 11 & 12)

#### 3.1.  `Dockerfile` untuk Website Utama (direktori `website-utama`)

```dockerfile
FROM nginx:latest 
# ... Instruksi untuk menyalin isi direktori `website-utama` 
# ... Instruksi untuk mendefinisikan port 80
```

#### 3.2.  `Dockerfile` untuk Website Profil (direktori `website-profil`)

```dockerfile
FROM nginx:latest
# ... Instruksi untuk menyalin isi direktori `website-profil` 
# ... Instruksi untuk mendefinisikan port 80 
```

#### 4. Build Image

-   **Bangun dua image Docker** dari Dockerfile yang sudah dibuat. Berikan nama yang jelas untuk setiap image (misalnya, website-utama, website-profil).
  
### 5. Docker Volume (Modul 14) (Opsional)

* **Tantangan Tambahan:** 
    *  Buat volume bernama `profile-images`.
    * Konfigurasikan agar container website utama dan profil mengakses gambar profil melalui volume ini.

### 6. Menjalankan Container (Modul 9 & 10)
*Jalankan container dengan menyambungkan ke docker network yang sudah kalian buat sebelumnya*

1. **Jalankan Container Website Utama**

2. **Jalankan Container Website Profil:**

## Pengujian 

1. Akses website  
2. Klik link "profil".  Apakah link tersebut mengarah dan menampilkan gambar profil Anda?

## Pengumpulan

1. **Buat repositori Git** dan unggah semua file yang diperlukan (Dockerfile, HTML, gambar).
2. **Buat file README.md**. Jelaskan cara menjalankan website di Killercoda Ubuntu Playground (lengkap dengan perintah Docker).

