# 🚚 Bandla Logistics - Cloud Transport & Payroll Platform

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

An enterprise-grade, cloud-hosted **Transport Management System (TMS), Automated CSV Payroll Reconciliation Hub, and Fleet Telematics CRM** built for multi-depot courier operations in the United Kingdom.

---

## 🌟 Core Enterprise Features

### 1. 📊 Automated CSV & Excel Reconciliation Hub
* **Dynamic Base Stop Pay**: Automatically reconciles dispatched stops vs. paid stops.
* **Fail (%) Calculation**: Matches standard courier reconciliation formula:
  $$\text{Fail (\%)} = \frac{\text{Dispatched Stops} - \text{Paid Stops}}{\text{Dispatched Stops}} \times 100$$
* **£100 Minimum Day Rate Top-Up Guarantee**: Automatically calculates top-up subsidies for shifts under 100 stops ($$100 - \text{Paid Stops}$).
* **1-Click Top-Up Cancellation Override**: Toggle to override or restore day-rate subsidies.
* **£0.05 Excess Parcel Bonus**: Automatically calculated for parcels above base stops.

### 2. 🧾 Contractor Self-Billing Invoices (State Machine)
* **Audit-Locked Lifecycle**: `Draft ➔ Checked ➔ Approved ➔ Locked 🔒`.
* **Breakdown**: Itemized gross pay, excess parcel pay, weekly van rental deductions (£135.00/wk), and 20% VAT calculations.
* **PDF Statements**: Automated contractor statement generation.

### 3. 🚐 Fleet Asset Inventory & Telematics (78 Vehicles)
* Live interactive status switcher: *Available, Deployed on Route, Under Maintenance, Breakdown, Decommissioned*.
* MOT, Road Tax, and Insurance expiry countdowns with 1-click decommission recovery.

### 4. 👥 Driver Personnel & Compliance Register (101 Couriers)
* Right to Work (RTW) visa compliance matrix (British Citizen, Settled Status, Student 20h, Skilled Worker).
* DVLA license point tracking, VAT status, and holiday planning.

---

## 🚀 Quick Start & Deployment

### Deploy to Vercel (1-Click)
1. Fork or import this repository into your GitHub account.
2. Go to [vercel.com/new](https://vercel.com/new) and select this repository.
3. Click **"Deploy"** (Vercel automatically detects `vercel.json` and `api/index.js`).

### Local Development
```bash
# Install backend and frontend dependencies
npm install
npm --prefix client install

# Run backend & frontend concurrently
npm run dev
```

---

## 🏗️ Architecture & Technology Stack
* **Frontend**: React 19, Vite, Tailwind CSS, Lucide Icons, Chart.js.
* **Backend**: Express.js (REST API, JWT Authentication, Role-Based Access Control).
* **Database**: PostgreSQL with Drizzle ORM and embedded `@electric-sql/pglite` WebAssembly engine.
* **Hosting**: Configured for Vercel Serverless Functions & Static Edge CDN.
