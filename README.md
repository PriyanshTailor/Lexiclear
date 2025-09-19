# ⚖️ LexiClear

> **AI-Powered Legal Document Assistant**  
> Upload contracts or legal docs → get plain-language summaries, risk flags, clause comparisons, and conversational Q&A.

---

## ✨ Features

- 📄 **Document Upload** — Supports PDF, text, and image-based files
- 📝 **Plain-Language Summaries** — Understand complex legal terms instantly
- ⚠️ **Risky Clause Detection** — Highlight suspicious clauses
- 💬 **AI Q&A Chat** — Ask document-related questions conversationally
- 📑 **Document Comparison** — Compare clauses side-by-side
- 🌐 **Language Toggle** — Switch between English ↔ Hindi
- ⚡ **Mock AI Logic Included** — Easily replace with your own AI backend

---

## 🧠 Tech Stack

- **Framework:** :contentReference[oaicite:1]{index=1} (App Router) + :contentReference[oaicite:2]{index=2}  
- **Styling:** :contentReference[oaicite:3]{index=3} + :contentReference[oaicite:4]{index=4} primitives  
- **Icons:** :contentReference[oaicite:5]{index=5}  
- **Fonts:** :contentReference[oaicite:6]{index=6}  
- **Analytics (optional):** :contentReference[oaicite:7]{index=7}  
- **Runtime:** :contentReference[oaicite:8]{index=8} 18+ / 20+

---

## 📁 Project Structure
```bash
/ (repo root)
├─ app/ # App Router pages + layouts
│ ├─ page.tsx # Main UI (tabs: upload, summary, chat, compare)
│ └─ layout.tsx # Global layout + fonts + metadata
├─ components/
│ ├─ ui/ # Reusable UI primitives (button, card, modal, etc.)
│ ├─ document-upload.tsx
│ ├─ document-summary.tsx
│ ├─ chat-interface.tsx
│ └─ document-comparison.tsx
├─ lib/ # Utility functions (dropzone, translation helpers)
├─ scripts/ # Helper scripts (create sample docs)
├─ public/ # Static assets
├─ styles/ or app/globals.css
├─ package.json
└─ README.md


yaml
Copy code
```
---

## 🚀 Quick Start

**Prerequisites:** :contentReference[oaicite:9]{index=9} 18+ and npm / pnpm / yarn

```bash
# 1. Clone the repo
git clone <repo-url>
cd <repo-folder>

# 2. Install dependencies
npm install
# or: pnpm install / yarn install

# 3. Run in development
npm run dev
# → open http://localhost:3000

# 4. Build for production
npm run build
npm start
```

## 💡 The app ships with mock/sample data and logic.
Upload your own files from the UI or edit scripts/create-sample-documents.js to add test documents.

## ⚙️ How It Works
Upload: components/document-upload.tsx handles file selection + mock processing.

Summaries & Risk Flags: components/document-summary.tsx shows mock AI output.

Chat Interface: components/chat-interface.tsx gives conversational Q&A on doc context.

Compare: components/document-comparison.tsx aligns similar clauses from two docs.

Translation: lib/translate.ts toggles English ↔ Hindi content.

## 🧩 Replacing Mock Logic with Real AI
Want production-ready behavior? Swap mocks for your real backend:

Integrate OpenAI, Anthropic, or other LLM APIs in the summary/chat modules.

Add a Pinecone / Weaviate vector store for document retrieval.

Store and process uploaded files via an API route (/api/upload).

Secure API keys using .env.local.

## 🧪 Scripts & Utilities
scripts/create-sample-documents.js → creates sample contracts for UI testing

lib/dropzone.ts → drag & drop helper

lib/translate.ts → basic translation stub

## 🎨 UI & Design
Responsive layout built with Tailwind CSS

Modular reusable UI components in components/ui/

Icons from lucide-react

Clean typography with Geist font

## 🛠 Troubleshooting
Make sure Node 18+ is installed.

If npm run dev fails, delete node_modules and reinstall.

Ensure you are using the App Router (app/ directory), not the older pages/ one.

## 🤝 Contributing
Pull requests are welcome!
Please open an issue to discuss major changes before submitting.

## 📜 License
This project is licensed under the MIT License — feel free to use, modify, and shar
