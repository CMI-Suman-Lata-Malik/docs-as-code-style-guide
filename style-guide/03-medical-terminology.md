# Medical Terminology Standards

Consistent terminology is the foundation of trustworthy clinical software documentation. A single ambiguous term — "study" vs "exam", "error" vs  "fault" — can cause misunderstanding across engineering, clinical, and  
support teams.

This guide defines approved terms, avoided terms, and correct usage for documentation written for medical imaging informatics software.

---

## Why Terminology Matters in Clinical Software

Medical imaging software sits at the intersection of three vocabularies:

- **Clinical vocabulary** — used by radiologists, technologists, clinicians
- **Engineering vocabulary** — used by software developers and architects
- **Standards vocabulary** — defined by DICOM, HL7, FHIR, IHE, and HL7 FHIR R4

When documentation mixes these without discipline, it creates:
- Misinterpretation of clinical workflows
- Integration errors between systems
- Support tickets caused by user confusion
- Failed regulatory reviews

---

## General Terminology Rules

1. **Always spell out abbreviations on first use**
   > Picture Archiving and Communication System (PACS)

2. **Use the standards body definition first**
   > If DICOM defines it, use DICOM's definition — not an internal one.

3. **Never invent synonyms for established terms**
   > If the standard says "SOP Class", do not write "service class" or  
   > "object type" interchangeably.

4. **Distinguish clinical terms from software terms explicitly**
   > "Study" means something specific in DICOM. Clarify when using it  
   > in a non-DICOM context.

---

## Core Terminology: Approved and Avoided Terms

### Imaging and DICOM Terms

| Approved Term | Avoid | Notes |
|---|---|---|
| study | exam, case, scan | Use "study" for a DICOM Study (0020,000D). Use clinical term only in clinical context |
| series | sequence, set, group | A DICOM Series (0020,000E) — always use "series" |
| instance | image, slice, frame | A DICOM SOP Instance — "image" is acceptable in UI-facing text only |
| SOP Class | service class, object type | Defined by DICOM standard — do not paraphrase |
| SOP Instance UID | image ID, file ID | Always use full term in technical docs |
| modality | imaging type, scan type | CT, MR, US, PET — use "modality" not "imaging type" |
| DICOM tag | DICOM field, DICOM attribute | "Attribute" is acceptable in standards context; "field" is not |
| window level | brightness, contrast | Window Level (0028,1050) and Window Width (0028,1051) — use exact terms |
| window width | contrast range | See above |
| pixel spacing | resolution, pixel size | Use "pixel spacing" — defined in DICOM tag (0028,0030) |
| transfer syntax | file format, encoding | Transfer Syntax UID (0002,0010) — do not simplify to "format" |
| DICOM object | DICOM file, DICOM image | "Object" is the correct DICOM term |
| hanging protocol | display protocol, layout | Use "hanging protocol" — an established clinical term |

---

### PACS Terms

| Approved Term | Avoid | Notes |
|---|---|---|
| PACS | picture archive, image archive | Always capitalize; spell out on first use |
| AE Title | AET, application entity | Spell out as Application Entity (AE) Title on first use |
| worklist | work list, task list | One word: "worklist" — DICOM Modality Worklist |
| C-FIND | query, search request | Use DICOM service name in technical docs |
| C-STORE | send, transmit, push | Use DICOM service name in technical docs |
| C-MOVE | retrieve, pull, fetch | Use DICOM service name in technical docs |
| C-ECHO | ping, connection test | "Connection test" acceptable in UI text only |
| prefetch | pre-fetch, preload | One word: "prefetch" |
| prior study | previous exam, old study | Use "prior study" — standard radiology term |

---

### HL7 Terms

| Approved Term | Avoid | Notes |
|---|---|---|
| HL7 message | HL7 record, HL7 packet | Always "message" |
| ADT message | admission message, patient message | ADT = Admit, Discharge, Transfer — spell out on first use |
| ORM message | order message | ORM = Order Message — spell out on first use |
| ORU message | result message | ORU = Observation Result — spell out on first use |
| MSH segment | message header, header segment | Always "MSH segment" in technical docs |
| PID segment | patient segment, patient info | Always "PID segment" |
| message trigger event | trigger, event type | Full term: "message trigger event" |
| HL7 v2.x | HL7 version 2, legacy HL7 | Specify exact version: HL7 v2.5.1, HL7 v2.8 |
| HL7 FHIR | FHIR, Fast Healthcare | Always "HL7 FHIR" on first use; "FHIR" acceptable thereafter |

---

