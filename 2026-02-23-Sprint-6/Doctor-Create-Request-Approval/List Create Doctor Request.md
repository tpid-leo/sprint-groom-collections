# List Create Doctor Request
## Overview
UI ini menampilkan list request create yang dilakukan oleh doctor untuk membuat/create data yang baru.
## Requirement Visual
- **List Approval Update**
  ![](../assets/approval-request.png)
## Logic UI / UX
- **Tab Header:** Tab active adalah "Update"
- **Tab Header Table:** Tab active adalah "Request"
- **Loading:** menampilkan spinner pada pada data table setiap memuat data baru.
- **Error:** menampilkan toast error/not found page
- **Empty State**: menampilkan data kosong pada data table.
- **Filled State:** menampilkan data list dengan state button create aktif.
- **Search:** menampilkan data list sesuai dengan inputan search.
## API Needs
- `API Get List Create Doctor Request`