# BUSTER BUILD — WHATSAPP QUOTATION WEBSITE

Independent from Maliks Hub / Cloudflare. This is a static HTML quotation website that sends customer-selected items to a chosen salesperson via WhatsApp.

## Important: salesperson configuration

Open `index.html` in the GitHub web editor (press `.` from the repository page, or click the pencil). Search for `const SALESPEOPLE=` and replace the sample salesperson entries with real names, confirmed WhatsApp numbers and optionally photo links. Example:

const SALESPEOPLE=[
  {id:'rakesh',name:'Rakesh Sobaram',phone:'0795122078',photo:'',role:'Sales Consultant'}
];

The example above is NOT an authorised contact and MUST NOT be published without confirming it.

Numbers: use 0795122078 or 27795122078. The page converts South African mobile numbers for WhatsApp automatically.

Until you configure a real number, salesperson cards remain disabled and customers cannot send a quotation. Never publish the pamphlet QR before testing the live salesperson link.

## Create a SEPARATE new GitHub repository

1. Sign in to https://github.com/new
2. Set owner to your own GitHub account and repository name `busterbuild-whatsapp-quotes` (or your preferred name).
3. Public is simplest for free Git-powered hosting. Do not put private customer records in this public repo.
4. Create the repository, then choose `Add file` > `Upload files`, and upload the FILES INSIDE THIS ZIP: `index.html` and `netlify.toml`.
5. Commit those files to the main branch.
6. Confirm `index.html` sits at the TOP LEVEL of the new repository, not inside a folder.

NOTE: The GitHub connector available in the chat cannot create brand-new repositories for you; repository creation needs your own one-time GitHub action.

## Host FREE with Netlify, NOT GitHub Pages

GitHub Pages does not permit use as commercial online business / transaction hosting. Keep your SOURCE on GitHub, but host the website with Netlify instead.

1. Go to https://app.netlify.com/start or https://app.netlify.com/ and sign in.
2. Choose `Add new project` > `Import an existing project` > GitHub, then select ONLY the new `busterbuild-whatsapp-quotes` repository.
3. Set the production branch to `main`. This is a static site: no build command. Publish directory is `.` (repo root).
4. Deploy the project. Netlify will assign a public HTTPS URL ending in `.netlify.app`.
5. Open that URL on a phone that has never logged in to the Maliks Hub, search items, add quantities and test WhatsApp to a confirmed salesperson.

You can alternatively publish this ZIP through https://app.netlify.com/drop to get a temporary working site without connecting GitHub first. You can connect a repository afterward. Netlify's free usage allowance is limited: check your account plan and usage. No Cloudflare R2 needed.

## QR for the pamphlet

Do NOT print the old QR that points to https://maliks.co.za/pamphlet-quote.html. That is a different address.

Only after Netlify gives you the actual live URL, generate a new QR for exactly that address. Send the actual URL back to ChatGPT and ask for the print-ready white transparent PNG + black-on-white backup + SVG.

White QR codes should be printed only on a solid dark background with sufficient contrast and quiet zone. Test with an Android and iPhone before distributing printed pamphlets.

## How customers use the site

- Choose quantities on the mobile product list (105 pamphlet item/variant options), or add custom requested items.
- Enter name, phone, delivery/collection and delivery address if needed.
- Pick an active salesperson; tap Send Quotation on WhatsApp.
- WhatsApp opens with prefilled message; CUSTOMER must press Send there.

Privacy: saved quote history is only in the customer's localStorage on their own browser. It is NOT a central company database, not visible to managers remotely, and not proof the WhatsApp was sent. If staff must see all requests, add a secure server/database later.

## Maintenance

Change `const SALESPEOPLE=` or the embedded `const PRODUCTS=` list inside `index.html`, then commit to the new GitHub repo. Netlify redeploys from the linked repo, without updating Maliks Hub.

This version includes the attached four-page Buster Build Dezemba Build Blitz 2026 flyer, with the promotional period 25 November–15 December 2026; edit/remove time-limited prices after the sale.
