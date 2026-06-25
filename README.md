# GroupDNA_Analyzer
# GroupDNA  | WhatsApp Chat Analyzer
 "Spotify Wrapped, but for your friend group."

![GroupDNA Terminal Output](Link_To_Your_Screenshot_Here.png) 

## Overview
GroupDNA is a custom-built text-mining and behavioral analytics engine that runs entirely in the terminal. It ingests raw, exported WhatsApp chat files and transforms them into a formatted, highly visual UI report. 

Instead of relying on heavy data science libraries like Pandas or pre-built Regex parsers, this engine is built from scratch to handle messy, real-world conversational data, time-series binning, and rule-based classification.

##  Key Features
* **Custom Chat Parser:** Handles multi-line messages, skips system notifications, and scrubs timestamps without using `re`.
* **The 24-Hour Matrix:** Utilizes NumPy to generate an hourly activity heatmap rendered entirely with ASCII block characters.
* **Response Patterns:** Calculates average reply speeds and the longest consecutive "ghosting" streaks per user using `datetime` deltas.
* **Rule-Based Archetypes:** An algorithmic engine that scans for burst messages, capitalization ("shouting"), and specific keywords to assign dynamic titles (e.g., *The Spammer*, *The Night Owl*, *The Drama Queen*).
* **Console UI:** A highly polished, completely aligned terminal output using Python f-strings.

##  Tech Stack
* **Python 3** (Dictionaries, Sets, String Manipulation)
* **NumPy** (Matrix generation and argmax indexing)
* **Datetime** (Time-series mapping)
* *Note: Deliberately built without Pandas, Regex, or external plotting libraries to focus on algorithmic logic and native Python data structures.*

## How to Run It Yourself
1. Open WhatsApp on your phone, go to any group chat, and select **Export Chat** (Choose "Without Media").
2. Save the resulting text file in the same directory as this project.
3. Update the file path in the execution block of the `.ipynb` notebook:
   ```python
   chat_data = parse_whatsapp_chat('your_chat_name.txt')
