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
    A1 -->|Input| B1
    A2 -->|Input| B1
    A3 -->|Input| B1
    B1 -->|Frame Processing| B2
    B2 -->|Inference Results| C1
    B2 -->|Inference Results| C2
    B2 -->|Inference Results| C3
    C1 -->|Display| D2
    C2 -->|Display| D2
    C3 -->|Display| D2
    D1 -->|User Interaction| D2
```
