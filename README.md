# Create-An-Application-using-Apache-Cordova
This is a step by step how to create an application using apache cordova

Buat Folder yang nantinya akan menjadi alamat dari semua bahan yang diinstall, kalau saya menyimpan di C:\Users\Mark Azaz\Android dan didalamnya buat folder baru lagi bernama jdk,jre,nodejs

Setelah di download, run atau install file tersebut.

Cara install JDK
1. Klik jdk nya, setelah installer nya muncul ubah alamat folder sesuai dengan tempat penyimpanan yang kita buat tadi. Kalau saya di C:\Users\Mark Azaz\Android\jdk
2. setelah itu klik next, lalu masukkan lagi jre nya ke folder yang udah dibuat tadi. kalau saya di C:\Users\Mark Azaz\Android\jre
3. lalu klik next,next sampai proses semuanya selesai.
4. Jdk terinstall.

Cara install Git
1. Sama seperti proses install JDK, hanya saja alamat folder diubah sesuai dengan folder yang kita buat. Kalau saya di C:\Users\Mark Azaz\Android\git
2. setelah itu di next, lalu ada tampilan code editor, pilih sesuai dengan text editor yang kalian gunakan. disini saya menggunakan VS Code Editor.

Cara Install Gradle 
1. Ekstrak foldernya ke tempat folder yang kalian buat. Kalau saya di C:\Users\Mark Azaz\Android
2. Ubah nama gradle-7.3 menjadi gradle aja.

Cara install node js
1. sama seperti sebelumnya, klik next next aja nanti yang diubah cuma alamat foldernya. Kalau saya di C:\Users\Mark Azaz\Android\nodejs

Cara install commandline-tools
1. Cara nya sama seperti gradle, kalian tinggal ekstrak aja commandline-tools nya ke alamat folder yang telah dibuat. kalau saya di C:\Users\Mark Azaz\Android
2. Setelah itu kalian klik folder commandline-toolsnya, terus muncul bin,lib NOTICE, source.properties. Disini kalian buat folder baru dengan nama tools, lalu masukkan bin,lib,NOTICE, source.properties tadi ke dalam folder tools.


Setelah semuanya terinstall, cara selanjutnya yaitu kalian masukkan alamat folder kalian ke environment variabel. Caranya, kalian ketik Control Panel, lalu ke system and security => system => scroll ke bawah => klik advanced system settings => klik environment variabel => ke system variabels => cari path, lalu klik => nah disini kalian harus memasukkan alamat folder dengan benar dengan cara => klik new => browse => cari alamat folder kalian.

Alamat folder saya yaitu
1. C:\Users\Mark Azaz\Android\jdk\bin
2. C:\Users\Mark Azaz\Android\jre
3. C:\Users\Mark Azaz\Android\gradle\bin
4. C:\Users\Mark Azaz\Android\git\Git\cmd
5. C:\Users\Mark Azaz\Android\nodejs\

Untuk memastikan bahwa path yang kalian masukkan sudah benar, buka CMD run as administrator 

1. Ketik $ java -version kalau sudah muncul versi dari java nya berarti sudah benar.
2. Ketik $ git ==version kalau sudah muncul versi dari git nya berarti sudah benar.
3. Ketik $ gradle -version kalau sudah muncul versi dari gradle nya berarti sudah benar.
4. Ketik $ node -v kalau sudah muncul versi dari nodejs nya berarti sudah benar.

NOTE : Tidak perlu pakai ($).

Setelah itu, masuk ke folder commandline-tools => tools => bin => lalu klik kanan pada mouse dan klik "git bash here".
Setelah muncul terminalnya, copy teks berikut 
./sdkmanager.bat "build-tools;29.0.3" "emulator" "extras;intel;Hardware_Accelerated_Execution_Manager" "platforms;android-29" "platform-tools" "system-images;android-29;google_apis;x86" --verbose

tunggu proses intalasi selesai, biasanya membutuhkan waktu yang lumayan lama.

Kalau yang udah install Cordova tinggal ke tahap selanjutnya.

Bagi yang belum install Cordova, caranya begini

Pertama paste ini untuk install Cordova
npm install -g cordova
 
cordova create MyApp (MyApp ini bisa diganti dengan aplikasi yang ingin kalian buat misalnya saya buat cordova create Marka)

cd MyApp ( cd nama aplikasi yang tadi dibuat misalnya saya buat cd Marka)
cordova platform add browser
cordova run browser

Setelah semuanya terinstall, tinggal install android nya
karena saya ingin membuat di C:\Users\Mark Azaz\Android
maka tinggal ketik aja perintahnya

cordova create (Nama folder) com.add.database (namaAplikasi)

misalnya begini cordova create MyApp com.add.database Aplikasi_Saya
tunggu sampai "creating a new project"

lalu ketik lagi 
cd (nama foldernya)

kalau saya tadi kan membuat folder MyApp jadi

cd MyApp

terus ketik lagi

cordova platform add android

terus kalau mau install plugin bisa

cordova plugin add (nama plugin misalnya cordova-sqlite-storage)

cordova plugin add cordova-sqlite-storage

Setelah itu ketik

cordova build android

setelah build sukses, maka terdapat alamat dari aplikasi yang sudah anda buat. Anda perlu ke alamat sana, lalu membukanya pada emulator android seperti Bluestacks, NoxPlayer dll.

atau bisa juga mengkoneksi kan dengan device anda menggunakan kabel USB dan menginstall vysor di PC/laptop dan di HP.

setelah terkoneksi tinggal ketik perintah 

cordova run


Proses pembuatan aplikasi menggunakan Cordova dapat berjalan dengan sukses.
