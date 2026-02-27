# Detail Create Doctor Request
## Overview
Menampilkan data request create yang digunakan untuk membuat data doctor baru. Ada 2 sisi yaitu sebagai 'Maker' dan 'Approval'. User aprroval dapat melakuakn action 'Approve' dan 'Reject'
## Requirement Visual
- **Tampilan User Maker**

	![](../assets/use-maker.png)
- **Tampilan User Approval**

	![](../assets/user-approve.png)

	
- **Tampilan Approve Confirmation*
  
  ![](../assets/approve-confirmation.png)
  
- **Tampilan Reject Confirmation** 

	![](../assets/reject-empty-state.png)

- **Tampilan Reject Consirmation(Terisi)** 

	![](../assets/reject-filled-state.png)
## Logic UI / UX
- **Loading:** Saat melakukan load halaman maka berikan loader spinner.
- **Maker/Approval:** Tampilan UI request didapat dari key role pada user yang sedang login( melalui jwt, session).
- **Button Approve:** Saat klik button tersebut maka akan muncul modal sesuai dengan tampilan approve confirmation yang berisi data apa saja yang akan terupdate, setelah success maka akan kembali ke list awal.
- **Button Reject:** Saat klik button tersebut maka akan muncul modal sesuai dengan tampilan reject confirmation., , setelah success maka akan kembali ke list awal
## API Needs
- `API Get Detail Schedule Create Doctor Request`(https://tpid.atlassian.net/wiki/spaces/FR/pages/818020403/API+Get+List+Weekly+Doctor+Schedule)

  	**Endpoint:** (GET) `{base_url}/api/v1/cms/doctors/:doctorUUID/weekly-schedules`
	### Header
	
	| Key | Type | Rule |
	| :--- | :--- | :--- |
	| `Authorization` | `string bearer` | Mandatory. Check on middleware |
	
	### Request Parameter
	
	| Key | Type | Rule |
	| :--- | :--- | :--- |
	| `doctorUUID` | `string` | Mandatory. Format: UUID |


-  `API Approval Create Doctor Request`(https://tpid.atlassian.net/wiki/spaces/FR/pages/775749635/API+Approval+Request+Doctor)
	**Endpoint:** `{base-url}/v1/cms/doctors/requested/:doctorUUID/approval`  
	**Method:** `POST`  
	**Content-Type:** `application/json`

	### 2.1. URL Parameter

	| Key | Tipe Data | Aturan Validasi | Keterangan |
	| :--- | :--- | :--- | :--- |
	| `:doctorUUID` | `string` | • Mandatory<br>• Harus format UUID | UUID unik dari dokter yang akan diproses. |
	
	### 2.2. Request Body
	
	| Key | Tipe Data | Aturan Validasi | Keterangan |
	| :--- | :--- | :--- | :--- |
	| `action` | `string` | • Mandatory<br>• Nilai harus: APPROVE or REJECT | Tindakan yang akan diambil. |
	| `accepted_by_uuid` | `uuid` | Mandatory | UUID dari pengguna (admin) yang melakukan approval/rejection. |
	| `accepted_by_name` | `string` | Mandatory | Nama dari pengguna (admin) yang melakukan approval/rejection. |
