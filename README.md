<div id="top"></div>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- ABOUT THE PROJECT -->
## Dashboard Demam Berdarah Dengue (DBD) Provinsi Jawa Barat Tahun 2014-2020

Data yang digunakan adalah data dari website opendata.jabarprov.go.id dengan studi kasus DBD berdasarkan kabupaten/kota dan jenis kelamin di Jawa Barat pada tahun 2014-2020. Data ini memiliki 13 variabel yang dapat dilihat pada gambar Dataset. Adapun penjelasan variabel-variabel tersebut diantaranya sebagai berikut: 
1.	Id berisi nomor urut data.
2.	Kode_provinsi berisi kode dari provinsi yang dijadikan studi kasus, dalam hal ini Provinsi Jawa Barat berkode 32.
3.	Nama_provinsi berisi nama dari provinsi yang dijadikan studi kasus, dalam hal ini Provinsi Jawa Barat.
4.	Kode_kabupaten_kota berisi kode kabupaten/kota setiap data.
5.	Latitude berisi letak latitude kabupaten/kota setiap data.
6.	Longitude berisi letak longitude kabupaten/kota setiap data.
7.	Kode_pos berisi kode pos kabupaten/kota setiap data.
8.	Jenis_kelamin berisi jenis kelamin dari setiap data.
9.	Jumlah_kasus berisi jumlah kasus terdampak dari setiap data.
10.	Jumlah_kasus_meninggal berisi jumlah kasus meninggal dari setiap data
11.	Total_kasus berisi jumlah kasus terdampak dan meninggal dari setiap data.
12.	Satuan berisi satuan dari variabel jumlah_kasus, jumlah_kasus_meninggal, dan total_kasus yaitu jiwa.
13.	Tahun berisi tahun yang terjadi dari setiap data. 


<p align="right">(<a href="#top">back to top</a>)</p>



## Pembuatan Visualisasi jumlah Kasus DBD Berdasarkan Jenis Kasus dan Kabupaten/Kota 

1. Memasukkan variabel longitude ke dalam columns
2. Memasukkan variabel latitude ke dalam rows. 
3. Membuat parameter dengan nama jenis kasus yang diawali dengan mengklik tanda segitiga kebalik dan pilih create parameter seperti pada gambar create parameter.
4. Kemudian mengubah format data type, allowable values, dan memasukkan parameternya dengan terdampak dan meninggal seperti pada gambar membuat parameter.
5. Membuat fungsi calculatednya dengan nama JenisKasusCalc yang diawali dengan mengklik tanda segitiga kebalik dan pilih create calculated field seperti pada gambar create calculated field.
6. Kemudian masukkan code berikut ini.
    ```sh
    CASE [Jenis Kasus]
    WHEN "Terdampak" THEN [Jumlah Kasus]
    WHEN "Meninggal" THEN [Jumlah Kasus Meninggal]
    END
    ```
7. Mengubah tampilan maps menjadi streets seperti pada gambar mengubah tampilan peta.
8. Masukkan variabel nama kabupaten/kota, variabel kode kabupaten kota, dan kode pos ke dalam detail, serta fungsi JenisKasusCalc ke dalam size seperti pada gambar marks.
9. Mengedit measure kode kabupaten kota dan kode pos menjadi min seperti pada gambar edit measure.
10. Mengedit format tulisan kode kabupaten kota dan kode pos dengan mengklik format pada gambar di atas, kemudian edit format menjadi seperti gambar edit format kode.
11. Mengganti warna sesuai yang diinginkan seperti pada gambar ganti warna.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Pembuatan Visualisasi Jumlah Kasus DBD Berdasarkan Jenis Kasus dan Jenis Kelamin per Tahun

1. Memasukkan variabel tahun ke dalam columns.
2. Memasukkan JenisKasusCalc ke dalam rows. 
3. Memasukkan variabel jenis kelamin ke dalam color di marks.
4. Mengedit axis dengan mengklik kanan lalu pilih format seperti pada gambar edit axis line chart.
5. Menampilkan parameter dengan mengklik kanan parameter jenis kasus dan klik show parameter seperti pada gambar show parameter line chart. 

<p align="right">(<a href="#top">back to top</a>)</p>



## Pembuatan Visualisasi Jumlah Kasus DBD per Tahun

1. Memasukkan variabel tahun ke dalam columns.
2. Memasukkan variabel total kasus ke dalam rows. 
3. Memasukkan variabel total kasus ke dalam color dan label di marks.
4. Mengedit axis dengan mengklik kanan lalu pilih format seperti pada tahap 4 pembuatan visualisasi sebelumnya.
5. Mengedit warna bar chart dengan mengklik tanda segitiga kebalik pada legenda visualisasi dan pilih edit colors seperti pada gambar edit warna bar chart.
6. Mengedit judul legenda dengan langkah yang sama sebelumnya, namun pilih edit title.

<p align="right">(<a href="#top">back to top</a>)</p>



## Pembuatan Visualisasi Peringkat Kasus DBD Berdasarkan Kabuoaten/Kota

1. Memasukkan variabel total kasus ke dalam columns.
2. Memasukkan variabel nama kabupaten ke dalam rows. 
3. Memasukkan variabel kode kabupaten kota dan kode pos ke dalam detail di marks.
4. Mengganti measure dan format tulisan kode kabupaten kota dan kode pos seperti langkah 9 dan 10 pada Pembuatan Visualisasi jumlah Kasus DBD Berdasarkan Jenis Kasus dan Kabupaten/Kota.
5. Mengedit axis dengan mengklik kanan lalu pilih format seperti pada tahap 4 pembuatan visualisasi sebelumnya.
6. Mengganti warna sesuai yang diinginkan seperti langkah 11 pada Pembuatan Visualisasi jumlah Kasus DBD Berdasarkan Jenis Kasus dan Kabupaten/Kota.

<p align="right">(<a href="#top">back to top</a>)</p>



## Pembuatan Visualisasi Presentase Kasus DBD Berdasarkan Jenis Kelamin

1. Memasukkan variabel total kasus ke dalam columns.
2. Memasukkan variabel jenis kelamin ke dalam rows. 
3. Mengubah quick table calculation menjadi percent of total seperti pada gambar change percent.
4. Mengubah bentuk visualisasi menjadi pie chart seperti pada gambar ubah diagram.
5. Memasukkan variabel jenis kelamin ke dalam color dan label serta variabel total kasus ke dalam label di marks.

<p align="right">(<a href="#top">back to top</a>)</p>



## Pembuatan Dashboard DBD Provinsi Jawa Barat Tahun 2014-2020

1. Mengubah penganturan dashboard dari tiled menjadi floating dan mengklik show dashboard title seperti pada gambar pengaturan dashboard.
2. Menyusun semua visualisasi seperti pada gambar tampilan dashboard.

<p align="right">(<a href="#top">back to top</a>)</p>

Catatan: Semua gambar ada di folder images

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
