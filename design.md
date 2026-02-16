# BharatSense – System Design

## 1. Architecture Overview
Hybrid Offline + Online AI Architecture

Client (Android App)
- Local AI model (quantized LLM)
- Speech-to-text engine
- Local knowledge base
- Form templates
- Document scanner

Cloud (Optional Sync)
- Updated scheme data
- Model updates
- Analytics dashboard
- Admin moderation panel

## 2. Data Flow
User Query → Local AI → Rule Validation → Response  
If internet available → Sync scheme updates → Update local cache

## 3. AI Stack
- On-device lightweight LLM
- Local embeddings for scheme retrieval
- Rule-based eligibility engine
- OCR for document scanning
- Multilingual speech pipeline

## 4. Privacy Architecture
- No raw user data sent to cloud
- Local encryption
- Differential privacy for analytics
- Explicit consent for sync

## 5. Offline Strategy
- Preloaded scheme datasets
- Cached FAQs
- Local vector database
- Model quantization for low RAM devices

## 6. Scalability
- CDN-based scheme updates
- Incremental model updates
- Horizontal scaling of cloud sync servers

## 7. Failure Handling
- Graceful degradation when offline
- Fallback to static knowledge base
- Error correction suggestions

## 8. Security
- Encrypted local storage
- Tamper detection
- Signed updates
- Minimal permissions model

## 9. Extensibility
- Plugin support for new schemes
- Modular language packs
- Integration hooks for government portals
