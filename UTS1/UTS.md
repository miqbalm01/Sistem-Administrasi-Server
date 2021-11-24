# Ujian Tengah Semester (Sistem Administrasi Server)

###### Muhamad Iqbal Maulana 1202190023 IT-02-02



## Instalasi Windows Server 2022 di VirtualBox

- Pertama, Unduh file **ISO** **Windows Server 2022** dari https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022 .
- Untuk melakukan Instalasi, Buat Sebuah Project Baru. Lalu isikan sebuah nama **(Windows Server)**, Type Sistem Operasi **(Microsoft Windows)** serta Versi Sistem operasi **(Other Windows 64-bit).** 
- Lalu Tentukan Ukuran Memori**(1040 MB)**, Pilih Jenis Hardisk**(VDI)**, Ukuran Hardisk**(20 GB)**, Pilih Tempat Penyimpanan Project Tersebut.

![image1](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image1.png)



- Selanjutnya, Masukkan File Iso Windows Server. Jika Belum Terdapat List Instalasi Iso, kita dapat buka browser kedalam file Explorer.
- Jika File iso sudah masuk, kita dapat melakukan **Start** Virtual Machine (Klik Tombol Mulai)

![image2](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image2.png)



- Pada Tampilan Awal instalasi Windows Server, kita dapat melakukan **konfigurasi bahasa** yang di pakai Sistem Operasi, Waktu dimana nantinya akan Mengikuti **Waktu setempat**, serta **Jenis Keyword** yang di pakai.

![image3](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image3.png)



- Untuk Instalasi kita dapat memilik 4 jenis pilihan, jika ingin simple dapat milih **(Windows Server 2022 Standard Evalution GUI)** karena pastinya memiliki tampilan, untuk melakukan proses perlu perintah code khusus. 
- Standar Evalution ini memiliki basis yang ringan karena tampilannya hanya berbasis CLI ( Command Line Interface ) yang tidak menampilkan tool dan tidak bergambar. Sedangkan Untuk Gui memiliki Ukuran yang lebih besar dari Standar Evalution karena pada edisi ini tampilannya akan seperti Windows yaitu yang meload GUI ( Graphycal User Interface ) dan tampilnnya akan bergambar yang di lengkapi dengan tool.  

![image4](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image4.png)



- Untuk jenis instalasi, dapat menggunakan **custom** karena dalam hal ini kita tidak mengupgrade server windows versi sebelumnya.

![image5](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image5.png)



- Selanjutnya, Kita dapat lakukan **pembagian partisi**. Pada kasus ini kita menggunakan 1 partisi aja (20 GB), pembagian ini dapat disesuaikan kebutuhan saja.

![image6](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image6.png)



- Setelah proses instalasi berhasil, lakukan setting profile pengguna, berupa **username serta password**. Pengaturan ini nantinya digunakan untuk masuk kedalam Windows Server

![image7](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image7.png)



- Pertama pastikan konfigurasi network pada virtual machine menggunakan **adapter ter bridge**, untuk dapat melakukan koneksifitas terhadap internet. 

![image8](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image8.png)



- Kita juga dapat melihat informasi dari windows server yang kita miliki, dengan **perintah win + ropen** (windows run) lalu ketik **winver**

![image9](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image9.png)





## **Konfigurasi IP Static**

- Sebelum Kita Melakukan Instalasi Active Directory Domain Services, pastikan windows server menggunakan IP Static agar memudahkan kita saat melakukan beberapa konfigurasi dan pastinya IP tidak berubah-ubah.
- Untuk konfigruasi IP Static, kita masuk kedalam **settings network dan internet**. Pilih properties ethernet, lalu pilih internet protocol Version 4(Ipv4) dan use the following IP Address.
- Di konfigurasi ini, kita dapat memasukkan IP address yang kita inginkan serta subnet mask.

![image10](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image10.png)



- Untuk Memastikan IP Static sudah berganti, kita dapat cek didalam Command Prompt. Dengan Mengetikkan **ipconfig**

![image11](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image11.png)



## Instalasi Active Directory Domain Services, Instalasi DNS server dan Instalasi Net Framework 3.5

- Masuk Ke Dalam Windows Server Manager, lalu klik **Add roles and features** 

![image12](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image12.png)



- Lalu pilihan **role-based or feture bases Installation** untuk menambahkan roles service

![image13](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image13.png)



- Nah disini kita ceklis roles server yang kita butuhkan. Seperti kasus kita ini, kita menambahkan **Active Directory Domain Service** dan **DNS Server**.

