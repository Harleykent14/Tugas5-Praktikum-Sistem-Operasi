**1. Eksekusi seluruh profile yang ada :**

a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :

      echo “Profile dari /etc/profile”

![T(1)](https://github.com/user-attachments/assets/021c4c11-aa30-47aa-9aae-ca0f27d8bde6)

![T(2)](https://github.com/user-attachments/assets/2b4a1bb4-9bb6-4b5d-b8b7-1d3a4070ef97)


b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :

   
    /home/stD02001/.bash_profile 
    /home/. stD02001/.bash_login 
    /home/mahasiswa/.profile 
    /home/mahasiswa/.bashrc

   
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap 
file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile : 

    echo “Profile dari .bash_profile”
  
Saya memakai 2 user account, yaitu satu dengan nama "kentvb" dan satunya "guest"

![T(3)](https://github.com/user-attachments/assets/49cc4a39-297c-4dfd-b75d-819338300131)

  `  nano /home/angga/.bash_profile
![T(4)](https://github.com/user-attachments/assets/3aff7d49-ac75-468d-a149-0a88d084edcd)

      nano /home/angga/.bash_login  
![T(5)](https://github.com/user-attachments/assets/fd1ce705-a826-4fb2-8481-a8c17e2f73b9)

      nano /home/guest/.profile
![T(6)](https://github.com/user-attachments/assets/f78e8016-6d6d-45ab-a32a-3b3dba64c450)

      nano /home/guest/.bashrc
![T(7)](https://github.com/user-attachments/assets/7fe4469b-d721-4a6b-b389-cac8c9d1666c)


c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:

    $ su mahasiswa 
    $ exit
    
kemudian gunakan opsi – sebagai berikut :

    $ su – mahasiswa 
    $ exit
    
Jelaskan perbedaan kedua utilitas tersebut.

Jawab : perbedaan dari kedua Utilitas tersebut adalah pada :


    $ su mahasiswa
itu tidak memuat profil login pengguna baru, dan hanya mengganti pengguna saja.


sedangkan :

    $ su - mahasiswa
itu mengganti pengguna sekaligus memuat profil pengguna tersebut sehingga seperti benar benar login dari awal.

![T(8)](https://github.com/user-attachments/assets/07f04bde-57a1-4542-b197-e53449fc9796)



**2. Prompt String (PS)**

 
a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan 
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell

    PS1='>' 
    export PS1 
    
![T(9)](https://github.com/user-attachments/assets/a26b08fb-95f1-475f-ae22-83e767d939ec)


b. Eksperimen hasil PS1 : 


command line dan keterangannya :


Mengubah prompt String menjadi urutan perintah :

    $ PS1=“\! > “ 

Mengubah prompt String menjadi tanggal :

    $ PS1=”\d > “ 
    
Mengubah prompt String menjadi waktu :

    $ PS1=”\t > “ 

Mengubah prompt String menjadi nama pengguna :

    $ PS1="\u > “ 

Mengubah prompt String menjadi dir saat ini :

    $ PS1=”\w >” 

    
Mengubah prompt String menjadi nama host :

    $ PS1="\h >”

![T(10)](https://github.com/user-attachments/assets/8bf0ee37-5d81-4896-a730-a58b3d55a703)


**3. Logout**

Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout

      Echo “Terima kasih atas sesi yang diberikan”
      Sleep 5 
      clear

![T(11)](https://github.com/user-attachments/assets/bfe7aa06-5119-4af3-9250-42b59d350509)

![T(12)](https://github.com/user-attachments/assets/e86e1a34-64c6-4040-adcd-bca6f405b9d0)


**4. Bash script**

   
a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing : 

![T(16)](https://github.com/user-attachments/assets/6e2f07c7-9a6b-4134-a8f1-b38b89e7d170)

 #p1.sh
  
    #! /bin/bash 
    echo “Program p1” 
    ls –l   

![T(13)](https://github.com/user-attachments/assets/5ccfbdca-e504-4617-a7a9-c794951aa453)

#p2.sh
  
    #! /bin/bash 
    echo “Program p2” 
    who 

![T(14)](https://github.com/user-attachments/assets/79e49e47-fe3d-4a3a-a425-09984a0c2f19)

#p3.sh
  
    #! /bin/bash 
    echo “Program p3” 
    ps x

![T(15)](https://github.com/user-attachments/assets/4a45db52-d387-414f-a412-e6595846a8c1)















