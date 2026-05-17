# fundamentals-of-git
Dokumen ini membahas fundamental penggunaan Git sebagai sarana pengelolaan perubahan file dan kolaborasi pengembangan proyek. Materi mencakup alur kerja dasar, pengelolaan versi, percabangan, serta sinkronisasi repository untuk mendukung proses pengembangan yang lebih terstruktur dan efisien. 
## Apa itu Git? 
Git adalah sistem kontrol versi terdistribusi yang digunakan untuk melacak perubahan pada kode dan memungkinkan banyak orang berkolaborasi secara efisien dalam satu proyek.

Git seperti mesin waktu untuk folder proyek, yang bisa membawa kamu kembali ke versi sebelumnya kapan pun tanpa kehilangan jejak perubahan.

### Apa itu Git CLI dan Mengapa? 
Git CLI (Command Line Interface) adalah cara menjalankan perintah git dengan mengetikkan teks di terminal atau command prompt, bukan dengan mengklik tombol di aplikasi GUI seperti GitHub Desktop atau Sublime Merge.

#### Mengapa harus dipelajari?
1. **Bisa digunakan di mana saja:** Aplikasi seperti GitHub Desktop sering kali dikunci untuk layanan tertentu. Dengan CLI, perintah yang kamu gunakan akan sama persis baik saat memakai GitHub, GitLab, maupun Gitea di VPS sendiri.
2. **Paham "Cara Kerja" yang sebenarnya:** Menggunakan CLI memaksa kita memahami alur kerja Git secara mendalam—mulai dari memindahkan file ke _Staging Area_ hingga melakukan _Commit_. Ini membangun "mental model" yang kuat bagi seorang profesional agar tidak bingung saat terjadi error.
3. **Standar Profesional:** Di dunia kerja, hampir semua dokumentasi teknis dan solusi masalah di forum (seperti Stack Overflow) menggunakan format CLI. Menguasainya membuat tim kamu lebih mandiri dan kompeten di berbagai lingkungan kerja.
#### Kelebihan dan Kekurangan Git CLI dibandingkan GitHub Dekstop
| Aspek             | Git CLI                                                                                                                                                                                  | GitHub Desktop                                                                                                               |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Kompabilitas      | + **Universal.** Bekerja di semua layanan (Gitea, GitLab, GitHub) dan bisa digunakan di lingkungan server/VPS                                                                            | - **Terbatas.** Teroptimasi khusus untuk GitHub dan tidak bisa digunakan VPS                                                 |
| Kontrol dan Fitur | + **Penuh.** Memberikan akses ke seluruh perintah Git, sangat kuat untuk menangani error kompleks atau otomatisasi (scripting).                                                          | - **Dasar.** Hanya menyediakan fitur-fitur yang paling sering digunakan; perintah tingkat lanjut sering kali tidak tersedia. |
| Efisiensi         | + **Sangat Cepat:** Jika sudah memahami fundamentalnya, mengetik perintah (dan menggabungkan ke perintah lain dalam satu baris) terasa jauh lebih cepat dibandingkan klik-klik bertahap. | = **Menengah:** Masih bergantung terhadap klik-klik bertahap, namun ideal jika belum memahami alur kerja dasarnya.           |
| Kurva Belajar     | - **Sulit:** Harus menghafal dan memahami perintah teks (syntax) dan membayangkan alur kerja sendiri tanpa bantuan tombol visual.                                                        | + **Mudah:** Sangat ramah pemula karena prosesnya tinggal klik-klik saja dan semua perubahan terlihat jelas di layar.        |

**Kesimpulannya:** Git CLI menawarkan kompabilitas dan kontrol yang sangat fleksibel (dapat bekerja di semua provider Git), namun memiliki kurva belajar yang sulit dibandingkan aplikasi GitHub Desktop.

----

### Sumber 
**Untuk informasi lebih mendalam dan mendasar, kunjungi:**

- [Pro Git Book; Scott Chacon & Ben Straub](https://git-scm.com/book/en/v2)
- [HowToGeek: Introduction to Git](https://www.howtogeek.com/beginning-git-what-it-is-and-why-its-crucial/)

#### > [Fundamental Git](1-fundamental-git.md)


---

Made by curious with 🌆 NISY. 
