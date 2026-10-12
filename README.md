# L. Mugo & Co. Advocates — Website

Static production website. All files live in the repository root. No framework or build step required. The visual colour scheme follows the supplied navy-and-maroon crest: primary brand maroon #8A283C, lighter rose #EBA4AE on dark backgrounds, navy #081637. Gold accents from the original reference template have been replaced sitewide.

## Source and factual caveats
- Firm name, offices, telephone and emails from supplied screenshots. Verify directly before client launch.
- Practice areas and stated foundation year 2020 are taken from supplied Lawzana screenshots and its publicly indexed directory profile.
- Person depicted in supplied portrait is not independently identity-verified; profile uses only supplied name initials and no invented credentials.
- +254 20 210 0102 is a landline. WhatsApp compatibility is NOT verified. The floating round contact control therefore opens the Contact page rather than impersonating a working WhatsApp link. Once a verified mobile WhatsApp number is supplied, replace the floating contact href and icon with the same circular WhatsApp UI as the reference.
- The 4K-width logo files are upscale/composites of the provided low-resolution crest. This does not invent fine details absent from the source.
- External Pexels imagery requires an internet connection. See PHOTO-SOURCES.md.
- Enquiry form opens a draft in the visitor’s email app. It is not a server-backed contact form.
- Domain in canonical URLs and XML sitemap: https://l-mugo-co-advocates.vercel.app . Update if your final Vercel URL differs.
- No fabricated testimonials, unverified case outcomes, or team credentials.

## Launch
```bash
gh auth status
vercel whoami
gh repo create l-mugo-co-advocates --public --source=. --remote=origin --push
npx vercel --prod
```

## Update after first deployment
```bash
git add -A && (git diff --cached --quiet || git commit -m "Update L Mugo Advocates website") && git push origin main && npx vercel --prod
```
