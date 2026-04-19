# 🔧 Workshop Parts Lookup — Arabic SAP DBM AI Tool

> Intelligent Arabic part name → SAP part number resolver, built for automotive workshop after-sales operations in the Gulf market.

[![Live Demo](https://img.shields.io/badge/Live_Demo-Try_It_Now-00d4a0?style=for-the-badge)](https://m441995.github.io/workshop-parts-lookup/)
[![Language](https://img.shields.io/badge/Language-Arabic_RTL-blue?style=for-the-badge)]()
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)]()
[![Status](https://img.shields.io/badge/Status-Month_1_Complete-orange?style=for-the-badge)]()

---

## 🔗 Live Demo

👉 **[https://m441995.github.io/workshop-parts-lookup/](https://m441995.github.io/workshop-parts-lookup/)**

Select a car model → type or paste Arabic part names → get SAP codes in under 2 seconds.

---

## The Problem

Workshop staff in Arabic-speaking markets enter part names inconsistently into SAP DBM:

| What they type | What they mean |
|---|---|
| فلتر زيت / فيلتر الزيت / oil filter | Same part — Oil Filter |
| كالبير / كلابة الفرامل / caliper | Same part — Brake Caliper |
| شمعات / شمعة اشعال / spark plug | Same part — Spark Plug |

**Root causes:**
- Hamza variations: أ إ آ ا — all treated as different characters
- Tashkeel (diacritics) included by some, skipped by others
- Dialect differences across 22 Arabic-speaking countries
- Mixed Arabic-English in the same SAP field
- No autocorrect for Arabic technical vocabulary

**Result:** Manual lookups take 10–15 minutes per request. Wrong part numbers cause procurement errors and customer delays.

---

## The Solution

A standalone browser-based tool that:

1. Takes **free Arabic text input** — typed or pasted, typos included
2. **Normalizes** the text: removes tashkeel, unifies hamza, handles spelling variants
3. **Fuzzy-matches** against a car model–specific SAP parts database
4. Returns the **correct SAP part code** in under 2 seconds
5. Outputs are **copy-ready** for direct paste into SAP or Excel

---

## Features

- 🚗 **6 car models** with model-specific OEM part numbers
  - Toyota Camry 2020 | Nissan Patrol 2018 | Hyundai Accent 2021
  - Honda Civic 2020 | Kia Sportage 2022 | Nissan Altima 2020
- 🔤 **Arabic NLP** — normalization, fuzzy matching, typo tolerance
- 📋 **Two Excel copy modes:**
  - Part codes only → paste into one Excel column
  - Description + code → paste into two Excel columns instantly
- ⚡ **Zero dependencies** — runs entirely in browser, no server, no API calls
- 🔒 **No data leaves the machine** — 100% local processing
- 🌐 **Full RTL Arabic interface** — designed for Arabic-first workflows

---

## Tech Stack

| Layer | Technology |
|---|---|
| Arabic normalization | Vanilla JS — hamza unify, tashkeel strip, ta marbuta normalize |
| Fuzzy matching | Custom bigram similarity scoring tuned for Arabic short terms |
| UI | HTML5 + CSS3 + JS — IBM Plex Arabic font — full RTL |
| Hosting | GitHub Pages (free, permanent) |
| Database | OEM part numbers per car model (JSON embedded) |
| Backend | None — zero server dependency |

---

## How It Works

```
User input (messy Arabic)
        ↓
Arabic Normalizer
  → strip tashkeel (حركات)
  → unify hamza (أ إ آ → ا)
  → normalize ta marbuta (ة → ه)
  → lowercase + trim
        ↓
Bigram Similarity Engine
  → compare against all keys in selected car's parts DB
  → score each candidate (0.0 → 1.0)
  → threshold: score > 0.35 to match
        ↓
SAP Part Code Resolved
  → return description + code
  → flag medium/low confidence matches
  → mark unrecognized parts clearly
        ↓
Copy-ready output
  → codes only (Excel single column)
  → description + code (Excel two columns)
```

---

## Project Roadmap

This is **Month 1** of a larger after-hours project building an AI-powered workshop reply generation system on SAP DBM historical data.

| Month | Deliverable | Status |
|---|---|---|
| Month 1 | Standalone Arabic parts lookup tool — browser-based | ✅ Complete |
| Month 2 | Local vector search (FAISS) + RAG pipeline on historical SAP data | 🔄 In progress |
| Month 3 | LLM reply generator (Ollama + Mistral) — full Arabic customer replies | 📅 Planned |
| Month 4 | Desktop app (Flask) with SQLite audit log + glossary editor | 📅 Planned |

**Tech stack for Month 2+:** Python · camel-tools · FAISS · sentence-transformers · Ollama · Flask · SQLite

---

## Why This Matters for the Gulf Market

The Arabic automotive aftermarket is a multi-billion dollar industry. Almost none of the operational tooling is built for Arabic-first data entry workflows.

Every fleet operator, workshop chain, and spare parts distributor in KSA, UAE, Kuwait, Qatar, and Egypt faces the same SAP Arabic data quality problem. This project is a proof of concept for a category of tooling that doesn't exist yet.

---

## Sample Inputs to Try

Open the demo and try typing these into the parts input box:

```
فلتر زيت
تيل فرامل امامي
شمعات اشعال
فيلتر الهواء
كالبير
مستشعر اكسجين
بطاريه
فلتر مكيف
```

Note: intentional typos like `بطاريه` (should be `بطارية`) are handled correctly.

---

## Author

**Mohamed — Brand Manager → Supply Chain Data Analyst**

- 🎓 MBA (Excellent) | Engineering Degree (Honours) | SAP SD Certified
- 🔧 Background: Supply chain · After-sales · Spare parts management · Brand management
- 🌍 Gulf market focus | Arabic NLP | AI Engineering
- 🏗️ Building: AI tools for Arabic supply chain and automotive operations

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077b5?style=flat-square&logo=linkedin)](https://linkedin.com/in/your-profile)
[![GitHub](https://img.shields.io/badge/GitHub-m441995-181717?style=flat-square&logo=github)](https://github.com/m441995)

---

## License

MIT — free to use, modify, and distribute. Attribution appreciated.

---

*Built after work. 2 hours a night. Free stack only.*
