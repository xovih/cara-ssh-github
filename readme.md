#   Cara Menggunakan SSH Key Untuk Koneksi Ke GitHub

Referensi jika ingin googling dengan kata kunci **github ssh key**

##  Mengapa Menggunakan SSH ?

*   Alasan keamanan repository anda
*   Tidak repot menuliskan username dan password setaiap kali **push & pull**
*   Lebih cepat akses remote ke server
*   Cara kerjanya adalah GitHub mengidentifikasi ke laptop anda dengan key number

##  Cara Generate SSH Baru di Laptop Anda

Cara cek SSH di laptop anda, ketik kode brikut :

``` 
cat ~/.sssh/id_rsa.pub
```

Apabila muncul seperti ini :
```
ssh-rsa
AAAAB3Nza..xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz xovih@divmu.local
```

xyz adalah key yang saya samarkan ^_^

##  Apabila tidak muncul baris seperti diatas?

Anda harus generate key baru, caranya:

```
ssh-keygen -t rsa -b 4096 -C "email_anda@contoh.com"
```

Kemudian muncul pertanyaan, anda enter-enter saja untuk set secara default.

##  Apabila muncul baris seperti diatas?
Anda harus menambahkan key tsb ke SSH-Agent, cara nya:

```
eval $(ssh-agent -s)
--> akan muncul: Agent pid xxxxx
```

Tambahkan key ke ssh-agent:
```
ssh-add -K ~/.ssh/id_rsa
```

Kemudian tambahkan SSH key ke account Github anda.
Sebelumnya copy dulu key anda ke clipboard, dengan cara:

```
pbcopy < ~/.ssh/id_rsa.pub
```
Anda login ke account github.com, dengan langkah:

Ke profile anda.
Klik Setting.
Klik ssh key.
Beri nama pada form.
Paste key ke dalam kotak yang disediakan.
Pelajari Git lebih lanjut:

https://git-scm.com/book/id/v1/Memulai-Git-Dasar-Git