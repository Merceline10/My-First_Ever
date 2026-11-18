
import base64
import requests

mermaid_code = """
flowchart TD
    classDef startend fill:#1e293b,stroke:#0f172a,stroke-width:2px,color:#ffffff,font-weight:bold
    classDef setup fill:#e0f2fe,stroke:#0284c7,stroke-width:2px,color:#0c4a6e
    classDef execution fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#78350f
    classDef synthesis fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d

    Ch1["<b>Chapter 1: Introduction & Problem Statement</b><br/>• Background & Context<br/>• Research Questions / Hypotheses<br/>• Scope & Significance"]:::startend
    Ch2["<b>Chapter 2: Literature Review</b><br/>• Synthesis of Existing Work<br/>• Identification of Research Gaps<br/>• Theoretical / Conceptual Framework"]:::setup
    Ch3["<b>Chapter 3: Methodology & Design</b><br/>• Sampling Strategy & Participants<br/>• Data Collection Instruments<br/>• Validity, Reliability & Ethics"]:::execution
    Ch4["<b>Chapter 4: Findings / Results</b><br/>• Objective Data Presentation<br/>• Statistical Outputs / Themes"]:::execution
    Ch5["<b>Chapter 5: Discussion & Analysis</b><br/>• Interpreting Results vs. Literature<br/>• Unexpected Findings<br/>• Study Limitations"]:::synthesis
    Ch6["<b>Chapter 6: Conclusion & Recommendations</b><br/>• Summary of Contributions<br/>• Practical Implications<br/>• Future Research Directions"]:::startend

    Ch1 --> Ch2 --> Ch3 --> Ch4 --> Ch5 --> Ch6
    Ch5 -. "Answers questions posed in" .-> Ch1
    Ch5 -. "Validates or challenges" .-> Ch2
"""

# Encode the Mermaid string to base64 and fetch the rendered image
graphbytes = mermaid_code.encode("utf8")
base64_string = base64.urlsafe_b64encode(graphbytes).decode("ascii")
url = f"https://mermaid.ink/img/{base64_string}"  # Change /img/ to /svg/ for vector output

response = requests.get(url)
with open("research_structure.png", "wb") as f:
  f.write(response.content)

print("Saved as research_structure.png")
