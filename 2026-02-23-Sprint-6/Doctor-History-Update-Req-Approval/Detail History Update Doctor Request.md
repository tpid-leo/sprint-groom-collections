# Detail History Update Doctor Request
## 1. Overview
Menampilkan data request update history untuk mengecek data apa saja yang di update. Ada 2 sisi yaitu sebagai 'Maker' dan 'Approval'. 
## 2. Requirement Visual

- **Tampilan Update History Accepted**

	![](../assets/update-history-accepted.png)

-  **Tampilan Update History Rejected**

	![](../assets/update-history-rejected.png)
## 3. Logic UI / UX
- **Loading:** Saat melakukan load halaman maka berikan loader spinner.
- **Maker/Approval:** menampilkan halaman yang sama.
- Jika tidak ada perubahan di antara data_before dan data_after table tidak ada perlu ditampilkan datnya cukup => Unchanged.

## 4. API Needs
- `API Get Detail History Update Doctor Request`
	- **Endpoint : {base-url}/api/v1/cms/customers/requested-update/:requestUUID**
	- **Header :**
	 
	### Header
	
	| Key | Type | Rule |
	| :--- | :--- | :--- |
	| `Authorization` | `string` | • Mandatory |

- **200 (Success)**

```json
{
    "api_id": "API_CALL_...",
    "status": "SUCCESS",
    "message": "Success get data",
    "data": {
	    "request_information": {
				  "name": "Lisa",
				  "legacy_no_customer": "NTSH-00123",
				  "status": "REQUESTED",
				  "requested_by_name": "Irfan",
				  "requested_at": "2025-11-10T23:59:59Z",
			},
			"detail_data": [
					"data_before": {
							"name": "Sukonto",
							"phone_code": "+62",
							"phone_number": "8223613561",
							"email": "sukonto@gmail.com",
							"identity_number": "1654361231",
							"gender": "MALE",
							"birth_date": "2025-11-10T23:59:59Z",
							"country_name": "Indonesia",
							"province_name": "DIY",
							"city_name": "Jogja",
							"district_name": "Jogja",
							"subdistrict_name": "Pakualaman",
							"address": "Jl. Bausasran",
					},
					"data_after": {
							"name": "Sukanti",
							"phone_code": "+62",
							"phone_number": "8223613561",
							"email": "sukanti@gmail.com",
							"identity_number": "1654361231",
							"gender": "FEMALE",
							"birth_date": "2025-11-10T23:59:59Z",
							"country_name": "Indonesia",
							"province_name": "DIY",
							"city_name": "Jogja",
							"district_name": "Jogja",
							"subdistrict_name": "Suryatmajan",
							"address": "Jl. Malioboro",
					}
					
			],
		},
    "meta": null
}
```

- **400 (Bad request)**

```json
{
    "api_id": "API_CALL_1770622356143236_5900547",
    "status": "BAD_REQUEST",
    "message": "Invalid request uuid",
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
