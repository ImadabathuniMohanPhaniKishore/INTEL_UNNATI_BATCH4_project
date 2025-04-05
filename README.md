```mermaid
graph TD
    subgraph Input
        A1[Single Image]
        A2[Local Video]
        A3[Webcam Feed]
    end

    subgraph Processing
        B1[OpenCV]
        B2[OpenVINO Inference Engine]
    end

    subgraph Output
        C1[Live Feed Display]
        C2[Detection Results]
        C3[Statistics: Count & Duration]
    end

    subgraph Web Interface
        D1[User Controls]
        D2[Visualization]
    end
```

```mermaid
graph TD
    A1[Single Image] --> B1[OpenCV]
    A2[Local Video] --> B1
    A3[Webcam Feed] --> B1
    B1 --> B2[OpenVINO Inference Engine]
    B2 --> C1[Live Feed Display]
    B2 --> C2[Detection Results]
    B2 --> C3[Statistics: Count & Duration]
    C1 --> D2[Web Interface: Visualization]
    C2 --> D2
    C3 --> D2
    D1[User Controls] --> D2
```


### 🧠 Architecture Explanation

#### 🔹 Input  
The application accepts various input sources:
- Single images  
- Local video files  
- Webcam feeds  

---

#### 🔹 Processing  
Frames from the input sources are:
- Processed using **OpenCV**  
- Analyzed with the **OpenVINO Inference Engine** for **person detection**  

---

#### 🔹 Output  
The output includes:
- **Live feed display**  
- **Detection results**  
- **Statistics**, such as:
  - Count of people in the frame  
  - Duration each person stays  

---

#### 🔹 Web Interface  
Users interact via a web interface that provides:
- **User controls**
- **Visualization of detection results**  

---

✅ This architecture enables **real-time people counting** with a clean, interactive interface and insightful visual feedback.
