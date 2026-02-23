# [Nama Fitur / Judul Task]

---

## 1. Overview
[Tulis ringkasan singkat, tujuan fitur, atau referensi tiket Jira/Trello di sini]

---

## 2. Requirement Visual
### 2.1 [Nama Tampilan Utama - misal: Halaman List Patient]
![Tampilan Halaman](media-template/overall-view.png)
* **Komponen A:** [Penjelasan komponen]
* **Modal / Pop-up:** [Penjelasan behavior modal jika ada]

### 2.2 [Nama Tampilan Kedua - misal: Modal Create]
![Tampilan Modal](link-gambar-di-sini.png)
* **Dropdown Dokter:** [Penjelasan komponen]

---

## 3. Form Validation
### 3.1 [Nama Form - misal: Form Create Doctor]

<table width="100%">
  <thead>
    <tr>
      <th align="left" width="25%">Label</th>
      <th align="left" width="30%">Example Data</th>
      <th align="left" width="45%">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>Nama Lengkap</code></td>
      <td>dr. Budi Santoso</td>
      <td>Wajib diisi, maksimal 50 karakter</td>
    </tr>
    <tr>
      <td><code>Email</code></td>
      <td>budi@rs.com</td>
      <td>Format email valid, wajib diisi</td>
    </tr>
    <tr>
      <td><code>Spesialis</code></td>
      <td>Poli Gigi</td>
      <td>Dropdown list, pilih salah satu</td>
    </tr>
  </tbody>
</table>

**Note:** Pastikan *button submit* dalam keadaan *disabled* jika form mandatory belum terisi semua.

---

## 4. Logic UI / UX
### 4.1 [Judul Logic - misal: State Management & Feedback]
* **Loading State:** Muncul *skeleton loader* pada tabel saat *fetching* data.
* **Empty State:** Tampilkan ilustrasi "Data Kosong" jika array kembalian API kosong.
* **Error Handling:** Tampilkan *toast alert* warna merah jika API mengembalikan status 400/500.

---

## 5. API Needs
* `GET /api/v1/doctor/patient-log` - Mengambil list data pasien.
* `POST /api/v1/doctor/request` - Submit data form pembuatan dokter baru.