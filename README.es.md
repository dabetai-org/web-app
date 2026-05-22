# dabetai — Portal Web (Profesionales de la Salud)

<p align="center">
  <img src="https://img.shields.io/badge/Angular-19-red?logo=angular" alt="Angular">
  <img src="https://img.shields.io/badge/Tailwind_CSS-4.x-blue?logo=tailwindcss" alt="Tailwind CSS">
  <img src="https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white" alt="TypeScript">
</p>

<p align="center">
  <em>Portal web para profesionales de la salud, con monitoreo de pacientes diabéticos, visualización de datos clínicos y predicciones de riesgo mediante IA.</em>
</p>

<p align="center">
  <a href="https://github.com/dabetai-org/web-app">Repositorio</a>
  ·
  <a href="https://github.com/dabetai-org/web-app/issues">Reportar Bug</a>
  ·
  <a href="https://chrisssp.vercel.app/assets/docs/papers/Prevenci%C3%B3n-de-Riesgos-de-la-Diabetes-Mediante-una-Plataforma-Inteligente-de-Monitorizaci%C3%B3n-y-Predicci%C3%B3n-de-Complicaciones-con-Inteligencia-Artificial.pdf">Artículo de Investigación</a>
</p>

<p align="center">
  <a href="README.md">🇬🇧 English</a> · <a href="README.es.md">🇪🇸 Español</a>
</p>

---

## Acerca de dabetai

**dabetai** es un ecosistema preventivo integral para la diabetes que predice complicaciones como retinopatía, nefropatía, neuropatía y pie diabético antes de que sean irreversibles.

Este repositorio contiene el **Portal Web** — una aplicación web para profesionales de la salud que permite:

- Monitorear glucosa, actividad y datos clínicos de pacientes en tiempo real
- Visualizar predicciones de riesgo de complicaciones generadas por IA
- Gestionar expedientes e historial médico de pacientes
- Generar reportes clínicos y alertas tempranas
- Comunicarse con los pacientes a través de la plataforma

### Ecosistema

| Componente | Repositorio | Stack |
|-----------|-----------|-------|
| **App Móvil** | [dabetai-org/mobile-app](https://github.com/dabetai-org/mobile-app) | React Native 0.79, Expo 53, Tailwind CSS |
| **Portal Web** (este) | [dabetai-org/web-app](https://github.com/dabetai-org/web-app) | Angular 19, Tailwind CSS |
| **Core API** | [dabetai-org/api](https://github.com/dabetai-org/api) | NestJS 11, PostgreSQL, Prisma |
| **API de IA** | [dabetai-org/ai-api](https://github.com/dabetai-org/ai-api) | FastAPI, Python 3.11, MongoDB |
| **Modelos IA** | [dabetai-org/ai-models](https://github.com/dabetai-org/ai-models) | Python, scikit-learn, XGBoost, PyTorch |
| **Landing** | [dabetai-org/landing](https://github.com/dabetai-org/landing) | Astro, Tailwind CSS |

## Funcionalidades

- **Gestión de Pacientes** — Expedientes completos y visualización de datos
- **Monitoreo Glucémico** — Niveles de glucosa y actividad en tiempo real
- **Predicciones IA** — Alertas tempranas de riesgo de complicaciones diabéticas
- **Reportes Clínicos** — Generación y exportación de reportes
- **Control de Acceso** — Roles de paciente, médico y administrador
- **UI Responsiva** — Interfaz moderna con Tailwind CSS

## Inicio rápido

### Prerrequisitos

- Node.js 18+
- Angular CLI 19+: `npm install -g @angular/cli`
- npm 9+

### Instalación

```bash
git clone https://github.com/dabetai-org/web-app.git
cd web-app
npm install
ng serve
```

Abrir `http://localhost:4200`

## Arquitectura

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

## Contribuciones

Por favor lee [CONTRIBUTING.md](CONTRIBUTING.md) para nuestras convenciones de ramas, commits y flujo de PRs.

## Licencia

Este proyecto está licenciado bajo GNU General Public License v3.0 — consulta el archivo [LICENSE](LICENSE) para más detalles.

## Reconocimientos

**Autores:**
- Cardenas Cabal Fermín
- Ortiz Pérez Alejandro — alex03ortizperez@gmail.com
- Serrano Puertos Jorge Christian — christian.serrano.puertos@gmail.com

**Asesores:**
- Guarneros Nolasco Luis Rolando
- Cruz Ramos Nancy Aracely

**Apoyo Académico:**
- Universidad Tecnológica del Centro de Veracruz
