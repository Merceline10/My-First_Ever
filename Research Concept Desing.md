
flowchart TB

    A["<b>Research problem</b><br/>Misclassification of dryland forests and other vegetation types"]

    B["<b>Field observations</b><br/>Vegetation structure, composition, field spectroscopy and reference data"]

    C["<b>Satellite observations</b><br/>Hyperspectral, multispectral, seasonal and spatial information"]

    D["<b>Spectral and vegetation feature analysis</b><br/>Spectral separability, vegetation indices, structural and temporal features"]

    E["<b>Classification model development</b><br/>Comparing classification approaches and data integration strategies"]

    F["<b>Independent validation and evaluation</b><br/>Forest discrimination, classification accuracy, uncertainty and transferability"]

    G["<b>Improved dryland land-cover mapping</b><br/>More reliable identification and representation of dryland forests in Kenya"]

    A --> B
    A --> C

    B --> D
    C --> D

    D --> E
    E --> F
    F --> G

    classDef blue fill:#E7EFFB,stroke:#E7EFFB,color:#111111,stroke-width:1px;
    classDef green fill:#E2F4EF,stroke:#E2F4EF,color:#111111,stroke-width:1px;
    classDef purple fill:#F1E9FA,stroke:#F1E9FA,color:#111111,stroke-width:1px;

    class A,G blue;
    class B,C,F green;
    class D,E purple;

    linkStyle default stroke:#666666,stroke-width:1.5px;

