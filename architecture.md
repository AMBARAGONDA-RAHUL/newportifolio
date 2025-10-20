## 🏗️ System Architecture — AgriVoiceAI
                  ┌─────────────────────────────
                  │ 👩‍🌾  Farmer (Caller)        
                  │  Dials Toll-Free Number     
                  └──────────────┬──────────────
                                 │
                                 ▼
                  ┌─────────────────────────────   
                  │ ☎️ IVR Gateway (Twilio/Exotel) 
                  │  Captures keypad/voice input   
                  └──────────────┬──────────────   
                                 │ Webhook
                                 ▼
                  ┌─────────────────────────────
                  │ 🧠 Flask Backend (ivr_api.py)
                  │  Handles call routing, logic 
                  │  & integrates ML components  
                  └─────┬───────────────────────
                        │
                        │ 1️⃣ Check data freshness  
                        │ 2️⃣ Auto-update if outdated
                        ▼
             ┌───────────────────────────────
             │ 📈 Data Updater (data_updater.py) 
             │  Fetches weather/soil data from  
             │  live APIs & updates CSV files   
             └─────────────────────────────────
                        │
                        ▼
            ┌─────────────────────────────      
            │ 📊 ML Models (Prophet / LSTM)       
            │  Forecast rainfall, suggest crops    
            │  Generate soil & fertilizer logic    
            └────────────────────────────      
                        │
                        ▼
           ┌───────────────────────────────     
           │ 🔉 Text-to-Speech Engine (gTTS /    
           │  Azure Speech / Polly)              
           │  Converts AI result → Telugu/Hindi  
           └───────────────────────────────    
                        │
                        ▼
             ┌──────────────────────────    
             │ ☎️ IVR Voice Response           
             │  Speaks AI insight to farmer    
             └─────────────────────────────   
                        │
                        ▼
        ┌──────────────────────────────────────  
        │ 📱 QR Traceability Dashboard (React)     
        │  Displays farm history, crop data, etc.  
        └─────────────────────────────────────── 

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
