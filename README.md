## Modul base64 di Python

Modul base64 memiliki fungsi yang membantu menyandikan teks atau data biner ke dalam format base64 dan mendekodekan data base64 ke dalam teks atau data biner. Modul base64 digunakan untuk menyandikan dan mendekodekan data dengan cara berikut:

## Pengkodean Base64

Modul base64 menyediakan fungsi b64encode(). Fungsi ini mengkodekan sebuah objek berbentuk byte menggunakan Base64 dan mengembalikan byte yang telah dikodekan. Mari kita lihat bagaimana cara menggunakan fungsi ini.

```py
import base64

data = "Python adalah bahasa pemrograman"
data_bytes = data.encode('ascii')

base64_bytes = base64.b64encode(data_bytes)
base64_string = base64_bytes.decode('ascii')

print("Data yang disandikan: ", base64_string)

# Keluaran:
Data yang disandikan:  UHl0aG9uIGlzIGEgcHJvZ3JhbW1pbmcgbGFuZ3VhZ2U=
```

Pada contoh di atas, pertama-tama kita mengonversi string input menjadi objek seperti byte dan kemudian mengkodekan objek seperti byte tersebut ke format base64.

## Penguraian kode Base64

Penguraian string base64 berlawanan dengan pengodean. Modul base64 menyediakan fungsi b64decode() yang memecahkan kode byte yang dikodekan Base64 seperti objek atau string ASCII dan mengembalikan byte yang telah diterjemahkan. Mari kita lihat bagaimana cara menggunakan fungsi ini.

```py
import base64

base64_string = "UHl0aG9uIGlzIGEgcHJvZ3JhbW1pbmcgbGFuZ3VhZ2U="
base64_bytes = base64_string.encode('ascii')

data_bytes = base64.b64decode(base64_bytes)
data = data_bytes.decode('ascii')

print("Data yang diuraikan:", data)

# Keluaran:
Data yang diuraikan: Python adalah sebuah bahasa pemrograman
```

Pada contoh di atas, pertama-tama kita mengonversi string base64 menjadi byte data yang tidak disandikan, lalu memecahkan kode byte tersebut untuk mendapatkan string asli.

Catatan: Untuk mencegah kerusakan data, pastikan untuk menggunakan format penyandian yang sama ketika mengonversi dari string ke byte, dan dari byte ke string.
