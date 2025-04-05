```mermaid
graph TD
    %% Input Section
    subgraph Input
        A1[Single Image]
        A2[Local Video]
        A3[Webcam Feed]
    end

    %% Processing Section
    subgraph Processing
        B1[OpenCV]
        B2[OpenVINO Inference Engine]
    end

    %% Output Section
    subgraph Output
        C1[Live Feed Display]
        C2[Detection Results]
        C3[Statistics: Count & Duration]
    end

    %% Web Interface Section
    subgraph Web Interface
        D1[User Controls]
        D2[Visualization]
    end
```
    %% Flow connectors (for vertical alignment)
    A1 --> B1
    A2 --> B1
    A3 --> B1
    B1 --> B2
    B2 --> C1
    B2 --> C2
    B2 --> C3
    C1 --> D2
    C2 --> D2
    C3 --> D2
    D1 --> D2
