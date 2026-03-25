<div align="center">
  <img
    src="./public/banner.png"
    alt="Horizon Banking App Banner"
  />
  <br />

  <div>
    <img src="https://img.shields.io/badge/Next.js_14-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js" />
    <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
    <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
    <img src="https://img.shields.io/badge/Appwrite-FD366E?style=for-the-badge&logo=appwrite&logoColor=white" alt="Appwrite" />
    <img src="https://img.shields.io/badge/Plaid-111827?style=for-the-badge&logo=plaid&logoColor=white" alt="Plaid" />
    <img src="https://img.shields.io/badge/Dwolla-FF6B35?style=for-the-badge&logoColor=white" alt="Dwolla" />
  </div>

  <h3 align="center">A modern fintech web app for linking bank accounts, tracking transactions, and moving money securely.</h3>
</div>

---

## 📖 Overview

**Horizon Banking App** is a comprehensive, full-stack financial SaaS platform built with **Next.js 14**, **TypeScript**, and **Tailwind CSS**. It enables users to authenticate securely, connect multiple bank accounts through **Plaid Sandbox**, view real-time balances and transaction history, and seamlessly transfer funds between linked accounts using **Dwolla**.

Designed with scalable architecture and a polished user experience, this project serves as a robust foundation for learning how to build and integrate real-world financial dashboards.

---

## 🚀 Demo

![Horizon Banking Demo](./public/demo-banking.gif)

---

## ✨ Key Features

- 🔐 **Secure Authentication**: User registration, login, and session management powered by Appwrite with protected routing.
- 🏦 **Bank Account Linking**: Seamless integration with Plaid Link (Sandbox) to connect and sync external bank accounts.
- 📊 **Account Insights**: A dynamic dashboard displaying connected accounts, total balances, and contextual overviews.
- 📜 **Transaction History**: Paginated, detailed transaction logs combining Plaid data with internal transfer records.
- 💸 **Money Transfers**: Secure, ACH-style fund transfers between linked accounts using the Dwolla API.
- 📱 **Modern UI/UX**: Fully responsive, dashboard-first design built with reusable React components and Tailwind CSS.
- 🛡️ **Error Monitoring**: Real-time error tracking and observability integrated via Sentry.

---

## 🛠️ Tech Stack

**Frontend**

- **Framework:** Next.js 14 (App Router)
- **Language:** TypeScript
- **UI Library:** React 18, Tailwind CSS, Shadcn UI _(if applicable)_

**Backend & Services**

- **BaaS:** Appwrite (Database, Auth)
- **Banking API:** Plaid
- **Payment Gateway:** Dwolla
- **Monitoring:** Sentry

---

## 📂 Project Structure

```text
horizon-banking-app/
├── app/
│   ├── (auth)/          # Authentication routes (sign-in, sign-up)
│   └── (root)/          # Main app routes (dashboard, accounts, transfers)
├── components/          # Reusable UI components & layouts
├── lib/
│   ├── actions/         # Server actions (user, bank, transfer logic)
│   ├── appwrite.ts      # Appwrite client configuration
│   └── plaid.ts         # Plaid client setup
├── constants/           # Static data, navigation links, and configs
├── types/               # TypeScript type definitions
└── public/              # Static assets (images, icons)
```

---

## 🔐 Environment Variables

Create a `.env.local` file in the project root and add the following values:

```env
# Appwrite
NEXT_PUBLIC_APPWRITE_ENDPOINT=
NEXT_PUBLIC_APPWRITE_PROJECT=
NEXT_APPWRITE_KEY=
APPWRITE_DATABASE_ID=
APPWRITE_USER_COLLECTION_ID=
APPWRITE_BANK_COLLECTION_ID=
APPWRITE_TRANSACTION_COLLECTION_ID=

# Plaid
PLAID_CLIENT_ID=
PLAID_SECRET=

# Dwolla
DWOLLA_ENV=sandbox
DWOLLA_KEY=
DWOLLA_SECRET=
```

---

## ⚡ Getting Started

1. Install dependencies

```bash
npm install
```

2. Add environment variables

Create `.env.local` in the project root and paste the variables from the section above.

3. Run the development server

```bash
npm run dev
```

4. Open the app

```text
http://localhost:3000
```

---

## 📜 Available Scripts

- `npm run dev` - Start local development server
- `npm run build` - Create production build
- `npm run start` - Start production server
- `npm run lint` - Run lint checks
