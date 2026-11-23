# Buster Build — Interactive WhatsApp Flyer

This static Netlify site shows the four-page Dezemba Build Blitz 2026 flyer for the 25 November–15 December 2026 promotion. No build command is required; `netlify.toml` publishes the repository root.

## How quotes work

1. Tap a yellow **+** on a flyer product, choose a quantity, and add it to the quote.
2. Open **Review WhatsApp quote**, enter your name and phone number, and choose collection or delivery. Delivery requires an address.
3. Select **Send via WhatsApp**. The site opens a prefilled message without a preset recipient. Choose a contact in WhatsApp and press **Send** there.

Selected products and quantities are saved in the current browser so the draft survives a reload. Customer details are not saved by the site, and there is no central order history. Prices, stock and delivery charges must be confirmed by the recipient.

## Updating the flyer

The logo and flyer pages are in `assets/buster-build/`. `index.html` contains the product names, prices, and percentage coordinates for the buttons on each page. When replacing a flyer, update that catalog and verify that the buttons align with the intended products on a phone. Test the WhatsApp recipient-selection flow before distributing a printed QR code.
