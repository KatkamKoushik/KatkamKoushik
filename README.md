<div align="center">

# Koushik Katkam

**Full-Stack Systems Builder · AI & Data Engineering · Mobile & Creative Computing**

Building applied software across data pipelines, AI-assisted applications, mobile sensing, and interactive graphics.

[LinkedIn](https://linkedin.com/in/koushik-katkam) · [Instagram](https://www.instagram.com/koushik_katkam) · [Email](mailto:koushikkatkam@gmail.com)

</div>

---

### About

- **Education:** B.Tech Data Science student at Kakatiya University College of Engineering and Technology, Warangal.
- **Focus:** Earth-observation data pipelines, SQL safety, document intelligence, on-device pose tracking, and interactive WebGL graphics.
- **Approach:** Emphasis on explicit validation, testable boundaries, data provenance, and transparent reporting of prototype limitations.

---

### Featured Projects

#### [CycloneSense](https://github.com/KatkamKoushik/cyclonesense)
**Tropical-cyclone data ingestion, analysis, and model-interpretability research prototype**
- Ingests and validates Earth-observation data alongside official storm-track records, including workflows for NOAA GOES-16/18 ABI data and NASA Earthdata CMR.
- Uses Python and PyTorch for exploratory cyclone modeling, Grad-CAM spatial visualizations, and provenance tracking aligned with W3C PROV concepts.
- Handles scientific data formats including NetCDF4, HDF5, and xarray-based datasets.
- **Validation Caveat:** The repository's October 2026 model audit identifies the image-only model's raster inputs as synthetic proxy data and the fusion model as a hybrid using proxy rasters plus environmental variables. Reported scores should not be described as validated predictive accuracy on authentic satellite imagery.
- **Stack:** Python, FastAPI, PyTorch, Next.js, NetCDF4, HDF5, xarray, SQLAlchemy, Celery

#### [SchemaSense](https://github.com/KatkamKoushik/schemasense)
**AI-assisted database exploration and AST-based SQL guardrails**
- Connects to relational databases to build data dictionaries, profile column quality, and support natural-language-assisted querying.
- Implements `SQLGuard` with `sqlglot`: limits queries to a single read-only SELECT/UNION statement, applies table allowlists, blocks protected system catalogs and prohibited functions, and enforces execution limits.
- Supports Google Gemini cloud inference and optional local GGUF inference through llama.cpp.
- Includes automated tests for query validation, table restrictions, and execution-safety behavior.
- **Stack:** Python, Streamlit, SQLAlchemy, sqlglot, PostgreSQL, MySQL, SQLite, Google Gemini API, llama.cpp

#### [NoticeSync](https://github.com/KatkamKoushik/NoticeSync)
**Academic-document intelligence and calendar-event extraction**
- Next.js application for parsing academic circulars and syllabi into structured dates and events.
- Uses document-grounded retrieval with Supabase pgvector and 768-dimensional Google Gemini embeddings.
- Adds temporal-conflict checks, human review for ambiguous or conflicting dates, idempotency controls, and downloadable `.ics` calendar exports.
- Includes automated tests for parsing, date handling, idempotency, provider behavior, and security-sensitive flows. Calendar events can be exported as `.ics` files; automatic Google Calendar synchronization is not implemented.
- **Stack:** Next.js, React, TypeScript, Supabase (pgvector), Vercel AI SDK, Tesseract.js, pdf-parse, Langfuse

#### [GuardAI](https://github.com/KatkamKoushik/guardai)
**URL threat analysis and security telemetry**
- Combines DNS/TLS inspection, external threat-intelligence lookups, lexical heuristics, and entropy-based risk scoring.
- Supports Server-Sent Events (SSE) for scan telemetry, webhook alerts, and PDF report export.
- Features an interactive Three.js/WebGL threat globe with custom GLSL shaders and GSAP animation.
- **Live Demo:** [guardai-six.vercel.app](https://guardai-six.vercel.app)
- **Stack:** Next.js, React, TypeScript, Prisma, NextAuth, Three.js, GLSL, Tailwind CSS

#### [KinexMed](https://github.com/KatkamKoushik/KinexMed)
**On-device movement tracking for rehabilitation-exercise observation**
- Built for the iQOO Hackathon 2026 — Hyderabad City Battle.
- Uses MediaPipe Tasks Vision (Pose Landmarker) and CameraX for on-device pose tracking on Android.
- Sends exercise metrics to a FastAPI backend and a React-based clinician-facing web portal.
- Includes tests for domain calculations, finite-state-machine transitions, and API behavior.
- **Release:** [KinexMed v1.2.0 on GitHub Releases](https://github.com/KatkamKoushik/KinexMed/releases/tag/v1.2.0) (includes downloadable Android APK asset).
- **Stack:** Kotlin, Android, MediaPipe Tasks Vision, CameraX, Python, FastAPI, React, Vite, SQLite

#### [BuildMart](https://github.com/KatkamKoushik/BuildMart)
**Construction-materials procurement marketplace monorepo**
- Combines a Next.js web application, a FastAPI service, and a Flutter mobile client.
- Implements marketplace and order-management workflows with backend API tests and multi-target CI configuration.
- Includes backend API tests and a documented test-execution report.
- **Release:** [BuildMart v2.0.0 on GitHub Releases](https://github.com/KatkamKoushik/BuildMart/releases/tag/v2.0.0) (includes downloadable Android APK asset).
- **Stack:** Next.js, TypeScript, FastAPI, Python, Flutter, Dart, pnpm, Turborepo

#### [VYSHUUU](https://github.com/KatkamKoushik/vyshuuu)
**Digital fashion experience exploring the Indian saree and computational textiles**
- Builds an interactive digital-fashion experience around the saree and textile form.
- Uses React Three Fiber and custom GLSL shaders for cloth draping and pleat animation, with Lenis and GSAP for smooth-scroll choreography.
- **Deployment Status:** The repository README reports that production deployment is pending.
- **Stack:** Next.js, React, TypeScript, Three.js, React Three Fiber, GLSL, GSAP, Lenis, Zustand, Tailwind CSS

#### [Restaurant Ecosystem](https://github.com/KatkamKoushik/restaurant-ecosystem)
**Four-brand restaurant web-platform monorepo**
- Consolidates four restaurant applications: Sampradaya, Majesty Mandi House, Mandiwala, and Aroma, with separate designs and deployment workflows.
- Repository documentation describes digital menus, portion-based pricing, reservation flows, Clerk authentication, and Firebase/Firestore integrations.
- Co-authored with [Vyshnavi Nagavelli](https://github.com/nagavellivyshnavi).
- **Live Deployments:** [Sampradaya](https://sampradaya-multicuisine-family-rest.vercel.app/) · [Majesty Mandi House](https://majesty-mandi-house-eight.vercel.app/) · [Mandiwala](https://mandiwala-arabian-restaurant.vercel.app/) · [Aroma](https://aroma-fine-dine-restaurant-banquet.vercel.app/)
- **Stack:** Next.js, React, TypeScript, Turborepo, Tailwind CSS, Clerk, Firebase/Firestore

#### [StreetSense](https://github.com/KatkamKoushik/streetsense)
**Adaptive mobile sensing for pedestrian-safety research**
- Combines Android sensor inputs such as accelerometer, gyroscope, GPS, ambient light, and camera-related signals with a backend event pipeline.
- Implements a selective-escalation architecture intended to call more expensive specialist checks when sensor evidence is ambiguous.
- **Model Caveat:** The repository's verification matrix states that edge-vision weights are not pre-packaged; when absent, the vision expert reports `UNAVAILABLE` rather than returning fabricated detections. This is described as an architecture prototype, not as a fully operational trained vision model.
- Includes offline Room/SQLite persistence and a FastAPI/PostGIS backend with WebSocket event streaming.
- **Stack:** Kotlin, Jetpack Compose, CameraX, Android Room, Python, FastAPI, React, SQLite, PostGIS, WebSockets

#### [HealX](https://github.com/KatkamKoushik/HealX)
**Accessible bilingual healthcare-facility navigation prototype**
- Provides English/Telugu interfaces, browser text-to-speech, high-contrast controls, and adjustable typography.
- Offers Gemini-assisted search and a Supabase-backed facility store, with an in-memory Demo Mode for offline/evaluation use.
- **Data & Scope Disclosure:** The project's default facility records are simulated sample data across South India. The repository explicitly states HealX does not provide medical diagnosis, emergency dispatch, or official government health-record integration.
- **Stack:** Next.js, React, TypeScript, Supabase, Google Gemini API, Tailwind CSS

---

### Technical Skills

- **Languages:** Python, TypeScript, JavaScript, Kotlin, Dart, SQL, HTML, CSS, GLSL
- **Web & Mobile:** Next.js, React, FastAPI, Flutter, Android SDK, Jetpack Compose, Turborepo, Tailwind CSS, Zustand
- **AI, ML & Data:** PyTorch, MediaPipe Tasks Vision, document-grounded retrieval, Grad-CAM, sqlglot, NetCDF4, HDF5, xarray, Langfuse, Plotly
- **Databases & Storage:** PostgreSQL, Supabase (pgvector), PostGIS, SQLite / Android Room, Firebase Firestore, Prisma, SQLAlchemy
- **Graphics & Real-Time:** Three.js, React Three Fiber, WebGL, custom GLSL shaders, GSAP, Lenis, Framer Motion, Server-Sent Events (SSE), WebSockets
- **Tooling & Infrastructure:** Git, GitHub Actions, Docker, pnpm workspaces, Vercel

---

### Connect

- **LinkedIn:** [Koushik Katkam](https://linkedin.com/in/koushik-katkam)
- **Instagram:** [koushik_katkam](https://www.instagram.com/koushik_katkam)
- **Email:** [koushikkatkam@gmail.com](mailto:koushikkatkam@gmail.com)