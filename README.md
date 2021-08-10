# Web Service Project

Projek Web Service dengan menggunakan framework **django**

Untuk menjalankan server secara lokal dapat menggunakan langkah berikut
1. `cd <File location>`
2. `python manage.py makemigrations`
3. `python manage.py migrate`
4. `python manage.py runserver`

## Document Conversion
***
Mengkonversi file dengan format **.docx**, **.dox** menjadi format **pdf**. 

### Modul yang dibutuhkan
Metode konversi file menggunakan library [win32com](https://pypi.org/project/pywin32)
untuk melakukan instalasi dapat menggunakan command
> pip install pywin32

*Library ini perlu dijalankan pada os Windows*

### Features
Fitur-fitur yang dapat digunakan antara lain:
1. Mengkonversi beberapa file `.docx` sekaligus
2. Hasil konversi pdf berupa text dan gambar
3. Layout halaman, format teks, tabel dan kolom hasil konversi sesuai dengan dokumen

### Letak Penyimpanan Hasil Konversi
Pada scripts python **PDFConverter.py** di line 19 : 
`directory = "../ConvertDoctoPdf/media"`

### How To Use
Simulasi konversi dokumen dapat menggunakan **postman** dengan api berikut:
* Asumsi menggunakan localhost:8000
1. Upload file
metode POST pada `http://127.0.0.1:8000/file/upload/`

kemudian memasukkan key-value pada form-data seperti berikut:

'file' : (File yang ingin dikonversi)

'remark' : (deskripsi file)

### Sample
Contoh hasil konversi dapat dilihat pada directory berikut:
`media/PDFS`
