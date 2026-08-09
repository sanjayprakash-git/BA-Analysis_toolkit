# BA Analysis Toolkit

An AI-powered Business Analysis tool that runs any business idea or problem through standard BA frameworks using live web research and an LLM. Produces consulting-grade structured output (McKinsey/Bain/BCG style) with real citations, tables, and exportable reports — no signup required.

**Live:** https://sanjayprakash-git.github.io/BA-Analysis_toolkit/

---

## What It Does

Paste a business idea or problem. Select a framework. Get a structured analysis backed by live web research in seconds.

7 built-in frameworks:

| Framework | Output |
|-----------|--------|
| Market Sizing | TAM/SAM/SOM with calculated tables |
| Competitor Landscape | Gaps, positioning, funding benchmarks |
| SWOT | 4-quadrant colour grid |
| Porter's Five Forces | Industry forces analysis |
| PESTLE | Macro environment breakdown |
| Stakeholder Analysis | Power/interest mapping |
| Requirements | Functional + non-functional specs |

Plus:
- **Executive Summary** — synthesises all 7 frameworks in one pass
- **Run Full Analysis** — runs all frameworks sequentially
- **Custom Framework** — type any framework name (e.g. "BCG Growth Matrix")
- **Comparison Mode** — side-by-side analysis of two businesses
- **Go Deeper** — challenges assumptions and cites specific sources
- **PDF Export** — branded cover page + full report
- Context filters — Industry, Region, Company Stage

---

## How It Works

```
User Input → GitHub Pages frontend → Vercel proxy → Tavily (live web research) → Groq LLM → Structured output
```

- **Tavily API** — live web search for real data and citations
- **Groq (llama-3.3-70b-versatile)** — structured analysis generation
- **Vercel serverless** — proxy that holds API keys securely

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | Vanilla HTML/CSS/JS (single file, no framework) |
| LLM | Groq API — llama-3.3-70b-versatile |
| Web Research | Tavily API |
| Backend | Vercel serverless function (Node.js proxy) |
| PDF Export | html2pdf.js |
| Hosting | GitHub Pages |

---

## Running Locally

The live version works instantly with no setup:
**https://sanjayprakash-git.github.io/BA-Analysis_toolkit/**

To run locally with your own API keys:

1. Clone the repo
```bash
git clone https://github.com/sanjayprakash-git/BA-Analysis_toolkit
```

2. Deploy your own Vercel proxy with:
```env
GROQ_API_KEY=your_groq_key
TAVILY_API_KEY=your_tavily_key
```

3. Update the API endpoint in `index.html` to point to your proxy

4. Open `index.html` in a browser

---

## Built By

[Sanjay Prakash Ravi](https://sanjayprakash-git.github.io/portfolio/) — MSc Business Analytics, Dublin Business School
