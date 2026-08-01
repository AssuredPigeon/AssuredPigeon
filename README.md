<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:667eea,50:764ba2,100:f093fb&height=200&section=header&text=Daniel%20Tornero&fontSize=50&fontColor=fff&animation=fadeIn&fontAlignY=38&desc=Software%20Engineer%20%7C%20AI%20Developer%20%7C%20Backend-Focused&descAlignY=55&descAlign=50" />

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=667EEA&center=true&vCenter=true&multiline=true&width=600&height=100&lines=Building+intelligent+systems;From+idea+to+deployment;AI+%7C+Backend+%7C+Cloud+%7C+Game+Dev" alt="Typing SVG" /></a>
</p>

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/daniel-tornero-solano-1107ba1a0)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=flat&logo=gmail&logoColor=white)](https://mail.google.com/mail/?view=cm&to=danieltornero4@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-AssuredPigeon-181717?style=flat&logo=github)](https://github.com/AssuredPigeon)

</div>

<br>

---

## About me

I'm a Software Engineer specializing in backend systems and AI/LLM integration, currently in my 7th semester at UABC. I work as an independent AI contractor evaluating frontier language models, and I've built and deployed production systems integrating Google Gemini API, OpenAI Whisper, and custom LLM workflows. I have 257 certified hours in AI (Guayerd & IBM SkillsBuild, 2024) and presented research at a postgraduate seminar at Instituto Tecnológico de Tijuana (2026).

---

## Technologies

<table>
<tr>
<td valign="top" width="33%">

### Languages

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)

</td>
<td valign="top" width="33%">

### Frameworks & AI

