
# 🚗 L-Shape Reverse Vehicle Detection AI

This project detects if a vehicle successfully performs an **L-shape reverse movement** using an AI model trained with synthetic path data. It’s designed to evaluate driving candidates for license eligibility.

---

## 🧠 Features

- ✅ Vehicle detection using COCO-SSD (TensorFlow.js)
- ✅ Reverse path movement recognition using custom-trained LSTM model
- ✅ Detection logic runs in React frontend
- ✅ Displays result: **Pass or Fail** for license test

---

## 📂 Project Structure

```
.
├── public/
│   └── tfjs_model/           # TensorFlow.js model files (.json, .bin)
├── src/
│   ├── components/
│   │   ├── UploadVideo.js    # UI for uploading and detecting video
│   │   ├── ResultPage.js     # Displays results
│   │   └── AI.js             # TensorFlow.js model logic
│   ├── App.js                # Router setup
│   └── aiLogic.js            # Model execution logic
├── tfjs_model.zip            # Model zip (optional)
└── README.md
```

---

## 📥 How to Run

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/l-shape-detection-ai.git
cd l-shape-detection-ai
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Add Model Files

- Unzip `tfjs_model.zip` (from Colab output)
- Place the folder inside `public/`:

```
public/tfjs_model/
  ├── model.json
  └── group1-shard1of1.bin
```

### 4. Start the React App

```bash
npm start
```

The app will open in your browser at [http://localhost:3000](http://localhost:3000)

---

## 🎓 How the AI Works

- In Google Colab, synthetic trajectory data (with L-shaped paths) was generated
- A Keras LSTM model was trained to recognize valid L-shape reverse paths
- The model was exported and converted to TensorFlow.js format
- React reads the video input, detects vehicles using COCO-SSD
- Extracted path coordinates are passed into the model
- Final output: displays if the driver passes the L-shape reverse test

---

## 🧪 Tech Stack

- React.js
- TensorFlow.js
- COCO-SSD
- Python + TensorFlow (for training)
- Google Colab (for training and export)

---

## 📁 Google Colab Training Notebook

The model training notebook is available in this repo:  
📎 `LShapeDetection.ipynb`

---

## ✍️ License

This project is for educational/demo purposes only.

---

## 🙋‍♂️ Author

**Kishan Shan**  
GitHub: [Link](https://github.com/kishan-ctrl)  
University: KIU University – Sri Lanka
