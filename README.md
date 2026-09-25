# minor_-project_1
minor_project_1 GroupDNA: WhatsApp Hostel Group Chat Analytics
# GroupDNA — WhatsApp Group Chat Analytics

## Minor Project 1 — Data Science & Data Analytics

**Student Name:** Naga Chaitanya
**Project Name:** GroupDNA
**Project Type:** Minor Project 1
**Technology:** Python, NumPy
**Dataset:** `hostel_bois.txt`

---

## 1. Project Overview

**GroupDNA** is a WhatsApp hostel group chat analytics project.

The project analyzes a raw WhatsApp group chat export and converts the messages into useful information about the group's communication patterns.

The project answers questions such as:

* Who sends the most messages?
* Who is the most active member?
* What is the busiest day?
* What is the busiest hour?
* What words are commonly used?
* How quickly do members respond?
* When does the group become silent?
* What communication style does each member have?

The final output is a **GroupDNA report** containing activity statistics and personality archetypes for the group members.

---

## 2. Objective

The main objective of this project is to demonstrate how raw chat data can be cleaned, processed, analyzed, and converted into meaningful information using Python.

The project uses:

* Python fundamentals
* Lists and dictionaries
* Functions
* String processing
* Date and time handling
* NumPy arrays
* Basic data analysis

---

## 3. Dataset

The supplied dataset is:

```text
hostel_bois.txt
```

It contains a synthetic WhatsApp hostel group conversation.

### Dataset information

* **Physical lines:** 3,178
* **Sender messages:** 3,174
* **Participants:** 6
* **Calendar days:** 60
* **Media entries:** 32
* **Deleted-message entries:** 15
* **System messages:** 4

Media and deleted messages are retained for activity/message counts where required, but their unavailable content is excluded from word-frequency and message-length analysis.

---

## 4. Technologies Used

### Python

Python is used for:

* Reading the chat file
* Parsing messages
* Cleaning text
* Calculating statistics
* Finding dates and times
* Creating reports
* Detecting personality patterns

### NumPy

NumPy is used for numerical analysis, especially for the activity heatmap.

A **6 × 24 NumPy matrix** is created to represent:

* Rows → participants
* Columns → hours of the day

---

## 5. Project Features

The project contains the following major features.

### Feature 1 — Chat Parser

The raw WhatsApp export is read and converted into structured message information.

The parser identifies:

* Date
* Time
* Sender
* Message text

It also handles special cases such as:

* Media messages
* Deleted messages
* System messages
* Multi-line messages

---

### Feature 2 — Group Overview

This section provides an overall summary of the group.

It calculates:

* Total messages
* Number of participants
* Number of active days
* Messages sent by each participant

---

### Feature 3 — Most Active Day and Hour

The project analyzes timestamps to find:

* Most active day
* Most active hour
* Number of messages during the busiest periods

This helps understand when the group is most active.

---

### Feature 4 — NumPy Activity Heatmap

A NumPy matrix is created with:

```text
6 participants × 24 hours
```

Each cell represents the number of messages sent by a participant during a particular hour.

This gives a simple view of each person's activity pattern.

---

### Feature 5 — Top Words

The project analyzes message text to identify frequently used words.

Basic cleaning is performed by:

* Converting text to lowercase
* Removing unnecessary punctuation
* Ignoring unsuitable entries
* Counting word occurrences

Common words are then displayed with simple text bars.

---

### Feature 6 — Response Speed and Silent Streaks

The project studies communication behaviour.

It calculates response-time information based on consecutive messages from different participants.

It also identifies periods where the group remains inactive for longer periods.

These statistics help describe the group's communication rhythm.

---

### Feature 7 — Personality Archetype Detection

Each participant is assigned one exclusive communication archetype based on measurable chat behaviour.

The project includes archetypes such as:

* **THE SPAMMER**
* **THE GROUP MOM**
* **THE NIGHT OWL**
* **THE STORYTELLER**
* **THE DRAMA QUEEN**
* **THE GHOST**

The archetype is determined from the participant's activity and message characteristics rather than from personal information outside the dataset.

---

### Bonus — THE HOSTEL PLANNER

An additional archetype called:

**THE HOSTEL PLANNER**

is included as a bonus feature.

