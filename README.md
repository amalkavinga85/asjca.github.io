# A. S. Junior Cricket Academy: website files

## What's in this folder
- `index.html`: the whole website (Home, Contact Us and Admin Portal), with styles, scripts, logo and coach photos built in.
- `videos/new-enrolments.mp4`: the New Enrolments video. Keep it in the `videos` folder next to `index.html`.

## How to put it online
Upload both items, keeping the same folder structure, to any static web host, such as:
- Netlify Drop (app.netlify.com/drop): drag the whole folder in.
- GitHub Pages, Cloudflare Pages, or your own hosting (cPanel → File Manager → `public_html`).

You can also open `index.html` straight from your computer to preview it.

## Admin Portal
- The link is at the bottom of every page ("Admin Portal →").
- Username: `amilasampath`. Password: `cricket2027`. You can change the password inside the portal.
- Clicking Home or Contact Us signs the admin out automatically.

## Important: before going live
1. **Shared content.** News, gallery uploads, coaches, enquiries and the password are currently saved in the admin's own browser (localStorage). Visitors won't see changes made in the Admin Portal until the site is connected to a database, for example Firebase or Supabase.
2. **Enquiry notifications.** In `index.html`, search for `const NOTIFY`. Then:
   - `email.accessKey`: a free key from web3forms.com (sign up with amilasampathanton@gmail.com).
   - `whatsapp.apiKey`: a free key from callmebot.com, activated from +94 77 782 5909.
3. **Security.** The admin login runs in the browser, which is fine for a demo. For the live site it should move to a proper sign-in service, such as Firebase Auth.
4. **Prototype banner.** The yellow "PROTOTYPE" strip at the top can be removed: delete the line `<div class="proto">…</div>`.
