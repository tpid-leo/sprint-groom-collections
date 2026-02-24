# List History Update Doctor Request
## Overview
UI ini menampilkan list request update history yang dilakukan oleh doctor dan untuk mengecek riwayat status data yang di update.
## Requirement Visual
- **Approval Request**

	![](../assets/list-update-req-history.png)
## Logic and UX
- **Tab Header:** Tab yang active adalah "Update"
- **Tab Header Table:** Tab yang active adalah "History"
- **Loading:** menampilkan spinner pada pada data table setiap memuat data baru.
- **Error:** menampilkan toast error/not found page
- **Empty State**: menampilkan data kosong pada data table.
- **Filled State:** menampilkan data list dengan state Tab button, request adalah aktif.
- **Search:** menampilkan data list sesuai dengan inputan search.
## API Needs
- `API Get List History Update Doctor Request`