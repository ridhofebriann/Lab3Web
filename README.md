# Lab3Web
# Praktikum 3: Membuat List, Tabel dan Form
### NAMA : M. Ridho Febrian
### NIM : 312410500
### KELAS : TI.24.A5

## 📍LANGKAH - LANGKAH PRAKTIKUM

### 1. MEMBUAT DOKUMEN HTML
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>HTML Lanjutan</title>
  </head>
  <body>
    <header>
      <h1>Membuat List</h1>
    </header>
</body
</head>
```

### 2. lab3_list.html Membuat List (Ordered, Unordered, Description)

**code ordered list**
```html
<section id="order-list">
      <h2>Ordered List</h2>
      <ol>
        <li>Pemrograman Web</li>
        <li>Sistem Informasi</li>
        <li>Basis Data 2</li>
      </ol>
    </section>
```

**code Unordered list**
```html
<section id="unorder-list">
      <h2>Unordered List</h2>
      <ul type="square">
        <li>Jaringan Komputer</li>
        <li>Struktur Data</li>
        <li>JavaScript</li>
      </ul>
    </section>
```

**code Description List**
```html
<section id="unorder-list">
      <h2>Description List</h2>
      <dl>
        <dt>Fakultas Teknik</dt>
        <dd>Teknik Informatika</dd>
        <dd>Teknik Informatika</dd>
        <dd>Teknik lingkungan</dd>
        <dt>Fakultas Ekonomi dan Bisnis</dt>
        <dd>Akuntansi</dd>
        <dd>manajemen</dd>
        <dd>bisnis Digital</dd>
      </dl>
    </section>
```

**Penjelasan:**

`<ol>` menghasilkan daftar bernomor; atribut type mengubah format (A, a, I, i).

`<ul>` adalah daftar tanpa urutan; atribut type="square" mengganti bullet.

`<dl>`, `<dt>`, `<dd>` untuk pasangan istilah dan deskripsinya (description list).

**TAMPILAN dan VSCODE**

<img src="tampilan dan vscode list.png" width="700">

### 3. lab3_tabel.html — Membuat Tabel dan Penggabungan Sel

Buat file baru dengan nama lab3_tabel.html seperti berikut.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>HTML Lanjutan</title>
  </head>
  <body>
    <header>
      <h1>Membuat Table</h1>
    </header>
  </body>
</html>
```

**code membuat tabel**
```html
<table border="1" cellpadding="4" cellspacing="0">
  <thead>
    <tr>
      <th>No.</th>
      <th>Fakultas</th>
      <th>Program Studi</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1.</td>
      <td>Teknik</td>
      <td>Teknik Informatika</td>
    </tr>
    <tr>
      <td>2.</td>
      <td>Teknik</td>
      <td>Teknik Industri</td>
    </tr>
    <tr>
      <td>3.</td>
      <td>Teknik</td>
      <td>Teknik Lingkungan</td>
    </tr>
  </tbody>
</table>
```

**TAMPILAN dan VSCODE**

<img src="tampilan dan vscode tabel.png" width="700">

**Penjelasan:**

`<table>`: wadah tabel. `border`, `cellpadding`, `cellspacing` membantu tampilan cepat (bisa diganti CSS).
  
`<thead>` berisi header kolom; `<tbody>` untuk baris data.

**code membuat tabel dan  Penggabungan Sel**
```html
<table border="1" cellpadding="10" cellspacing="0">
      <thead>
        <tr>
          <th>No.</th>
          <th>Fakultas</th>
          <th>Program Studi</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>1.</td>
          <td rowspan="3">Teknik</td>
          <td>Teknik Informatika</td>
        </tr>
        <tr>
          <td>2.</td>
          <td>Teknik Industri</td>
        </tr>
        <tr>
          <td>3.</td>
          <td>Teknik Lingkungan</td>
        </tr>
      </tbody>
    </table>
```

**Penjelasan:**

`<table>`: wadah tabel. `border`, `cellpadding`, `cellspacing` membantu tampilan cepat (bisa diganti CSS).
  
`<thead>` berisi header kolom; `<tbody>` untuk baris data.

`rowspan="3"` menggabungkan satu sel secara vertikal ke 3 baris. `colspan` untuk horizontal.

**TAMPILAN dan VSCODE**

<img src="tabel dan penggabungan sel.png" width="700">

### 4. lab3_form.html — Membuat From

Buat file baru dengan nama lab3_form.html seperti berikut.
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>HTML Lanjutan</title>
  </head>
  <body>
    <header>
      <h1>Membuat Form</h1>
    </header>
  </body>
</html>
```

**code membuat Form**
```html
<form action="proses.php" method="post">
  <fieldset>
    <legend>Data Pelanggan</legend>
    <p>
      <label for="nama">Nama</label>
      <input type="text" id="nama" name="nama" />
    </p>
    <p>
      <label for="alamat">Alamat</label>
      <textarea id="alamat" name="alamat" cols="20" rows="3"></textarea>
    </p>
    <p>
      <label>Jenis Kelamin</label>
      <input id="jk_l" type="radio" name="kelamin" value="L" /><label for="jk_l"
        >Laki-laki</label
      >
      <input id="jk_p" type="radio" name="kelamin" value="P" /><label for="jk_p"
        >Perempuan</label
      >
    </p>
    <p><input type="submit" value="Login" /></p>
  </fieldset>
