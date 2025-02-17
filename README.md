# Web Mapping

Menurut Wikipedia, Web mapping merupakan proses penggunaan peta berdasarkan Sistem Informasi Geografi pada World Wide Web (www). Sebuah peta web pada World Wide Web tidak hanya disediakan untuk pengguna tetapi pengguna juga dapat menentukan apa yang akan ditampilkan oleh peta tersebut. Sedangkan Web GIS memiliki fokus pada aspek pemrosesan geodata yang lebih melibatkan pada aspek desain seperti akuisisi data dan arsitektur software server. Penggunaan istilah web GIS dan web mapping seringkali memiliki maksud yang sama. 


## Web Map Service (WMS) 
WMS merupakan protokol standar yang dikembangkan oleh Open Geospatial Consortium (OGC) untuk pelayanan citra peta yang telah dilakukan proses georeferensi di internet. Citra ini biasanya diproduksi oleh map server berdasarkan data yang diambil dari GIS database. Beberapa contoh software yang mendukung web map service ialah:
- deegree
- GeoServer
- MapServer
- MapGuide Open Source
- QGIS Server

# Tutorial penggunaan GeoServer untuk web mapping
Pada kesempatan ini akan dibahas cara untuk menampilkan shape file dari peta indonesia pada web. Untuk melakukannya setidaknya dibutuhkan:

## Setting up GeoServer
### Download dan install OpenJDK
 - `sudo apt-get install openjdk-8-jre`

### Download dan install Apache2
 - `sudo apt-get install apache2`

### GeoServer, versi yang digunakan pada tutorial ini adalah versi 2.14.2
 - Unduh pada laman [ini](http://geoserver.org/release/stable/).
 - Pilih Platform Independent Binary
 - `sudo apt install unzip`
 - `mkdir -p /var/www/geoserver`
 - `cd /var/www/geoserver`
 - pindahkan file yang telah didownload ke folder `/var/www/geoserver`
 - `unzip geoserver-2.14.2-bin.zip`
 - `mv geoserver-2.14.2/* .`
 - `echo "export GEOSERVER_HOME=/var/www/geoserver" >> ~/.profile`
 - `. ~/.profile`

### Running
 - `JAVA_HOME="/usr/lib/jvm/java-8-openjdk-amd64"`
 - `sudo /etc/init.d/apache2 start` 
 - `sudo ./bin/startup.sh`

Pada browser buka `http://localhost:8080/geoserver/web/`

Selanjutnya di dalam folder tex terdapat file pdf mengenai cara menampilkan peta berformat shapefile pada web.

### Tampilan Hasil
![hasil](https://github.com/aimanyongki/webgis/blob/master/hasil.png?raw=true)
