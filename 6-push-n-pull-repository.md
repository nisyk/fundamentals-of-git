#### < [Membuat dan mendowload repository di GitHub](5-making-github-repo.md)

# Push dan pull repository dari local ke GitHub
Setelah berhasil mengelola perubahan di dalam komputer pribadi (lokal), langkah berikutnya adalah melakukan sinkronisasi dengan server internet seperti GitHub atau Gitea agar proyek dapat diakses oleh anggota tim lainnya. Proses ini melibatkan pengiriman data ke server (_push_) dan pengambilan data terbaru dari server (_pull_) untuk menjaga konsistensi kode di semua perangkat. Memahami alur interaksi antara repositori lokal dan _remote_ adalah kunci utama dalam kolaborasi pengembangan proyek secara profesional.

### Alur Kerja Utama (Collaboration Workflow)

Siklus kerja dalam tim yang menggunakan Git selalu berputar pada tiga perintah utama ini untuk memastikan tidak ada data yang tumpang tindih:

1. **`git pull`**: Langkah pertama sebelum mulai bekerja adalah mengambil versi terbaru dari server agar file di komputer tidak tertinggal dari perubahan rekan tim.
    
2. **Siklus Lokal (Edit - Add - Commit)**: Melakukan pengerjaan tugas secara mandiri di komputer masing-masing hingga perubahan tersimpan di repositori lokal.
    
3. **`git push`**: Langkah terakhir untuk membagikan hasil pekerjaan ke server agar bisa dilihat dan digunakan oleh seluruh anggota tim.

### Upload (push) repository dari Local ke GitHub 
1. Buka repo yang sebelumnya sudah didownload (via git clone)

2. Buat file baru, lalu lakukan **`git add`** dan **`git commit`**, *[Klik untuk intruksi selengkapnya](4-git-basic-command.md)*

3. **Upload repository yang sudah dicommit ke repository GitHub**
```bash
git push -u origin main
```

| **Komponen**   | **Fungsi**                                                                                                        |
| -------------- | ----------------------------------------------------------------------------------------------------------------- |
| **`git push`** | Instruksi utama untuk mengirim data ke server.                                                                    |
| **`-u`**       | _Set-upstream_. Berfungsi untuk "mengingat" jalur pengiriman, sehingga kedepannya cukup mengetik `git push` saja. |
| **`origin`**   | Nama panggilan (alias) untuk alamat URL server tujuan.                                                            |
| **`main`**     | Nama cabang (_branch_) utama tempat data akan disimpan di server.                                                 |

💡 Jika repo yang dibuat bukan repo yang dibuat dari GitHub, melainkan git local (dari `git init`) [klik di sini untuk step-by-stepnya](6a-push-repo-local.md)

> 📝 **Catatan:** Git versi terbaru menggunakan `main` sebagai branch utama. Jika tertulis `master` di terminal, ubah perintahnya menjadi `git push -u origin master`

### Mengsinkronkan (pull) repository dari GitHub ke Local
Jika ada perubahan terbaru dari GitHub yang tidak dilakukan dari local yang biasanya terjadi karena:
- Mengedit dari website GitHub/server.
- Mengedit dari komputer lain, lalu push ke GitHub/server.
- Anggota tim lain melakukan perubahan di repository GitHub/server.
Anda tidak dapat melakukan `push`, karena git mendeteksi ada perbedaan antara repository local anda dengan repository sehingga diperlukan menggunakan `pull` untuk sinkronisasi repository local dengan repository GitHub/server.

Untuk sinkronisasi repository, cukup mengetikkan command ini
```bash
git pull
```

Git langsung mengsinkronisasi repository local dengan yang ada di repository GitHub/server.

### Git pull vs git fetch
Dalam kerja profesional yang penuh kehati-hatian, sangat penting sekali untuk memeriksa repository yang ada di GitHub/server sebelum mengsinkronisasi dengan repository local. 

Oleh karena itu `git fetch` sering menjadi alur kerja para profesional, karena dapat mengaudit kode/file sebelum disinkronkan oleh `git pull` atau `git merge` karena perintah tersebut bersifat read-only.

#### > [Branching dasar](7-basic-branching.md)
