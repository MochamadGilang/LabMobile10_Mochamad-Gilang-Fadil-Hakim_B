## LOGIN PAGE
![Screenshot 2024-11-14 145502](https://github.com/user-attachments/assets/8ffd150b-30bf-472a-84c9-b3f03dc23b57)

![Screenshot 2024-11-14 221718](https://github.com/user-attachments/assets/d95539d1-4c0a-44c3-bd1c-c577a85c546b)

## HOME PAGE 
![Screenshot 2024-11-14 145336](https://github.com/user-attachments/assets/ebaea531-9bc6-4bbc-93d1-6822ef3e4679)

## PROFILE PAGE
![Screenshot 2024-11-14 145312](https://github.com/user-attachments/assets/65268b49-8b88-43e7-acde-8e4e5043fa21)

- Firebase

Langkah pertama adalah menyiapkan Firebase Authentication melalui Firebase Console. Di bagian Authentication, metode login menggunakan Google perlu diaktifkan pada menu Sign-in method. Setelah metode ini diaktifkan, aplikasi akan mendapatkan Client ID yang diperlukan untuk konfigurasi Google Sign-In. Langkah ini juga melibatkan pengaturan aplikasi untuk meminta izin pengguna mengakses data dasar mereka, seperti nama lengkap (displayName), alamat email (email), dan foto profil (photoURL). Data ini dibutuhkan agar aplikasi dapat menampilkan informasi pengguna setelah login berhasil.

- Autentikasi

Proses autentikasi dimulai ketika pengguna memilih untuk masuk dengan akun Google mereka. Setelah memilih akun, aplikasi meminta izin untuk mengakses informasi dasar pengguna, seperti nama, email, dan foto profil. Jika izin ini diberikan, Google mengeluarkan token autentikasi sebagai bukti bahwa pengguna telah login dengan sukses. Token ini kemudian dikirim ke Firebase untuk diverifikasi. Firebase memvalidasi token tersebut untuk memastikan keabsahan akun pengguna. Jika verifikasi berhasil, Firebase akan mengembalikan objek user yang berisi data pengguna, seperti nama lengkap (displayName), alamat email (email), dan foto profil (photoURL). Data ini kemudian digunakan dalam aplikasi untuk menampilkan informasi pengguna.

- Fetching data/ pengambilan data

Setelah berhasil login, aplikasi menggunakan data dari objek user yang diterima dari Firebase untuk menampilkan informasi pengguna di layar. Data seperti nama lengkap, email, dan foto profil diakses melalui properti user.displayName, user.email, dan user.photoURL Selain itu, aplikasi menyediakan fitur logout yang memungkinkan pengguna untuk keluar dari sesi login. Saat logout, aplikasi akan mengakhiri sesi autentikasi dengan Firebase dan Google, serta menghapus data pengguna dari aplikasi. Langkah ini memastikan data pengguna tidak tersimpan secara permanen dan sesi berakhir aman.
