<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=260&color=0:0d1117,40:1e1b4b,100:4f46e5&text=Digvijay%20Kumar%20Singh&fontSize=44&fontColor=ffffff&fontAlignY=38&animation=fadeIn&desc=Full%20Stack%20Engineer%20%E2%80%A2%20AI-Integrated%20Systems%20%E2%80%A2%204%20Products%20Shipped%20Solo&descAlignY=58&descSize=16" />
</p>

<p align="center">
  <img width="64" height="64" alt="digvijay-logo-512" src="https://github.com/user-attachments/assets/5539f298-9f2f-48d2-bf16-3f734fcf7a71"  style="border-radius:50%;border:3px solid #4f46e5;"/>
</p>

<p align="center">
 <img src="https://readme-typing-svg.demolab.com?font=Inter&weight=600&size=17&duration=3200&pause=1000&color=58A6FF&center=true&vCenter=true&width=820&lines=4+production+SaaS+platforms+%E2%80%94+solo%2C+end-to-end%2C+all+live;TypeScript+%C2%B7+PostgreSQL%2FSupabase+%C2%B7+MongoDB+%C2%B7+Next.js%2FReact+19;Multi-provider+AI+%C2%B7+Real-time+systems+%C2%B7+Browser+automation;Open+to+Junior+Full-Stack+Roles+%26+Remote+Freelance" alt="Typing SVG" />
</p>

<p align="center">
  <a href="https://github.com/chauhandigvijay1"><img src="https://img.shields.io/badge/GitHub-chauhandigvijay1-181717?style=flat-square&logo=github&logoColor=white" /></a>
  <a href="https://www.linkedin.com/in/digvijaykumarsingh"><img src="https://img.shields.io/badge/LinkedIn-digvijaykumarsingh-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:chauhandigvijay669@gmail.com"><img src="https://img.shields.io/badge/Email-chauhandigvijay669%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white" /></a>
  <a href="https://dsc-portfolio-website.netlify.app"><img src="https://img.shields.io/badge/Portfolio-Live-00C896?style=flat-square&logo=netlify&logoColor=white" /></a>
</p>

<p align="center"><sub>📍 Greater Noida, India &nbsp;·&nbsp; 🕐 IST (UTC+5:30) &nbsp;·&nbsp; 🌍 Remote-ready &nbsp;·&nbsp; 🎓 MCA, graduate 2026</sub></p>

<br/>

## About

I ship complete products, not feature fragments. Four SaaS platforms, built solo end-to-end — schema design, API, frontend, deployment, and the boring-but-critical parts most portfolios skip: auth revocation, payment signature verification, row-level multi-tenant isolation, and browser automation that survives a site redesign instead of breaking on it.

