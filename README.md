# AgriVoiceAI

**AI-powered IVR system for farmers** with rainfall prediction, crop suggestions, soil guidance, mandi prices, and QR traceability dashboard — integrated with Coordination Economy principles for reliable and scalable AI services.

---

## **Project Overview**

AgriVoiceAI enables farmers without smartphones to access AI-driven agricultural insights through a simple phone call. The system predicts rainfall, suggests crops based on soil and weather, provides fertilizer/water guidance, displays mandi prices, and tracks produce via QR codes linking to a dashboard.  

This project demonstrates:

- **End-to-end AI pipeline:** Prophet/LSTM rainfall models, crop recommendation logic  
- **Voice integration:** Twilio/Exotel IVR + Telugu/Hindi TTS  
- **Full-stack development:** Flask backend, React/Flask dashboard, QR code integration  
- **Coordination Economy:** Ensuring reliable, intelligence-supported, human-overseen AI systems

---

## **Key Features**

| Feature                         | Description |
|---------------------------------|-------------|
| Rainfall Prediction              | Uses Prophet/LSTM models to forecast rainfall for the next 30 days |
| Crop Suggestion                  | Recommends seasonal crops based on rainfall forecast and soil type |
| Soil Health Guidance             | Provides basic advice based on Soil Health Cards |
| Fertilizer & Water Advisory      | Suggests optimal fertilizer/water usage |
| Mandi Price Info                 | Real-time price information for crops in Telangana |
| IVR System                       | Farmers call a toll-free number and select options to hear AI responses |
| Text-to-Speech                   | Telugu/Hindi voice output for all options |
| QR Traceability Dashboard        | Scan QR codes to see farm history, crop data, photos, and videos |
| Coordination Economy Integration | Optimizes reliability, intelligence, and human oversight |

---

## **Tech Stack**

- **Programming & AI:** Python, Pandas, NumPy, Prophet, TensorFlow/Keras (optional LSTM)  
- **ML Deployment:** Flask API, Joblib model serialization  
- **Voice & IVR:** Twilio / Exotel, gTTS / Azure Speech API  
- **Frontend Dashboard:** React.js or Flask templates  
- **QR Code Generation:** pyqrcode, Pillow  
- **Data Sources:** IMD rainfall dataset, Telangana crop data, Soil Health Cards, Mandi prices  

---

## **Project Structure**



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

`

---

## **Installation & Setup**

1. Clone the repo:
bash
git clone https://github.com/rahulambaragonda/AgriVoiceAI.git
cd AgriVoiceAI
`

2. Install Python dependencies:

bash
pip install -r requirements.txt


3. Run Flask backend:

bash
cd backend
python ivr_api.py


4. Test IVR locally (via ngrok for public URL):

bash
ngrok http 5000


5. Run dashboard (React or Flask):

bash
cd frontend/dashboard
npm install
npm start


6. Test QR code generation:

bash
python backend/utils.py



## *Demo Workflow*

1. Farmer calls toll-free number → IVR menu options:

   * Press 1 for rainfall prediction
   * Press 2 for crop suggestions
   * Press 3 for soil guidance
   * Press 4 for fertilizer/water advice
   * Press 5 for mandi prices

2. TTS provides voice response in Telugu/Hindi

3. Scan QR code → opens dashboard showing farm history, crop data, photos/videos

*Demo Video:* demo/demo_video.mp4

---

## *Coordination Economy Integration*

* The system incorporates *Coordination Value Theorem*:

  V_system = C_reliability × I_intelligence × H_human_oversight

* *C_reliability:* Redundant checks on rainfall & crop data

* *I_intelligence:* ML models for rainfall & crop recommendation

* *H_human_oversight:* Manual verification & farmer feedback loop

> Applied these principles to ensure AI recommendations are trustworthy and scalable for rural farmers.

---

## *Resume & Portfolio Ready Bullets*

> * Developed AI-powered IVR system enabling farmers without smartphones to access rainfall forecasts, crop suggestions, soil guidance, and mandi prices. Integrated ML backend, Telugu/Hindi voice AI, and QR traceability dashboard.
> * Designed Prophet/LSTM rainfall forecasting model achieving *X% prediction accuracy* (replace with your testing results).
> * Built QR-based traceability dashboard linking farm-to-consumer journey, improving transparency and user engagement.
> * Applied Coordination Economy principles to optimize reliability, intelligence, and human oversight in AI services.

---

## *Future Enhancements*

* Integrate live weather APIs for real-time predictions
* Add farmer feedback & rating system
* Expand coverage to other states and languages
* Integrate voice-to-text for user query handling

---

## *License*

MIT License

