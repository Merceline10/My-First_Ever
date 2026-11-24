
# Conceptual Framework

```mermaid
%%{init: {
  "theme": "base",
  "themeVariables": {
    "fontFamily": "Arial, sans-serif",
    "fontSize": "14px",
    "lineColor": "#666666"
  },
  "flowchart": {
    "htmlLabels": true,
    "curve": "linear",
    "nodeSpacing": 25,
    "rankSpacing": 30
  }
}}%%

flowchart TB

    A["<span style='font-family:Georgia,serif;font-size:19px;font-weight:bold'>Research Problem</span><br/><span style='font-family:Arial,sans-serif;font-size:16px;font-style:italic'>Difficulty of reliably distinguishing dryland forests from other vegetation types, particularly wooded grasslands and other herbaceous vegetation in Kenya's dryland ecosystems.</span>"]

    B["<span style='font-family:Georgia,serif;font-size:17px;font-weight:bold'>Dimension 1: Vegetation Characteristics</span><br/><span style='font-family:Arial,sans-serif;font-size:14px'>Vegetation Structure, Species Composition, Canopy Characteristics and Seasonal Dynamics</span>"]

    C["<span style='font-family:Georgia,serif;font-size:17px;font-weight:bold'>Dimension 2: Observation Characteristics</span><br/><span style='font-family:Arial,sans-serif;font-size:14px'>Spectral information, Spatial Resolution, Temporal Information and Sensor Characteristics</span>"]

    D["<span style='font-family:Georgia,serif;font-size:17px;font-weight:bold'>Observable Vegetation Features</span><br/><span style='font-family:Arial,sans-serif;font-size:14px'>Spectral signatures, Vegetation indices, Structural features and Temporal characteristics</span>"]

    E["<span style='font-family:Georgia,serif;font-size:17px;font-weight:bold'>Vegetation Separability and Discrimination</span><br/><span style='font-family:Arial,sans-serif;font-size:14px'>Distinguishability of dryland forests from other vegetation types</span>"]

    F["<span style='font-family:Georgia,serif;font-size:17px;font-weight:bold'>Classification and Data Integration Strategies</span><br/><span style='font-family:Arial,sans-serif;font-size:14px'>Classification approaches, Feature combinations and Integration of different observation sources</span>"]

    G["<span style='font-family:Georgia,serif;font-size:17px;font-weight:bold'>Classification Performance and Robustness</span><br/><span style='font-family:Arial,sans-serif;font-size:14px'>Accuracy, Uncertainty, Class discrimination and Transferability</span>"]

    H["<span style='font-family:Georgia,serif;font-size:19px;font-weight:bold'>Improved Dryland Forest identification and Mapping</span><br/><span style='font-family:Arial,sans-serif;font-size:16px'>More reliable spatial representation of Dryland Forests in Kenya</span>"]

    A --> B
    A --> C
    B --> D
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H

    classDef blue fill:#E7EFFB,stroke:#E7EFFB,color:#111111,stroke-width:1px;
    classDef green fill:#E2F4EF,stroke:#E2F4EF,color:#111111,stroke-width:1px;
    classDef purple fill:#F1E9FA,stroke:#F1E9FA,color:#111111,stroke-width:1px;

    class A,G blue;
    class B,C,F green;
    class D,E,G purple;
    class H blue;

    linkStyle default stroke:#666666,stroke-width:1.5px;

```
