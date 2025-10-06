# Praktikum Membuat form yang menampilkan dropdown menu dan listbox dengan menggunakan multiple selection

  
# List
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Lanjutan - Dropdown menu dan listbox</title>
</head>
<body>
    <header>
        <h1>Membuat List</h1>
    </header>

    <section id="order-list">
        <h2>Ordered List</h2>
        <ol>
            <li>Pemrograman Web</li>
            <li>Sistem Informasi</li>
            <li>Basis Data 2</li>
        </ol>
    </section>

    <section id="unorder-list">
        <h2>Unordered List</h2>
        <ul type="square">
            <li>Jaringan Komputer</li>
            <li>Struktur Data</li>
            <li>Algoritma &amp; Pemrograman</li>
        </ul>
    </section>

    <section id="unorder-list">
        <h2>Description List</h2>
        <dl>
            <dt>Fakultas Teknik</dt>
            <dd>Teknik Industri</dd>
            <dd>Teknik Informatika</dd>
            <dd>Teknik Lingkungan</dd>
            <dt>Fakultas Ekonomi dan Bisnis</dt>
            <dd>Akuntansi</dd>
            <dd>Manajemen</dd>
            <dd>Bisnis Digital</dd>
        </dl>
    </section>
</body>
</html>
```
<h4>Output nya yaitu:</h4>
<img width="305" height="620" alt="image" src="https://github.com/user-attachments/assets/ece6b858-004a-43cb-8955-e5f42e3a1f95" />

# Form
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Lanjutan - Form</title>
    <style>
        form p > label {
            display: inline-block;
            width: 100px;
        }
        form input[type="text"], form textarea {
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
                <input type="text" id="nama" name="nama">
            </p>
            <p>
                <label for="alamat">Alamat</label>
                <textarea id="alamat" name="alamat" cols="20" rows="3"></textarea>
            </p>
            <p>
                <label>Jenis Kelamin</label>
                <input id="jk_l" type="radio" name="kelamin" value="L" /> <label for="jk_l">Laki-laki</label>
        <input id="jk_p" type="radio" name="kelamin" value="P" /><label for="jk_p">Perempuan</label>
            </p>
            <p><input type="submit" value="Login"></p>
        </fieldset>
    </form>
</body>
</html>
```
<h4>Output nya yaitu:</h4>
<img width="759" height="382" alt="image" src="https://github.com/user-attachments/assets/3bdb06cd-ad28-4244-b8b9-040f01f5c034" />

# Tabel
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Lanjutan - Tabel</title>
</head>
<body>
    <header>
        <h1>Membuat Table</h1>
    </header>

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

<table border="1" cellpadding="6" cellspacing="0">
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
</body>
</html>
```
<h4>Output nya yaitu:</h4>
<img width="350" height="383" alt="image" src="https://github.com/user-attachments/assets/1c5a0619-eaaa-43d6-9e77-2f9bfa369528" />

# Pertanyaan dan Tugas
1. Buatlah form yang menampilkan dropdown menu dan listbox dengan multiple selection

# Jawaban
***Code***
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Latihan - Dropdown & Listbox</title>
    <style>
        body {
            font-family: "Poppins", sans-serif;
            background: linear-gradient(135deg, #053a96);
            color: #333;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding-top: 40px;
        }
        h2 {
            color: white;
            text-align: center;
            margin-bottom: 10px;
        }
        .info {
            background: white;
            padding: 15px 25px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
            margin-bottom: 20px;
            line-height: 1.5;
        }
        fieldset {
            width: 350px;
            padding: 20px;
            border: 2px solid white;
            border-radius: 15px;
            background: white;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        header {
            font-weight: bold;
            font-size: 18px;
            color: #065f46;
        }
        label {
            display: block;
            margin-top: 10px;
            margin-bottom: 5px;
            font-weight: bold;
            color: #065f46;
        }
        input[type="text"], textarea, select {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 7px;
            transition: 0.3s;
            font-family: inherit;
        }
        input[type="text"]:focus, textarea:focus, select:focus {
            border-color: #053a96;
            box-shadow: 0 0 5px #053a96;
            outline: none;
        }
        select[multiple] {
            background: linear-gradient(145deg, #f0fdfa, #ecfdf5);
            height: 100px;
        }
        input[type="submit"] {
            margin-top: 15px;
            background-color: #053a96;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 7px;
            cursor: pointer;
            transition: 0.3s;
            width: 100%;
        }
        input[type="submit"]:hover {
            background-color: #07cae8;
            transform: scale(1.03);
        }
    </style>
</head>

<body>
    <div class="info">
        <b>Nama:</b> Ari Cakra Kurniawan <br>
        <b>NIM:</b> 312410248 <br>
        <b>Kelas:</b> TI.24.A2 <br>
        <b>Mata Kuliah:</b> Pemrograman Web 1
    </div>

    <h2>Membuat Form</h2>
    <form action="frm.php" method="post" onsubmit="kirimData(event)">
        <fieldset>
            <header>Data Pelanggan</header>
            
            <label for="nama">Nama:</label>
            <input type="text" id="nama" name="nama" required>

            <label for="alamat">Alamat:</label>
            <textarea id="alamat" name="alamat" rows="3" required></textarea>

            <label>Jenis Kelamin:</label>
            <label><input type="radio" name="gender" value="Laki-laki" required> Laki-laki</label>
            <label><input type="radio" name="gender" value="Perempuan" required> Perempuan</label>

            <label for="kota">Jurusan :</label>
            <select id="kota" name="kota" required>
                <option value="">-- Pilih Jurusan --</option>
                <option value="Bekasi">Teknik Informatika</option>
                <option value="Jakarta">Teknik Industri</option>
                <option value="Bandung">Teknik Arsitektur</option>
                <option value="Surabaya">Teknik Sipil</option>
            </select>

            <label for="hobi">Hobi:</label>
            <select id="hobi" name="hobi[]" multiple size="4" required>
                <option value="Membaca">Membaca</option>
                <option value="Olahraga">Olahraga</option>
                <option value="Gaming">Gaming</option>
                <option value="Musik">Musik</option>
                <option value="Travelling">Travelling</option>
            </select>

            <input type="submit" value="Kirim Data">
        </fieldset>
    </form>
</body>
</html>
```

***Outputnya akan menghasilkan:***

<img width="518" height="839" alt="image" src="https://github.com/user-attachments/assets/b87d7540-e492-4e78-b685-59b18ef49f35" />

Sekian dan Terimakasih