![image14](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image14.png)



- Muncul notifikasi Instalasi, Lalu klik **add features** 

![image15](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image15.png)



- Pada Instalasi Features, Tambahkan Net Framework 3.5 Features. 

![image16](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image16.png)



- Setelah Memilih Roles dan Features untuk di install. Pada form konfirmasi, lalu klik **Install**

![image17](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image17.png)



- Jika **Mengalami Masalah** Pada instalasi, tidak perlu kwatir. Ulangi lagi Kembali ke form konfirmasi dengan **catatan jangan lakukan instalasi terlebih dahulu.**

![image18](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image18.png)



- Nah disini kita sebelum lakukan instalasi, terlebih dahulu settings lokasi tempat file sistem operasi Windows Server ISO. 

![image20_2](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image20_2.png)



- Disini kita buka file ISO menggunakan **Windows Explorer pada Windows Utama(Windows 10)**

![image19](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image19.png)



- Lalu Kembali ke **Virtual Box(Windows Server). Buka File Explorer** cari lokasi tempat penyimpanan Source file ISO. Salin lokasi penyimpanan **(D:\sources\sxs).** 

![image20](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image20.png)



- Selanjutnya Masukkan lokasi penyimpanan didalam settings path **(D:\sources\sxs)**

![image21](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image21.png)



- Lalu Klik Install dan tunggu sampai proses selesai.

![image22](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image22.png)



- Untuk memastikan Net Framework 3.5 sudah terinstall. Buka **win-r** lalu ketiikan **regedit**, disini kita cari tempat net framework 3.5 **(Software->Microsoft->Ne Framework Setup->NDIP->v3.5)**

![image23](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image23.png)





## **Promote Server to a Domain Controller**

- Untuk Promote Server to a Domain Controller, kita dapat **klik notifikasi warna kuning tanda seru**. Nah di situ kita menemukan notifikasi menuju ke konfigurasi Promote domain.
- Active Directory Domain Services (ADDS) adalah layanan untuk mengelola aturan, hak akses, dan security pada pengguna atau jaringan komputer. ADDS mampu mengatur komunikasi user dan domain yang meliputi proses login, autentikasi, dan directory searches. Untuk menjalankan ADDS diperlukan domain controller.

![image24](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image24.png)



- Disini kita **tambahkan domain url** yang ingin dipakai. Selanjutnya Klik Next.

![image25](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image25.png)



- Pilih Jenis Forest Functional Level (Windows Server 2016) serta Domain Funcation Level (Windows Server 2016), lalu Masukkan Password yang kita gunakan pada saat awal masuk kedalam windows server. Pastikan juga DNS server terceklis. 

![image26](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image26.png)



- Disini kita dapat memilih tempat penyimpanan Database, log files, serta SYSVQL

![image27](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image27.png)



- Lalu sistem akan melakukan check pada instalasi apakah ada kekurangan pada sistem untuk melakukan instalasi Domain Controller. Jika sudah kita dapat **klik Install**

![image28](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image28.png)



- Setelah instalasi Promote Server to a Domain Controller Berhasil, Windows akan otomatis melakukan restart. Nah disini kita dapat masuk memakai akun VM yang kita buat tadi. 

![image29](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image29.png)



- Untuk Memastikan instalasi Promote Server to a Domain Controller berhasil, kita dapat membuka **Menu Tools ->Active Directory Users and Computers**

![image30](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image30.png)



- Disini kita dapat melihat, terdapat domain url **vm.local** yang kita terlah buat tadi.

![image31](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image31.png)



- Kita Juga dapat melakukan Ping terdapat url domain agar memastikan memiliki konektifitas domain. 

![image32](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image32.png)



- ·Untuk dapat mengetahui IP yang digunakan Domain Kita dapat menggunakan perintah nslookup. 

![image33](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image33.png)



- Lalu disini kita coba menggunakan Windows 10 untuk memastikan apakah bisa juga domain di akses oleh komputer client.
- Pertama, cari file host yang terdapat di directory Windows 10 **(C: -> Windows -> System32 -> Drivers -> etc)**
- Didalam File Host kita bisa **menambahkan IP dan domain** yang telah di konfigruasi pada Windows Server. 

![image34](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image34.png)



- Untuk memastikan Windows Server terhubung dengan komputer client kita coba lakukan **ping terhadap domain wm.local** dan Hasilnya berhasil.

![image35](https://github.com/miqbalm01/Sistem-Administrasi-Server/blob/main/UTS1/assets/image35.png)
