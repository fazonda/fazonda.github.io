# ONDA — Project Context

Context for working on this repo in Claude Code. Read this first.

## What ONDA is
An **AI-powered program that prepares university students in São Paulo for their first job** —
their first estágio or trainee. The AI is the *engine* (scalable, personalized practice),
not the product. The product is structure + practice + accountability + outcomes.

**Decided against:** a "study companion" for coursework (microaulas, provas, semester planning).
That market is crowded and hard to monetize. We are NOT that. Don't reintroduce that framing.

**Core promise:** "A faculdade te forma. A ONDA te prepara para conquistar a vaga."

## Strategy (the why — so we don't drift)
- A landing page / chatbot wrapper has no moat. The defensible assets are:
  proprietary process data (what specific SP companies' selection processes actually test),
  the employer/demand side, distribution (WhatsApp + university partnerships), and
  measured completion + placement outcomes.
- Sequencing: nail the student side first (this program). Scale becomes the magnet that
  later attracts employers (the two-sided marketplace).
- **Never publish fake outcome stats** (e.g. "73% aprovados") pre-launch. All claims on the
  site must be promises we can keep on day one. Stats are offer-based, not results-based.

## Audience
University students in São Paulo chasing a first estágio/trainee. Personas in use:
Administração (FGV), Engenharia (Poli USP), Letras (USP). Pains: never get callbacks,
freeze in interviews, don't know how to position themselves.

## The product (proposed — confirm against real curriculum)
Four trilhas / modules, ~6 weeks total:
1. Currículo & LinkedIn — pass ATS filters (Gupy etc.) — 1 wk
2. Testes online — lógica, português, inglês, Excel — 2 wks
3. Entrevista & Dinâmica — STAR, entrevista gravada, dinâmica de grupo — 2 wks
4. Cases & Painel — business reasoning for consultoria, trainee, bancos — 1 wk

## This repo = the landing page
- Static site, **no build step**. Plain `index.html` + `assets/`. Hosted on GitHub Pages
  (Deploy from branch → `main` → root).
- All copy is **pt-BR**. Keep relative asset paths (e.g. `assets/onda-mark.png`) so they
  resolve on `user.github.io/<repo>/`.
- Sections (in order): hero → trilhas (#trilhas) → como funciona (#como) → depoimentos → CTA → footer.

## Design system (don't replace without reason)
- Fonts: `DM Serif Display` (display/headings, italic for emphasis) + `DM Sans` (body).
- Colors (CSS vars in `index.html`): `--black #0a0a0a`, `--white #fafafa`, `--blue #1a6cff`,
  grays. Editorial black/white/blue, thin hairline borders, generous whitespace, grid layouts.
- Logo: concentric offset rings reading as a ripple (onda = wave). `assets/onda-mark.png`
  is the circular badge used in nav/footer/favicon.
- Aesthetic intent: refined, minimal, editorial. Not generic SaaS.

## Open TODOs
- [ ] Wire the waitlist form to a real backend (Formspree or Tally). Right now it only shows
      a ✓ and stores nothing.
- [ ] Replace placeholders: the "247 na lista" count and `contato@ondaeducacao.com.br`.
- [ ] After deploy, set absolute URLs in the Open Graph tags (`og:image`) so link previews work.
