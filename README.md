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

## License

MIT
