
markdown
<h1 align="center">🌾 AgriVoiceAI</h1>

<p align="center">
  <b>AI-powered IVR system for farmers</b> — providing rainfall prediction, crop suggestions, soil guidance, mandi prices, and QR traceability dashboard.  
  <br>Built with <b>Coordination Economy</b> principles for <i>reliable, intelligent, and human-overseen</i> AI services.
</p>

---

## 📜 Overview

**AgriVoiceAI** empowers farmers — even those without smartphones — to access AI-driven agricultural insights using a simple **phone call**.  
The system predicts rainfall, recommends crops, provides fertilizer/water guidance, displays mandi prices, and tracks produce via **QR-coded dashboards**.

### 🚀 Core Capabilities

- 🌦️ **Rainfall Prediction:** Prophet/LSTM models for 30-day weather forecasts  
- 🌾 **Crop Suggestion:** Based on rainfall, soil type, and seasonal data  
- 🧪 **Soil & Fertilizer Guidance:** Soil Health Card + nutrient advisory  
- 🏷️ **QR Traceability:** Scan to view farm/crop history, media, and supply chain  
- 📞 **Voice IVR (Telugu/Hindi):** Twilio/Exotel integration + gTTS / Azure Speech  
- 🧩 **Coordination Economy Layer:** Ensures reliability × intelligence × human oversight  

---

## ⚙️ Tech Stack

| Layer | Technologies |
|-------|---------------|
| **AI/ML Models** | Python, Pandas, NumPy, Prophet, TensorFlow/Keras |
| **Backend API** | Flask, FastAPI (optional), Joblib for model deployment |
| **Frontend Dashboard** | React.js / Flask templates, Chart.js |
| **Voice & IVR** | Twilio / Exotel, gTTS / Azure Speech API |
| **QR Generation** | pyqrcode, Pillow |
| **Data Sources** | IMD rainfall dataset, Telangana crop data, Soil Health Cards, Mandi prices |

---

## 🧠 Project Structure

```

AgriVoiceAI/
│
├── data/
│   ├── rainfall.csv
│   ├── crop_data.csv
│   ├── soil_data.csv
│   ├── mandi_prices.csv
│
├── backend/
│   ├── rainfall_model.py
│   ├── crop_suggestion.py
│   ├── ivr_api.py
│   ├── tts.py
│   └── utils.py
│
├── frontend/
│   ├── dashboard/
│   │   ├── App.js
│   │   └── components/
│   │       └── QRViewer.js
│
├── qr_codes/
├── demo/
├── requirements.txt
├── README.md
└── LICENSE

````

---

## 🧩 Installation & Setup

```bash
# 1️⃣ Clone the repository
git clone https://github.com/rahulambaragonda/AgriVoiceAI.git
cd AgriVoiceAI

# 2️⃣ Install dependencies
pip install -r requirements.txt

# 3️⃣ Run Flask backend
cd backend
python ivr_api.py

# 4️⃣ Expose to internet using ngrok (for IVR testing)
ngrok http 5000

# 5️⃣ Run React dashboard
cd ../frontend/dashboard
npm install
npm start

# 6️⃣ Generate QR codes
python ../backend/utils.py
````

---

## 📞 Demo Workflow

1. 👩‍🌾 Farmer dials toll-free number → hears IVR menu

   * Press 1 → Rainfall prediction
   * Press 2 → Crop suggestions
   * Press 3 → Soil guidance
   * Press 4 → Fertilizer/water advice
   * Press 5 → Mandi prices

2. 🗣️ TTS plays audio in Telugu/Hindi

3. 📱 Farmer receives/prints QR → scanned on dashboard

4. 🖥️ Dashboard shows farm history, data, and crop cycle

🎥 *Demo Video:* `demo/demo_video.mp4`

---

## 🌐 Coordination Economy Integration

> Applying the **Coordination Value Theorem**
> `V_system = C_reliability × I_intelligence × H_human_oversight`

| Component               | Implementation                                     |
| ----------------------- | -------------------------------------------------- |
| **C (Reliability)**     | Multi-source data validation, error tolerance      |
| **I (Intelligence)**    | ML models (Prophet/LSTM) for rainfall & crop logic |
| **H (Human Oversight)** | Farmer feedback loop, admin data verification      |

🧩 These principles ensure that AgriVoiceAI’s recommendations are **trustworthy, auditable, and scalable** — vital for rural adoption.

---

## 💼 Resume-Ready Highlights

> ✅ Built AI-powered IVR enabling farmers to access rainfall forecasts, crop suggestions, soil & fertilizer guidance, and mandi prices via voice.
> ✅ Integrated ML backend (Prophet/LSTM), Telugu/Hindi voice synthesis, and QR traceability dashboard.
> ✅ Achieved *X%* rainfall forecast accuracy (update with test result).
> ✅ Applied Coordination Economy principles to ensure reliability, intelligence, and human oversight in agricultural AI systems.

---

## 🔮 Future Enhancements

* 🌦️ Integrate **live weather APIs** for real-time predictions
* 💬 Add **farmer feedback & rating** system
* 🌎 Expand **regional language** support across India
* 🎙️ Enable **voice-to-text AI queries**
* ☁️ Host on AWS Lambda + S3 for scalable deployment

---

## 📜 License

This project is licensed under the **MIT License** — see [LICENSE](./LICENSE) for details.

---

<p align="center">
  Built with ❤️ by <b>Rahul Ambaragonda</b>  
  <br>
  <a href="https://linkedin.com/in/rahulambaragonda">LinkedIn</a> • 
  <a href="https://github.com/rahulambaragonda">GitHub</a> • 
  <a href="mailto:rahulambaragonda9@gmail.com">Email</a>
</p>
```

---

Would you like me to make a **matching LinkedIn Featured Post (with hashtags + recruiter-focused caption)** that markets this project and ties it to your *Coordination Economy research* next?
It’ll be written to *boost engagement + job visibility*.
