# Dilks For Sheriff 2028 — Campaign Website (Light / Patriotic theme)

Static site. Pages: index.html, about.html, donate.html, 404.html + images/dilks.jpg.
The campaign logo is embedded directly in the pages (no logo file needed).

## Update the live site
GitHub repo -> Add file -> Upload files -> drag the 4 HTML files -> Commit.
Vercel auto-redeploys in ~20s. Use an incognito tab / add ?v=6 to bust phone cache.

## Contact form (Formspree, free)
formspree.io -> create form -> notify dilksforsheriff@gmail.com.
Replace YOUR_FORM_ID in index.html with your form id.

## Donations (Stripe Payment Links)
See the comment block at the top of donate.html. Create Stripe Payment Links with the
required custom fields (name, address, occupation, employer) and paste each URL into the
PASTE_STRIPE_LINK_..._HERE placeholders.
