
flowchart TB

    Ch1["Chapter 1: Introduction and Problem Statement<br/>• Background and Context<br/>• Research Questions / Hypotheses<br/>• Scope and Significance"]

    Ch2["Chapter 2: Literature Review<br/>• Synthesis of Existing Work<br/>• Identification of Research Gaps<br/>• Theoretical / Conceptual Framework"]

    Ch3["Chapter 3: Methodology and Design<br/>• Sampling Strategy and Participants<br/>• Data Collection Instruments<br/>• Validity, Reliability and Ethics"]

    Ch4["Chapter 4: Findings / Results<br/>• Objective Data Presentation<br/>• Statistical Outputs / Themes"]

    Ch5["Chapter 5: Discussion and Analysis<br/>• Interpreting Results vs. Literature<br/>• Unexpected Findings<br/>• Study Limitations"]

    Ch6["Chapter 6: Conclusion and Recommendations<br/>• Summary of Contributions<br/>• Practical Implications<br/>• Future Research Directions"]

    Ch1 --> Ch2
    Ch2 --> Ch3
    Ch3 --> Ch4

    subgraph Discussion[" "]
        direction LR
        Ch4 --> Ch5
    end
    Ch5 --> Ch6
    Ch5 -.->|"Answers questions posed in"| Ch1
    Ch5 -.->|"Validates or challenges"| Ch2

    classDef dark fill:#1C2940,stroke:#111827,color:#FFFFFF,stroke-width:2px;
    classDef blue fill:#E5F3FF,stroke:#0085D0,color:#003B70,stroke-width:2px;
    classDef orange fill:#FFF0D5,stroke:#F28C00,color:#783900,stroke-width:2px;
    classDef green fill:#D9FBE7,stroke:#28A45A,color:#075B2A,stroke-width:2px;

    class Ch1,Ch6 dark;
    class Ch2 blue;
    class Ch3,Ch4 orange;
    class Ch5 green;
    style Discussion fill:transparent,stroke:transparent

