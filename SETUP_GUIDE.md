# Farzan Supply Chain AI - Setup & Running Guide

## Project Fully Built ✓

Your Supply Chain AI application has been successfully built at:
```
a:\data analytics\projrctsss\algoo\supply-chain-ai
```

## Project Structure

All files have been created and organized:

```
supply-chain-ai/
├── src/
│   ├── app/
│   │   ├── layout.tsx              ← Root layout with NavBar
│   │   ├── page.tsx                ← Redirects to /upload
│   │   ├── upload/page.tsx         ← CSV upload UI
│   │   ├── dashboard/page.tsx      ← Charts + alerts + AI insights
│   │   ├── chat/page.tsx           ← AI chat interface
│   │   ├── globals.css             ← Tailwind CSS imports
│   │   └── api/
│   │       ├── upload/route.ts     ← Parses CSV, returns data
│   │       ├── analyze/route.ts    ← Computes metrics + forecasts
│   │       └── chat/route.ts       ← Proxies questions to Gemini
│   ├── components/
│   │   ├── NavBar.tsx
│   │   ├── AlertCard.tsx
│   │   ├── MetricCard.tsx
│   │   ├── SalesChart.tsx
│   │   └── InventoryChart.tsx
│   └── lib/
│       ├── types.ts                ← TypeScript interfaces
│       ├── parseCSV.ts             ← CSV parsing
│       ├── computeMetrics.ts       ← Analytics engine
│       ├── forecast.ts             ← Demand forecasting
│       └── gemini.ts               ← Gemini AI client
├── .env.local                      ← GEMINI_API_KEY (needs your key)
├── .eslintrc.json
├── .gitignore
├── next.config.js
├── tsconfig.json
├── tailwind.config.js
├── postcss.config.js
├── package.json
├── package-lock.json
├── node_modules/                   ← Already installed
└── README.md
```

## Before Running - Add Your Gemini API Key

1. **Get a free Gemini API key:**
   - Go to https://aistudio.google.com
   - Click "Get API Key"
   - Create a new API key
   - Copy the key

2. **Add the key to `.env.local`:**
   ```
   GEMINI_API_KEY=your_actual_key_here
   ```

3. The file is located at: `a:\data analytics\projrctsss\algoo\supply-chain-ai\.env.local`

## Running the Development Server

From PowerShell or Command Prompt:

```powershell
cd "a:\data analytics\projrctsss\algoo\supply-chain-ai"
npm run dev
```

Then open: http://localhost:3000

The app will automatically reload when you edit files.

## Available Commands

```bash
npm run dev      # Start development server (port 3000)
npm run build    # Create production build (already tested ✓)
npm start        # Start production server
npm run lint     # Run ESLint
```

## How to Use the Application

### 1. **Upload Page** (`/upload`)
   - Upload a CSV file with columns: `date, product, sales, inventory, supplier_delay`
   - Or download sample CSV from the button
   - The app parses and analyzes automatically

### 2. **Dashboard Page** (`/dashboard`)
   - View key metrics (total sales, products, avg delays)
   - See monthly sales trend chart
   - View inventory levels by product (color-coded by risk)
   - Read AI-generated insights
   - View active alerts
   - Browse detailed product breakdown table

### 3. **AI Chat Page** (`/chat`)
   - Ask questions about your supply chain
   - Get AI-powered answers with specific data
   - Multi-turn conversation support
   - Pre-built suggestions to get started

## Sample CSV Format

Download or create a CSV with this structure:

```csv
date,product,sales,inventory,supplier_delay
2024-01-01,Widget A,45,320,1
2024-01-01,Widget B,30,180,3
2024-01-01,Gadget X,22,95,8
2024-01-02,Widget A,52,268,1
2024-01-02,Widget B,28,152,4
2024-01-02,Gadget X,25,70,9
```

**Column requirements:**
- `date`: YYYY-MM-DD format
- `product`: Product name (string)
- `sales`: Units sold (number)
- `inventory`: Current inventory (number)
- `supplier_delay`: Delay in days (number)

## Build Status ✓

**Build completed successfully!**

Output from `npm run build`:
```
✓ Compiled successfully
+ Routes created:
  - / (redirects to /upload)
  - /upload (page)
  - /dashboard (page)
  - /chat (page)
  - /api/upload (route)
  - /api/analyze (route)
  - /api/chat (route)
```

## Technologies Used

- **Next.js 14** - React framework with App Router
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Recharts** - Data visualization
- **Google Generative AI** - AI insights
- **PapaParse** - CSV parsing
- **Lucide React** - Icons (installed but not used yet)

## What Each Part Does

### Frontend (Client Components)
- **Upload Page**: File drag-and-drop, CSV parsing progress
- **Dashboard**: Metrics cards, charts, alerts, product table
- **Chat**: Real-time AI conversation interface

### Backend (API Routes)
- **POST /api/upload**: Receives CSV → Returns parsed transactions
- **POST /api/analyze**: Computes metrics, generates AI insights
- **POST /api/chat**: Answers questions using Gemini with data context

### Data Flow
1. User uploads CSV → `/api/upload` parses it
2. Transactions sent to `/api/analyze` → Computes all metrics
3. Analysis stored in browser `sessionStorage`
4. Dashboard reads from `sessionStorage`, displays charts
5. Chat sends questions + context to `/api/chat` → Gemini responds

## Deployment to Vercel

When ready to deploy:

```bash
git init
git add .
git commit -m "initial commit: supply chain AI app"
gh repo create supply-chain-ai --public --push
```

Then:
1. Go to https://vercel.com
2. Import your GitHub repo
3. Add environment variable: `GEMINI_API_KEY=your_key`
4. Deploy (live in ~90 seconds)

## Troubleshooting

**Error: "Cannot find module 'papaparse'"**
- All packages were installed via `npm install`
- If this persists, run: `npm install` again

**Error: "GEMINI_API_KEY is undefined"**
- Make sure you added your key to `.env.local`
- Restart the dev server after adding the key

**Build fails with TypeScript errors**
- The build was already tested and passes ✓
- If you see errors after editing, run: `npm run build` to debug

**Port 3000 already in use**
- The dev server will auto-increment to 3001, 3002, etc.
- Or kill the process using port 3000 and restart

## Next Steps

1. ✓ Add your Gemini API key to `.env.local`
2. ✓ Run `npm run dev`
3. ✓ Navigate to http://localhost:3000
4. ✓ Download sample CSV or upload your own
5. ✓ Explore the dashboard and chat

**Your AI Supply Chain Intelligence System is ready to go! 🚀**
