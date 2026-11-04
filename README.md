<div align="center">

# Koushik Katkam

**Full-Stack Systems Builder | AI & Data Engineering | Mobile & Spatial Computing**

Warangal / Hyderabad, India

[GitHub](https://github.com/KatkamKoushik) | [LinkedIn](https://linkedin.com/in/koushik-katkam) | [Instagram](https://www.instagram.com/koushik_katkam) | [Email](mailto:koushikkatkam@gmail.com)

</div>

---

## About

I am a B.Tech Data Science student at Kakatiya University College of Engineering and Technology (KUCET), Warangal. I design and build applied software systems spanning edge computer vision, AST-based data governance, document intelligence, privacy-first geospatial routing, and interactive graphics.

My work emphasizes explicit validation boundaries, mathematical invariant guarantees, data provenance, and transparent reporting of prototype constraints.

---

## Featured Projects

### [K² — Classroom Attendance Proposal System](https://github.com/KatkamKoushik/K-Squared-Face-Recognition-Attendance-System)
**Institutional classroom-photo attendance proposal system for Kakatiya University College of Engineering & Technology (KUCET)**
- Replaces single-face biometric punch kiosks and paper ledgers with an asynchronous, multi-face classroom sweep workflow.
- Computer vision operates strictly as an evidence producer rather than an authoritative decision maker: faculty captures sweep photos, reviews candidate proposals against immutable roster snapshots, and commits atomic verified attendance records.
- Integrates SCRFD face detection and ArcFace ResNet-50 embeddings (open-set threshold tau = 0.60) with ONNX Runtime.
- **Security & Privacy:** Ephemeral frame wiping, client SHA-256 anchoring, zero raw facial image storage.
- **Verification:** 86 unit and governance tests, 15 Playwright E2E browser tests, 5 mathematical invariant suites, Flutter static analysis, and TypeScript/Dart cross-language contracts.
- **Documentation:** [Official Technical Wiki](https://github.com/KatkamKoushik/K-Squared-Face-Recognition-Attendance-System/wiki)
- **Stack:** Python 3.12, FastAPI, Flutter, Next.js 15, PostgreSQL 16, SCRFD, ArcFace, ONNX Runtime, Docker Compose

### [NoticeSync](https://github.com/KatkamKoushik/NoticeSync)
**Academic-document intelligence and calendar-event extraction**
- Ingests university circulars, exam timetables, and syllabi into structured dates using document-grounded RAG with Supabase pgvector and 768-dimensional embeddings.
- Resolves multi-document deadline revisions and temporal conflicts with human-in-the-loop review gating for ambiguous or conflicting dates.
- **Verification & Limitations:** 144 tests across 38 suites, streaming byte bounds, decompression bomb defense, CSRF Fetch Metadata protection, and an empirical benchmark suite (100% extraction F1, 0% false confirmations). Evaluated on 11 synthetic, privacy-safe university circulars; calendar events export as .ics files (automatic Google Calendar synchronization is not implemented).
- **Live Demo:** [notice-sync.vercel.app](https://notice-sync.vercel.app) | **Documentation:** [NoticeSync Wiki](https://github.com/KatkamKoushik/NoticeSync/wiki)
- **Stack:** Next.js 16, React 19, TypeScript, Supabase (pgvector), Vercel AI SDK, Tesseract.js, pdf-parse, Langfuse

### [GuardAI](https://github.com/KatkamKoushik/guardai)
**URL threat analysis and real-time security telemetry**
- Automated threat intelligence, lexical heuristic evaluation, and active cryptographic scanning platform.
- Combines DNS/TLS inspection, external reputation lookups (VirusTotal, Google Safe Browsing, AbuseIPDB, URLhaus), Shannon entropy heuristics, and Server-Sent Events (SSE) scan telemetry.
- Features an interactive Three.js/WebGL threat globe with custom GLSL shaders and GSAP animation.
- **Security & Abstention Policy:** 80 Vitest security/regression tests, 11 Playwright E2E tests, 20-vector SSRF test suite with pinned IP transport, rootless multi-stage Docker container (UID 1001), and OpenAPI 3.1 schema. When external threat feeds are absent, the scanner returns an INCONCLUSIVE verdict rather than producing fabricated risk classifications.
- **Live Demo:** [guardai-six.vercel.app](https://guardai-six.vercel.app) | **Documentation:** [GuardAI Wiki](https://github.com/KatkamKoushik/guardai/wiki)
- **Stack:** Next.js 16, React 19, TypeScript, Prisma, PostgreSQL 16, NextAuth, Three.js, GLSL, Tailwind CSS v4, Docker

### [SchemaSense AI](https://github.com/KatkamKoushik/schemasense)
**Enterprise AI Data Steward and multi-cloud schema intelligence console**
- Connects to relational and cloud databases (PostgreSQL, MySQL, SQLite, AWS RDS, Cloud SQL, Supabase, Neon) to generate interactive data dictionaries, audit column quality, classify sensitive PII entities, and export DBML/DDL schemas.
- Implements SQLGuard via sqlglot: dialect-aware AST parser restricting queries to read-only SELECT/UNION operations, enforcing table allowlists, blocking system catalogs, and preventing injection.
- Features an enterprise zero-trust access gate supporting Google and GitHub OAuth 2.0 SSO, with universal cloud and local model inference (Gemini, Claude, GPT-4o, llama.cpp).
- **Verification:** 417 tests passing (91% code coverage), 54 adversarial SQL AST tests, CycloneDX SBOM v1.5, and detect-secrets audited baseline.
- **Live Demo:** [SchemaSense on Streamlit](https://neural-nexus-schemasense-n9aixu78zu8ebbbahcvvhc.streamlit.app/)
- **Stack:** Python, Streamlit, SQLAlchemy, sqlglot, PostgreSQL, MySQL, SQLite, Google Gemini API, Anthropic Claude, llama.cpp

### [Walkscope](https://github.com/KatkamKoushik/Walkscope)
**Transparent, privacy-first pedestrian walking companion and route context scoring engine**
- Mobile-first pedestrian navigation companion that replaces opaque, subjective safety scores with verifiable Route Context Coverage (0 to 100%) and Route Context Intelligence.
- Evaluates OpenStreetMap venue opening hours at projected arrival time, along-route venue distribution gaps, major-road share breakdown, verified support-point registry, and an auditable "Why This Route?" evidence drawer.
- **Privacy & Resilience:** Zero analytics SDKs or advertising trackers; all journey history remains in local-first SQLite. Dedicated Fastify gateway with request deduplication, rate limiting, and in-memory TTL caching with graceful standalone fallback. Verified support-point registry strictly requires independently audited access evidence (defaults to 0 points).
- **Verification:** 229/229 passing tests, SLA latency bounds (p50 < 100ms), ReDoS fuzzing immunity across 500+ patterns, and nearest line-segment off-route detection with kinematic teleportation filtering.
- **Stack:** React Native, Expo 58, TypeScript, Node.js 22 LTS, Fastify, MapLibre Native, SQLite, Docker, Redis, PostGIS

### [KinexMed](https://github.com/KatkamKoushik/KinexMed)
**Edge-native clinical movement intelligence and physical rehabilitation**
- Real-time rehabilitation-exercise observation built for the iQOO Hackathon 2026 (Hyderabad City Battle).
- Employs MediaPipe Tasks Vision (Pose Landmarker) and CameraX for 100% on-device pose tracking, One-Euro temporal filtering, Euclidean joint geometry, and finite-state machine repetition counting across 15 clinical exercises.
- Integrates Alembic database migrations, clinician REST endpoints with API-key authentication and strict CORS whitelisting, and a React clinician portal.
- **Verification, Privacy & Disclaimer:** 87 automated tests passing across Backend and Playwright (50), Android Subsystem (32), and Web Clinician Portal (5). Raw camera frames are analyzed in-memory and immediately freed with zero video/images stored or transmitted. Assistive observation tool; not a substitute for professional medical diagnosis or unsupervised prescription.
- **Release:** [KinexMed v1.0.0 on GitHub Releases](https://github.com/KatkamKoushik/KinexMed/releases/tag/v1.0.0) (includes downloadable Android debug APK).
- **Stack:** Kotlin, Android SDK, MediaPipe Tasks Vision, CameraX, Python 3.12, FastAPI, React, Vite, SQLite, Alembic

### [CycloneSense](https://github.com/KatkamKoushik/cyclonesense)
**Tropical-cyclone satellite telemetry ingestion, analysis, and model-interpretability research prototype**
- Ingests and validates Earth-observation data alongside official storm-track records, including workflows for NOAA GOES-16/18 ABI data and NASA Earthdata CMR.
- Uses Python and PyTorch for exploratory cyclone modeling, Grad-CAM spatial visualizations, and provenance tracking aligned with W3C PROV concepts across NetCDF4, HDF5, and xarray scientific data.
- **Verification & Validation Caveat:** 55 automated tests passing. The repository model audit identifies the image-only model raster inputs as synthetic proxy data and the fusion model as a hybrid; reported scores reflect exploratory architecture rather than validated predictive accuracy on authentic satellite imagery.
- **Release:** [CycloneSense v1.0.0 on GitHub Releases](https://github.com/KatkamKoushik/cyclonesense/releases/tag/v1.0.0).
- **Stack:** Python, FastAPI, PyTorch, Next.js, NetCDF4, HDF5, xarray, SQLAlchemy, Celery

### [BuildMart](https://github.com/KatkamKoushik/BuildMart)
**Construction-materials procurement marketplace monorepo**
- Consolidates a Next.js 15 commercial procurement web application, a FastAPI backend service, and a Flutter mobile client.
- Implements multi-tenant marketplace workflows, role-based procurement operations, backend API tests, and multi-target CI configuration.
- **Verification & Release:** 59 backend API tests passing with documented test-execution report. [BuildMart v2.0.0 on GitHub Releases](https://github.com/KatkamKoushik/BuildMart/releases/tag/v2.0.0) (includes downloadable Android APK asset).
- **Stack:** Next.js 15, TypeScript, FastAPI, Python, Flutter, Dart, pnpm, Turborepo

### [Restaurant Ecosystem](https://github.com/KatkamKoushik/restaurant-ecosystem)
**Four-brand restaurant web-platform monorepo**
- Consolidates four restaurant applications: Sampradaya, Majesty Mandi House, Mandiwala, and Aroma, with distinct brand aesthetics and deployment workflows.
- Implements digital menus, portion-based pricing calculators, reservation workflows, Clerk authentication, and Firebase/Firestore real-time persistence.
- Co-authored with [Vyshnavi Nagavelli](https://github.com/nagavellivyshnavi).
- **Live Deployments:** [Sampradaya](https://sampradaya-multicuisine-family-rest.vercel.app/) | [Majesty Mandi House](https://majesty-mandi-house-eight.vercel.app/) | [Mandiwala](https://mandiwala-arabian-restaurant.vercel.app/) | [Aroma](https://aroma-fine-dine-restaurant-banquet.vercel.app/)
- **Stack:** Next.js 16, React, TypeScript, Turborepo, Tailwind CSS, Clerk, Firebase/Firestore

### [HealX](https://github.com/KatkamKoushik/HealX)
**Accessible bilingual healthcare-facility navigation prototype**
- Provides English/Telugu interfaces, browser text-to-speech, high-contrast controls, adjustable typography, and telephony simulation.
- Offers Gemini-assisted natural-language search and a Supabase-backed facility store, with an in-memory Demo Mode for offline evaluation.
- **Data & Scope Disclosure:** Prototype developed for the Seva First Innovation Challenge (SFIC) Level 3. Default facility records are simulated sample data across South India; does not provide medical diagnosis, emergency dispatch, or official government health-record integration.
- **Live Demo:** [healx-six.vercel.app](https://healx-six.vercel.app)
- **Stack:** Next.js, React, TypeScript, Supabase, Google Gemini API, Tailwind CSS

### [VYSHUUU — The Unstitched Continuum](https://github.com/KatkamKoushik/vyshuuu)
**Digital haute couture house and computational textile experience**
- Immersive digital-fashion experience devoted to the Indian saree, unstitched silk architecture, and computational textile intelligence.
- Employs React Three Fiber and custom GLSL shaders (catenary drape, dynamic traveling pleats, anisotropic zari specular glints) with Lenis smooth-scroll and GSAP ScrollTrigger choreography across 11 curatorial chapters.
- **Asset Architecture & Live Experience:** 95 locked production assets resolved via Cloudinary CDN manifest; 10 curated saree concepts honoring classical Indian textile lineages.
- **Live Experience:** [vyshuuu-five.vercel.app](https://vyshuuu-five.vercel.app)
- **Stack:** Next.js, React, TypeScript, Three.js, React Three Fiber, GLSL, GSAP, Lenis, Zustand, Tailwind CSS

### [StreetSense](https://github.com/KatkamKoushik/streetsense)
**Adaptive mobile sensing for pedestrian-safety research**
- Combines Android sensor inputs (accelerometer, gyroscope, GPS, ambient light, camera) with a backend event pipeline.
- Implements a selective-escalation architecture intended to call more expensive specialist checks when sensor evidence is ambiguous.
- **Verification, Limitations & Release:** 16 passing tests (12 backend + 4 on-device). The repository verification matrix clarifies that edge-vision weights are not pre-packaged; when absent, the vision expert safely reports UNAVAILABLE rather than returning fabricated detections. [StreetSense v1.0.0 on GitHub Releases](https://github.com/KatkamKoushik/streetsense/releases/tag/v1.0.0).
- **Stack:** Kotlin, Jetpack Compose, CameraX, Android Room, Python, FastAPI, React, SQLite, PostGIS, WebSockets

### [Proposal Website](https://github.com/KatkamKoushik/proposal-website)
**Cinematic interactive scroll-based narrative experience**
- Dark-mode visual storytelling experience featuring smooth Framer Motion scene transitions, glowing typography, and interactive particle effects.
- **Live Demo:** [proposal-website-drab.vercel.app](https://proposal-website-drab.vercel.app/)
- **Stack:** Next.js, TypeScript, Tailwind CSS, Framer Motion, Vercel

---

## Technical Skills

- **Languages:** Python, TypeScript, JavaScript, Kotlin, Dart, SQL, HTML, CSS, GLSL
- **Frameworks & Runtimes:** Next.js (15/16), React (18/19), FastAPI, Fastify, Node.js (22 LTS), Flutter, Android SDK, Jetpack Compose, React Native / Expo, Streamlit, Turborepo
- **AI, ML & Computer Vision:** PyTorch, MediaPipe Tasks Vision, SCRFD Face Detection, ArcFace ResNet-50, ONNX Runtime, Document-Grounded RAG, Google Gemini API, Anthropic Claude, Vercel AI SDK, sqlglot, Langfuse, Grad-CAM, NetCDF4, HDF5, xarray
- **Databases & Storage:** PostgreSQL 16 (pgvector), Supabase, PostGIS, SQLite / Android Room, Firebase Firestore, MySQL, Redis, Prisma, SQLAlchemy, Alembic
- **Graphics & Real-Time:** Three.js, React Three Fiber, WebGL, Custom GLSL Shaders, MapLibre Native, GSAP, Lenis, Framer Motion, Server-Sent Events (SSE), WebSockets
- **DevOps, Security & Tooling:** Docker & Docker Compose (rootless multi-stage), GitHub Actions CI/CD, Playwright E2E, Vitest, Pytest, CycloneDX SBOM, Git, pnpm workspaces, Vercel

---

## Connect

- **LinkedIn:** [Koushik Katkam](https://linkedin.com/in/koushik-katkam)
- **Instagram:** [koushik_katkam](https://www.instagram.com/koushik_katkam)
- **Email:** [koushikkatkam@gmail.com](mailto:koushikkatkam@gmail.com)
