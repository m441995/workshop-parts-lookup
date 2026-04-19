# 🔧 Workshop Parts Lookup — Arabic SAP DBM AI Tool

> Intelligent Arabic part name → SAP part number resolver, built for automotive workshop after-sales operations in the Gulf market.

[![Demo](https://img.shields.io/badge/Live_Demo-Click_Here-00d4a0?style=flat-square)](https://yourusername.github.io/workshop-parts-lookup)
[![Language](https://img.shields.io/badge/Language-Arabic_RTL-blue?style=flat-square)]()
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)]()

---

## The Problem

Workshop staff in Arabic-speaking markets enter part names inconsistently into SAP DBM:
- **Spelling variants**: فلتر زيت / فيلتر الزيت / filtar zeit
- **Dialect differences**: كالبير / كلابة الفرامل / مشبك
- **Mixed scripts**: Oil filter + Arabic text in the same field
- **Typos**: missing letters, wrong hamza, no tashkeel

Result: manual lookups take 10–15 minutes per request. Wrong part numbers cause procurement errors and customer delays.

## The Solution

A standalone browser-based tool that:
1. Takes free Arabic text input (typed or pasted)
2. Normalizes spelling: removes tashkeel, unifies hamza, handles typos
3. Fuzzy-matches against a car model–specific SAP parts database
4. Returns the correct SAP part code in under 2 seconds
5. Outputs are copy-ready for direct paste into SAP or Excel

## Features

- 🚗 **6 car models** with model-specific OEM part numbers (Toyota, Nissan, Hyundai, Honda, Kia)
- 🔤 **Arabic NLP** — normalization, fuzzy matching, typo tolerance
- 📋 **Excel-ready copy** — one-click copy of codes only (single column) or description + code (two columns)
- ⚡ **Zero dependencies** — runs entirely in browser, no server, no API calls
- 🌐 **RTL Arabic interface** — designed for Arabic-first workflows

## Tech Stack

| Layer | Technology |
|---|---|
| Arabic normalization | Vanilla JS (hamza unify, tashkeel strip, bigram similarity) |
| Fuzzy matching | Custom similarity scoring |
| UI | HTML + CSS + JS, IBM Plex Arabic font |
| Hosting | GitHub Pages (free) |
| Data | OEM part number database (JSON) |

## Project Context

Built as a portfolio piece targeting the **Gulf automotive aftermarket** and **SAP supply chain** space. This is Month 1 of a larger project:

- **Month 1 (current)**: Standalone part lookup tool — browser-based, zero backend
- **Month 2**: Local AI reply generator using RAG + Ollama + FAISS
- **Month 3**: Full desktop app with SQLite storage and audit log

## Live Demo

👉 **[Try it here](https://yourusername.github.io/workshop-parts-lookup)**

Select a car model → type or paste Arabic part names → get SAP codes in seconds.

---

## Author

**Mohamed [Your Last Name]**
Brand Manager → Supply Chain Data Analyst | SAP SD Certified | MBA
Gulf market focus | Arabic NLP | AI Engineering

[LinkedIn](https://linkedin.com/in/yourprofile) · [Email](mailto:your@email.com)
