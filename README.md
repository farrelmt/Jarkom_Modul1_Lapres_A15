Kelompok A15 :

Farrel Muhammad Taqi     05111840000071

Muhammad Iqbal Humam     05111840000103

**A. Display Filter**

1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"

    a. menggunakan syntax ``` http.host.contains "testing.mekanis.me" ```
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/1.1.png)
    
    b. kemudian klik kanan dan ```follow http stream```
    
    ![fotooo](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/1.2.png)

2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!
    
    a. klik file kemudian pilih ```Export Objects```
    
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/2.1.png)
    
    b. mencari file yang ingin didownload pada search bar
    
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/2.2.png)
    
    c. save dan beri nama sesuai yang diinginkan
    
    d. hasil :
    
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/2.3.jpg)


3. Cari username dan password ketika login di "ppid.dpr.go.id"!

    a. mencari dengan syntax ```http.host contains "ppid.dpr.go.id" && http.request.method == POST```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/3.1.png)
    
    b. klik 2x pada record yang ada, kemudian akan terlihat username dan password 
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/3.2.png)

4. Temukan paket dari web-web yang menggunakan basic authentication method!

    a. mencari dengan syntax ``` http.authbasic ```
    
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/4.1.PNG)

5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!

    a. membuka dulu ```aku.pengen.pw``` pada browser 
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/5.1.png)
    
    b. mencari di wireshark dengan syntax ```http.host contains "aku.pengen.pw"``` untuk mencari username dan password
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/5.2.png)
    
    c. klik 2x pada record dan mencari username dan password pada isi file
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/5.3.png)
    
    d. memasukkan username dan password ke ```aku.pengen.pw``` yang sudah dibuka pada langkah pertama, dan menjawab pertanyaan di dalamnya
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/5.4.png)

6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).

    a. mencari di display capture wireshark dengan syntax ```ftp-data.command contains "STOR Answer.zip"```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/6.1.png)
    
    b. klik kanan record yang ada dan follow tcp stream
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/6.2.png)
    
    c. ubah format file menjadi raw kemudian save as dan beri nama sesuai yang diinginkan
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/6.3.png)
    
    d. ekstrak file zip yang sudah didownload, namun kita belum mencari passwordnya
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/6.4.png)
    
    e. mencari di display capture wireshard dengan syntax ```ftp-data.command contains "STOR zipkey.txt"```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/6.5.png)
    
    f. klik kanan dan pilih follow tcp stream
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/6.6.png)
     
    g. maka akan langsung terlihat passwordnya
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/6.7.png)
    
    h. extract file zip tadi dengan password yang sudah ditemukan, kemudian terdapat file ```open this.pdf``` dan apabila dibuka akan ada tampilan sebagai berikut
     ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/6.8.png)


7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"
    
    a. mencari di display capture wireshark dengan syntax ```frame contains "Yes.pdf"```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/7.1.png)
    
    b. lakukan ```follow tcp stream``` kemudian ubah format menjadi ```raw``` dan save as puisi.zip
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/7.2.png)
    
    c. extract file ```puisi.zip``` dan nantinya akan ada file ```Yes.pdf```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/7.3.png)
    
    d. hasil :
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/7.4.png)
    



8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

    a. mencari ip dari Microsoft FTP Service terlebih dahulu
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/8.1.png)
    
    b. mencari di wireshark display capture dengan syntax ```ftp.request.command == RETR" && ip.dst == 198.246.117.106"``` yang merupakan ip dari Microsoft FTP Service
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/8.2.png)
    
    c. ditemukan 1 file readme
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/8.3.png)
    
    d. isi dari readme tersebut :
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/8.4.png)


9. Cari username dan password ketika login FTP pada localhost!

    a. mencari di display capture dengan syntax    ```tcp.dst == 21```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/9.1.png)
    
    b. klik kanan dan pilih ```follow tcp stream```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/9.2.png)
    


10. Cari file .pdf di wireshark lalu download dan buka file tersebut! clue: "25 50 44 46"
    
    a. tekan ```ctrl + f``` untuk menggunakan fitur find
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/10.1.png)
    
    b. follow tcp stream dan ubah ke raw, kemudian save as dengan nama sesuai yang diinginkan
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/10.2.png)
    
    c. hasilnya :
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/10.3.png)




**B. Capture Filter**

11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
    a. test ```test```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/11.1.PNG)
    
    b. test
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/11.2.PNG)


12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
    a. test ```test```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/12.1.PNG)
    
    b. test
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/12.2.PNG)



13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
    a. test ```test```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/13.1.PNG)
    
    b. test
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/13.2.PNG)



14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
    a. test ```test```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/14.1.PNG)
    
    b. test
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/14.2.PNG)

    c. test
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/14.3.PNG)


15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
    a. test ```test```
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/15.1.PNG)
    
    b. test
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/15.2.PNG)

    c. test
    ![](https://github.com/farrelmt/Jarkom_Modul1_Lapres_A15/blob/main/Screenshot/15.3.PNG)


