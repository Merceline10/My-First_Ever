
flowchart TD

    A["Research Problem and Knowledge Gap"]
    B["Study Area and Reference Data Development"]
    C["Remote-Sensing Data Acquisition and Pre-processing"]
    D["Hyperspectral Data"]
    E["Multispectral Data"]
    F["Feature Analysis and Vegetation Discrimination"]
    G["Comparative Classification Experiments"]
    G1["Approach A<br/>Hyperspectral"]
    G2["Approach B<br/>Multispectral"]
    G3["Approach C<br/>Integrated"]
    H["Independent Validation and Comparative Evaluation"]
    I["Improved Dryland Forest Mapping and Monitoring"]

    A --> B --> C
    C --> D
    C --> E
    D --> F
    E --> F
    F --> G
    G --> G1
    G --> G2
    G --> G3
    G1 --> H
    G2 --> H
    G3 --> H
    H --> I

    classDef green fill:#dceee7,stroke:#7aa890,color:#000;
    classDef blue fill:#dce7f4,stroke:#7c9bc0,color:#000;
    classDef purple fill:#ebe3f5,stroke:#9b86b8,color:#000;
    classDef orange fill:#f3e5d6,stroke:#c29b72,color:#000;

    class B,F green;
    class C,I blue;
    class G purple;
    class D,E,H orange;
