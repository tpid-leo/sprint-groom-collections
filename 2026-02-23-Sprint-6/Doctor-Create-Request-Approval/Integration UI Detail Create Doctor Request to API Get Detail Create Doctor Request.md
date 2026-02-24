# Integration UI Detail Create Doctor Request to API Get Detail Create Doctor Request
## 1. Overview
Menampilkan data request yang digunakan untuk membuat data doctor baru. Ada 2 sisi yaitu sebagai 'Maker' dan 'Approval'
## 2. Requirement Visual
- **Tampilan User Maker**

	![](../assets/use-maker.png)
- **Tampilan User Approval**

	![](../assets/user-approve.png)
## 3. Logic UI / UX
- **Loading:** Saat melakukan load halaman maka berikan loader spinner.
- **Maker/Approval:** Tampilan UI request didapat dari key role pada user yang sedang login( melalui jwt, session).
## 4. API Needs
- `API Get Detail Create Doctor Request`