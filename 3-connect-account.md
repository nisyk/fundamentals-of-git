#### < [Perintah UNIX](2-unix-command.md)

# Menghubungkan git ke akun GitHub
Setelah berhasil mengelola perubahan di komputer lokal, langkah krusial selanjutnya adalah menghubungkan proyek tersebut ke server luar agar dapat diakses oleh tim atau disimpan sebagai cadangan (_backup_). Dalam konteks profesional, server ini bisa berupa GitHub, GitLab, atau Gitea di VPS.

### 1. Konfirmasi Identitas (Wajib)
Sebelum melakukan pengiriman data, Git memerlukan identitas pengguna agar setiap perubahan memiliki keterangan penulis yang jelas. Konfigurasi ini hanya perlu dilakukan satu kali di perangkat yang digunakan.
```bash
# Mengatur nama lengkap
git config --global user.name "Nama Pengguna"

# Mengatur email aktif
git config --global user.email "email@contoh.com"
```

Untuk login ke GitHub, Git akan memunculkan jendela _pop-up_ browser (Git Credential Manager). Kamu cukup klik "Sign in with your browser" dan login seperti biasa.
Jika tidak berhasil, kamu harus membuat **Personal Access Token (PAT)** karena GitHub sudah tidak mengizinkan login pakai password biasa di terminal.
Untuk [Mendapatkan PAT](https://github.com/settings/tokens), klik hyperlink di samping, dan klik Generate new token. 
> Untuk tutorial lebih lengkapnya, [klik di sini](https://www.geeksforgeeks.org/git/how-to-login-using-the-git-terminal/)

### 2. Konsep Dasar: Local ke Remote

Menghubungkan Git ke server berarti menghubungkan **Local Repository** (di komputer) dengan **Remote Repository** (di internet/VPS).

| **Istilah** | **Penjelasan**                                            | **Analogi**                    |
| ----------- | --------------------------------------------------------- | ------------------------------ |
| **Remote**  | Alamat URL server tempat proyek disimpan secara daring.   | Alamat Gudang Pusat.           |
| **Origin**  | Nama panggilan (alias) standar untuk alamat server utama. | Nama Gudang Pusat.             |
| **Push**    | Proses mengirimkan _commit_ dari lokal ke server.         | Mengirim barang ke gudang.     |
| **Pull**    | Proses mengambil perubahan terbaru dari server ke lokal.  | Mengambil kiriman dari gudang. |

#### > [Perintah Dasar Git](4-git-basic-command.md)