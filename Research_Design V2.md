%%{init: {'flowchart': {'curve': 'stepAfter'}}}%%
flowchart TD
    %% Styling to match your image
    classDef chapterBox fill:#fde8e8,stroke:#1f2937,stroke-width:1.5px,rx:8,ry:8,color:#111827,font-size:15px
    classDef subBox fill:#f8fafc,stroke:#3b82f6,stroke-width:1.5px,rx:8,ry:8,color:#1f2937,font-size:13px

    %% Chapter 1 (Exact match to your image)
    Ch1["<span style='color:#dc2626;font-weight:bold'>Chapter 1</span><br/><b>Introduction</b>"]:::chapterBox
    
    C1_1("Background of<br/>the study"):::subBox
    C1_2("Research problem<br/>or research<br/>questions"):::subBox
    C1_3("Research<br/>objectives"):::subBox
    C1_4("Rationale and<br/>significance of the<br/>study"):::subBox
    C1_5("Structure of the<br/>thesis"):::subBox

    Ch1 --> C1_1
    Ch1 --> C1_2
    Ch1 --> C1_3
    Ch1 --> C1_4
    Ch1 --> C1_5

 
