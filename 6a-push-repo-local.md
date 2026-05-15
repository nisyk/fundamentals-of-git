#### < [Push dan pull repository dari local ke GitHub](6-push-n-pull-repository.md)

# Push dan pull repository dari local ke GitHub (git init)
Setelah perubahan tersimpan di repositori lokal melalui _commit_, langkah selanjutnya adalah mengirimkan data tersebut ke server (_remote repository_)

Sebelum melakukan `push`, alamat server harus didaftarkan terlebih dahulu ke dalam sistem lokal.

```bash
# 1. Daftarkan alamat server (hanya dilakukan sekali di awal proyek)
git remote add origin https://github.com/username/nama-repo.git

# 2. Kirim data dan atur jalur utama (upstream)
git push -u origin main
```