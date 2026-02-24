# Integration UI Detail Create Doctor Request to API Approval Create Doctor Request
## 1. Overview
Menampilkan modal yang beirisi ringkasan data request create yang akan di konfirmasi oleh user approval. User aprroval dapat melakuakn action 'Approve' dan 'Reject'.
## 2. Requirement Visual
- **Tampilan Approve Confirmation*
  
  ![](../assets/approve-confirmation.png)
  
- **Tampilan Reject Confirmation** 

	![](../assets/reject-empty-state.png)

- **Tampilan Reject Consirmation(Terisi)** 

	![](../assets/reject-filled-state.png)
## 3. Logic UI / UX
- **Loading:** Saat melakukan load halaman maka berikan loader spinner.
- **Button Approve:** Saat klik button tersebut maka akan muncul modal sesuai dengan tampilan appove confirmation, setelah success maka akan kembali ke list awal.
- **Button Reject:** Saat klik button tersebut maka akan muncul modal sesuai dengan tampilan reject confirmation, setelah success maka akan kembali ke list awal.
## 4. API Needs
- `API Approval Create Doctor Request`
- `API Reject Create Doctor Request blom terdefine mas bintang`