Each project solved a genuinely different hard problem: **real-time consistency** at scale (DsSync Hub), **AI provider resilience** when a single vendor can't be trusted to stay up (Valtrexa V2), **token-streaming UX** over standard HTTP (DevFlow AI), and **structured extraction that degrades gracefully** across 50+ unstructured websites (JobPilot). I'd rather talk about *why* I made a tradeoff than list what I used — see the [Engineering Decisions](#-engineering-decisions) table below.

Graduating MCA in 2026. Actively looking for **junior full-stack roles** and **remote freelance work**.

---

## 🎯 Currently

- Extending **Valtrexa V2** with additional AI pipeline phases and an interview-prep module
- Studying **system design** and distributed-architecture patterns
- Sharpening **DSA in C++** for technical interviews
- Open to **junior full-stack / frontend roles** — India + international remote
- Available for **freelance work**: AI integrations, SaaS MVPs, MERN/Next.js builds

---

## 🚀 Featured Projects

<table>
<tr>
<td valign="top" width="50%">

### 🧠 [Valtrexa V2](https://valtrexa-v2.vercel.app/) — AI Career Automation OS

Not a tracker — an operator. An 8-phase pipeline that actually **applies to jobs** via Playwright (3-tier self-healing selectors: exact CSS → fallback chain → fuzzy/ARIA matching) across 9 job sources, and runs AI-personalized recruiter outreach through Gmail with a day-3/7/14 follow-up cadence.

AI runs on a **3-provider fallback chain** (Gemini → Groq → OpenRouter) — a single vendor outage never stops the pipeline. Every one of 70 Supabase tables enforces Row-Level Security, and 145+ write paths were manually audited for user-scope leaks: zero found. Full remote control via a 32-command Telegram bot, plus an n8n webhook event bus for external automation.

<sub>**83+** API endpoints · **70** tables / **28** migrations · **9** job sources · **32** Telegram commands · **3**-provider AI fallback</sub>

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React 19](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Redis](https://img.shields.io/badge/BullMQ_%2F_Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![TanStack](https://img.shields.io/badge/TanStack_Start-FF4154?style=flat-square)

[![Live](https://img.shields.io/badge/Live-Demo-00C896?style=flat-square)](https://valtrexa-v2.vercel.app/)
[![Source](https://img.shields.io/badge/Source-Code-181717?style=flat-square&logo=github)](https://github.com/chauhandigvijay1/Valtrexa-V2)

</td>
<td valign="top" width="50%">

### 💬 [DsSync Hub](https://dssync-hub-client.vercel.app) — Multi-Tenant Team Collaboration SaaS

Tasks, notes, real-time chat, video (Jitsi), AI, and billing unified into one workspace — so a team stops paying for five overlapping tools. The hard problem was keeping Socket.io broadcasts from racing REST writes. Fixed with one strict rule: **clients never emit state changes over the socket** — only REST calls do — the server writes to MongoDB first, then broadcasts, so the database is always the source of truth.

Multi-tenancy enforced through a `Membership` join table across 4 RBAC roles (owner/admin/member/viewer) over 17 data models. JWT sessions with Google OAuth, Helmet + rate limiting + input sanitization at the edge, and 92 backend tests via `mongodb-memory-server`.

<sub>**17** data models · **4** RBAC roles · REST-writes-then-broadcast (race-safe) · **92** backend tests</sub>

![React 19](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Node/Express](https://img.shields.io/badge/Express_5-000000?style=flat-square&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socket.io)
![Razorpay](https://img.shields.io/badge/Razorpay-02042B?style=flat-square)

[![Live](https://img.shields.io/badge/Live-Demo-00C896?style=flat-square)](https://dssync-hub-client.vercel.app)
[![Source](https://img.shields.io/badge/Source-Code-181717?style=flat-square&logo=github)](https://github.com/chauhandigvijay1)

</td>
</tr>
<tr>
<td valign="top" width="50%">

### 📋 [JobPilot AI](https://jobpilot-client-chi.vercel.app) — Job Application Tracker + Chrome Extension

A Chrome MV3 extension that ingests job postings from 50+ boards through a **3-tier extraction cascade** — JSON-LD Schema.org first, Microdata second, prioritized DOM selectors last — so one site's UI redesign can't silently break ingestion. Groq Llama 3 powers 8 AI actions: ATS scoring, cover letters, interview prep, skill-gap analysis, and more.

Auth is dual-JWT (15-min access + 30-day refresh) with a `tokenVersion` integer for instant global session revocation — no Redis blocklist required. ~25K LOC backed by 162 tests across 19 suites (Vitest, RTL, Playwright).

<sub>**8** AI actions · **50+** job boards · dual JWT + tokenVersion revocation · **162** tests / 19 suites</sub>

![Next.js 14](https://img.shields.io/badge/Next.js_14-000000?style=flat-square&logo=next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Express 5](https://img.shields.io/badge/Express_5-000000?style=flat-square&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Groq](https://img.shields.io/badge/Groq_API-F5A623?style=flat-square)
![Chrome MV3](https://img.shields.io/badge/Chrome_MV3-4285F4?style=flat-square&logo=googlechrome&logoColor=white)

[![Live](https://img.shields.io/badge/Live-Demo-00C896?style=flat-square)](https://jobpilot-client-chi.vercel.app)
[![Source](https://img.shields.io/badge/Source-Code-181717?style=flat-square&logo=github)](https://github.com/chauhandigvijay1)

</td>
<td valign="top" width="50%">

### ⚡ [DevFlow AI](https://devflow-ai-client.netlify.app) — AI Chat SaaS

Sub-second token streaming from Groq's LPU inference, delivered over **Server-Sent Events** instead of WebSockets — simpler, auto-reconnecting, and a natural fit for a one-directional token stream. Razorpay billing runs a three-layer payment-verification chain (HMAC signature check, duplicate-payment detection, nonce rotation) so even a 100%-off coupon can't be replayed.

Deliberately built in **plain JavaScript, not TypeScript** — a conscious tradeoff to keep the contribution barrier low, backed by strict ESLint and test discipline instead of compile-time types.

<sub>SSE token streaming · 3-layer payment verification · 24 REST endpoints · plain JS by design</sub>

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Groq](https://img.shields.io/badge/Groq_API-F5A623?style=flat-square)
![Razorpay](https://img.shields.io/badge/Razorpay-02042B?style=flat-square)
![Cloudinary](https://img.shields.io/badge/Cloudinary-3448C5?style=flat-square&logo=cloudinary&logoColor=white)

[![Live](https://img.shields.io/badge/Live-Demo-00C896?style=flat-square)](https://devflow-ai-client.netlify.app)
[![Source](https://img.shields.io/badge/Source-Code-181717?style=flat-square&logo=github)](https://github.com/chauhandigvijay1)

</td>
</tr>
</table>

---

## 🧩 Engineering Decisions

Specific tradeoffs I reasoned through and can defend in an interview — not just tools I used.

| Decision | Project | Why |
|---|---|---|
| SSE over WebSockets for AI token streaming | DevFlow AI | Simpler over plain HTTP, auto-reconnects, and matches a one-directional token flow — a WebSocket upgrade handshake would be unused complexity |
| REST writes first, socket broadcasts second — never client-emitted state | DsSync Hub | Eliminates race conditions between HTTP responses and real-time pushes; the database is always the single source of truth |
| `tokenVersion` integer instead of a Redis session blacklist | DsSync Hub · JobPilot | Instant "log out everywhere" on password change, with zero extra infrastructure to run or fail |
| Cookie-based provider auth, AES-256-GCM encrypted per-user | Valtrexa V2 | Job boards don't expose public application APIs — session cookies are the only way in, and they survive CAPTCHA/MFA since the session is already authenticated |
| RLS *and* mandatory `.eq("user_id", …)` in every service-role query | Valtrexa V2 | Trust nothing by default — 145+ write operations audited by hand, zero unscoped writes found |
| 3-tier selector fallback (exact CSS → fallback chain → fuzzy match) | Valtrexa V2 · JobPilot | Browser automation and scraping degrade gracefully when a site changes its DOM, instead of failing outright |
| Embedded MongoDB subdocuments for chat messages | DevFlow AI | The dominant access pattern is "load one chat's full history" — embedding avoids a join for the one query that matters |

---

## ⚙️ Core Stack

**Languages & Types**
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript_ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)

**Frontend**
![React 19](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js 14](https://img.shields.io/badge/Next.js_14-000000?style=flat-square&logo=next.js&logoColor=white)
![TanStack Start](https://img.shields.io/badge/TanStack_Start-FF4154?style=flat-square)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square)
![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-764ABC?style=flat-square&logo=redux&logoColor=white)

**Backend & Real-Time**
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Express 4/5](https://img.shields.io/badge/Express_4%2F5-000000?style=flat-square&logo=express&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socket.io)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)

**Data**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

**AI & Integrations**
![Groq](https://img.shields.io/badge/Groq_API-F5A623?style=flat-square)
![OpenRouter](https://img.shields.io/badge/OpenRouter-7C3AED?style=flat-square)
![n8n](https://img.shields.io/badge/n8n_Workflows-EA4B71?style=flat-square)
![Razorpay](https://img.shields.io/badge/Razorpay-02042B?style=flat-square)
![Google APIs](https://img.shields.io/badge/Google_APIs-4285F4?style=flat-square&logo=google&logoColor=white)

**Auth & Security**
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![OAuth 2.0](https://img.shields.io/badge/Google_OAuth_2.0-4285F4?style=flat-square&logo=google&logoColor=white)
![Helmet.js](https://img.shields.io/badge/Helmet.js-grey?style=flat-square)

**Testing & Deployment**
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white)

---

## 📊 GitHub Activity

<p align="center">
  <img width="49%" src="https://streak-stats.demolab.com/?user=chauhandigvijay1&theme=tokyonight&hide_border=true&border_radius=8" />
</p>



---

## 📬 Let's Work Together

Open to full-time junior roles and remote freelance projects. I typically respond within 24 hours.

| | |
|---|---|
| 📧 **Email** | [chauhandigvijay669@gmail.com](mailto:chauhandigvijay669@gmail.com) |
| 💼 **LinkedIn** | [linkedin.com/in/digvijaykumarsingh](https://www.linkedin.com/in/digvijaykumarsingh) |
| 🌐 **Portfolio** | [dsc-portfolio-website.netlify.app](https://dsc-portfolio-website.netlify.app) |
| 📍 **Location** | Greater Noida, India — IST (UTC+5:30) |

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=150&section=footer&color=0:4f46e5,50:1e1b4b,100:0d1117" />
</p>
