# Writing for Engineers

Engineers in medical imaging informatics are subject matter experts.  
They understand the system deeply — but documentation written only for  
engineers often fails the people who need it most: other engineers,  
integrators, clinical informaticists, and support teams.

This section helps engineers write documentation that is technically  
accurate AND genuinely usable.

---

## Why Engineers Struggle with Documentation

This is not a criticism, it is a pattern. Engineers are trained to think  
in systems, edge cases, and implementation details. Documentation requires  
a different skill: thinking from the reader's perspective first.

Common patterns to watch for:

| Pattern | Problem | Fix |
|---|---|---|
| Explaining implementation instead of behavior | Reader needs to know what it does, not how it works internally | Describe the outcome, not the code |
| Assuming shared context | Reader may not know your system's history or architecture | Define terms, link to architecture docs |
| Writing for the happy path only | Real users hit errors constantly | Document failure states and edge cases |
| Using internal names | Jira ticket numbers, internal codenames, team nicknames | Use the product feature name as shipped |
| Skipping the why | Steps without context feel arbitrary | Add one sentence explaining the purpose |

---

## The Engineer's Documentation Mindset Shift

Before writing, ask these three questions:

1. **Who will read this?**  
   A new integration engineer? A clinical informaticist? A support technician?  
   Write for the least-experienced person likely to need it.

2. **What do they need to do?**  
   Complete a task? Understand a concept? Diagnose a problem?  
   Structure your doc around that goal.

3. **What do they already know?**  
   Assume DICOM literacy for integration docs. Do not assume familiarity  
   with your internal architecture.

---

## How to Write a Good Technical Explanation

### Start with the outcome
Tell the reader what they will be able to do after reading this section.

**Avoid:**
This section covers the HL7 ADT message parsing pipeline, including inbound socket handling, message validation, and event routing logic.

**Use:**
After reading this section, you will be able to configure inbound HL7 ADT messages to automatically create worklist entries in the system.

---

### Use the concept-then-detail pattern
Introduce the concept in one sentence. Then explain the detail.

**Avoid jumping straight into detail:**
Set the CalledAETitle to match the AE Title configured in the PACS admin console under Network > DICOM Nodes > Remote AE Titles.

**Use concept first:**
Each DICOM connection requires an Application Entity (AE) Title — a unique identifier that tells the PACS which system is connecting. Set the CalledAETitle to match the AE Title configured in the PACS admin console under Network > DICOM Nodes > Remote AE Titles.

---

### Write steps as single actions
Each numbered step should contain exactly one action.

**Avoid:**
> 1. Open the configuration panel, navigate to DICOM settings, and enter the AE Title and port number, then click Save and restart the service.

**Use:**
> 1. Open the configuration panel.  
> 2. Navigate to **DICOM Settings**.  
> 3. Enter the AE Title and port number.  
> 4. Click **Save**.  
> 5. Restart the service.

---

### Document the error states
For every procedure, answer: what happens if it goes wrong?

Include at minimum:
- The error message the user will see
- The most likely cause
- The recommended action

**Example:**
> **Error:** `DICOM C-STORE failed: Connection refused (0x0111)`  
> **Cause:** The destination PACS is not reachable on the specified port.  
> **Action:** Verify the AE Title, IP address, and port in the PACS  
> configuration. Confirm the destination PACS service is running.

---

## Code and Command Documentation Standards

When documenting code, commands, or configuration values, follow these rules:

### Always use code blocks for commands