# PublicSCRCPY
access the scrcpy service using a public address

# Tools
- SCRCPY (PC/Desktop) https://github.com/Genymobile/scrcpy

- localtonet (APK) https://play.google.com/store/apps/details?id=com.localtonet.localtonetapp

# Langkah Kerja
1. download dan install semua tools
2. koneksikan android dan PC menggunakan kabel USB
3. scan perangkat android menggunkan adb </br>
command :
```
adb devices
```
result :
```
List of devices attached
**ID_DEVICE**        device
```
![image](https://github.com/user-attachments/assets/aca3aa62-6cb0-4345-a9eb-8556643533b9) </br>
4. setelah device terdeteksi, lanjut untuk konfigurasi port tcpip adb </br>
command :
```
adb tcpip <custom port>
```
example :
```
adb tcpip 4321
```
result :
```
restarting in TCP mode port: 4321
```
![image](https://github.com/user-attachments/assets/15614a73-b4aa-4877-82c9-9094e044e5da) </br>
5. buka aplikasi localtonet </br>
![image](https://github.com/user-attachments/assets/9b75dac1-dad0-4d91-afce-a656f8cdd566) </br>
6. register terlebih dahulu, kemudian tempelkan kunci akun ke kolom input "Enter Authtoken" </br>
![image](https://github.com/user-attachments/assets/1f878666-c620-4a66-9b73-6ce39e4082d3) </br>
7. Buka dashboard akun "localtonet" di http://localtonet.com </br>
![image](https://github.com/user-attachments/assets/377288e9-2f12-4b20-a6fe-e7b61f3a499c) </br>
![image](https://github.com/user-attachments/assets/2b37d689-af2d-484b-8b01-99a993dd7148) </br>
8. Buka menu "My Tunnels" lalu pilih submenu "TCP - UDP" </br>
![image](https://github.com/user-attachments/assets/6faf360a-5cbe-4a70-bcb6-40620d3765b0) </br>
![image](https://github.com/user-attachments/assets/f780eb67-74ca-406c-b96b-d833ed88f57d) </br>
9. pilih protokol "TCP", lalu pilih server (bebas), lalu isi pada kolom ip menggunakan ip lokal (127.0.0.1) dan port sesuai yang telah dikonfigurasi menggunakan adb (example: 4321), lalu create </br>
![image](https://github.com/user-attachments/assets/84d2b9ff-3f55-4502-b80e-f53d19873af7) </br>
![image](https://github.com/user-attachments/assets/60fbfbb6-8b37-4629-8c39-be68c1c7ead8) </br>
10. Setelah berhasil create, bisa langsung strat service </br>
![image](https://github.com/user-attachments/assets/ace04985-1e3a-457f-87ff-3de3310c389c) </br>
11. Buka kembali aplikasi "localtonet" maka akan muncul Tunnel yg telah kita buat tadi dengan status online </br>
![image](https://github.com/user-attachments/assets/49b51c89-7f7f-442a-b4cc-fa6315291506) </br>
12. akses scrcpy via localto.net </br>
example :
```
host:port = id1.localto.net:1735
```
![image](https://github.com/user-attachments/assets/aee302a1-de74-4358-8eb3-1440f9fe2c89) </br>
scrcpy command :
```
scrcpy --tcpip=id1.localto.net:1735
```
result :
```
scrcpy 2.3.1 <https://github.com/Genymobile/scrcpy>
INFO: Connecting to id1.localto.net:1735...
INFO: Connected to id1.localto.net:1735
C:\Users\video\scrcpy-win64-v2.3.1\scrcpy-server: 1 file pushed, 0 skipped. 50.0 MB/s (66007 bytes in 0.001s)
[server] INFO: Device: [Xiaomi] Redmi **DEVICE** (Android 14)
[server] ERROR: Encoding error: java.lang.IllegalArgumentException:
[server] INFO: Retrying with -m1920...
[server] INFO: Retrying...
INFO: Renderer: direct3d
INFO: Texture: 1080x2400
INFO: Texture: 864x1920
```
![image](https://github.com/user-attachments/assets/2115b416-5abf-4fa4-af29-cf86a0ca21ef)

# Penutup
- Kekurangan :
   - Tampilan lambat, tidak secepat menggunakan kabel
   - Bila ada orang lain yang mengetahui ip dan port nya, maka mereka juga bisa mengakses
- Kelebihan
   - Bisa melakukan remote perangkat android jarak jauh













