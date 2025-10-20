## 🏗️ System Architecture — AgriVoiceAI
                        ┌──────────────────────────────┐
                        │ 👩‍🌾  Farmer (Caller)         │
                        │  Calls Toll-Free Number      │
                        └──────────────┬───────────────┘
                                       │
                                       ▼
                        ┌──────────────────────────────┐
                        │ ☎️  IVR Gateway (Twilio)     │
                        │  Captures keypad/voice input │
                        └──────────────┬───────────────┘
                                       │ Webhook (HTTP POST)
                                       ▼
                        ┌──────────────────────────────────┐
                        │ 🧠 Flask Backend (API Layer)    │
                        │  Logic: routes + responses       │
                        └──────────────┬──────────────────┘
                                       │
                      ┌────────────────┴────────────────┐
                      ▼                                 ▼
          ┌────────────────────────────┐     ┌────────────────────────────────┐
          │ 🌦️ Data Fetcher (APIs)     │     │ 🤖 ML Engine (Prophet/LSTM)   │
          │ - Weather & Soil APIs      │     │ - Forecast rainfall            │
          │ - Updates internal CSVs    │     │ - Crop/Fertilizer logic        │
          └────────────────────────────┘     └────────────────────────────────┘
                      │                                 │
                      └────────────────┬────────────────┘
                                       ▼
                        ┌──────────────────────────────┐
                        │ 🔉 Text-to-Speech Engine     │
                        │  Converts AI text → Telugu   │
                        │  / Hindi voice response      │
                        └──────────────┬───────────────┘
                                       │
                                       ▼
                        ┌────────────────────────────────────┐
                        │ ☎️ IVR Response to Farmer         │
                        │  Speaks forecast/advice           │
                        └───────────────────────────────────┘

---

### 🧩 **Data Flow Summary**

| Step | Component | Function |
|------|------------|-----------|
| 1️⃣ | **Farmer** | Calls toll-free number |
| 2️⃣ | **IVR Gateway** | Captures input (keypad or speech) |
| 3️⃣ | **Flask Backend** | Handles call flow, invokes ML logic |
| 4️⃣ | **Data Updater** | Fetches live rainfall/soil data automatically |
| 5️⃣ | **ML Models** | Predicts rainfall & suggests crops |
| 6️⃣ | **TTS Engine** | Converts AI insights to Telugu/Hindi speech |
| 7️⃣ | **IVR Output** | Plays AI-generated voice response |
| 8️⃣ | **QR Dashboard** | Displays farm data & traceability info |

---

### 🧠 **End-to-End Flow (In Words)**

A farmer dials a toll-free number which routes through an **IVR Gateway** like Twilio or Exotel. The **Flask Backend** receives the webhook, processes voice or keypad input, and triggers a **Data Updater** to fetch the latest rainfall, soil, and weather information via live APIs. This data is stored automatically in CSV files for ML pipelines. The **ML Models (Prophet/LSTM)** analyze patterns to predict rainfall and recommend crops. The **Text-to-Speech Engine** converts AI insights into local language audio (Telugu/Hindi), which is played back to the farmer in real-time through IVR. Meanwhile, the **QR Traceability Dashboard** visualizes all farm and crop data for monitoring and transparency.

---

### 🌾 **Key Highlights**

- **Fully automated data pipeline** — no manual CSV updates needed  
- **Voice-first AI platform** — built for accessibility via phone calls  
- **Real-time intelligence** — AI models update continuously with fresh data  
- **Transparent traceability** — QR dashboard connects farmers and buyers  
- **Easily scalable** — plug in new APIs, states, or languages anytime  

---
