
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

    A["<span style='font-family:Georgia,serif;font-size:19px;font-weight:bold'>Research problem</span><br/><span style='font-family:Arial,sans-serif;font-size:15px;font-style:italic'>Difficulty of reliably distinguishing dryland forests from other vegetation types, particularly wooded grasslands and other herbaceous vegetation in Kenya's dryland ecosystems.</span>"]

    B["<span style='font-family:Georgia,serif;font-size:17px;font-weight:bold'>Dimension 1: Vegetation characteristics</span><br/><span style='font-family:Arial,sans-serif;font-size:13px'>Vegetation structure, Species composition, Canopy characteristics and Seasonal dynamics</span>"]

    C["<span style='font-family:Georgia,serif;font-size:17px;font-weight:bold'>Dimension 2: Observation characteristics</span><br/><span style='font-family:Arial,sans-serif;font-size:13px'>Spectral information, Spatial resolution, Temporal information and Sensor characteristics</span>"]

    D["<span style='font-family:Georgia,serif;font-size:17px;font-weight:bold'>Observable vegetation features</span><br/><span style='font-family:Arial,sans-serif;font-size:13px'>Spectral signatures, vegetation indices, structural features and temporal characteristics</span>"]

    E["<span style='font-family:Georgia,serif;font-size:17px;font-weight:bold'>Vegetation separability and discrimination</span><br/><span style='font-family:Arial,sans-serif;font-size:13px'>Distinguishability of dryland forests from other vegetation types</span>"]

    F["<span style='font-family:Georgia,serif;font-size:17px;font-weight:bold'>Classification and data integration strategies</span><br/><span style='font-family:Arial,sans-serif;font-size:13px'>Classification approaches, feature combinations and integration of different observation sources</span>"]

    G["<span style='font-family:Georgia,serif;font-size:19px;font-weight:bold'>Classification performance and robustness</span><br/><span style='font-family:Arial,sans-serif;font-size:15px'>Accuracy, uncertainty, class discrimination and transferability</span>"]

    H["<span style='font-family:Georgia,serif;font-size:19px;font-weight:bold'>Improved dryland forest identification and mapping</span><br/><span style='font-family:Arial,sans-serif;font-size:15px'>More reliable spatial representation of dryland forests in Kenya</span>"]

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
