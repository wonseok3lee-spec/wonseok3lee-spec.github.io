+++
title = "TaxVista"
description = "A Bloomberg Terminal for individual tax returns. Turning 1040s into multi-year financial stories."
date = 2026-04-17
categories = ["Project"]
tags = ["React", "Python", "Tax Tech", "Data Visualization"]
image = "cover.png"
weight = 1
+++

## A Bloomberg Terminal for individual tax returns

Most tax software is built for **filing**. TaxVista is built for **understanding.**

Individuals don't have financial statements the way companies do — but a 1040 contains the same underlying signals. TaxVista takes the numbers from your 1040 and turns them into a multi-year financial story: where your income comes from, how it's growing, and how efficiently you're retaining it after tax.

## What it does

- **Horizontal analysis** — multi-year trend comparison (income growth, after-tax retention, effective tax rate change)
- **Vertical analysis** — income composition and tax burden breakdown for any given year
- **Signal engine** — automated insights (growth phase detection, deduction efficiency, tax burden flags)
- **Privacy-first architecture** — no SSN, no names, no uploads; everything runs in the browser
- **Downloadable Financial Story Report** — shareable PDF summary

## Stack

- **Frontend:** React 19, Vite
- **Visualization:** Recharts
- **PDF processing:** PDF.js (pdfjs-dist)
- **Icons:** Lucide React
- **Analytics:** Vercel Analytics
- **Deploy:** Vercel
- **Built with:** AI-assisted development (Claude Code)

## Key idea

A 1040 isn't just a compliance document. It's a personal P&L. TaxVista makes that visible.

**[🔗 Try TaxVista →](https://taxvista.vercel.app/)**

**Status:** ✅ Live — upgrades in progress