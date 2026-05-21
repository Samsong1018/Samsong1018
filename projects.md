# Projects
[Return](ReadMe.md)
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

A local AI assistant with a custom trained voice, face animation, passive listening, and a custom PCB. Built around Piper TTS for low-latency on-device speech synthesis with a character model for visual response feedback.

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
