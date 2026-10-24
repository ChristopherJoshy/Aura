<div align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:172554,35:4338ca,70:8b5cf6,100:f5d0fe&height=190&section=header&text=Aura&fontSize=68&fontColor=ffffff&animation=twinkling&fontAlignY=36&desc=A%20gentler%20interface%20for%20memory%20care.&descAlignY=58&descSize=17" alt="Aura animated header" />

  <p>
    <img src="https://img.shields.io/badge/Expo-React%20Native-4630EB?style=for-the-badge&logo=expo&logoColor=white" alt="Expo and React Native" />
    <img src="https://img.shields.io/badge/API-FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
    <img src="https://img.shields.io/badge/Edge-Raspberry%20Pi-BC2C2C?style=for-the-badge&logo=raspberrypi&logoColor=white" alt="Raspberry Pi module" />
    <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-E9D5FF?style=for-the-badge" alt="MIT License" /></a>
  </p>
</div>

## 💜 What it is

Aura is a multi-part memory-care companion prototype: a mobile app, a FastAPI backend, and an optional Raspberry Pi module for local voice and camera processing. The repository brings together patient and caregiver flows, reminders, memory records, and service integrations.

## 🧩 System overview

```mermaid
flowchart LR
  A[Expo mobile app] --> B[FastAPI service]
  B --> C[MongoDB]
  B --> D[Firebase Auth and notifications]
  B --> E[WebSocket updates]
  F[Raspberry Pi module] --> B
  F --> G[Local speech and vision processing]
```

## ✨ Project areas

- The Expo app contains patient/caregiver-facing screens and notification flows.
- The API provides authentication, persisted records, and realtime endpoints.
- The `auramodule/` directory contains edge-side Python components for camera/voice workflows.
- The `rules/` directory holds project behavior and care-flow material.

## 🧰 Stack

| Area | Tools |
|---|---|
| Mobile | Expo 55, React Native, TypeScript, Expo Router |
| API | Python, FastAPI, Uvicorn, Beanie/MongoDB |
| Identity and notifications | Firebase Auth, Firebase messaging |
| Edge prototype | Python, OpenCV, faster-whisper, InsightFace |
| Realtime | WebSockets |

## 🚀 Start the app

Install frontend dependencies and run Expo:

```bash
git clone https://github.com/ChristopherJoshy/Aura.git
cd aura/frontend
npm install
npm run start
```

The backend and edge module have separate Python requirements and environment settings. Configure Firebase, MongoDB, and provider credentials from the relevant example files before starting those services. Run device-only camera, microphone, notification, and location flows on supported hardware.

## 🗂️ Layout

```text
frontend/    Expo app
backend/     FastAPI service
auramodule/  edge-device scripts and processing
rules/       product and care-flow rules
```

## 📄 License

MIT. See [`LICENSE`](LICENSE).

## ⚠️ Scope and privacy

This is a software prototype, not a medical device or substitute for professional care. The project handles sensitive health, location, voice, and image data; do not use real patient data without appropriate consent, access controls, retention rules, and security review.