# Projects
[Return](ReadMe.md)
---

## zero-2-llm — LLM From Scratch

Started as me following Karpathy's Zero to Hero series, but with my own Tensor class on numpy instead of torch. It does autograd over whole arrays, has pytorch-style layers (Linear, BatchNorm, LayerNorm, Embedding, Dropout) and Adam, and can swap to CuPy to run on the GPU. On top of it I built a 10.8M parameter character-level GPT trained on Shakespeare (val loss 1.486) and a 2x2 Rubik's cube solver, trained on all 3,674,160 cube states with a BFS dataset. With a beam search it solved every cube I tested.

From there I moved to PyTorch to pretrain an 805M parameter Llama-style model (RoPE, RMSNorm, SwiGLU, GQA) that I plan on using as Somab's offline mode. I built the 17.7B token dataset myself from FineWeb-Edu, DCLM, FineMath, Cosmopedia, Wikipedia and Stack-Edu code, with a filter for junk docs I found after the first pilot run kept memorizing them. I ran two 151M pilots on Kaggle's 2x T4s with DDP, and the full model is currently training on an AWS spot GPU. It checkpoints to S3 and resumes bit-exact after interruptions.

**Skills demonstrated:** Autograd and backprop from scratch, transformer architecture, distributed training (DDP), mixed precision (fp16/bf16), dataset building and filtering, cloud GPU infrastructure (EC2 spot, S3, IAM), cost control

**Stack:** Python · NumPy · CuPy · PyTorch · bitsandbytes · AWS (EC2, S3) · Kaggle · Hugging Face

**Repo:** https://github.com/Samsong1018/zero-2-llm

---

## DashGen — Dashboard Generator (Kiroween Hackathon 2026)

A team hackathon project for Kiroween 2026. You connect data sources (REST APIs, JSON, your own MySQL database, scraped web pages, log files, or uploaded spreadsheets), drop charts and KPIs onto a drag-and-drop grid, and share the dashboard with a public link. I built the read-only viewer and public sharing, the SQL, scraping, log and Excel sources, and did security passes on the backend. Every source is fetched server-side so credentials never reach the browser, SQL runs in a read-only transaction, and private hosts are blocked.

**Skills demonstrated:** Full-stack web development, team collaboration, SSRF and injection prevention, input validation, testing (node:test, fast-check)

**Stack:** Node.js · Express 5 · MySQL · Vanilla JS · Chart.js · zod

**Repo:** Private (hackathon in progress)

---

## D2D — WebRTC P2P File Sharing

Instant cross-device file sharing using WebRTC data channels with QR/code pairing. Files transfer peer-to-peer with an ECDH handshake → AES-GCM encryption pipeline. Includes a Socket.IO relay fallback for NAT traversal, optional share links with password protection (scrypt-hashed), folder support via client-side zip (fflate), Redis-backed persistence, and Docker deployment with Caddy TLS.

**Skills demonstrated:** WebRTC, end-to-end encryption (Web Crypto API, ECDH, AES-GCM), real-time signaling, monorepo architecture, rate limiting, CI/CD (GitHub Actions), Docker

**Stack:** Next.js 14 · Socket.IO · TypeScript · Redis · Zustand · Caddy · Docker · pnpm workspaces

**Live:** https://D2D-Filetransfer.onrender.com

---

## Floret — Period & Cycle Tracker

A period and cycle tracking web app with cycle prediction, confidence scoring, sleep tracking, partner mode, and doctor-ready PDF report generation. Built with Google OAuth and deployed as a PWA, with a React Native mobile app via Expo.

**Skills demonstrated:** Health data modeling, cycle prediction algorithms, OAuth 2.0, PWA, cross-platform mobile (React Native/Expo), PDF generation, responsive design

**Stack:** Vanilla JS · Node.js · Express · PostgreSQL · Google OAuth · React Native · Expo · PWA

**Live:** https://Floret.fyi

---

## Somab — AI Voice Assistant

A local AI assistant with a custom trained voice, face animation, passive listening, and a custom PCB. Built around Piper TTS for low-latency on-device speech synthesis with a character model for visual response feedback. Currently on hold while I train its offline LLM (see zero-2-llm above).

