#### < [Push dan pull repository dari local ke GitHub](6-push-n-pull-repository.md)

# Push dan pull repository dari local ke GitHub (git init)
Setelah perubahan tersimpan di repositori lokal melalui _commit_, langkah selanjutnya adalah mengirimkan data tersebut ke server (_remote repository_)

Sebelum melakukan `push`, alamat server harus didaftarkan terlebih dahulu ke dalam sistem lokal.

1. Daftarkan alamat server (hanya dilakukan sekali di awal proyek)
```bash
git remote add origin https://github.com/username/nama-repo.git
```

2. Buat file baru, lalu lakukan **`git add`** dan **`git commit`**, *[Klik untuk intruksi selengkapnya](4-git-basic-command.md)*

3. **Upload repository yang sudah dicommit ke repository GitHub**
```bash
git push -u origin main
```
