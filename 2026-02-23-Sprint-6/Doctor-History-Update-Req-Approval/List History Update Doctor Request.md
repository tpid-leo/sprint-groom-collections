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
	- **Endpoint : {base-url}/api/v1/cms/doctors/requested-update/history**
	- **Header :**
   ### Header
	| Key | Type | Rule |
	| :--- | :--- | :--- |
	| `Authorization` | `string` | • Mandatory |
	
	### Request Parameter
	
	| Key | Type | Rule |
	| :--- | :--- | :--- |
	| `page` | `int` | • Optional<br>• Default: 1 |
	| `limit` | `int` | • Optional<br>• Default: 10 |
	| `search` | `string` | • Optional<br>• Search by doctor_name |
