## LOGIN PAGE
![Screenshot 2024-11-14 145502](https://github.com/user-attachments/assets/8ffd150b-30bf-472a-84c9-b3f03dc23b57)

Pertama waktu kita mengakses aplikasi ini muncul halaman seperti di atas, lalu kita klik "SIGN IN WITH GOOGLE" untuk login 

<!-- Button Sign In -->
                <ion-button @click="login" color="light">
                    <ion-icon slot="start" :icon="logoGoogle"></ion-icon>
                    <ion-label>Sign In with Google</ion-label>
                </ion-button>

![Screenshot 2024-11-14 221718](https://github.com/user-attachments/assets/d95539d1-4c0a-44c3-bd1c-c577a85c546b)
Selanjutnya pilih akun yang sudah di daftar dan kemudian klik "lanjutkan"

di bawah  ini ada kode ketika berhasil login dan langsung di arahkan ke homepage namun ketika gagal kita akan kembali pada halaman loginpage

router.beforeEach(async (to, from, next) => {
  const authStore = useAuthStore();
  
  if (to.path === '/login' && authStore.isAuth) {
    next('/home');
  } else if (to.meta.isAuth && !authStore.isAuth) {
    next('/login');
  } else {
    next();
  }
});


## HOME PAGE 
![Screenshot 2024-11-14 145336](https://github.com/user-attachments/assets/ebaea531-9bc6-4bbc-93d1-6822ef3e4679)

## PROFILE PAGE
![Screenshot 2024-11-14 145312](https://github.com/user-attachments/assets/65268b49-8b88-43e7-acde-8e4e5043fa21)
