#### < [Fundamental Git](1-fundamental-git.md)

# Perintah UNIX
Untuk menggunakan Git CLI, perlu tahu cara "berjalan" di dalam folder komputer menggunakan perintah teks, bukan klik mouse. Perintah-perintah dasar UNIX ini adalah bahasa standar untuk mengelola repository git (karena secara default git CLI menggunakan perintah UNIX, baik di Windows, macOS, dan Linux) dan server (VPS) dan merupakan keahlian wajib bagi seorang profesional agar bisa bekerja secara mandiri. Cukup pelajari beberapa kata kunci navigasi sederhana agar tidak tersesat di dalam terminal saat mengelola proyek. 

| Perintah     | Fungsi                                                                                                         |
| ------------ | -------------------------------------------------------------------------------------------------------------- |
| pwd          | **Print Working Directory**. Menunjukkan posisi directory/folder mana yang kamu operasikan.                    |
| ls           | **List**. Melihat daftar file dan directory/folder yang ada di lokasi sekarang.                                |
| cd {nama}    | **Change Directory.** Masuk ke dalam sebuah directory/folder.                                                  |
| mkdir {nama} | **Make Directory**. Membuat directory/folder baru.                                                             |
| tree         | **Tree**. Melihat daftar seluruh isi directory/folder serta isi directory/folder di dalamnya (secara beranak). |
### pwd
Perintah ini dapat menunjukkan posisi directory/folder mana yang kamu operasikan. Ibarat  bertanya ke sistem "Saya ada di mana?", dan sistem menunjukkan sebuah koordinat.
```bash
(base) [nisyk@arch USER]$ pwd               # input
/home/nisyk/Documents/USER                  # output
```

### ls
Perintah ini dapat melihat daftar file dan directory/folder yang ada di lokasi sekarang. Ibarat bertanya ke sistem "Aku ingin melihat isinya!", dan sistem menunjukkan list isi di dalamnya.
```bash
(base) [nisyk@arch USER]$ ls                # input

CODINGAN.py                   INABAKUMORI_LAGTRAIN.mp3  PHOTO_BURUNG.jpg
FOLDER_RAHASIA_JANGAN_DIBUKA  LAPRAK.docx   # output
```

### cd 
Perintah ini digunakan untuk masuk ke directory/folder yang ada di dalam directory/folder yang dioperasikan. Ibarat meminta ke sistem "Aku ingin masuk ke sana", dan sistem  memindahkan ke sana. 
```bash
(base) [nisyk@arch USER]$ cd FOLDER_RAHASIA_JANGAN_DIBUKA    # input
(base) [nisyk@arch FOLDER_RAHASIA_JANGAN_DIBUKA]$            # output
Instalasi```

### mkdir
Perintah ini digunakan untuk membuat directory/folder baru yang ada di dalam directory/folder yang dioperasikan. Ibarat meminta ke sistem "Buatkan aku ruangan baru", dan sistem membuatkan ruang baru.
```bash
(base) [nisyk@arch USER]$ mkdir FOLDER_BARU     # input

(base) [nisyk@arch USER]$ ls                    # gunakan ls utk melihat isi
CODINGAN.py  FOLDER_RAHASIA_JANGAN_DIBUKA  LAPRAK.docx
FOLDER_BARU  INABAKUMORI_LAGTRAIN.mp3      PHOTO_BURUNG.jpg  
# output (terdapat file baru, yaitu FOLDER_BARU) 
```

### tree
Perintah ini mirip seperti ls, namun tree memberikan list file yang berasal dari directory turunannya, dalam bentuk mirip cabang-cabang pohon. Ibarat meminta ke sistem "Aku ingin melihat semua isinya, termasuk isinya dari tempat itu (yang belum kumasuki)", dan sistem menunjukkan isinya, termasuk anak-anak (turunan)-nya
```bash
(base) [nisyk@arch USER]$ tree                     # input
.
├── CODINGAN.py                                    # output
├── FOLDER_BARU
├── FOLDER_RAHASIA_JANGAN_DIBUKA
│   └── KODE_NUKLIR.txt
├── INABAKUMORI_LAGTRAIN.mp3
├── LAPRAK.docx
└── PHOTO_BURUNG.jpg                              
```

> **⚠️ Catatan Penting:** Berbeda dengan sistem command Windows, sistem command UNIX tergolong case-sensitive. Jadi perhatikan nama dan kapitalisasi file/directory yang dituju. UNIX memberi pesan error jika kapitalisasinya salah, meskipun nama sudah benar. 
> 	Contoh: FOLDER_BARU, harus diketik dengan FOLDER_BARU, bukan folder_baru
#### > [Menghubungkan git ke akun GitHub](3-connect-account.md)
