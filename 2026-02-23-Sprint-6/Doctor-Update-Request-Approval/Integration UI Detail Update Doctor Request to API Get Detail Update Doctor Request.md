# Integration UI Detail Update Doctor Request to API Get Detail Update Doctor Request
## 1. Overview
Menampilkan data request yang digunakan untuk membuat data doctor baru. Ada 2 sisi yaitu sebagai 'Maker' dan 'Approval'
### 2. Requirement Visual
#### 2.1. User Maker
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

- **Tampilan User Maker Request Update Time Off**
#### 2.1. User Aprroval
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
## 3. Logic UI / UX
- **Loading:** Saat melakukan load halaman maka berikan loader spinner.
- **Maker/Approval:** Tampilan UI request didapat dari key role pada user yang sedang login( melalui jwt, session).
- **Maker** Tampilan request didapat dari role pada user yang sedang login(jwt, session).
- **Approval:** Tampilan request didapat dari role pada user yang sedang login(jwt, session), memiliki action button dan backgorund form yang berbeda.
## 4. API Needs
- `API Get Detail Update Doctor Request`