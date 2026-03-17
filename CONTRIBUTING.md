# Contributing to the Docs-as-Code Style Guide

Thank you for your interest in contributing! This guide is built by and for  
the medical imaging informatics community — every improvement makes it more  
valuable for everyone.

---

## 👥 Who Can Contribute

- Technical writers working in health IT or medical imaging
- Software engineers documenting DICOM, HL7/FHIR, or PACS systems
- Clinicians who want clearer software documentation
- Anyone who has spotted a gap, error, or improvement opportunity

---

## 🛠️ Ways to Contribute

### 1. Fix a typo or clarify existing content
Small improvements are just as welcome as large ones.

### 2. Add a new terminology entry
Know a DICOM tag, HL7 segment, or FHIR resource that should be in the  
terminology guide? Add it.

### 3. Submit a real-world example
Anonymized before/after documentation rewrites from real projects are  
extremely valuable to the community.

### 4. Propose a new section
If you think a topic is missing — open an Issue and describe the gap.

### 5. Translate the guide
If you'd like to translate any section into another language, please open  
an Issue first so we can coordinate.

---

## 📋 Contribution Process

### Step 1 — Fork the repository
Click the **Fork** button at the top right of this page.

### Step 2 — Clone your fork

git clone https://github.com/YOUR-USERNAME/docs-as-code-style-guide.git
cd docs-as-code-style-guide

### Step 3 — Create a branch
Name your branch descriptively:

git checkout -b add-fhir-terminology


### Step 4 — Make your changes
Edit or add Markdown files following the writing standards in this guide.

### Step 5 — Commit your changes

git add .
git commit -m "Add FHIR R4 terminology entries to medical-terminology.md"


### Step 6 — Push and open a Pull Request

git push origin add-fhir-terminology

Then go to GitHub and open a **Pull Request** against the `main` branch.

---

## ✅ Contribution Standards

Please follow these guidelines when contributing:

- Write in **plain, clear English** — this guide is for global audiences
- Follow the voice and tone established in [01-voice-and-tone.md](style-guide/01-voice-and-tone.md)
- Use **sentence case** for all headings (not Title Case)
- Keep line length under **100 characters** for readability in code editors
- Do not include proprietary, confidential, or patient-identifiable information
- All medical terms must include a source or reference where applicable

---

## 🐛 Reporting Issues

Found an error, outdated term, or missing topic?

1. Go to the **Issues** tab on GitHub
2. Click **New Issue**
3. Use a clear title: `[Terminology] DICOM tag SR is missing from glossary`
4. Describe what's wrong and what you'd suggest instead

---

## 📄 License

By contributing, you agree that your contributions will be licensed under  
the same **MIT License** that covers this project.

---

## 🙏 Thank You

Every contribution, no matter how small!, it helps engineers and writers  
build better, clearer, safer medical imaging software documentation.