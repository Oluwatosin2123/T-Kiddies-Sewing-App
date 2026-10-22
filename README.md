# T-Kiddies-Sewing-App
👗 T-Kiddies Fashion Store

A smart digital management system for children's-wear tailoring businesses.

T-Kiddies Fashion Store is a mobile-first, installable web application designed to help children's fashion designers and tailoring businesses manage customers, measurements, clothing styles, cutting plans, sewing workflows, orders, inventory, payments, and business reports in one place.

The application is designed to simplify daily operations, improve production tracking, reduce recordkeeping errors, and help fashion business owners make better business decisions.

«Project status: Ready for a careful pilot. Complete the recommended testing and review the limitations below before relying on it for live business operations.»

---

📌 Table of Contents

- "Overview" (#-overview)
- "Key Features" (#-key-features)
- "Technology Stack" (#-technology-stack)
- "Getting Started" (#-getting-started)
- "Deploying with GitHub Pages" (#-deploying-with-github-pages)
- "Installing the App" (#-installing-the-app)
- "First-Time Setup" (#-first-time-setup)
- "Database and Data Storage" (#-database-and-data-storage)
- "Security and Backup" (#-security-and-backup)
- "Testing and Quality Assurance" (#-testing-and-quality-assurance)
- "Project Structure" (#-project-structure)
- "Limitations and Future Improvements" (#-limitations-and-future-improvements)
- "Privacy and Data Protection" (#-privacy-and-data-protection)
- "Development Process" (#-development-process)
- "License" (#-license)

---

🌟 Overview

T-Kiddies Fashion Store is built for a children's-wear tailoring business that needs a practical way to manage its operations digitally.

Instead of relying entirely on paper records, the application brings essential business activities together in a single interface.

It supports:

- Customer and guardian records.
- Children's garment measurements.
- Clothing style references and photographs.
- Fabric calculations and cutting instructions.
- Sewing tasks and production timers.
- Order tracking and delivery scheduling.
- Fabric and accessories inventory.
- Production costing, pricing, and profit tracking.
- Payment records and outstanding balances.
- Business performance reports.
- Data export, backup, and restoration.

The application uses plain HTML, CSS, and JavaScript. It does not require a server, a package installation, or a build process.

✨ Key Features

Feature| Description
👥 Customer Management| Store child and guardian details, notes, customer balances, and payment histories. Archive customers or use the delete-all-records tool.
📏 Measurements| Maintain versioned measurement records for garments and display measurements in centimetres or inches.
👗 Style Gallery| Keep clothing style references and photographs. Uploaded images are re-encoded, removing embedded camera metadata.
✂️ Cutting Plans| Calculate pattern pieces and fabric requirements, require tailor approval, and print cutting instructions.
🧵 Sewing Workflow| Organise sewing tasks and track work using start, pause, and resume timers that persist across page refreshes.
📦 Order Management| Track order statuses, delivery dates, and production schedules using board and calendar views. Print order sheets.
🪡 Inventory Management| Manage fabric and accessories, monitor stock levels, record wastage and leftover fabric, and receive low-stock and shortage warnings.
💰 Costing and Pricing| Calculate material, accessory, labour, and additional costs. Set selling prices, profit margins, and manual price overrides.
💳 Payment Records| Track order prices, deposits, additional payments, payment dates, balances, and payment histories.
📊 Business Reports| Review orders, revenue, costs, recorded profit, outstanding balances, fabric usage, wastage, popular styles, and delivery performance.
📤 Export and Printing| Export CSV files, generate Excel-compatible tables, and print measurement charts, cutting instructions, order sheets, and production summaries.
🔐 Access Control| Use a passcode lock, Owner and Staff roles, failed-attempt lockout, and automatic locking after inactivity.
💾 Backup and Restore| Create encrypted or plain JSON backups, validate restored data, check integrity, and receive backup reminders.
📱 Mobile-First Design| Use the application through a mobile browser or install it as a Progressive Web App.
🌐 Offline Support| Continue using the app after its files have been cached, with data stored locally on the device.

---

🛠️ Technology Stack

The project uses lightweight web technologies without a server-side application.

- HTML5 — application structure.
- CSS3 — styling and responsive layouts.
- JavaScript — application logic, calculations, and interactions.
- IndexedDB — local database storage.
- Progressive Web App (PWA) — installation and offline support.
- Service Worker — caching application files for offline use.
- Web Crypto API — passcode hashing and encrypted backups.

Architecture

The application is a single-page web app built around "index.html", with supporting files for installation metadata, offline caching, and application icons.

Important: The application does not currently have a backend, cloud database, or automatic synchronisation between devices.

---

🚀 Getting Started

Prerequisites

You need:

- A GitHub account.
- A copy of the project files.
- A modern web browser.
- An HTTPS hosting service for installation and full Progressive Web App functionality.

No additional package installation or build tools are required.

Run Locally

1. Download or clone the repository.
2. Open the project folder.
3. Serve the files through a local development server for testing.
4. Open the application in your browser.

For full PWA functionality, including secure-context features, use HTTPS or an appropriate local development environment.

---

🌐 Deploying with GitHub Pages

GitHub Pages provides a straightforward way to publish this static web application.

Step 1: Create a Repository

Create a new repository on GitHub.

Step 2: Upload the Project Files

Upload all required project files and folders, including:

- "index.html"
- "manifest.webmanifest"
- "sw.js"
- "icons/"
- ".nojekyll"
- "README.md"

Keep the directory structure intact.

Step 3: Enable GitHub Pages

1. Open your repository on GitHub.
2. Go to Settings.
3. Select Pages.
4. Under Build and deployment, choose Deploy from a branch.
5. Select the "main" branch and the "/ (root)" folder.
6. Save your settings.

Step 4: Open Your Published App

After deployment, your application should be available at:

"https://YOUR-USERNAME.github.io/YOUR-REPOSITORY-NAME/"

Replace the placeholders with your actual GitHub username and repository name.

Step 5: Update the Application

When publishing changes:

1. Update the relevant project files.
2. Change the "CACHE" version in "sw.js" (for example, to "tkiddies-v2") so installed copies can refresh their cached application files.
3. Commit and push your changes.
4. Test the deployed version.

Other static HTTPS hosting providers, such as Netlify and Cloudflare Pages, can also host the application.

---

📲 Installing the App

T-Kiddies Fashion Store is designed to work as an installable Progressive Web App.

Android

1. Open the published website in Chrome.
2. Tap the three-dot menu.
3. Select Install app or Add to Home screen, depending on the available option.

iPhone and iPad

1. Open the website in Safari.
2. Tap Share.
3. Select Add to Home Screen.

Windows, Mac, and Chromebook

1. Open the website in Chrome or Edge.
2. Look for the install option in the address bar or browser menu.
3. Select Install T-Kiddies, or the equivalent option shown by your browser.

Once the application files have been cached, the app can operate offline. Each browser or device maintains its own separate database.

---

⚙️ First-Time Setup

Before entering real business records:

1. Open Settings → Security and privacy and create an owner passcode of at least eight characters.
2. Set your business name, phone number, and preferred currency. The default currency is Nigerian naira (₦).
3. Open Costing → Pricing and configure your hourly labour rate and default profit margin.
4. Remove any demonstration data from the dashboard.
5. Create an encrypted backup through Settings → Backup and restore and store it securely.

Create backups regularly, especially before making major changes or restoring data.

---

🗄️ Database and Data Storage

The application uses IndexedDB for browser-based storage.

The database is named:

"tkiddies"

Its object stores include:

- "settings"
- "customers"
- "measurements"
- "styles"
- "orders"
- "orderItems"
- "materials"
- "payments"
- "fabricCalcs"
- "workflows"

Data Validation

The application validates saved data to help prevent common errors. Examples include:

- Payments must be greater than zero.
- Stock quantities cannot fall below zero.
- A customer record must include a name.

Backups include the application data stores but exclude passcodes.

Data remains local to the browser. There is no automatic cloud synchronisation or shared database between devices.

---

🔐 Security and Backup

The application includes several security and recovery features:

- Passcode hashing using PBKDF2-SHA-256 with a salt.
- Owner and Staff roles.
- Lockout after five failed passcode attempts.
- Automatic locking after inactivity.
- Encrypted JSON backups using AES-GCM.
- Optional plain JSON backups.
- Validation during restoration.
- Data integrity checks and backup reminders.

Recommended Backup Practice

1. Open Settings → Backup and restore.
2. Create an encrypted backup.
3. Store the backup file somewhere secure.
4. Keep the encryption passphrase safe.
5. Periodically test restoration using a separate device or test environment.

Security note: The passcode lock is not equivalent to server-side authentication. Browser data is not encrypted at rest, and someone with sufficient technical access to the device may bypass the lock. Staff restrictions do not hide order prices on order pages.

A forgotten passcode cannot be reset through the application. The documented recovery method is to clear the site's data, restore a backup, and set a new passcode.

---

🧪 Testing and Quality Assurance

Quality checks have been run in a headless Chromium browser.

Testing has covered:

- Unit conversions between yards and metres.
- Fabric stock deductions and leftover fabric.
- Cost, profit, deposit, and balance calculations.
- Report calculations and filtering.
- CSV export safety.
- Backup validation.
- Data persistence after page refresh.
- Sign-out and sign-in.
- Backup, data erasure, and restoration.
- Role restrictions.
- Automatic inactivity locking.
- Responsive layouts across 29 screen configurations at 360 × 640 pixels.

A layout issue involving two-column forms overflowing small screens was identified and fixed during testing.

Built-in Tests

In the running application, open Settings and use the available test tools.

These include:

- Unit and calculation tests.
- Report tests and filters.
- Data self-tests.
- Data problem checks.
- Backup validation tests.
- Pattern and workflow tests.

Recommended Pre-Launch Checks

Before using the application for live customer orders:

- Complete a test order from customer registration through final payment.
- Verify all financial calculations manually.
- Test encrypted backup restoration and compare the restored totals.
- Compare application reports with existing business records for at least one week.
- Test passcode locking, automatic locking, and failed-attempt lockout on each staff device.
- Print and check an order sheet, measurement chart, and cutting sheet.
- Ask a qualified tailor to verify a cutting plan against a test garment.
- Run the data checks and report tests after restoring a backup.

Testing status: iOS Safari, physical Android devices, very large datasets, and physical printers have not yet been fully tested.

---

📁 Project Structure

T-Kiddies-Fashion-Store/
│
├── index.html              # Main application: HTML, CSS and JavaScript
├── manifest.webmanifest    # PWA metadata, name and appearance
├── sw.js                   # Service worker for application-file caching
├── icons/                  # App icons and Apple touch icon
├── .nojekyll               # GitHub Pages configuration
└── README.md               # Project documentation

---

⚠️ Limitations and Future Improvements

The current version provides a broad set of business-management features, but some capabilities require further development.

Current Limitations

1. Local-only data: No cloud database or automatic synchronisation between devices.
2. Browser storage risks: Clearing browser data can permanently delete local records if no backup exists.
3. Limited authentication: The passcode lock does not provide server-grade protection.
4. Local image storage: Style photographs remain on the device; there is no cloud image storage or malware scanning.
5. No payment gateway: Payments are bookkeeping records. No payment provider is connected.
6. Excel-compatible export: The export is an HTML table that Excel can open, not a native ".xlsx" file.
7. Estimated cutting calculations: Fabric and pattern calculations require approval by a qualified tailor.
8. Device compatibility: Some browsers, devices, and printers still need additional testing.

Potential Future Improvements

Possible future development areas include:

- Cloud storage and secure synchronisation.
- Secure server-side authentication and staff permissions.
- Integration with payment providers such as Paystack or Flutterwave.
- Native Excel ".xlsx" exports.
- Improved automated testing across devices.
- More advanced inventory and production analytics.

These are potential enhancements, not features currently implemented.

---

🔏 Privacy and Data Protection

Customer records, children's measurements, and style photographs may contain sensitive business or personal information.

The application stores its records locally unless the user exports a backup. Treat backup files as confidential and avoid publishing customer information in a public repository.

Recommended practices:

- Use encrypted backups and protect their passphrases.
- Do not commit real customer data, measurements, or photographs to GitHub.
- Keep exported records in secure locations.
- Review applicable data-protection requirements before storing children's information.
- In Nigeria, consider the requirements of the Nigeria Data Protection Act.

---

🏗️ Development Process

The application was developed in phases, with each phase building on the existing project.

Phase 1: Foundations

- Customer management.
- Measurements.
- Style gallery.
- Settings, logo, and currency configuration.

Phase 2: Production Management

- Pattern and fabric calculations.
- Tailor approval workflow.
- Sewing tasks and persistent timers.

Phase 3: Order Management

- Order lifecycle.
- Delivery dates.
- Board and calendar views.
- Printable order sheets.

Phase 4: Materials, Costing, and Payments

- Inventory and unit conversions.
- Stock deduction after confirmed fabric usage.
- Wastage and leftover fabric tracking.
- Labour rates, profit margins, and pricing.
- Deposits, balances, and payment histories.

Phase 5: Reporting, Security, and Release

- Business reports and filters.
- CSV and Excel-compatible exports.
- Printable business documents.
- Passcode protection and user roles.
- Encrypted backup and restoration.
- Database validation and error handling.
- Mobile layout improvements.
- Offline installation and PWA support.

---

📄 License

No license has been specified yet.

Before making this repository public, add a "LICENSE" file that reflects how you want others to use, modify, and distribute your work. For example, the MIT License is one option for an open-source project.

---

❤️ About the Project

T-Kiddies Fashion Store demonstrates how web technologies can support the day-to-day operations of a children's-wear tailoring business.

By bringing customer records, garment production, inventory, costing, and reporting into one application, the project aims to make fashion business management more organised and accessible.

Built for a more organised children's-fashion business. 👗🧵
