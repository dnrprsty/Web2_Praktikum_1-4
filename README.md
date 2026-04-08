# Web2_Praktikum_1-4
# Praktikum 1 - CodeIgniter 4 (MVC)

## Deskripsi

Modul Praktikum 1 ini bertujuan untuk memahami konsep dasar **Framework CodeIgniter 4** dan arsitektur **MVC (Model-View-Controller)**.
Mahasiswa diharapkan mampu membuat aplikasi web sederhana dengan routing, controller, dan view.

---

## Konsep MVC (Diagram)

```mermaid
flowchart TD
    A[User Request / Browser] --> B[Router]
    B --> C[Controller]
    C --> D[Model]
    D --> C
    C --> E[View]
    E --> F[Response ke User]
```

**Penjelasan:**

* **Router** → Menentukan controller mana yang dipanggil
* **Controller** → Mengatur alur logika
* **Model** → Mengelola data
* **View** → Menampilkan ke user

---

## Alur Aplikasi CI4

```mermaid
sequenceDiagram
    participant User
    participant Browser
    participant CI4
    participant Controller
    participant View

    User->>Browser: Akses URL (/about)
    Browser->>CI4: Request
    CI4->>Controller: Routing ke Page::about
    Controller->>View: Kirim data (title, content)
    View-->>Browser: HTML ditampilkan
```

---

## Cara Menjalankan (Linux Native PHP)

Jalankan perintah berikut di terminal:

```bash
php spark serve
```
![Terminal](assets/terminal.png)

Kemudian buka browser:

```
http://localhost:8080
```

Penjelasan:

* `php spark serve` → Menjalankan server bawaan CodeIgniter
* Tidak perlu Apache/XAMPP
* Cocok untuk Linux seperti CachyOS

---

## Struktur Folder (Sederhana)

```mermaid
graph TD
    A[app/] --> B[Controllers]
    A --> C[Views]
    C --> D[template/header.php]
    C --> E[template/footer.php]
    C --> F[about.php]
    C --> G[contact.php]
    C --> H[faqs.php]
    C --> I[tos.php]
```

---

## Tampilan Aplikasi

---

### Home

![Home](assets/home.png)

**Penjelasan:**
Halaman utama website yang menampilkan pesan selamat datang.
Menggunakan template layout (header & footer).

---

### About

![About](assets/about.png)

**Penjelasan:**
Menampilkan informasi tentang website.
Data dikirim dari controller ke view menggunakan array.

---

### Contact

![Contact](assets/contact.png)

**Penjelasan:**
Halaman kontak sederhana.
Menampilkan informasi kontak menggunakan struktur MVC.

---

### FAQ

![FAQ](assets/faq.png)

**Penjelasan:**
Berisi pertanyaan umum (Frequently Asked Questions).
Menggunakan layout yang sama untuk konsistensi UI.

---

### Terms of Service (ToS)

![ToS](assets/tos.png)

**Penjelasan:**
Menampilkan syarat dan ketentuan penggunaan website.
Ditambahkan sebagai pengembangan dari tugas utama.

---

## Kesimpulan

* Framework CodeIgniter mempermudah pengembangan web
* Konsep MVC membuat kode lebih terstruktur
* Routing menghubungkan URL dengan controller
* View digunakan untuk tampilan
* Controller sebagai penghubung utama

---

## Catatan

Project ini dijalankan menggunakan:

* PHP Native (CLI)
* CodeIgniter 4
* Linux (CachyOS)

---
