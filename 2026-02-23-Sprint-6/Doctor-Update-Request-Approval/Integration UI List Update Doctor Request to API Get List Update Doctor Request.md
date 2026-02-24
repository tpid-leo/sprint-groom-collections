# Integration UI List Update Doctor Request to API Get List Update Doctor Request
## 1. Overview
UI ini menampilkan list request yang dilakukan oleh doctor ketikan baru akan membuat/create data yang baru.
## 2. Requirement Visual
- **Approval Request**

	![](../assets/list-update-request.png)
## 3. Logic UI / UX
- **Loading:** menampilkan spinner pada pada data table setiap memuat data baru.
- **Error:** menampilkan toast error/not found page
- **Empty State**: menampilkan data kosong pada data table.
- **Filled State:** menampilkan data list dengan state Tab button, request adalah aktif.
- **Search:** menampilkan data list sesuai dengan inputan search.
## 4. API Needs
- `API Get List Update Doctor Request`