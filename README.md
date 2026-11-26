# KHURJIN | خورجین
**Everything, Everywhere, Live. From Home to Home.**

**Khurjin** (*خورجین* — traditional woven saddlebag) is a modern, multi-category live-commerce marketplace built with **Next.js (App Router)**, **TypeScript**, and **Tailwind CSS**. It connects home-based creators, local artisans, and shops directly with buyers through real-time live video selling and escrow-protected checkout.

---

## Key Features

### Live Commerce & Storefront
- **Live-Stream Shopping (`/live`):** Sellers broadcast live video to showcase products in real time while buyers chat and purchase pinned items in one click.
- **Multi-Category Marketplace (`/category/[slug]`):** Supports fashion, clothes, homemade food, cookies, jewelry, socks, and daily goods.
- **Khurjin Shopping Bag (`/bag`):** Custom cart experience inspired by the traditional woven *khurjin*.

### Three-Tier Role Architecture & Anti-Scam Protection
- **Buyer Portal (`/buyer`):** Track deliveries, confirm item receipt, manage saved sellers, and open disputes if an order is incorrect.
- **Seller Studio (`/seller`):** Complete KYC verification, manage inventory, broadcast live streams (`/seller/go-live`), fulfill orders, and track escrow earnings.
- **Super Admin Control Center (`/admin`):**
  - **Seller Verification Gate:** Reviews seller IDs and shop details before granting permission to list items or go live.
  - **Escrow Payment Holding:** Holds buyer funds safely until delivery is confirmed, preventing payment fraud.
  - **Live-Stream Moderation:** Monitors active streams with an instant force-stop switch to prevent off-platform scams.
  - **Dispute Resolution:** Freezes payouts and resolves buyer-seller conflicts fairly.

---

## Tech Stack
- **Framework:** Next.js (App Router)
- **Language:** TypeScript
- **Styling:** Tailwind CSS (Herat Kilim & Lapis Theme)
- **Version Control:** Git & GitHub

---

## Project Structure

```text
khurjin/
├── middleware.ts                 # Role-based route guard (/buyer, /seller, /admin)
└── app/
    ├── (auth)/                   # Login & Role Registration
    ├── (marketplace)/            # Public Storefront, Live Streams, Bag & Checkout
    ├── (buyer)/buyer/            # Protected Buyer Dashboard, Orders & Disputes
    ├── (seller)/seller/          # Protected Seller Studio, KYC, Go-Live & Wallet
    └── (admin)/admin/            # Protected Admin Verification, Escrow & Moderation
```

---

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd khurjin
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Run the development server:**
   ```bash
   npm run dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser and start editing `app/(marketplace)/page.tsx`.
