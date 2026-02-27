# Detail Update Doctor Request
## Overview
Menampilkan data request update yang digunakan untuk membuat data doctor baru. Ada 2 sisi yaitu sebagai 'Maker' dan 'Approval'. Use Approval dapat melakukan update aproval request yang akan di edit.
## Requirement Visual
- **Tampilan User Maker Request Update Detail Info**

	![](../assets/update-request-doctor-info.png)

-  **Tampilan User Maker Request Update Detail Professioal & Exp**

	![](../assets/update-request-prof-doctor.png)
- **Tampilan User Maker Request Update Weekly Schedule**

	![](../assets/update-request-weekly-doctor.png)
- **Tampilan User Maker Request Update Special Schedule**
	 
	![](../assets/update-request-special-doctor.png)
	
 - **Tampilan User Maker Request Update Time Off**
	 
	![](../assets/update-request-off-doctor.png)

- **Tampilan User Approve Approval Update Detail Info**

	![](../assets/update-approval-info-doctor.png)

- **Tampilan User Approve Approval Update Detail Professioal & Exp**
	
	![](../assets/update-approval-prof-doctor.png)

- **Tampilan User Approve Approval Update Weekly Schedule**
  
  ![](../assets/update-approval-weekly-doctor.png)
  
- **Tampilan User Approve Approval Update reject Weekly Schedule**

	![](../assets/update-approval-reject-weekly.png)

-  **Tampilan User Approve Approval Update Special Schedule**

	![](../assets/update-approval-special-doctor.png)

- **Tampilan User Approve Approval Update Time Off**

	![](../assets/update-approval-off-doctor.png)

- **Tampilan User Approval Modal Confirmation**  
  
	![](../assets/update-approval-confirmation.png)
- **Tampilan User Approval Reject Modal Confirmation**
  
    ![](../assets/empty-modal-reject-state.png)
	![](../assets/filled-state-modal-confirm.png)
	
- **Tampilan User Approval Reject Modal Confirmation**
## Logic and UI/UX
- **Loading:** Saat load halaman maka berikan loader spinner.
- **Maker** Tampilan request didapat dari role pada user yang sedang login(jwt, session).
- **Approval:** Tampilan request didapat dari role pada user yang sedang login(jwt, session), memiliki action button dan backgorund form yang berbeda.
-  **Button Approve:** Saat klik button tersebut maka akan muncul modal sesuai dengan tampilan approve confirmation yang berisi data apa saja yang akan terupdate, setelah success maka akan kembali ke list awal.
- **Button Reject:** Saat klik button tersebut maka akan muncul modal sesuai dengan tampilan reject confirmation., , setelah success maka akan kembali ke list awal
- **Table:** Jika ada perbedaan 

## API Needs
- ### `API Get Detail Update Doctor Request`
  	**Method:** `GET`  
	**Endpoint:** `{base-url}/api/v1/cms/doctors/requested-update/:requestUUID`

### Header

| Key | Type | Rule |
| :--- | :--- | :--- |
| `Authorization` | `string` | • Mandatory |



- ### `API Approval Update Doctor Request`
	- **Method : POST**
	- **Endpoint : {base-url}/api/v1/cms/doctors/requested-update/:requestUUID/approval**
	- **Request :**
	    - Type : Request Body

| Key | Type | Rule |
| :--- | :--- | :--- |
| `action` | `string` | • Mandatory<br>• Value only: `APPROVE` dan `REJECT` |
| `reason` | `string` | • Optional<br>• Required If `action` = `REJECT` |
| `reason_description` | `string` | • Optional<br>• Required If `reason` != `null` |
| `action_by_uuid` | `string` | • Mandatory<br>• Valid uuid format |
| `action_by_name` | `string` | • Mandatory<br>• Valid uuid format |
- **200 (Success)**

```json
{
  "api_id": "API_CALL_......",
  "status": "SUCCESS",
  "message": "Success approval data",
  "data": null,
  "meta": null
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
