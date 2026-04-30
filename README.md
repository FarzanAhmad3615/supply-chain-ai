# Farzan Supply Chain AI

An AI-powered supply chain intelligence system built with Next.js 14, Tailwind CSS, Recharts, and Google Generative AI.

## Getting Started

### Prerequisites
- Node.js 18+
- A Google Gemini API key (get one free at [aistudio.google.com](https://aistudio.google.com))

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/supply-chain-ai.git
cd supply-chain-ai
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables by creating `.env.local`:
```bash
GEMINI_API_KEY=your_gemini_api_key_here
```

4. Run the development server:
```bash
npm run dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Features

- **CSV Upload**: Upload supply chain data with sales, inventory, and supplier delay information
- **Real-time Analytics**: Automatic computation of metrics, trends, and risk assessments
- **AI Insights**: AI-powered analysis and recommendations using Google Gemini
- **Interactive Dashboards**: Visualize trends with charts and monitor product-level metrics
- **AI Chat**: Ask questions about your supply chain data and get intelligent responses
- **Risk Management**: Automatic detection of stockout and supplier delay risks

## Project Structure

```
src/
├── app/
│   ├── layout.tsx              # Root layout with navbar
│   ├── page.tsx                # Home page redirect
│   ├── upload/page.tsx         # CSV upload page
│   ├── dashboard/page.tsx      # Analytics dashboard
│   ├── chat/page.tsx           # AI chat interface
│   └── api/
│       ├── upload/route.ts     # CSV parsing endpoint
│       ├── analyze/route.ts    # Analytics computation endpoint
│       └── chat/route.ts       # AI chat endpoint
├── components/
│   ├── NavBar.tsx
│   ├── MetricCard.tsx
│   ├── AlertCard.tsx
│   ├── SalesChart.tsx
│   └── InventoryChart.tsx
└── lib/
    ├── types.ts                # TypeScript interfaces
    ├── parseCSV.ts             # CSV parsing utilities
    ├── computeMetrics.ts       # Analytics engine
    ├── forecast.ts             # Demand forecasting
    └── gemini.ts               # AI client and prompts
```

## CSV Format

Your CSV should have the following columns:
- `date` - Date in YYYY-MM-DD format
- `product` - Product name
- `sales` - Number of units sold
- `inventory` - Current inventory level
- `supplier_delay` - Average supplier delay in days

Example:
```csv
date,product,sales,inventory,supplier_delay
2024-01-01,Widget A,45,320,1
2024-01-01,Widget B,30,180,3
```

## Deployment

### Deploy to Vercel

1. Push your code to GitHub
2. Go to [vercel.com](https://vercel.com) and sign in with GitHub
3. Click "New Project" and select your repository
4. Add environment variable: `GEMINI_API_KEY`
5. Click Deploy

Your app will be live in ~90 seconds!

## Technologies Used

- **Next.js 14** - React framework with App Router
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first CSS
- **Recharts** - Data visualization
- **Google Generative AI** - AI insights and chat
- **PapaParse** - CSV parsing

<img width="1585" height="879" alt="Screenshot 2026-04-12 122058" src="https://github.com/user-attachments/assets/f8cff329-894a-410f-b38f-ad90ee3a1fbd" />
<img width="1572" height="639" alt="Screenshot 2026-04-12 122216" src="https://github.com/user-attachments/assets/a4c82e26-8cc2-4d2b-8cec-a67db51d289b" />
<img width="1615" height="661" alt="Screenshot 2026-04-12 122228" src="https://github.com/user-attachments/assets/40084398-a773-4ce3-ba5b-c5e691898a42" />
<img width="1484" height="756" alt="Screenshot 2026-04-12 122238" src="https://github.com/user-attachments/assets/5550d44a-193b-4977-8641-bb223182296f" />
<img width="1852" height="655" alt="Screenshot 2026-04-12 122247" src="https://github.com/user-attachments/assets/4e2320fa-1880-47a2-bd3f-59589b47dc52" />
<img width="1510" height="626" alt="Screenshot 2026-04-12 122259" src="https://github.com/user-attachments/assets/6ee48952-362e-48b9-b1fb-8f04561cce55" />
<img width="1614" height="722" alt="Screenshot 2026-04-12 122309" src="https://github.com/user-attachments/assets/48211a58-dffa-4946-81b8-98f21a00d868" />
<img width="1560" height="852" alt="Screenshot 2026-04-12 122438" src="https://github.com/user-attachments/assets/0ab9a2c7-7cc9-4b9a-91e7-0d01229e1043" />