It identifies communication patterns related to hostel planning and coordination.

---

### Feature 8 — Final GroupDNA Report

The final section combines the calculated statistics into one readable report.

The report includes:

* Group summary
* Participant statistics
* Activity patterns
* Response behaviour
* Silent periods
* Personality archetypes
* Group observations

---

## 6. Project Workflow

The overall workflow is:

```text
WhatsApp Chat Export
        ↓
Read Raw Text File
        ↓
Parse Chat Messages
        ↓
Clean and Structure Data
        ↓
Calculate Statistics
        ↓
NumPy Activity Analysis
        ↓
Word Frequency Analysis
        ↓
Response & Silence Analysis
        ↓
Archetype Detection
        ↓
Final GroupDNA Report
```

---

## 7. Project Constraints

The project follows the restrictions given in the project brief.

The implementation does **not** use:

* Pandas
* `collections.Counter`
* Regular expressions
* Matplotlib
* Seaborn
* Plotly
* Pre-built WhatsApp analytics libraries

The analysis is implemented using Python fundamentals and NumPy.

---

## 8. How to Run the Project

### Step 1

Install Python and Jupyter Notebook, or use Google Colab.

### Step 2

Keep these files in the same folder:

```text
GroupDNA_NagaChaitanya_24R11A0102.ipynb
hostel_bois.txt
```

### Step 3

Open the notebook.

### Step 4

Run all cells from top to bottom.

### Step 5

The notebook will generate the complete GroupDNA analysis and final report.

---

## 9. Expected Output

The notebook produces:

1. Parsed chat information
2. Group overview
3. Participant message statistics
4. Busiest day
5. Busiest hour
6. NumPy activity heatmap
7. Top-word analysis
8. Response-time analysis
9. Silent-streak analysis
10. Personality archetypes
11. Hostel Planner bonus archetype
12. Final GroupDNA report

---

## 10. Participants

The supplied dataset contains six participants.

The project analyzes each participant using only the information available in the chat dataset.

The detected archetypes in the completed analysis are:

| Participant | Detected Archetype |
| ----------- | ------------------ |
| Rahul       | The Spammer        |
| Priya       | The Group Mom      |
| Aman        | The Night Owl      |
| Karan       | The Storyteller    |
| Neha        | The Drama Queen    |
| Vikas       | The Ghost          |

---

## 11. Why This Project Is Useful

This project demonstrates how simple programming techniques can be used to analyze real-world-style text data.

The same concepts can be applied to:

* Social media analysis
* Customer reviews
* Chat applications
* Survey responses
* Communication analysis
* Business text analytics

It also demonstrates the basic workflow of a data analytics project:

**Collect → Clean → Process → Analyze → Interpret → Report**

---

## 12. Limitations

This project has some limitations:

* The dataset is synthetic.
* Personality archetypes are based only on chat behaviour.
* They should not be treated as psychological assessments.
* Deleted messages do not provide their original text.
* Media-only messages do not contain usable textual content.
* The analysis depends on the quality and format of the supplied WhatsApp export.

---

## 13. Reflection

The most challenging part of the project was handling a raw WhatsApp export because not every line represents a normal user message.

Special cases such as system messages, media placeholders, deleted messages, and continuation lines require different handling.

The NumPy heatmap was useful because it converts timestamp information into a compact **6 × 24 activity matrix**.

The archetype section then combines different chat statistics to assign one exclusive communication archetype to each participant.

If the project were developed further, additional validation checks and more advanced text-analysis features could be added.

---

## 14. AI-Assistance Disclosure

AI tools were used as a learning and development aid during the project.

AI assistance was used for:

* Understanding the project requirements
* Structuring parts of the solution
* Debugging and improving code
* Explaining Python concepts

The final project was reviewed and tested using the supplied dataset.

---

## 15. Conclusion

**GroupDNA** demonstrates how Python and NumPy can be used to transform a raw WhatsApp hostel group chat into meaningful analytical information.

The project combines message parsing, activity analysis, word analysis, response behaviour, NumPy-based numerical analysis, and communication archetype detection into one complete data analytics workflow.

---

## Author

**Naga Chaitanya**

**Project:** GroupDNA — WhatsApp Group Chat Analytics

**Minor Project 1 — Data Science & Data Analytics**
