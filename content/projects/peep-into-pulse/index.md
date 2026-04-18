+++
title = "Peep Into Pulse"
description = "A market-pulse dashboard for watching what moves stocks. Built around a 2×2 news classification matrix."
date = 2026-04-16
categories = ["Project"]
tags = ["React", "Python", "FastAPI", "OpenAI", "Fintech"]
image = "cover.png"
weight = 2
+++

## A market-pulse dashboard for watching what moves stocks

A personal watchlist + intelligence dashboard that tracks not just prices, but the **signals behind the moves** — earnings surprises, executive changes, layoffs, regulatory shifts, geopolitical risk.

Built around a simple but useful framework: news is classified across two axes — **Internal vs. External** and **Domestic vs. International** — so you can see at a glance *why* a ticker is moving, not just *that* it is.

## What it does

- Multi-ticker comparison with normalized % return tracking
- 4-quadrant news matrix (Internal/External × Domestic/International)
- Real-time price tracking with severity tags (Surprise / High / Medium)
- Per-ticker alerts and watchlist management

## Architecture highlight

A background scheduler runs every 5 minutes: `fetch_all → tag_all → store`. The frontend reads pre-computed snapshots, so every request is instant — no LLM call on the request path. This decouples cost from user traffic and keeps latency low.

## Stack

**Frontend:** React 19, Vite, Tailwind CSS, Recharts

**Backend:** FastAPI (Python), APScheduler, httpx

**Intelligence:** OpenAI GPT-4o-mini for news classification, batched inference for cost efficiency

**Core modules:**
- `news_fetcher.py` — multi-source news ingestion
- `tagger.py` — GPT-4o-mini classification engine with batched processing
- `main.py` — FastAPI server + scheduler orchestration

**Built with:** AI-assisted development (Claude Code)

## Key idea

Most stock dashboards show *what* happened. Peep Into Pulse tries to show *why*.

**Status:** 🔄 Local prototype — deployment in progress