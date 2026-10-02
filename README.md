# SPPG Bukit Kemuning 4 — Menu

Website menu MBG SPPG Bukit Kemuning 4 dengan Firebase.

## Login Admin
- Firebase Authentication: Email/Password
- Akses admin diverifikasi melalui Firestore collection `adminEmails`
- Tidak menggunakan OTP
- Tidak menggunakan Cloud Functions
- Tidak menggunakan Google Sign-In

## GitHub Pages
1. Upload seluruh isi folder ini ke repository GitHub.
2. Pastikan file utama bernama `index.html`.
3. GitHub → Settings → Pages → Deploy from branch.
4. Pilih branch `main` dan folder `/ (root)`.

## Firebase
Firebase config sudah ada di `index.html`.

Aktifkan:
- Authentication → Sign-in method → Email/Password
- Firestore Database

Buat admin pertama melalui Firebase Authentication → Users → Add user.
Kemudian buat dokumen Firestore:

Collection: `adminEmails`
Document ID: email admin yang sama
Field:
`email` = email admin

Contoh struktur:
`adminEmails/EMAIL_ADMIN` → `{ "email": "EMAIL_ADMIN" }`

## Security Rules
`firestore.rules` dan `storage.rules` disertakan untuk konfigurasi Firebase.

Catatan: `index.html` dapat dipublikasikan di GitHub Pages. Jangan memasukkan password Firebase, SMTP password, service account key, atau credential server ke repository.
