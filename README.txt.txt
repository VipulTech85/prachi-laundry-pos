PRACHI LAUNDRY - POS SYSTEM
===========================

FILES
-----
- index.html   → Public landing page (hero + login button)
- login.html   → Admin login page
- pos.html     → POS system (protected — only after login)


DEFAULT LOGIN
-------------
Username: admin
Password: prachi2026

⚠️ Change these in BOTH login.html and pos.html:
   const VALID_USERNAME = 'admin';
   const VALID_PASSWORD = 'prachi2026';


HOW TO CHANGE OWNER PHONE
-------------------------
In pos.html, search for "OWNER_PHONE_DISPLAY" and edit:
   const OWNER_PHONE_DISPLAY = '98765 43210';


HOW TO DEPLOY
-------------
1. Drag the whole "prachi-laundry" folder to app.netlify.com/drop
2. Wait ~10 seconds
3. Test:
   - Open the URL → Landing page
   - Click "Admin Login" → login.html
   - Sign in → pos.html
   - Click "Logout" → back to landing page


HOW PAYMENT TRACKING WORKS
--------------------------
- New bills default to "Pending" payment
- Toggle the payment switch to mark "Paid" at creation
- Pending bills appear in the dashboard's "Pending Payments" card
- Click "Mark Paid" on any pending bill to record the payment date
- Dashboard shows Billed / Paid / Pending totals for every period
- Export to Excel/PDF includes all three columns


DATA STORAGE
------------
All data (services, prices, sales history) is stored in the
browser's localStorage. Each device keeps its own data.