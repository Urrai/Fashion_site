FashionKurtas — Store

A single-file, no-build storefront (HTML/CSS/JS) with product browsing, cart, checkout, and a built-in seller/admin dashboard. No server, database, or hosting required — just open the file in a browser.

Getting started
Double-click anokhi-threads-store.html (or open it via File → Open in your browser).
That's it — no install, no server. Everything runs client-side.

For real use, upload the file to any static host (Netlify, GitHub Pages, your own server, etc.) so customers can reach it via a URL instead of a local file.

How it works
Storage: All data (products, cart, admin state, orders) is saved in the browser's localStorage, scoped to whichever browser + device the page is opened in.
Data does not sync across devices or browsers.
Clearing browser data/cache will erase it.
It persists across refreshes and closing/reopening the tab.
No backend: There's no real payment processing, email sending, or inventory sync. Orders are just recorded locally for the seller to view in the dashboard.
Customer-facing features
Browse products by category (filter chips)
Product detail pages with size selection
Cart drawer (add, change quantity, remove)
Checkout with delivery details and a payment method choice (UPI / Cash on Delivery / Card placeholder)
Order confirmation screen
Seller / Admin dashboard

Click Seller / Admin in the header and enter the passcode:

seller123

⚠️ This is a demo passcode. Before sharing this file with real customers, change it — search for ADMIN_PASSCODE near the top of the <script> section and replace 'seller123' with your own.

From the dashboard you can:

Add a product — upload a photo, set name, price, stock, category, and available sizes
Edit a product — click Edit on any existing product to update its photo or details, or Cancel to discard changes
Remove a product
Set your UPI ID — used at checkout for the UPI payment option (replace the demo fashionkurtas@upi with your real VPA)
View recent orders placed by customers
Known limitations
Product images are stored as compressed JPEG data URLs inside localStorage, which has a total size limit (typically ~5MB per browser origin). A large catalog of high-res photos could eventually hit that limit.
No real payment gateway — UPI/COD/Card are informational only at checkout.
Data is local to one browser; there's no multi-device or multi-user sync.
The admin passcode is stored in plain text in the file's source — fine for a demo, not for production security.
Customizing
Colors/theme: CSS variables are defined at the top of the <style> block (--wine, --gold, --ivory, etc.) — change these to re-theme the whole site.
Categories: edit the <option> list in the admin "Category" dropdown.
Sizes: edit the sizeOptions array near the admin product form code.
