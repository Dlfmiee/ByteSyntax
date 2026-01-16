# Pelan Implementasi: Parcel Collection Tracking System

Fail ini menerangkan langkah-langkah teknikal yang akan diambil untuk membina sistem penjejakan parcel.

## Fasa 1: Penyediaan Pangkalan Data (Database)
- **Fail: `schema.sql`**
- Membina table `admins` untuk menyimpan maklumat log masuk pentadbir.
- Membina table `parcels` untuk menyimpan maklumat parcel (Tracking No, Nama, No. Telefon, Status).
- Menambah akaun admin default untuk tujuan testing.

## Fasa 2: Pembangunan Backend (Logic & API)
- **Fail: `api/db.php`**: Menguruskan sambungan ke MySQL menggunakan PDO.
- **Fail: `api/auth.php`**: Logik pengesahan (Login/Logout) bagi Admin.
- **Fail: `api/parcels.php`**: 
    - Fungsi **Tambah**, **Padam**, dan **Kemaskini Status** parcel (untuk Admin).
    - Fungsi **Carian (Track)** parcel (untuk User).

## Fasa 3: Pembangunan Frontend (UI/UX)
- **Fail: `assets/css/style.css`**: Sistem gaya (styling) moden, premium, dan responsif.
- **Fail: `index.html`**: Halaman utama bagi User untuk membuat semakan.
- **Fail: `admin/login.html`**: Halaman log masuk bagi Admin.
- **Fail: `admin/dashboard.html`**: Halaman pengurusan parcel bagi Admin.
- **Fail: `assets/js/user.js` & `assets/js/admin.js`**: Logik interaksi (AJAX) untuk kelancaran sistem tanpa muat semula halaman (no page reload).

## Fasa 4: Pengujian (Testing)
1. Uji keupayaan admin untuk log masuk.
2. Uji kemasukan data parcel baharu.
3. Uji fungsi carian dari pihak user menggunakan butiran yang betul.
4. Uji pertukaran status parcel daripada "Pending" kepada "Collected".

---
**Nota**: Implementasi ini akan memastikan sistem adalah ringan, pantas, dan mudah untuk di-deploy ke pelayan XAMPP.
