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

### Sekian Pelajaran Pertaman Saya Di Github