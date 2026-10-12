# One-paste Ubuntu deployment

1. Save the supplied `l-mugo-co-advocates-production.zip` into `~/Downloads`.
2. Ensure the GitHub CLI (`gh`) and Vercel CLI (`vercel` or `npx vercel`) are authenticated.
3. Paste the complete command below once. This creates a **new public** GitHub repository and launches a separate Vercel project.

```bash
cd ~/Downloads && unzip -oq l-mugo-co-advocates-production.zip && cd l-mugo-co-advocates && git init && git branch -M main && git add -A && git commit -m "Launch L Mugo and Co Advocates website" && gh repo create l-mugo-co-advocates --public --source=. --remote=origin --push && npx vercel --prod
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