### FHIR Terms

| Approved Term | Avoid | Notes |
|---|---|---|
| FHIR resource | FHIR object, FHIR record | Always "resource" — core FHIR concept |
| FHIR endpoint | FHIR URL, FHIR address | Always "endpoint" |
| FHIR R4 | FHIR version 4, FHIR 4.0 | Specify release: R4, R4B, R5 |
| ImagingStudy resource | imaging FHIR object | Use full resource name: ImagingStudy |
| DiagnosticReport resource | report resource, result resource | Use full resource name: DiagnosticReport |
| Patient resource | patient record, patient object | Use full resource name: Patient |
| SMART on FHIR | SMART, FHIR auth | Always "SMART on FHIR" — spell out on first use |
| capability statement | conformance statement | "Capability Statement" replaced "Conformance" in FHIR R4 |

---

### AI and Radiology AI Terms

| Approved Term | Avoid | Notes |
|---|---|---|
| AI algorithm | AI model, AI engine | Use "algorithm" for specific processing; "model" acceptable in ML context |
| inference | prediction, result, output | "Inference" is the correct ML term for model output |
| confidence score | probability, certainty, accuracy | Use "confidence score" — do not imply clinical certainty |
| finding | detection, flag, alert | "Finding" aligns with radiology reporting language |
| secondary capture | AI overlay, AI result image | Use "secondary capture" for DICOM-encoded AI output |
| CAD | computer-aided detection | Spell out on first use: Computer-Aided Detection (CAD) |
| annotation | markup, label, tag | Use "annotation" for AI and structured reporting context |

---

## Terms That Mean Different Things in Different Contexts

These terms are frequently misused because they have different meanings in clinical, engineering, and standards contexts. Always clarify context.

| Term | Clinical Meaning | Engineering Meaning | Standards Meaning |
|---|---|---|---|
| **study** | A patient's imaging encounter | A DICOM Study object | DICOM Study (0020,000D) |
| **instance** | A single occurrence | An object in memory | A DICOM SOP Instance |
| **service** | A clinical service or department | A software microservice | A DICOM Service Class |
| **report** | A radiologist's diagnostic report | A software-generated output | A DICOM SR or FHIR DiagnosticReport |
| **query** | Not commonly used clinically | A database or API query | A DICOM C-FIND request |
| **object** | Not commonly used clinically | A software object/class | A DICOM Information Object |
| **node** | An anatomical structure | A network node or server | A DICOM network node |

---

## Abbreviation Reference

Always spell out on first use. Use abbreviation thereafter.

| Abbreviation | Full Term |
|---|---|
| PACS | Picture Archiving and Communication System |
| DICOM | Digital Imaging and Communications in Medicine |
| HL7 | Health Level Seven |
| FHIR | Fast Healthcare Interoperability Resources |
| AE | Application Entity |
| SOP | Service-Object Pair |
| UID | Unique Identifier |
| IHE | Integrating the Healthcare Enterprise |
| RIS | Radiology Information System |
| HIS | Hospital Information System |
| EMR | Electronic Medical Record |
| EHR | Electronic Health Record |
| CAD | Computer-Aided Detection |
| VNA | Vendor Neutral Archive |
| MPR | Multiplanar Reconstruction |
| MIP | Maximum Intensity Projection |
| GPU | Graphics Processing Unit |
| API | Application Programming Interface |
| REST | Representational State Transfer |
| JSON | JavaScript Object Notation |
| XML | Extensible Markup Language |
| TLS | Transport Layer Security |
| HIPAA | Health Insurance Portability and Accountability Act |

---

## Common Terminology Mistakes to Avoid

| Mistake | Correct Usage |
|---|---|
| "The image was sent to PACS" | "The DICOM instance was stored to the PACS via C-STORE" |
| "The patient's scan loaded" | "The patient's study loaded" |
| "The AI detected a nodule" | "The AI algorithm identified a finding consistent with a pulmonary nodule" |
| "Click the FHIR button" | "Click **Fetch FHIR Data**" — never expose protocol names in UI labels |
| "The HL7 feed is broken" | "The HL7 ADT message interface is not receiving messages" |
| "Invalid DICOM file" | "The DICOM object does not conform to the expected SOP Class" |
| "The system is down" | "The PACS connection is unavailable" — be specific about what is affected |

---

## Living Document Notice

This terminology guide is a living document. Medical imaging standards evolve — DICOM supplements are released regularly, and FHIR R5 introduced new resource definitions.

To suggest a new term or correction, please open an Issue or submit a Pull Request. See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.