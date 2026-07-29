# 📋 AFRIZONE CRM

A comprehensive Customer Relationship Management system built for COD (Cash on Delivery) e-commerce businesses in Morocco.

![React](https://img.shields.io/badge/React-19.2.6-61DAFB?logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9.3-3178C6?logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4.1.17-06B6D4?logo=tailwindcss)
![Vite](https://img.shields.io/badge/Vite-7.3.2-646CFF?logo=vite)

---

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

---

## 🔐 Demo Credentials

| Role | Email | Password |
|------|-------|----------|
| **Admin** | admin@afrizone.ma | demo123 |
| **Manager** | manager@afrizone.ma | demo123 |
| **Confirmateur** | confirm@afrizone.ma | demo123 |

---

## 🏗️ Tech Stack

| Technology | Version | Purpose |
|------------|---------|---------|
| React | 19.2.6 | UI Framework |
| Vite | 7.3.2 | Build Tool |
| TypeScript | 5.9.3 | Type Safety |
| Tailwind CSS | 4.1.17 | Styling |
| Recharts | 3.x | Charts & Graphs |
| Lucide React | 1.x | Icons |
| Almarai Font | - | Arabic Typography |

---

## 🌍 Language Support

The app supports **Arabic (RTL)** and **English (LTR)** with instant switching:

- **Toggle Button** in header: Click `🇬🇧 EN` or `🇲🇦 عربي` to switch
- **Settings Page**: Language tab for selection
- **120+ translations** covering all UI elements

---

## 📁 Project Structure

```
src/
├── App.tsx                     # Entry point + routing + auth + date filtering
├── types.ts                    # TypeScript interfaces
├── index.css                   # Tailwind + Almarai font + custom scrollbar
├── main.tsx                    # React DOM render
│
├── contexts/
│   └── LanguageContext.tsx     # i18n (AR/EN) + RTL support
│
├── data/
│   ├── mockData.ts             # 6 agents, 8 products, 200 orders, 490 ad records
│   └── platformIcons.tsx       # Platform colors & names
│
├── utils/
│   └── cn.ts                   # clsx + tailwind-merge utility
│
└── components/
    ├── LoginPage.tsx           # Authentication with demo credentials
    ├── Sidebar.tsx             # Navigation (collapsible + mobile responsive)
    ├── DateFilter.tsx          # Today/Yesterday/7days/30days/Custom
    ├── Dashboard.tsx           # KPIs + 3 Charts + Recent Orders
    ├── OrdersPage.tsx          # Orders management + inline status change
    ├── ProductsPage.tsx        # Products catalog + CRUD modal
    ├── TopProductsPerformance.tsx  # Product analytics + sorting
    ├── ConfirmationTeam.tsx    # Team performance + Ads + Charts
    ├── SettingsPage.tsx        # Settings (5 tabs)
    └── PlatformIcon.tsx        # SVG icons for platforms
```

---

## 🔐 Roles & Permissions

| Page | Admin | Manager | Confirmateur |
|------|:-----:|:-------:|:------------:|
| Dashboard | ✅ All orders | ✅ All orders | ✅ **Own orders only** |
| Confirmation Team | ✅ | ✅ | ❌ |
| Orders | ✅ All orders | ✅ All orders | ✅ **Own orders only** |
| Products | ✅ | ✅ | ❌ |
| Top Products | ✅ All data | ✅ All data | ✅ **Own data only** |
| Statistics & Charges | ✅ | ✅ | ❌ |
| Settings | ✅ | ❌ | ❌ |

> **Note:** Confirmateurs can only see and manage their own orders and statistics.

---

## 👥 Agents (6)

| # | Name | Arabic Name | Role | Email |
|---|------|-------------|------|-------|
| 1 | Fatima El Mansouri | فاطمة المنصوري | Confirmateur | fatima@afrizone.ma |
| 2 | Hassan Ouazzani | حسن الوزاني | Confirmateur | hassan@afrizone.ma |
| 3 | Sara El Fassi | سارة الفاسي | Confirmateur | sara@afrizone.ma |
| 4 | Karim Benjelloun | كريم بنجلون | Manager | karim@afrizone.ma |
| 5 | Amina Kettani | أمينة الكتاني | Confirmateur | amina@afrizone.ma |
| 6 | Youssef Tazi | يوسف التازي | Admin | youssef@afrizone.ma |

---

## 📦 Products (8)

| ID | Product | Arabic | Emoji | Price | Cost | Category |
|----|---------|--------|:-----:|------:|-----:|----------|
| p1 | Sérum Anti-Âge | سيروم مضاد للشيخوخة | 🧴 | 299 MAD | 89 MAD | Skincare |
| p2 | Huile d'Olive Bio | زيت زيتون عضوي | 🫒 | 149 MAD | 42 MAD | Food |
| p3 | Crème Éclat | كريم التألق | ✨ | 349 MAD | 105 MAD | Skincare |
| p4 | Savon Noir | صابون أسود | 🫧 | 89 MAD | 22 MAD | Body Care |
| p5 | Shampooing Naturel | شامبو طبيعي | 💇 | 129 MAD | 35 MAD | Hair Care |
| p6 | Masque Argile | قناع الطين | 🎭 | 199 MAD | 55 MAD | Skincare |
| p7 | Eau de Rose | ماء الورد | 💧 | 79 MAD | 18 MAD | Skincare |
| p8 | Huile d'Argan | زيت الأرغان | 🌰 | 249 MAD | 72 MAD | Beauty |

---

## 📱 Platforms (4)

| Platform | Color | Badge Style |
|----------|-------|-------------|
| 💬 WhatsApp | #25D366 | Green background |
| 📘 Facebook | #1877F2 | Blue background |
| 🎵 TikTok | #9333EA | Purple background |
| 🔍 Google | #FACC15 | Yellow background |

---

## 📊 Order Statuses (7)

| Status | English | Arabic | Color |
|--------|---------|--------|-------|
| 🟡 | Pending | قيد الانتظار | Yellow |
| 🔵 | Confirmed | مؤكد | Blue |
| 🟣 | Shipped | تم الشحن | Purple |
| 🟢 | Delivered | تم التسليم | Green |
| 🔴 | Cancelled | ملغي | Red |
| 🟠 | Returned | مرتجع | Orange |
| 🟠 | Refused | مرفوض | Orange |

---

## 📅 Date Filter Options

| Option | Description |
|--------|-------------|
| Today | Current day only |
| Yesterday | Previous day |
| Last 7 Days | Past week |
| Last 30 Days | Past month |
| This Month | From 1st of current month |
| Last Month | Previous month (full) |
| Custom | Custom date range picker |

**Affected Pages:** Dashboard, Orders, Top Products, Confirmation Team

---

## 🧮 Profit Formula

```
Profit = Revenue - Ad Spend - Product Cost - (5 MAD × Confirmed) - (10 MAD × Confirmed)
```

| Component | Description |
|-----------|-------------|
| Revenue | Sum of delivered orders |
| Ad Spend | Total advertising costs |
| Product Cost | Cost of goods sold |
| 5 MAD × Confirmed | Packaging (Lomblaj) fee |
| 10 MAD × Confirmed | Confirmation commission |

### Example Calculation

| Item | Amount |
|------|-------:|
| Revenue | 5,000 MAD |
| Ad Spend | -800 MAD |
| Product Cost | -1,500 MAD |
| Packaging (25 × 5) | -125 MAD |
| Commission (25 × 10) | -250 MAD |
| **Profit** | **2,325 MAD** |

---

## 📊 Pages Overview

### 1️⃣ Dashboard
- 6 KPI cards (Total Orders, Pending, Confirmed, Delivered, Cancelled, Revenue)
- Confirmation Rate & Delivery Rate progress bars
- Area Chart: Orders & Revenue trend (7 days)
- Pie Chart: Order status distribution
- Bar Chart: Orders by platform
- Recent Orders list
- **📅 Date filter** to select date range

### 2️⃣ Orders Page
- Search by name or order number
- Filter by status and platform
- **➕ Add Order button** with full modal form
- **✏️ Edit Order button** - modify any order details
- **⚡ Upsell & ➕ Cross-Sell Automation:**
  - **Upsell:** Triggered immediately when an agent increases an item's quantity above 1 (`Qte > 1`). Displays badge: `⚡ Upsell (Qte > 1)`.
  - **Cross-Sell:** Triggered when an agent adds an extra product to the order (`+Produit`). Displays badge: `➕ Cross-Sell (+Produit)`.
- **🏙️ Interactive City Selection & Strict Validation:** Fast, searchable ComboBox containing the full exhaustive list of **500+ Moroccan cities & communes**. Includes **strict real-time error validation** (`⚠️ خطأ: يجب اختيار مدينة صحيحة`) to prevent saving orders with unrecognized city names.
- Sortable table with 8 columns
- Inline status change dropdown
- Order details modal with:
  - Customer info
  - **📞 Call button** (opens phone dialer)
  - **💬 WhatsApp button** (opens WhatsApp chat)
  - Products list (multiple)
  - Notes
  - Edit button
- Pagination
- **📅 Date filter** to select date range
- **🔒 Confirmateurs see only their own orders**

### 3️⃣ Products Page
- 4 stat cards (Total, Inventory Value, Low Stock, Avg Margin)
- Product grid with emoji, prices, stock, margin
- Add/Edit product modal
- Profit margin progress bars

### 4️⃣ Top Products Performance
- Top 4 products cards with medals (🥇🥈🥉🏅)
- Filters: Search, Platform, Agent, Status
- Sortable table with **11 columns** (including Delivery Rate)
- **Delivery Rate** column with progress bar
- Dark gradient summary footer with 7 metrics
- **📅 Date filter** to select date range

### 5️⃣ Confirmation Team
- 7 KPI cards
- Best Performer banner (gold gradient)
- Agent Performance by Source table (13 columns)
- Platform Ads Performance table
- Orders by Product matrix
- Bar Chart: Confirmations by agent
- Radar Chart: Agent comparison
- **📅 Date filter** to select date range

### 6️⃣ Statistics & Charges Page (NEW)
- **6 KPI Cards:**
  - Total Revenue
  - Total Profit
  - Total Delivered
  - Total Confirmed
  - Total Costs
  - Average ROAS (%)
- **📢 Ad Charges Management (Manuel vs. Auto):**
  - **✍️ Manuel Input:** Agents/Admins can manually input custom Ad Spend amount (in MAD) and Lead count per Agent & Platform to recalculate profits in real-time.
  - **⚡ Auto Calculation:** Supports three automatic calculation rules:
    1. *Fixed Target CPL* (e.g., automatically spend = Leads × 15 MAD).
    2. *% of COD Revenue* (allocate a percentage of delivered sales as advertising costs).
    3. *Auto-Sync API Simulation* (live simulated synchronization with Meta Ads & TikTok Business).
- **Filters:**
  - 🔍 Search by product name
  - 📱 Filter by Platform (WhatsApp/Facebook/TikTok/Google)
  - 👤 Filter by Agent
- **Cost Breakdown** visual chart
- **Detailed Product Table** with 12 columns:
  - 🚚 Delivered
  - ✅ Confirmed
  - 💰 Revenue (CA)
  - 📦 Purchase Cost
  - 🚛 Delivery Cost (Casa=20 MAD, Others=30 MAD)
  - 📢 Advertising Cost
  - 📞 Confirmation Cost (**Delivered × 10 MAD**)
  - 🎁 Packaging Cost (Confirmed × 5 MAD)
  - 📈 Net Profit
  - 💵 Profit per Confirmed
  - 💶 Profit per Delivered
  - 🎯 ROAS (as **percentage %**)
- **Sortable columns**
- **Totals row** with dark gradient
- **Formula explanations**
- **📅 Date filter** support

### 7️⃣ Settings Page
- **General:** Company name, Currency
- **Language:** AR/EN toggle with flags
- **Delivery:** 
  - Default delivery fee
  - **City-specific fees:**
    - 🏙️ Casablanca: **20 MAD** (special reduced)
    - 🏘️ Rabat: 30 MAD
    - 🕌 Marrakech: 35 MAD
    - 🏛️ Fes: 35 MAD
    - ⛵ Tangier: 40 MAD
    - 🏖️ Agadir: 45 MAD
    - 🗺️ Other cities: 50 MAD
- **Notifications:** Email, Order alerts
- **Security:** Password, 2FA

---

## 🎨 Color Palette

### Primary Colors
| Usage | Tailwind | HEX |
|-------|----------|-----|
| Primary/Success | emerald-500 | #10B981 |
| Confirmed/Info | blue-500 | #3B82F6 |
| Delivered | green-500 | #22C55E |
| Pending/Warning | yellow-500 | #EAB308 |
| Cancelled/Error | red-500 | #EF4444 |
| Returned/Refused | orange-500 | #F97316 |
| Upsell | purple-500 | #8B5CF6 |
| Cross-Sell | pink-500 | #EC4899 |

### Gradients
```css
/* Sidebar */
bg-gradient-to-b from-emerald-900 via-emerald-800 to-emerald-900

/* Login Page */
bg-gradient-to-br from-emerald-900 via-emerald-800 to-teal-900

/* Logo */
bg-gradient-to-br from-amber-400 to-orange-500

/* Primary Button */
bg-gradient-to-r from-emerald-500 to-teal-500

/* Best Performer Banner */
bg-gradient-to-r from-amber-400 via-orange-400 to-amber-500
```

---

## 📱 Responsive Design

| Breakpoint | Width | Layout |
|------------|-------|--------|
| Mobile | < 768px | Single column, hamburger menu |
| Tablet | 768px - 1024px | 2-3 columns, collapsible sidebar |
| Desktop | > 1024px | 4-6 columns, fixed sidebar |

---

## 📦 Build Info

| Metric | Value |
|--------|-------|
| Bundle Size | ~771 KB |
| Gzip Size | ~218 KB |
| Build Time | ~5 seconds |
| Modules | 2,418 |

---

## ✅ Features Implemented

- [x] Arabic + English language support with RTL
- [x] Almarai Arabic font
- [x] 3 user roles with permissions
- [x] 7 date filter options
- [x] 4 advertising platforms (WhatsApp, Facebook, TikTok, Google)
- [x] 6 agents with full details
- [x] 8 products with Arabic names
- [x] 7 order statuses including refused
- [x] 200 seeded mock orders
- [x] 490 daily ad performance records
- [x] Profit formula for Moroccan COD
- [x] Responsive design (mobile/tablet/desktop)
- [x] Collapsible sidebar
- [x] Dark mode ready gradients
- [x] Custom scrollbars
- [x] Page transition animations

---

## 📄 License

MIT License - Free for commercial and personal use.

---

## 👨‍💻 Development

Built with ❤️ for the Moroccan e-commerce market.

**Currency:** MAD (الدرهم المغربي)  
**Default Language:** Arabic (العربية)  
**Direction:** RTL with LTR toggle
