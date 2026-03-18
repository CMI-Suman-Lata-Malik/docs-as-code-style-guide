# Voice and Tone

Before writing a single word for your audience, understand their persona. Consult with the marketing team and product management to understand the pain points of your personas, their pain points, and touch points with the product. Once you are armed with this knowledge, you will certainly arrive at this conclusion that good documentation for medical imaging software is not just about being correct. It is about being clear, consistent, and trustworthy, in a domain where ambiguity can affect clinical decisions.

This section defines the voice and tone standards for all documentation written for medical imaging informatics products.

---

## Core Principles

### 1. Clarity 
Write to be understood, not to impress. If a sentence can be simplified without losing meaning, simplify it.
Example:
**Avoid:**
> The system leverages advanced algorithmic processing to facilitate the retrieval of imaging data across distributed PACS nodes.

**Use:**
> The system retrieves imaging data from all connected PACS nodes.

---

### 2. Precision over approximation
Medical imaging software operates in clinical environments. Vague language creates risk. Be exact.

**Avoid:**
> The study may take some time to load depending on various factors.

**Use:**
> Load time depends on study size, network speed, and the number of series. A 1 GB study typically loads in under 10 seconds on a 1 Gbps network.

---

### 3. Active voice over passive voice
Active voice is shorter, clearer, and easier to translate.

**Avoid:**
> The DICOM header is parsed by the system before the image is displayed.

**Use:**
> The system parses the DICOM header before displaying the image.

---

### 4. Present tense over future tense
Write as if the software is in front of the user right now.

**Avoid:**
> Clicking Save will store the configuration to the database.

**Use:**
> Clicking Save stores the configuration to the database.

---

### 5. Human tone, not robotic tone
Clinical software documentation is often written in cold, mechanical language. This creates distance. Write as a knowledgeable colleague explaining something clearly — not as a legal disclaimer.

**Avoid:**
> Users must ensure that all required fields have been populated prior to  
> initiating the submission process.

**Use:**
> Fill in all required fields before you submit.

---

## Tone by Document Type

Different documents call for different tones. Use this table as a reference:

| Document Type | Tone | Example |
|---|---|---|
| User guide | Helpful, instructional | "Select the study you want to review." |
| Release notes | Factual, concise | "Fixed: Incorrect window level applied to CT series." |
| Error messages | Direct, non-alarming | "Cannot connect to PACS. Check your network settings." |
| API reference | Precise, technical | "Returns a 200 OK with the DICOM metadata object." |
| Troubleshooting | Calm, solution-focused | "If the study does not load, verify the AE Title is correct." |
| Known issues | Honest, clear workaround | "Workaround: Restart the viewer and reopen the study." |

---

## Writing for a Global Audience

Medical imaging software is used worldwide. Many readers are not native English speakers. Write with this in mind:

- Use short sentences — aim for 20 words or fewer per sentence
- Avoid idioms: "out of the box", "hit the ground running", "ballpark figure"
- Avoid humor or cultural references
- Spell out abbreviations on first use: PACS (Picture Archiving and  
  Communication System)
- Use the same term consistently — do not alternate between "study" and  
  "exam" to refer to the same concept

---

## Terminology Consistency

Always use the same term for the same concept throughout a document. Switching terms confuses readers and creates translation problems.

| Use This | Not This |
|---|---|
| study | exam, case, scan (unless clinically specific) |
| series | sequence, set |
| user | operator, end-user, customer |
| select | click, press, choose, hit, tap (pick one per platform) |
| configure | set up, setup, set-up |
| display | show, render, present |

> Full terminology standards are in  
> [03-medical-terminology.md](03-medical-terminology.md)

---

## What to Avoid

| Avoid | Why |
|---|---|
| Jargon without definition | Excludes new team members and global readers |
| Acronym stacking | "The DICOM SR UID in the MPPS RIS worklist" — unreadable |
| Negative instructions | "Do not fail to select the correct AE Title" |
| Warnings overused | If everything is a warning, nothing is |
| Filler phrases | "Please note that...", "It is important to...", "In order to..." |

---

## Quick Reference Checklist

Before publishing any documentation, verify:

- [ ] All sentences are 20 words or fewer where possible
- [ ] Active voice used throughout
- [ ] All abbreviations spelled out on first use
- [ ] Same term used consistently for the same concept
- [ ] No idioms or culturally specific language
- [ ] Tone matches the document type (see table above)
- [ ] All steps written in imperative mood ("Select", "Enter", "Click")