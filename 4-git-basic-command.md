#### < [Menghubungkan git ke GitHub](3-connect-account.md)

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
### Praktik 1: Membuat Directory Git Pertama

Berikut adalah urutan perintah untuk memulai proyek dari nol hingga tersimpan di dalam sistem Git:

**1. Menyiapkan Folder Proyek**
Buat folder baru dan masuk ke dalamnya menggunakan perintah UNIX yang telah dipelajari sebelumnya.


```bash
(base) [nisyk@arch ~]$ mkdir proyek_pertama
(base) [nisyk@arch ~]$ cd proyek_pertama
```

**2. Inisialisasi Git (git init)** 
Langkah ini wajib dilakukan untuk membuat folder rahasia `.git` yang berfungsi sebagai pusat data.

```bash
(base) [nisyk@arch proyek_pertama]$ git init
Initialized empty Git repository in /home/nisyk/proyek_pertama/.git/
```

**3. Membuat File & Cek Status** 
Buatlah sebuah file (misalnya file text baru) lalu periksa bagaimana Git mendeteksinya.

```bash
(base) [nisyk@arch proyek_pertama]$ touch halo.txt    # perintah membuat file

(base) [nisyk@arch proyek_pertama]$ git status        # mengecek status git
On branch master  
Untracked files:  
 (use "git add <file>..." to include in what will be committed)  
       halo.txt  
  
nothing added to commit but untracked files present (use "git add" to track)
# Sistem mendeteksi ada file baru, namun belum masuk ke Staging Area (dikategorikan sebagai Untracked files)
```

**4. Memindahkan ke Staging Area (git add)** 
Proses ini memindahkan file ke "Meja Packing" untuk persiapan penyimpanan.

```bash
(base) [nisyk@arch proyek_pertama]$ git add halo.txt   
# menambahkan halo.txt ke Staging Area

(base) [nisyk@arch proyek_pertama]$ git status
On branch master  
Changes to be committed:  
 (use "git restore --staged <file>..." to unstage)  
       new file:   halo.txt               
# Sistem mendeteksi file baru yang sudah masuk ke Staging Area
```

**5. Menyimpan ke Repository (git commit)**
Langkah ini mengunci perubahan secara permanen ke dalam "Gudang" (Repository).
```bash
(base) [nisyk@arch proyek_pertama]$ git commit -m "commit pertama saya"  
# input
[main (root-commit) 7a2b3c4] commit pertama saya 1 file changed, 0 insertions(+), 0 deletions(-)                                         
# output
```

**6. Memeriksa Riwayat (git log)** 
Pastikan perubahan telah tercatat di dalam sistem database Git.

```bash
(base) [nisyk@arch proyek_pertama]$ git log --oneline        # input
7a2b3c4 commit pertama saya                            # output
```
(Cara keluar dari git log, adalah dengan menekan tombol 'q')


