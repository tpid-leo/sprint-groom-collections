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
	- **Endpoint : (GET) {base-url}/api/v1/cms/doctors/requested-update/history**
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

## Response

- **200 (Success)**

```json
{
    "api_id": "API_CALL_172965703441714_2379313",
    "status": "SUCCESS",
    "message": "Success get data",
    "data": [
        {
            "requested_by": "Lisa",
            "requested_at": "2025-12-18 02:09:42.110 +0000",
            "status": "REJECTED",
            "entity": "INFO",
            "doctor": {
	            "uuid": "a7263fg1-542f-4145-a588-9e2b87987977c",
	            "name": "Rina setiawati",
            }

        },
        {
            "requested_by": "Mariana",
            "requested_at": "2025-12-18 02:09:42.110 +0000",
            "status": "APPROVED",
            "entity": "PROFESSIONAL"
            "doctor": {
	            "uuid": "a7287881-542f-4145-a588-9e2b87987977c",
	            "name": "Setiawati",
            }

        }
    ],
    "meta": {
        "page": 1,
        "limit": 10,
        "total": 2
    }
}
```

- **400 (Bad request)**

```json
{
    "api_id": "API_CALL_1770622356143236_5900547",
    "status": "BAD_REQUEST",
    "message": "Invalid payload data",
    "data": null,
    "meta": null
}
```

- **401 (Unauthorized)**

```json
{
    "api_id": "API_CALL_1770728356143236_5900547",
    "status": "UNAUTHORIZED",
    "message": "Authentication Failed",
    "data": null,
    "meta": null
}
```

- **422 (Something went wrong)**

```json
{
    "api_id": "API_CALL_1770623899145819_6412567",
    "status": "FAILED",
    "message": "Something Went Wrong",
    "data": null,
    "meta": null
}
```
