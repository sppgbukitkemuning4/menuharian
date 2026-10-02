# SPPG Bukit Kemuning 4 — GitHub Pages + Firebase

## Login Admin
Website menggunakan Firebase Authentication **Email/Password**.
Tidak menggunakan OTP, Cloud Functions, SMTP, atau billing Blaze.

## Struktur admin
Firestore collection:

`adminEmails`

Contoh document:

- Document ID: `sppgbukitkemuning4@gmail.com`
- Field `email`: `sppgbukitkemuning4@gmail.com` (string)

Email yang sudah terdaftar di `adminEmails` dapat login dan mengelola menu serta email admin lain.

## Firebase Authentication
Aktifkan:

Authentication → Sign-in method → Email/Password → Enable

Buat user admin pada tab Authentication → Users.

Email user harus sama dengan email pada `adminEmails`.

## Firestore
Gunakan `firestore.rules` pada folder ini, atau salin rules tersebut ke Firebase Console → Firestore Database → Rules → Publish.

## Storage
Gunakan `storage.rules` agar upload foto menu hanya dapat dilakukan oleh admin yang terdaftar.

## GitHub Pages
Upload `index.html` ke root repository dan pastikan GitHub Pages menggunakan branch `main` dan folder `/root`.

## Firebase config
Konfigurasi Firebase Web App sudah dimasukkan ke `index.html`.
Jangan memasukkan password Gmail, service account key, atau credential server ke GitHub.
