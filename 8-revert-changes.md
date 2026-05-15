#### < [Branching dasar](7-basic-branching.md)

# Mengembalikan (Revert) Perubahan di Git
Dalam pekerjaan, terkadang kesalahan bisa saja terjadi. Namun, semakin profesional skala pekerjaan, semakin kecil toleransi terhadap kesalahan. Oleh karena itu, sangat penting untuk mempelajari cara mengembalikan pekerjaan yang kacau menjadi kembali seperti semula. 

Dalam Git, **Revert** adalah perintah yang sangat penting untuk dipahami karena berfungsi sebagai "alat emergency utama" saat terjadi kesalahan yang sudah terlanjur dipublikasikan ke server.

`git revert <commit_id>` digunakan untuk membatalkan perubahan yang ada pada satu _commit_ tertentu dengan cara membuat satu _commit_ baru yang berisi "kebalikan" dari perubahan tersebut. Dengan cara ini, history proyek tetap terjaga dan tidak ada data yang hilang secara misterius, yang sangat penting saat bekerja di GitHub/VPS.

### Mengembalikan perubahan yang kacau menjadi seperti semula

**1. Mencari `commit_id`**
Gunakan `git log` untuk menemukan `commit_id` yang berupa hash dari commit yang ingin dibatalkan.
```bash
git log --oneline                            # input

# output 
7a2b3c4 feat: menambah fitur yang error     # <-- ambil commit_id dari sini
5d1e2f3 feat: commit sebelumnya yang stabil
```
(Cara keluar dari git log, adalah dengan menekan tombol 'q')

**2. Menjalankan revert**
Masukkan `commit_id` yang dianggap salah dalam perintah `git revert`
```bash
git revert 7a2b3c4
```

**3. Memeriksa hasil**
Periksa kembali riwayat untuk melihat bahwa Git telah membuat catatan baru.
```bash
git log --oneline                           # input

# output
a1b2c3d Revert "feat: menambah fitur yang error"   # <-- commit sudah direvert
7a2b3c4 feat: menambah fitur yang error 
5d1e2f3 feat: commit sebelumnya yang stabil
```


**⚠️ Catatan Penting:** Sangat penting membedakan antara `git revert` dan `git reset`. `git reset` menghapus Commit History yang ingin dihapus, sehingga sangat berbahaya jika dilakukan di tempat kolaborasi seperti server GitHub/VPS. 