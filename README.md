# SENA ⚡ Twende Kazi — 3D Technology Landing Page, Meta WhatsApp Bot & GCP Stack

A futuristic, 3D-interactive technology landing page for **SENA** (*"Next-gen transit, hyper-fluid speed — Powering Mombasa"*), built to explore **image clarity**, **upfront fare & service transparency**, **Meta Business Account WhatsApp integration**, and compliance with the **Kenya Data Protection Act, 2019 (No. 24 of 2019)**, ready for hosting on **Google Cloud Platform (GCP)**.

---

## 🌟 Key Features

1. **Three 3D Visual Assets & Optical Clarity Engine (`public/index.html`, `public/styles.css`, `public/app.js`)**:
   - **3D Asset 01 (`public/assets/sena-street-ar.jpg`)**: Your Mombasa street-level augmented reality hologram photo (`SENA — Twende Kazi`, `Standard Bike KES 132`, `3 Seater Tuk-Tuk`) rendered in multi-plane 3D perspective with extruded HUD telemetry badges.
   - **3D Asset 02 (`public/assets/sena-mobile-splash.jpg`)**: Your SENA mobile splash screen (`Next-gen transit, hyper-fluid speed — POWERING MOMBASA`) mounted in a floating 3D chassis.
   - **3D Asset 03 (`public/assets/sena-3d-fleet.jpg`)**: Custom-generated **Full-3D Isometric Electric Fleet Render** (`E-TU TUK 01 [87% BATTERY] | RANGE 210 KM` and `E-BODA BODA 14 [92% BATTERY] | DEST. NYALI`) on a glowing telemetry dock against the Mombasa coastal skyline.
   - **Interactive 4K Optical Clarity Loupe & Z-Depth Controls**: Hover over any 3D card to inspect pixel-level details with a 2.6x optical magnifier lens, adjust 3D Z-axis depth extrusion (`15px–95px`), boost HDR micro-clarity, or toggle the LiDAR telemetry wireframe sweep.
   - **Three.js WebGL Spatial Background**: Real-time 3D telemetry grid and amber/cyan energy particles reacting to pointer coordinates.

2. **Meta Business Account WhatsApp Integration Chatbot (`server.js` + On-Page Widget)**:
   - Interactive floating WhatsApp Business Chatbot drawer linked to your **Meta Business Account** (`META_BUSINESS_ACCOUNT_ID`, `META_WABA_ID`, `META_PHONE_NUMBER_ID`, `META_WHATSAPP_DISPLAY_NUMBER`).
   - Click the `⚙️` icon inside the WhatsApp chat header to configure your exact Meta Business Account ID and WhatsApp Business Number directly in the UI, or set them via `.env` / Google Secret Manager.
   - Backend Express endpoints for official **Meta WhatsApp Cloud API (Graph API v21.0)**:
     - `GET /api/whatsapp/webhook` — Webhook verification (`hub.mode`, `hub.verify_token`, `hub.challenge`).
     - `POST /api/whatsapp/webhook` — Incoming message handler with `X-Hub-Signature-256` HMAC-SHA256 verification.
     - `POST /api/whatsapp/send` — Interactive chatbot dispatch & `https://wa.me/...` deep-link generator.

3. **Kenya Data Protection Act, 2019 (No. 24 of 2019)**:
   - Direct statutory links in the top compliance ribbon, hero section, dedicated legal compliance panel, WhatsApp chatbot header, and footer pointing to:
     - [Kenya Data Protection Act, 2019 (Kenya Law Official Statute)](http://kenyalaw.org:8181/exist/kenyalex/actview.xql?actid=No.%2024%20of%202019)
     - [Office of the Data Protection Commissioner (ODPC Kenya)](https://www.odpc.go.ke/data-protection-act/)
   - Interactive on-page **KDPA 2019 Privacy Charter Modal** detailing compliance with Sections 25, 26, 30, and 41.

4. **Google Cloud Platform (GCP) Hosting & Configuration**:
   - `Dockerfile` & `.dockerignore`: Containerized for **Google Cloud Run** (`0.0.0.0:8080`).
   - `cloudbuild.yaml`: Automated CI/CD pipeline syncing 3D assets to **Google Cloud Storage (GCS)** and deploying the container to **Cloud Run** via **Artifact Registry**.
   - `app.yaml`: Alternative configuration for **Google App Engine (Node.js 20)** with static asset edge caching.
   - `infra/main.tf`: **Terraform Infrastructure-as-Code** provisioning Cloud Run v2, Cloud Storage bucket for 3D media, and Secret Manager secrets for Meta WhatsApp tokens.
   - `.env.example`: Complete environment variable template for GCP & Meta Business Account credentials.
