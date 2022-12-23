<h1 align="center">Tutorial Testnet Gaganode</h1>

- [Website](https://meson.network/)
- [Discord](https://discord.gg/N3zkPUcvve)
- [Doc offcial](https://docs.gaganode.com)
- [Dashbord Node](https://dashboard.gaganode.com/register?referral_code=lupxzjvztr)

## Spesifikasi Minimum
| Komponen  | Requirements minimal               |
|-----------|---------------------               |
|  sistem   |  Ubuntu 18.04 atau lebih tinggi    |
|CPU        |4 Cores                             |
|RAM        |8 GB                                |
|Penyimpanan|20 GB HDD                           |
|Koneksi    |50 mbps upload & bandwidth download |

# Buat akun dan dapatkan Token ID 
- [Dashboard Gaganode](https://dashboard.gaganode.com/register?referral_code=lupxzjvztr)
- Buka URL di atas 
- Buat akun isi informasi anda
- Email, Password, kode reff **lupxzjvztr**
- Verifikasi Email 
- Login dan Copy Token ID anda 
- Simpan dan Lanjut Step berikut

Jika menggunakan Android, PC, atau VPS silahkan ikuti tutorial masing-masing

## USER linux VPS 

### Step Add user gaganode
ini bisa di skip atau bisa menggunakan user root lanjut **Install**

- buat password untuk user gaganode masukan nama bebas detail user tidak usah di isi tekan **enter** sampai konfirmasi **y**
```
sudo adduser gaganode
```
memberikan izin admin ke user **gaganode**
```
sudo usermod -aG sudo gaganode
```
login sebagai user gaganode
```
su - gaganode
```

### Install
```
sudo apt-get update -y && sudo apt-get -y install curl tar ca-certificates
```
add user gaganode ke docker (skip jika menggunakan user root)
```
sudo usermod -aG docker $USER
```
```
exit
```
### RUN Node
login sebagai user gaganode
```
su - gaganode
```
### User Linux 64-bit
```
curl -o app-linux-amd64.tar.gz https://assets.coreservice.io/public/package/22/app/1.0.3/app-1_0_3.tar.gz && tar -zxf app-linux-amd64.tar.gz && rm -f app-linux-amd64.tar.gz && cd ./app-linux-amd64 && sudo ./app service install
```
### User Linux 32-bit
```
curl -o app-linux-386.tar.gz https://assets.coreservice.io/public/package/21/app/1.0.3/app-1_0_3.tar.gz && tar -zxf app-linux-386.tar.gz && rm -f app-linux-386.tar.gz && cd ./app-linux-386 && sudo ./app service install
```
Start Service
```
sudo ./app service start
```
Check APP Status
```
./app status
```
Set Token
```
sudo ./apps/gaganode/gaganode config set --token=TOKEN-ANDA
```
dibagian `TOKEN-ANDA` ganti dengan Token anda
Restart APP
```
./app restart
```
```
./app status
```
- Jika STATUS sudah [RUNNING] tandanya berhasil 
[![Screenshot-2022-12-24-021322.png](https://i.postimg.cc/hjZZ5Xfs/Screenshot-2022-12-24-021322.png)](https://postimg.cc/N9Txyf82)

## Command Berguna lainya

- Check Log
```
./app log   
```
- restart node
```
./app restart
```
- update node
```
./app upgrade
```
- check node running status
```
./app status
```

- start service node
```
sudo ./app service start
```
stop node
```
sudo ./app service stop 
```
- delete node
```
sudo ./app service remove
```


- delete file node
```
sudo rm -r /home/gaganode/
```
- delete user gaganode
```
sudo userdel gaganode
```

### Art-Team INFO
noted: **art team** here does not have any specific goals or intentions, they only collect data and share it with everyone.

untuk INFO Testnet lainya Silahkan join Discord 👇

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/ArtSy5team)
[![Discord](https://img.shields.io/badge/discord-7289d9?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/EAKEdZU6c8)
[![Github](https://img.shields.io/badge/GitHub-171515?style=for-the-badge&logo=GitHub&logoColor=white)](https://github.com/Art-Sy5team)
[![trakteer](https://img.shields.io/badge/trakteer.id-e31e1e?style=for-the-badge&logo=ko-fi&logoColor=white)](https://trakteer.id/Art-Sy5team/tip)
