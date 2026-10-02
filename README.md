# SPPG Bukit Kemuning 4 — GitHub + Firebase

Login admin menggunakan Firebase Authentication Email/Password.

## Firebase
- Project: sppg-bukit-kemuning-4-menu
- Authentication: Email/Password
- Firestore: collection `adminEmails`
- Dokumen admin pertama:
  - ID: `sppgbukitkemuning4@gmail.com`
  - field `email` (string): `sppgbukitkemuning4@gmail.com`

## Firestore Rules
Gunakan `firestore.rules` pada Firebase Console lalu klik Publish.

Aturan membolehkan akun login membaca dokumen admin miliknya sendiri, sementara daftar seluruh admin hanya dapat dibaca oleh admin yang sudah terverifikasi.

## GitHub Pages
Upload `index.html` ke repository GitHub Pages dan pastikan nama file tepat `index.html`.