![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Discord.py](https://img.shields.io/badge/Discord.py-5865F2?style=for-the-badge&logo=discord&logoColor=white)

</td>
<td valign="top" width="33%">

### DevOps & Cloud

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Oracle Cloud](https://img.shields.io/badge/Oracle_Cloud-F80000?style=for-the-badge&logo=oracle&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

</td>
</tr>
</table>

---

## Featured Projects

<details>
<summary><b>DanceLabo — Real-Time Dance Scoring System</b> &nbsp;·&nbsp; <a href="https://github.com/labtechmovilfcitec-hash/DanceLabo">GitHub ↗</a></summary>
<br>

Real-time dance evaluation system using computer vision and deep learning, developed for a Mobile Technology Lab course at UABC.

**Key features:**
- Led the full team as **Team Lead**, distributing tasks across ML, Unity, and backend roles
- Designed and implemented the complete ML pipeline: body pose estimation with **MediaPipe** + person detection with **YOLOv8**, 3D landmark extraction, sequence modeling with **LSTM** (9 movement classes), and a live scoring engine with per-body-segment feedback
- Built a **real-time UDP communication layer** between a Python/PyQt6 desktop app and a Unity scene, streaming normalized skeleton vectors at ~30fps with sub-frame latency
- Implemented a **full-body retargeting system** in Unity (C#): mapped MediaPipe landmarks to a humanoid Mixamo rig, including 3D body yaw rotation (full 360° turn tracking), root translation (walk/jump), and bone-level rotation using `FromToRotation` with T-pose calibration
- Solved coordinate system alignment between MediaPipe (camera space) and Unity (world space), including Z-axis depth correction, mirror-mode handling, and circular yaw smoothing to eliminate landmark swap spikes
- Built a per-bone visibility freeze system: when a limb leaves the camera frame, it holds its last valid pose — rotating naturally with the body as the user turns
- Integrated real-time visual feedback UI in **PyQt6** with live score overlay, pose recording/playback, and multi-camera support

**Stack:** `Python` `PyQt6` `MediaPipe` `LSTM` `YOLOv8` `Unity` `C#` `OpenCV` `UDP`

</details>

<details>
<summary><b>Vialix — Road Anomaly Detection Platform</b> &nbsp;·&nbsp; <a href="https://github.com/AssuredPigeon/ASPHALT">GitHub ↗</a></summary>
<br>

Full-stack mobile platform to detect, map, and crowdsource road anomalies (potholes, bumps, cracks) in real time using accelerometer data and geolocation. Built with a team of 4 as Lead Backend Developer.

**Key features:**
- REST API with **8 route modules** (auth, trips, anomalies, streets, vehicles, gamification, alerts, users) and JWT + bcrypt authentication
- **PostGIS spatial deduplication**: anomalies reported within 10 m of an existing one are merged — confidence score is incremented instead of creating duplicates, and state transitions automatically (`reportado → validado → confirmado`) after crowd validation thresholds
- **Confidence filtering pipeline**: events with confidence < 0.7 are rejected at the API level (HTTP 422); duplicate bursts from the same user within 5 seconds and 5 m are blocked (HTTP 409)
- **Geospatial viewport endpoint** (public, no auth): serves street geometry + road quality index for the visible map area, with dynamic `ST_Simplify` tolerance based on zoom level — supports `LineString` and `MultiLineString` from PostGIS
- **Geocoding service** (zero API key): dual-provider system using Photon (Elasticsearch over OSM, primary) and Nominatim (fallback), with a custom **LRU cache** (150 entries) and rate-limiter (1.2 s between Nominatim requests) to avoid bans
- **Gamification system**: auto badge assignment engine that evaluates detection count, validation count, and trips per user — badges unlock progressively and are awarded without manual triggers
- **Coordinate anonymization** (±50 m offset) to protect user privacy when exposing anomaly locations publicly
- Benchmarking scripts for spatial query performance across Tijuana street segments (`ST_DWithin`, nearest-street, bounding box)
- React Native + Expo mobile app with screens for live trip tracking, anomaly history, badge collection, vehicle selection, and profile

**Stack:** `Node.js` `Express` `PostgreSQL` `PostGIS` `Supabase` `React Native` `Expo` `TypeScript` `JWT` `bcrypt`

</details>

<details>
<summary><b>Semantic Visualization — ML Training Visualization Platform</b> &nbsp;·&nbsp; <a href="http://40.233.21.60/">Live Demo ↗</a></summary>
<br>

Research platform to visualize and analyze the training process of genetic programming models (GSGP), tracking semantic evolution across generations with interactive 2D/3D projections.

**Key features:**
- Evaluated the **Google Gemini API** for automatic interpretation of genetic algorithm outputs — identified precision limitations in specific mathematical contexts and built a **custom LLM-based workflow** as a more controllable alternative
- Built a **server-side animated GIF engine** (matplotlib + Pillow) supporting 2D/3D scatter plots, 360° rotation, progressive evolution trace, and convergence charts — all rendered server-side for instant downloads
- Implemented a **3D Generation View** that uses generation number as the Z axis on 2D data, with smooth real-time camera rotation and Play/Pause generation animation
- Designed a **Focus Mode** (full-screen immersive view) with a compact floating toolbar for distraction-free analysis
- Added a **bilingual i18n system** (EN/ES) with `data-i18n` attribute binding, localStorage persistence, and dynamic state-aware button translation
- Auto-generated **PDF interpretation reports** with ReportLab: statistical metrics, convergence charts, and Gemini-powered narrative analysis
- Compared four dimensionality reduction methods: **PCA, t-SNE, Kernel PCA, UMAP** with interactive switching
- Iterated on prompt engineering strategies during evaluation, analyzing model responses for coherence and usefulness

**Stack:** `Python` `Flask` `Gemini API` `matplotlib` `Pillow` `Plotly` `ReportLab` `PCA` `t-SNE` `UMAP` `JavaScript` `i18n`

</details>

<details>
<summary><b>Voice-Controlled Music Bot — Discord Production Bot</b> &nbsp;·&nbsp; <a href="https://github.com/AssuredPigeon/musicbot">GitHub ↗</a></summary>
<br>

Production-ready Discord music bot controlled by voice commands instead of text, deployed continuously on Oracle Cloud. Built solo end-to-end — architecture, audio pipeline, cloud deployment, and adaptive learning layer.

**Key features:**
- Designed and implemented a **real-time voice command pipeline**: custom `DiscordAudioSink` captures raw PCM (48kHz stereo) per user → VAD detects speech boundaries → resamples to 16kHz mono → **OpenAI Whisper** transcribes → regex-based `IntentProcessor` extracts intent and entities → `VoiceCommandHandler` executes the action — all non-blocking via `ThreadPoolExecutor`
- Built a **dual-engine transcription system**: local Whisper (primary, free, no internet) with automatic fallback to the OpenAI Whisper API — switchable via a single env flag (`WHISPER_USE_API`). Implemented hallucination filtering to discard Whisper artifacts on silent audio
- Implemented an **LRU audio cache** with configurable size limit (500 MB default), TTL expiry, and periodic background cleanup — reduces repeated downloads and lowers playback latency for frequently requested songs
- Developed a **personalized adaptive learning layer** for the real-time translator module: user speech history builds a dynamic Whisper `initial_prompt` that biases transcription toward the user's vocabulary and accent; a personal glossary applies pre/post-translation corrections that accumulate over time
- Built a **cookie health monitoring system**: parses `cookies.txt` expiry dates on startup and every 24h, DMs owners when cookies are near expiry, and identifies cookie-related `yt-dlp` failures with actionable error messages — with a local script (`refresh_cookies.sh`) that extracts fresh cookies from the browser and deploys them to the server via SSH
- **Multi-server isolated architecture**: each guild has its own queue, voice client, audio cache, and voice command session — state is never shared across servers
- Deployed on **Oracle Cloud Always Free** VM in Docker, managed by **PM2** (auto-restart, startup on boot, log management)

**Stack:** `Python` `Discord.py` `OpenAI Whisper` `yt-dlp` `edge-tts` `deep-translator` `Flask` `SQLite` `Tortoise ORM` `Docker` `Oracle Cloud` `PM2`

</details>

<details>
<summary><b>SDGKU — University Management System</b> &nbsp;·&nbsp; <a href="https://github.com/Garethsito/SDKGU-Subject-Sistem">GitHub ↗</a></summary>
<br>

Academic management system for a real client in San Diego, USA. Built in a team of 6.

**Key features:**
- Designed and implemented an **automatic student-course enrollment algorithm**: assigns students to required subjects based on program requirements, minimizing open sections while distributing enrollment equitably across groups
- Implemented the **full backend security layer**: JWT authentication, Bcrypt password hashing, Helmet HTTP hardening, and CORS — including protected endpoints and a seed file for audit activity types
- Built the **email notification system**: sends automated emails to students on enrollment events using Nodemailer
- Designed the **full database schema** (11 models with Prisma/MySQL), including session-subject-professor relationships and audit log tables
- Built individual **PDF report generation** per student: academic progress, GPA, grades per subject, and downloadable from the frontend
- Developed core **session management endpoints**: subject-professor assignment per session, student enrollment/removal, and session CRUD

**Stack:** `NestJS` `TypeScript` `Prisma` `MySQL` `Alpine.js` `Nodemailer`

</details>

<details>
<summary><b>El Último Commit — Typing Game</b> &nbsp;·&nbsp; <a href="https://gamejolt.com/games/KEYOCORP/991558">Play on GameJolt ↗</a></summary>
<br>

Programming-themed typing game where players destroy falling code words by typing them. Features a full combat system with three boss enemies.

**Key features (backend focus):**
- Built a **boss HP system**: 3 boss characters each with 10 HP, animated walk/attack/defeat states loaded from GIF frames; bosses absorb 1 HP per normal hit and 4 HP on **counterattack** (typing the boss's own attack word back at them)
- Implemented **boss-wall collision physics**: bosses move freely in 2D within the game area, reversing direction on boundary contact with randomized direction changes over time
- Engineered **8 unique attack effects** launched by bosses: text reversal, letter shuffling, input hiding, letter removal, word duplication, parenthesis removal, and a **chained error system** (unresolved `NameError` propagates a random secondary error with its own effect)
- Designed the **falling word engine**: velocity scaled by level, enemy type (bugs fall faster), and word length — with resolution-aware scaling that repositions all enemies on window resize
- Implemented a **progressive infection system**: words missed by the player accumulate infection %, which corrupts upcoming words' display with random symbol noise
- Integrated **Discord Rich Presence** to display live game state in the user's Discord profile

**Stack:** `Python` `Pygame` `Pillow`

</details>

<details>
<summary><b>ExoLab — NASA Space Apps Challenge 2025</b> &nbsp;·&nbsp; <a href="https://github.com/AssuredPigeon/ExoLab">GitHub ↗</a></summary>
<br>

Machine learning platform for classifying potential exoplanets from NASA Exoplanet Archive datasets (Kepler KOI, TESS TOI, and K2), developed for the NASA Space Apps Challenge 2025 with team Astro404.

**Key features:**
- Designed and implemented the **machine learning training pipeline**, integrating **Random Forest** (200 estimators, `class_weight='balanced'`, 5-fold stratified cross-validation) and **XGBoost** as selectable models, with UI-triggered training and model persistence via `joblib`
- Developed the **interactive Streamlit dashboard**, including a 3-page workflow (Data Exploration → ML Results → Prediction), session state management to carry model results across pages, and a custom CSS layer with animated metric cards
- Built an **interactive prediction interface** that dynamically generates input fields based on the trained model's feature set and displays both predicted class and probability scores using `predict_proba`
- Served as the project's **integration engineer**, consolidating independently developed modules into a single application by resolving merge conflicts, fixing compatibility issues, standardizing interfaces, and ensuring seamless communication between the data preprocessing, machine learning, backend API, and frontend layers
- Integrated the **Flask backend API** with the Streamlit frontend, enabling model training, prediction, and interactive Plotly visualizations (confusion matrix, feature importance, transit scatter plots)
- Performed debugging, testing, performance optimization, and final integration for the hackathon submission

**Stack:** `Python` `Streamlit` `Flask` `scikit-learn` `XGBoost` `Plotly` `pandas` `joblib` `NASA Exoplanet Archive`

</details>

<br>

---

## Certifications

**Artificial Intelligence Fundamentals** | Guayerd & IBM SkillsBuild · 2024  
257 hours of professional practice | ID: GUAYERD-IBM-IA-2025192130

**Mendix Rapid Developer Certification** | Mendix · 2025  
Official low-code development certification | Cert. No. 92922

**TensorFlow Developer Professional Certificate** | DeepLearning.AI / Coursera · 2026  
In progress — covers neural networks, CNNs, NLP, and time series with TensorFlow

---

## Recognition & Awards

**NASA Space Apps Challenge 2025** | Galactic Problem Solver | Oct 2025

**Postgraduate Seminar in Engineering Sciences** | TecNM Tijuana | Mar 2026  
Talk: *"Semantic Space Visualization in Augmented Reality"*

**Academic Week — Instituto Tecnológico de Tijuana** | Nov 2025  
Poster: *"Semantic Visualization"*

---

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:667eea,50:764ba2,100:f093fb&height=120&section=footer"/>
