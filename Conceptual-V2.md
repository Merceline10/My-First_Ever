
flowchart TD

    %% ==========================================
    %% A. RESEARCH PROBLEM
    %% ==========================================

    A["RESEARCH PROBLEM<br/>Spectral overlap and misclassification of<br/>open dryland forests, wooded grasslands<br/>and shrublands"]

    %% ==========================================
    %% B. ECOLOGICAL AND VEGETATION CHARACTERISTICS
    %% ==========================================

    subgraph ECO["B. ECOLOGICAL AND VEGETATION CHARACTERISTICS"]
        direction TB
        E1["Vegetation structure"]
        E2["Species composition"]
        E3["Canopy characteristics"]
        E4["Seasonal dynamics"]
        E5["Underlying ecological variability"]

        E1 --> E5
        E2 --> E5
        E3 --> E5
        E4 --> E5
    end

    %% ==========================================
    %% C. SENSOR AND REMOTE-SENSING OBSERVATIONS
    %% ==========================================

    subgraph SENSOR["C. SENSOR AND REMOTE-SENSING OBSERVATION CHARACTERISTICS"]
        direction TB

        subgraph HYP["Hyperspectral information"]
            direction TB
            H1["High spectral detail"]
            H2["Narrow spectral bands"]
            H3["Detailed vegetation properties"]
            H1 --> H3
            H2 --> H3
        end

        subgraph MULT["Multispectral information"]
            direction TB
            M1["Broader spectral bands"]
            M2["Temporal observations"]
            M3["Phenological trajectories"]
            M1 --> M3
            M2 --> M3
        end

        S1["Spectral resolution"]
        S2["Temporal resolution"]
        S3["Observation quality"]

        S1 --> HYP
        S1 --> MULT
        S2 --> MULT
        S3 --> HYP
        S3 --> MULT
    end

    %% ==========================================
    %% D. SPECTRAL AND TEMPORAL INFORMATION
    %% ==========================================

    subgraph INFO["D. SPECTRAL AND TEMPORAL INFORMATION AND VEGETATION SEPARABILITY"]
        direction TB

        I1["Hyperspectral spectral information"]
        I2["Multispectral spectral information"]
        I3["Temporal and phenological information"]

        I4["Integrated spectral and temporal information"]

        I5["Vegetation separability<br/>Spectral and temporal distinctiveness"]

        I6["Target vegetation formations<br/>Open dryland forests<br/>Wooded grasslands<br/>Shrublands<br/>Other relevant vegetation formations"]

        I1 --> I4
        I2 --> I4
        I3 --> I4
        I4 --> I5
        I5 --> I6
    end

    %% ==========================================
    %% E. CLASSIFICATION AND DATA INTEGRATION
    %% ==========================================

    subgraph CLASS["E. CLASSIFICATION APPROACHES AND DATA INTEGRATION"]
        direction TB

        C1["Hyperspectral classification"]
        C2["Multispectral classification"]
        C3["Temporal classification"]
        C4["Integrated hyperspectral and<br/>multispectral classification"]

        C5["Reference data quality<br/>Reference sample accuracy,<br/>representativeness and consistency"]

        C6["Reference samples interpreted<br/>from high-resolution imagery"]

        C6 --> C5
    end

    %% ==========================================
    %% F. PERFORMANCE AND MAPPING RELIABILITY
    %% ==========================================

    subgraph EVAL["F. CLASSIFICATION PERFORMANCE AND MAPPING RELIABILITY"]
        direction TB

        F1["CLASSIFICATION PERFORMANCE"]

        F2["Vegetation discrimination performance"]
        F3["Classification accuracy"]
        F4["Model transferability"]

        F1 --> F2
        F1 --> F3
        F1 --> F4

        F5["UNCERTAINTY ASSESSMENT"]

        F6["Classification uncertainty"]
        F7["Spatial distribution of uncertainty"]

        F5 --> F6
        F6 --> F7

        F8["MAPPING RELIABILITY"]

        F9["Confidence in vegetation class allocation"]
        F10["Reliability of spatial representation"]

        F8 --> F9
        F8 --> F10
    end

    %% ==========================================
    %% G. EXPECTED RESEARCH OUTCOME
    %% ==========================================

    G["EXPECTED RESEARCH OUTCOME<br/><br/>Improved identification, discrimination<br/>and spatial representation of<br/>dryland forests in Kenya"]

    %% ==========================================
    %% CROSS-COMPONENT CAUSAL RELATIONSHIPS
    %% ==========================================

    A --> E5

    E5 -->|"Influences vegetation responses"| I1
    E5 -->|"Influences vegetation responses"| I2
    E5 -->|"Influences seasonal responses"| I3

    H3 --> I1
    M3 --> I2
    M3 --> I3

    H3 -->|"Spectral discriminatory potential"| I1
    M3 -->|"Spectral and temporal information"| I2

    S1 -->|"Determines spectral detail"| H3
    S2 -->|"Determines temporal sampling"| I3
    S3 -->|"Controls observation quality"| I4

    I6 -->|"Separability informs classification"| C1
    I6 --> C2
    I6 --> C3
    I6 --> C4

    C1 --> F1
    C2 --> F1
    C3 --> F1
    C4 --> F1

    C5 -->|"Constrains validation quality"| F1

    F1 -->|"Performance evidence"| F8
    F5 -->|"Quantifies uncertainty"| F8

    F8 --> G

    %% ==========================================
    %% PROFESSIONAL COLOUR SCHEME
    %% ==========================================

    classDef problem fill:#FCE4D6,stroke:#C65911,stroke-width:2px,color:#702900;
    classDef ecology fill:#E2F0D9,stroke:#548235,stroke-width:1.5px,color:#274E13;
    classDef hyperspectral fill:#DDEBF7,stroke:#4472C4,stroke-width:1.5px,color:#17365D;
    classDef multispectral fill:#E4DFEC,stroke:#8064A2,stroke-width:1.5px,color:#403152;
    classDef sensor fill:#FFF2CC,stroke:#BF9000,stroke-width:1.5px,color:#674F00;
    classDef information fill:#DDEBF7,stroke:#2F75B5,stroke-width:1.5px,color:#17365D;
    classDef classification fill:#D9EAD3,stroke:#38761D,stroke-width:1.5px,color:#274E13;
    classDef performance fill:#FCE4D6,stroke:#C65911,stroke-width:1.5px,color:#783F04;
    classDef uncertainty fill:#F4CCCC,stroke:#CC0000,stroke-width:1.5px,color:#660000;
    classDef reliability fill:#D9EAD3,stroke:#38761D,stroke-width:2px,color:#274E13;
    classDef outcome fill:#C6E0B4,stroke:#548235,stroke-width:3px,color:#274E13;

    class A problem;
    class E1,E2,E3,E4,E5 ecology;
    class H1,H2,H3 hyperspectral;
    class M1,M2,M3 multispectral;
    class S1,S2,S3 sensor;
    class I1,I2,I3,I4,I5,I6 information;
    class C1,C2,C3,C4,C5,C6 classification;
    class F1,F2,F3,F4 performance;
    class F5,F6,F7 uncertainty;
    class F8,F9,F10 reliability;
    class G outcome;

    style ECO fill:#F2F8EC,stroke:#548235,stroke-width:2px
    style SENSOR fill:#FFF9E6,stroke:#BF9000,stroke-width:2px
    style HYP fill:#EDF4FC,stroke:#4472C4,stroke-width:1px
    style MULT fill:#F3EFF8,stroke:#8064A2,stroke-width:1px
    style INFO fill:#EEF5FB,stroke:#2F75B5,stroke-width:2px
    style CLASS fill:#F1F8EE,stroke:#38761D,stroke-width:2px
    style EVAL fill:#FFF4EF,stroke:#C65911,stroke-width:2px
