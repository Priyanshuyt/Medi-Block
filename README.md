# Medi-Block

MediBlock is an AI + Blockchain-powered solution that detects, reports, and logs counterfeit or expired medicines in real-time. It empowers citizens and health authorities to ensure medicine authenticity through a combination of computer vision, OCR, IPFS-based file storage, and blockchain logging for tamper-proof evidence.

🚨 The Problem We're Solving
Every year, millions of people — especially in rural and underserved regions — unknowingly consume expired or counterfeit medicines. These drugs often originate from unauthorized vendors, rejected pharma batches, or unverified donations. Due to the lack of infrastructure to trace such incidents, no proper reporting or accountability system exists.

Counterfeit medicines:

Cause preventable deaths and prolonged illnesses.

Erode trust in healthcare and pharmaceutical supply chains.

Are difficult to detect without lab testing or advanced scanners.

MediBlock solves this problem by putting detection, verification, and reporting in the hands of the public — powered by modern technologies.

✅ What MediBlock Does
Scans medicine strip images through the smartphone camera.

Uses OCR to extract and validate expiry dates and batch information.

Uses a lightweight AI model to detect counterfeit packaging (fake logos, layout mismatches, etc.).

Generates a SHA-256 hash of the full report.

Uploads image and report metadata to IPFS for decentralized storage.

Logs the hash and IPFS CID on Polygon blockchain for immutability.

Flags suspicious medical stores based on user reports and clusters.

Admin dashboard shows visualized data for investigation and alerts.

👥 Who Uses MediBlock
Consumers checking their own medicines.

Pharmacy buyers and clinic staff screening bulk purchases.

Health workers in rural areas.

Government departments wanting evidence-backed audit trails.

NGOs distributing medicines during relief efforts.

🌐 How It Works – Workflow Summary
The user opens the mobile app and clicks a picture of the medicine strip.

OCR extracts expiry and batch details from the text on the strip.

A TensorFlow Lite model checks whether the image matches known fake/real medicine patterns.

The backend generates a SHA-256 hash of the report (image + results).

The image and report are uploaded to IPFS via web3.storage.

The report hash and IPFS link are logged on the Polygon Mumbai blockchain.

All reports are stored in Firebase Firestore for real-time access.

Admins view heatmaps of risky stores, track trends, and can investigate flagged pharmacies.

🧠 Technologies Behind MediBlock
Frontend:
Flutter – Cross-platform mobile development for Android and iOS.

Backend:
FastAPI (Python) – High-performance async API server.

Tesseract OCR / Google Cloud Vision – Text extraction from medicine strip.

TensorFlow Lite – Real-time AI model for fake/real packaging detection.

IPFS (via web3.storage) – Decentralized file storage of images and metadata.

Polygon Mumbai Blockchain – Logs hashes and IPFS links immutably.

Firebase Firestore & Storage – For structured user data, authentication, and real-time reports.

Google Maps API – For locating nearby pharmacies and tracking risky areas.

ReactJS Admin Dashboard (optional) – For authorities to manage and monitor reports.

📊 Data Processing Pipeline
Image Capture: User takes or uploads a photo.

Preprocessing: Image is resized and normalized.

OCR Module: Extracts date, brand, batch from image using Tesseract or Vision API.

AI Classification: Determines if the medicine is fake based on packaging features.

Report Hashing: SHA-256 hash generated from full report content.

IPFS Upload: Full report + image sent to IPFS (returns CID).

Blockchain Log: CID + hash sent to smart contract (testnet).

Storage & Access: Firebase stores everything for future retrieval.

Admin Analysis: D3.js charts and React dashboard show live fraud hotspots.

🔐 Why Blockchain?
Even if the database is compromised or the app is tampered with, the hash and IPFS CID on blockchain remain verifiable. This ensures:

Evidence cannot be deleted or edited.

Users and government bodies can verify authenticity without needing full app access.

Real-world cases can be escalated for legal action.
