#### < [Menghubungkan git ke akun GitHub](3-connect-account.md)

# Perintah Dasar Git
Setelah memahami teori fundamental Git, saatnya langsung terjun ke mempraktikkan cara membuat directory "mesin-waktu" pertama. Kita akan mulai dengan membuat folder proyek baru dan menginisialisasi Git menggunakan terminal agar sistem siap melacak setiap perubahan. 

| **Perintah**          | **Fungsi Utama**                                                          | **Lokasi Operasi** |
| --------------------- | ------------------------------------------------------------------------- | ------------------ |
| `git init`            | Mengubah folder biasa menjadi repositori Git (Menyalakan mesin waktu).    | Working Directory  |
| `git status`          | Melihat kondisi file (apakah sudah di-edit, di-add, atau siap di-commit). | Seluruh Area       |
| `git add .`           | Memindahkan seluruh perubahan file ke Staging Area.                       | Staging Area       |
| `git commit -m "..."` | Menyimpan perubahan secara permanen ke dalam database.                    | Repository         |
| `git log --oneline`   | Melihat riwayat penyimpanan (commit) secara ringkas.                      | Repository         |

---
###  Membuat Directory Git Pertama

Berikut adalah urutan perintah untuk memulai proyek dari nol hingga tersimpan di dalam sistem Git:

**1. Menyiapkan Folder Proyek**
Buat folder baru dan masuk ke dalamnya menggunakan perintah UNIX yang telah dipelajari sebelumnya.


```bash
mkdir proyek_pertama
cd proyek_pertama
```

**2. Inisialisasi Git (git init)** 
Langkah ini wajib dilakukan untuk membuat folder rahasia `.git` yang berfungsi sebagai pusat data.

```bash
git init             
```

**3. Membuat File & Cek Status** 
Buatlah sebuah file (misalnya file text baru) lalu periksa bagaimana Git mendeteksinya.

```bash
touch halo.txt    # perintah membuat file

git status        # cek status git

# Sistem mendeteksi ada file baru, namun belum masuk ke Staging Area (dikategorikan sebagai Untracked files)
```

**4. Memindahkan ke Staging Area (git add)** 
Proses ini memindahkan file ke "Meja Packing" untuk persiapan penyimpanan.

```bash
git add halo.txt      # menambahkan halo.txt ke Staging Area

git status            # cek status git  

# Sistem mendeteksi file baru yang sudah masuk ke Staging Area
```

**5. Menyimpan ke Repository (git commit)**
Langkah ini mengunci perubahan secara permanen ke dalam "Gudang" (Repository).
```bash
git commit -m "commit pertama saya"      

# Sistem mendeteksi perubahan file
```

**6. Memeriksa Riwayat (git log)** 
Pastikan perubahan telah tercatat di dalam sistem database Git.

```bash
git log --oneline        

# Sistem memberikan data commit history
```
(Cara keluar dari git log, adalah dengan menekan tombol 'q')

#### > [Membuat dan mendownload repository di GitHub](5-making-github-repo.md)
