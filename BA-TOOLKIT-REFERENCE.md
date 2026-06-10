# BA Analysis Toolkit - Project Reference

## Live URLs
- GitHub Pages (live): https://sanjayprakash-git.github.io/BA-Analysis_toolkit/index.html
- GitHub Repo: https://github.com/sanjayprakash-git/BA-Analysis_toolkit
- Proxy API: https://portfolio-proxy-two.vercel.app/api/ba

## Local Files
- Toolkit source: /Users/rsp/Desktop/tool/index.html
- Proxy source: /Users/rsp/portfolio-proxy/api/ba.js
- Old version: /Users/rsp/ba-toolkit/index.html

## Architecture
- Single HTML file (no framework)
- Backend: Vercel serverless proxy
- Data flow: Tavily (web search) → Groq (LLM analysis) → Frontend
- Tavily API key stored in Vercel env vars (TAVILY_API_KEY)
- Groq API key stored in Vercel env vars (GROQ_API_KEY)
- Model: llama-3.3-70b-versatile on Groq
- Tavily free tier: 1,000 searches/month

## Features
- 7 BA frameworks: Market Sizing, Competitor, SWOT, Porter's Five Forces, PESTLE, Stakeholder, Requirements
- Executive Summary (synthesises all 7)
- Live web research via Tavily (real sources, real citations)
- Custom framework input (any framework name)
- Comparison mode (side-by-side two businesses)
- TAM concentric circles visual
- SWOT 4-quadrant colour grid
- PDF export with branded cover page (html2pdf.js)
- Copy all as markdown
- Email share
- Save/load sessions (localStorage)
- History tab
- Go Deeper button (challenges assumptions, cites specific sources)
- Consulting-grade prompts (McKinsey/Bain/BCG style, table-first, no filler)

## Theme
- GitHub-inspired dark theme (--bg:#0d1117)
- Inter font
- Blue/purple accent gradient
- Cards with hover glow + shadows
- Gradient Run Full Analysis button
- Smooth tab transitions

## Rate Limits
- Groq free tier: 12,000 TPM (tokens per minute)
- Tavily free tier: 1,000 API calls/month (~125 full analysis runs)
- 2-second delay between sequential calls in Run All

## Competitors Researched
- app.businessmodelanalyst.com (paid SaaS, SWOT/BMC/PESTLE)
- swotanalysis.com (SWOT only, team collab)
- Jeda.ai (enterprise, 300+ frameworks, expensive)
- Junia.ai (free single SWOT generator)
- Miro AI SWOT (whiteboard-first)
- CompetitiveAnalysisGPT (GitHub CLI tool)

## Unique Differentiators
1. All 7 frameworks + synthesis in one page
2. Zero signup, instant use
3. Live web-grounded data with real citations
4. Portfolio demonstration piece
5. Comparison mode (nobody else has this)
6. Custom framework flexibility

## Session Notes
- Perplexity API considered but user couldn't access (Airtel claim pending)
- Switched to Tavily+Groq hybrid (free, works in Ireland/EU)
- Gemini free tier blocked in EU (paid only for EEA)
- Proxy deployed on Vercel (sanjay-rsp-projects/portfolio-proxy)
- npm cache was corrupted (fixed with sudo rm -rf ~/.npm/_cacache)
- GitHub Pages enabled on main branch / root
