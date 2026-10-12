# One-paste Ubuntu deployment

1. Save the supplied `l-mugo-co-advocates-maroon-brand-update.zip` into `~/Downloads`.
2. Ensure the GitHub CLI (`gh`) and Vercel CLI (`vercel` or `npx vercel`) are authenticated.
3. Paste the complete command below once. For this **brand-colour update**, use the existing GitHub repository and Vercel project. This ZIP is not intended to create a new repository.

```bash
cd ~/Downloads && unzip -oq l-mugo-co-advocates-maroon-brand-update.zip && cd l-mugo-co-advocates && git add -A && (git diff --cached --quiet || git commit -m "Match website colours to Mugo maroon logo") && git push origin main && npx vercel --prod
```

For future edits, replace the website files inside the already cloned repository, then run:

```bash
cd ~/Downloads/l-mugo-co-advocates && git add -A && (git diff --cached --quiet || git commit -m "Update L Mugo Advocates website") && git push origin main && npx vercel --prod
```

### Checks before publicly presenting the demo

- Please verify the two office addresses, published landline and both email addresses directly with the firm.
- Provide a **WhatsApp-enabled mobile number** if you want the exact WhatsApp button from the Were reference. The round green contact button currently opens `/contact/`, because +254 20 210 0102 is a landline and is not verified on WhatsApp.
- The Vercel project URL is assumed to be `https://l-mugo-co-advocates.vercel.app/`. Update domain strings in HTML, `robots.txt`, and `sitemap.xml` if Vercel assigns a different name.
- The email enquiry form creates a draft in the visitor's mail application; it does not send automatically.
- Photographs loaded from Pexels are third-party resources. They need internet access. The profile image is the user's actual supplied file.
