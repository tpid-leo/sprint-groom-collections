# Create UI Doctor Detail Patient Log

## 1. Overview
Menampilkan seluruh daftar pasien dengan doctor terkait.
## 2. Requirement Visual
* Patient Log
![image-patient-log](../assets/patient-log.png)
## 3. Logic UI / UX
* **Loading State:** Muncul *skeleton loader* pada tabel saat *fetching* data.
* **Empty State:** Tampilkan ilustrasi "Data Kosong" jika array kembalian API kosong.
* **Error Handling:** Tampilkan *toast alert* warna merah jika API mengembalikan status 400/500.
## 4. API Needs
* `API Get List Doctor Patient Log` - Mengambil list data pasien