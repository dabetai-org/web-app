# dabetai — Web Portal (Healthcare Professionals)

<p align="center">
  <img src="https://img.shields.io/badge/Angular-19-red?logo=angular" alt="Angular">
  <img src="https://img.shields.io/badge/Tailwind_CSS-4.x-blue?logo=tailwindcss" alt="Tailwind CSS">
  <img src="https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white" alt="TypeScript">
</p>

<p align="center">
  <em>Healthcare professional web portal for diabetes patient monitoring, clinical data visualization, and AI-powered risk predictions.</em>
</p>

<p align="center">
  <a href="https://github.com/dabetai-org/web-app">Repository</a>
  ·
  <a href="https://github.com/dabetai-org/web-app/issues">Report Bug</a>
  ·
  <a href="https://chrisssp.vercel.app/assets/docs/papers/Prevenci%C3%B3n-de-Riesgos-de-la-Diabetes-Mediante-una-Plataforma-Inteligente-de-Monitorizaci%C3%B3n-y-Predicci%C3%B3n-de-Complicaciones-con-Inteligencia-Artificial.pdf">Research Paper</a>
</p>

<p align="center">
  <a href="README.md">🇬🇧 English</a> · <a href="README.es.md">🇪🇸 Español</a>
</p>

---

## About dabetai

**dabetai** is a comprehensive preventive ecosystem for diabetes that predicts complications like retinopathy, nephropathy, neuropathy, and diabetic foot before they become irreversible.

This repository contains the **Web Portal** — a web application for healthcare professionals to:

- Monitor patient glucose levels, activity, and clinical data in real time
- Visualize AI-powered risk predictions for diabetes complications
- Manage patient records and medical history
- Access clinical reports and early warning alerts
- Communicate with patients through the platform

### Ecosystem

| Component | Repository | Stack |
|-----------|-----------|-------|
| **Mobile App** | [dabetai-org/mobile-app](https://github.com/dabetai-org/mobile-app) | React Native 0.79, Expo 53, Tailwind CSS |
| **Web Portal** (this) | [dabetai-org/web-app](https://github.com/dabetai-org/web-app) | Angular 19, Tailwind CSS |
| **Core API** | [dabetai-org/api](https://github.com/dabetai-org/api) | NestJS 11, PostgreSQL, Prisma |
| **AI Inference API** | [dabetai-org/ai-api](https://github.com/dabetai-org/ai-api) | FastAPI, Python 3.11, MongoDB |
| **AI Models** | [dabetai-org/ai-models](https://github.com/dabetai-org/ai-models) | Python, scikit-learn, XGBoost, PyTorch |
| **Landing** | [dabetai-org/landing](https://github.com/dabetai-org/landing) | Astro, Tailwind CSS |

## Features

- **Patient Management** — Comprehensive patient records and data visualization
- **Glycemic Monitoring** — Real-time glucose levels and activity tracking
- **AI Predictions** — Early risk alerts for diabetic complications
- **Clinical Reports** — Generate and export patient reports
- **Role-Based Access** — Secure login with patient, doctor, and admin roles
- **Responsive UI** — Modern interface built with Tailwind CSS

## Quick Start

### Prerequisites

- Node.js 18+
- Angular CLI 19+: `npm install -g @angular/cli`
- npm 9+

### Setup

```bash
git clone https://github.com/dabetai-org/web-app.git
cd web-app
npm install
ng serve
```

Open `http://localhost:4200`

## Architecture

```
┌────────────────────────────────────────────────┐
│         Web Portal (Angular 19)                │
│  ┌─────────┐ ┌──────────┐ ┌──────────────┐   │
│  │ Patient │ │   AI     │ │  Clinical    │   │
│  │ Monitor │ │ Insights │ │   Reports    │   │
│  └────┤────┘ └────┤─────┘ └──────┤────────┘   │
│       │           │              │            │
│  ┌────├─────────├────────────────├─────────────────┐    │
│  │         HTTP Services (Axios)         │    │
│  └─────────────────────────┘    │
└───────────────────├───────────────────────────────┘
                    │ JWT Auth
         ┌──────────├──────────┐
         ├                     ├
┌──────────────┐     ┌──────────────┐
│  Core API    │     │  AI API      │
│  (NestJS)    │     │  (FastAPI)   │
└──────────────┘     └──────────────┘
```

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for branch naming, commit conventions, and PR workflow.

## License

This project is licensed under the GNU General Public License v3.0 — see the [LICENSE](LICENSE) file for details.

## Acknowledgments

**Authors:**
- Cardenas Cabal Fermín
- Ortiz Pérez Alejandro — alex03ortizperez@gmail.com
- Serrano Puertos Jorge Christian — christian.serrano.puertos@gmail.com

**Advisors:**
- Guarneros Nolasco Luis Rolando
- Cruz Ramos Nancy Aracely

**Academic Support:**
- Universidad Tecnológica del Centro de Veracruz