</form>
```

**PENJELASAN**

| Bagian                    | Fungsi                                             |
| :------------------------ | :------------------------------------------------- |
| `<form>`                  | Pembungkus semua input yang akan dikirim ke server |
| `<fieldset>` & `<legend>` | Mengelompokkan form dengan judul                   |
| `<input type="text">`     | Kolom teks untuk nama                              |
| `<textarea>`              | Kotak teks besar untuk alamat                      |
| `<input type="radio">`    | Pilihan jenis kelamin (satu dari dua)              |
| `<input type="submit">`   | Tombol untuk mengirim data ke file `proses.php`    |


**selanjutnya menambahkan style css**
Agar tampilan form lebih menarik, bisa ditambahkan CSS seperti berikut.
```css
 <style>
      form p > label {
        display: inline-block;
        width: 100px;
      }
      form input[type="text"],
      form textarea {
        border: 1px solid #197a43;
      }
      form input[type="submit"] {
        border: 1px solid #197a43;
        background-color: #197a43;
        color: #ffffff;
        font-weight: bold;
        padding: 5px 15px;
      }
    </style>
```

**TAMPILAN dan VSCODE**

<img src="tampilan dan vscode from.png" width="700">

**Pertanyaan dan Tugas**

1. Buatlah form yang menampilkan dropdown menu dan listbox dengan multiple selection.

**Jawaban**

**berikut codenya**
```html
<p>
          <label for="negara">Negara</label>
          <select id="negara" name="negara">
            <option value="indonesia">Indonesia</option>
            <option value="malaysia">Malaysia</option>
            <option value="singapore">Singapore</option>
            <option value="thailand">Thailand</option>
          </select>
        </p>
        <p>
          <label for="hobi">Hobi</label>
          <select id="hobi" name="hobi[]" multiple size="4">
            <option value="memasak">Memasak</option>
            <option value="membaca">Membaca</option>
            <option value="olahraga">Olahraga</option>
            <option value="musik">Musik</option>
            <option value="traveling">Traveling</option>
          </select>
        </p>
        <p><input type="submit" value="Login" /></p>
      </fieldset>
```

**PENJELASAN**

| Elemen                  | Fungsi                                          |
| :---------------------- | :---------------------------------------------- |
| `<select>`              | Membuat menu pilihan (dropdown atau listbox)    |
| `multiple`              | Mengizinkan pemilihan lebih dari satu opsi      |
| `size`                  | Mengatur tinggi listbox (berapa baris terlihat) |
| `name="hobi[]"`         | Menandakan nilai akan dikirim sebagai array     |
| `<option>`              | Menentukan pilihan yang tersedia                |
| `<input type="submit">` | Tombol untuk mengirim data ke server            |

**DIGABUNG**
```HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>HTML Lanjutan</title>
    <style>
      form p > label {
        display: inline-block;
        width: 100px;
      }
      form input[type="text"],
      form textarea {
        border: 1px solid #197a43;
      }
      form input[type="submit"] {
        border: 1px solid #197a43;
        background-color: #197a43;
        color: #ffffff;
        font-weight: bold;
        padding: 5px 15px;
      }
    </style>
  </head>
  <body>
    <header>
      <h1>Membuat Form</h1>
    </header>
    <form action="proses.php" method="post">
      <fieldset>
        <legend>Data Pelanggan</legend>
        <p>
          <label for="nama">Nama</label>
          <input type="text" id="nama" name="nama" />
        </p>
        <p>
          <label for="alamat">Alamat</label>
          <textarea id="alamat" name="alamat" cols="20" rows="3"></textarea>
        </p>
        <p>
          <label>Jenis Kelamin</label>
          <input id="jk_l" type="radio" name="kelamin" value="L" /><label
            for="jk_l"
            >Laki-laki</label
          >
          <input id="jk_p" type="radio" name="kelamin" value="P" /><label
            for="jk_p"
            >Perempuan</label
          >
        </p>
        <p>
          <label for="negara">Negara</label>
          <select id="negara" name="negara">
            <option value="indonesia">Indonesia</option>
            <option value="malaysia">Malaysia</option>
            <option value="singapore">Singapore</option>
            <option value="thailand">Thailand</option>
          </select>
        </p>
        <p>
          <label for="hobi">Hobi</label>
          <select id="hobi" name="hobi[]" multiple size="4">
            <option value="memasak">Memasak</option>
            <option value="membaca">Membaca</option>
            <option value="olahraga">Olahraga</option>
            <option value="musik">Musik</option>
            <option value="traveling">Traveling</option>
          </select>
        </p>
        <p><input type="submit" value="Login" /></p>
      </fieldset>
    </form>
  </body>
</html>
```

**TAMPILAN dan VSCODE**

<img src="dropdown menu dan listbox dengan multiple selection..png" width="700">




















