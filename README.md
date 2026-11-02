
OpenPACS-Protect: Open DICOM Privacy & Anonymization Engine for Regional Hospitals
An open-source, lightweight, offline-first DICOM metadata anonymization and privacy sanitization engine built for public and regional hospital radiology departments in resource-constrained environments.
📌 Executive Overview
Public health facilities across sub-Saharan Africa face critical data security risks when transferring patient radiology scans (CT, MRI, X-ray) for external specialist consultations, research, or cross-hospital referrals. Proprietary enterprise PACS anonymization modules carry high licensing fees and often depend on cloud connectivity unavailable in semi-urban or rural health centers.
OpenPACS-Protect provides a self-contained, lightweight software node deployed directly on local hospital intranet servers or low-cost hardware. It automates DICOM header de-identification, redacts burned-in patient metadata from pixels using lightweight optical character recognition (OCR), and maintains cryptographic audit logs—ensuring complete HIPAA/GDPR compliance without subscription fees or external internet dependencies.
🎯 Technical Architecture & Features
🔒 Deterministic DICOM Header Stripping: Python engine leveraging pydicom to scrub 18 HIPAA/GDPR Protected Health Information (PHI) attributes (e.g., Patient Name, ID, Address, Referring Physician) while maintaining crucial clinical metadata (kVp, mAs, slice thickness, modality).
👁️ Burned-In Pixel Text Redactor: Lightweight computer-vision module using OpenCV and Tesseract OCR to detect and black-out patient metadata accidentally embedded into the image pixel matrix during acquisition.
📜 Local Cryptographic Audit Logger: SQLite-backed audit logging system recording all image export events and de-identification tasks locally on the hospital network.
🌐 Intranet Browser Interface: Clean, accessible browser GUI for radiographers and technicians to drag, drop, inspect, and batch-anonymize DICOM files.
🗺️ 12-Month Project Implementation Plan