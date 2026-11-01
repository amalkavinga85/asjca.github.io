# A. S. Junior Cricket Academy: website files

Live address: **https://www.asjuniorcricketacademy.com/**

## What's in this folder
- `index.html`: the whole website (Home, Contact Us and Admin Portal), connected to Firebase (project `asjca-website`).
- `videos/new-enrolments.mp4`: the New Enrolments video. Keep it in the `videos` folder.
- `CNAME`: tells GitHub Pages to serve the site at www.asjuniorcricketacademy.com. Keep it in the top folder.

## Put it on GitHub Pages
1. In your GitHub repository, upload everything in this folder (keep the `videos` folder) to the top level of the branch GitHub Pages uses (usually `main`).
2. Repository **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main` / `(root)`.
3. Custom domain: `www.asjuniorcricketacademy.com` (the `CNAME` file fills this in). Tick **Enforce HTTPS** once it's available.
4. At your domain provider (DNS):
   - `CNAME` record: `www` → `yourusername.github.io`
   - `A` records for the bare domain `asjuniorcricketacademy.com` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`

## Firebase: one-time checks
- **Authentication → Settings → Authorized domains** must include `www.asjuniorcricketacademy.com` and `asjuniorcricketacademy.com`.
- **Security rules**: use the latest versions in the *Firebase setup guide* (the enquiry rule includes `notified`).

## First time after uploading
1. Open https://www.asjuniorcricketacademy.com/ and click **Admin Portal →** at the bottom of the page.
2. Sign in with **amalkavinga@gmail.com** and the password you set in Firebase.
3. On this first sign-in the site copies its starting content to Firebase: the 4 coaches, the trophy and enrolment posts, and the gallery links. Wait for "Saved ✓". Until then the public pages are empty.

## Admin Portal
- The link is at the bottom of every page ("Admin Portal →").
- Change password: Admin Portal → Change password. Forgotten it? Type the email on the sign-in screen and tap **Forgot password?**.
- Clicking Home or Contact Us signs the admin out automatically.
- Only the Firebase user whose UID is in the security rules can change content or read enquiries.

## Optional: automatic enquiry alerts
In `index.html`, search for `const NOTIFY` and fill in:
- `email.accessKey`: a free key from web3forms.com
- `whatsapp.apiKey`: a free key from callmebot.com (activated from +94 77 782 5909)

Without them, enquiries are still saved and appear in Admin Portal → Enquiries.