**Skills demonstrated:** TTS model training, audio pipeline engineering, Python, Claude API integration, PCB design (KiCad), real-time systems, hardware/software co-design

**Stack:** Piper TTS · Python · Claude API · KiCad · Linux

**Repo:** https://github.com/Samsong1018/Somab

---

## AMvpn — Self-Hosted WireGuard VPN

A production WireGuard VPN on Oracle Cloud free tier, built from scratch. Includes a full monitoring stack: AdGuard Home DNS with DoH, nginx HTTPS dashboard, FastAPI backend, GeoIP-enriched logging, fail2ban, port knocking (knockd), and a Cowrie SSH honeypot on a second VM with Telegram push notifications for alerts.

**Skills demonstrated:** Linux networking and sysadmin, WireGuard protocol, cloud infrastructure (Oracle Cloud), iptables/NAT, honeypot deployment, intrusion detection, real-time logging pipelines

**Stack:** WireGuard · FastAPI · AdGuard Home · Docker · Oracle Cloud · Linux · nginx · SQLite

**Repo:** Not included

---

## Fracture — Web Pentesting Suite

An open-source PyQt6 desktop pentesting application combining a full HTTP/HTTPS intercepting proxy (with Repeater, Intruder, Scanner, Logger, and Site Map tabs), a findings tracker with CVSS scoring and Obsidian-compatible Markdown export, and a utility belt covering reverse shell generation, hash identification, payload libraries, DNS recon, and security header analysis. Everything runs locally — no cloud, no telemetry.

**Skills demonstrated:** Python, GUI application development (PyQt6), HTTP/HTTPS proxy and MITM, SSL/TLS certificate handling, fuzzing engine design (sniper, pitchfork, cluster bomb modes), CVSS scoring, security tooling architecture

**Stack:** Python · PyQt6 · Linux

**Repo:** https://github.com/Samsong1018/Fracture

---

## TodoLander — Full-Stack Todo App

A daily task management web app with Google OAuth, service worker caching, responsive mobile layout, micro-animations, and a focus timer. Originally built in React, then rewritten to vanilla JS to eliminate the 3MB in-browser Babel dependency.

**Skills demonstrated:** Full-stack web development, OAuth 2.0 implementation (no library), SQL schema migrations, PWA/service workers, vanilla JS (no frameworks), responsive design, production debugging

**Stack:** Vanilla JS · Node.js · Express · PostgreSQL (Neon) · Render

**Live:** https://Todolander.com  
**Repo:** https://github.com/Samsong1018/TodoLander

---

## Security Scripts — Python Security Utilities

A collection of Python scripts for common security tasks. Includes a file integrity checker that generates per-file SHA-256 baselines and detects changes on subsequent runs, and a network ping scanner for LAN host discovery.

**Skills demonstrated:** Python scripting, file integrity monitoring, network scanning, SHA-256 hashing, input validation, security tooling fundamentals

**Scripts:**
- `integrity_checker.py` — baseline and drift detection for file sets
- `ping_scanner.py` — ICMP-based LAN host discovery

**Stack:** Python · hashlib · socket

**Repo:** https://github.com/Samsong1018/security-scripts

---

## Bumper the Band — Band Website

A full band website for Bumper, featuring a music player, show schedule, photo gallery, and booking contact. Built and deployed as a live production site.

**Skills demonstrated:** Frontend development, responsive design, static site deployment, media integration

**Stack:** HTML · CSS · JavaScript

**Live:** https://bumpertheband.com

---

## WTFlag — Shell Command Explainer for Claude Code

A Claude Code `PreToolUse` hook that intercepts every shell command before execution and displays a plain-English explanation. Uses the full tldr-pages dataset (7,070 commands) bundled as a local SQLite database — no network calls, no external dependencies. Includes danger detection for destructive commands, argument context (e.g. resolves `git push origin main` to branch/remote names), and a watcher terminal that displays explanations in a separate window via Unix domain sockets.

**Skills demonstrated:** CLI tool development, Node.js, SQLite, shell command tokenization and parsing, regex, Claude Code hook protocol, Unix IPC, npm packaging

**Stack:** Node.js · SQLite (node:sqlite) · tldr-pages dataset · commander.js

**Repo:** https://github.com/Samsong1018/WTFlag

[Return](ReadMe.md)
