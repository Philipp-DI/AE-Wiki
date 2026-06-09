# LF5.1.2: Extracting Chaos & Interviewing Stakeholders

<details>
<summary>Briefing</summary>

## 👤 User Story

> As a Requirements Engineer,  
> I want to extract actionable facts from chaotic statements and conduct proper interviews,  
> so that I can uncover the true needs of my stakeholders without missing hidden requirements.

## 🎉 Celebration Criteria (Learning Objectives)

- I can **extract** technical facts from unstructured, emotional text blocks. (K2)
- I **know how to formulate** open-ended interview questions. (K3)
- I **can separate** technical requirements from personal preferences. (K2)

## 🧠 Knowledge Briefing

Stakeholders rarely provide ready-to-use IT requirements. They talk about their fears, wishes, and problems.

**1\. Extraction:** You must read between the lines. If a user says, "I hate waiting for the spinning wheel", the extracted fact is: _The system has a performance/latency issue._

**2\. Interview Techniques:**

- **Open-ended questions:** "Can you describe how you currently handle X?" (Yields stories and processes).
- **Closed-ended questions:** "Do you use a Mac or Windows?" (Yields hard facts, but misses context).

## ⚠️ Common Pitfalls

- Asking leading questions like "Don't you think a database would be better?" forces the stakeholder into technical decisions they don't understand. Always ask about the _problem_, not the _solution_.

## 🛠️ Mandatory Tasks (K1 - K3)

1. Extract 3 distinct technical needs from this quote: _"My team is always complaining. They need to log in from home, but the VPN drops. Also, the app is ugly and the export function crashes if the file is over 50MB."_ (K1)
2. List 3 open-ended question types used in professional stakeholder interviews. (K1)
3. Describe the difference between a stakeholder's personal wish and a hard technical requirement. (K2)
4. Formulate 2 open-ended interview questions designed to uncover hidden quality expectations. (K3)
5. Summarize a chaotic paragraph of your choice (e.g., from a news article about a failed IT project) into a 3-point bulleted list. (K2)

## 🔥 Optional Tasks (K4 - K6)

1. Analyze the psychological risks of asking leading questions during an interview. (K4)
2. Evaluate a simulated interview transcript for missed critical information regarding data privacy. (K5)
3. Design a structured interview template for non-technical stakeholders in an initial project meeting. (K6)

## 🕸️ Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| Stakeholder Interviews | Google | "IREB Requirements Elicitation interview techniques" |
| Open vs Closed Questions | YouTube | "Open ended vs closed ended questions examples" |

</details>

### M1: Extract 3 distinct technical needs from this quote: "My team is always complaining. They need to log in from home, but the VPN drops. Also, the app is ugly and the export function crashes if the file is over 50MB." (K1)

**Identifiable Problems:**

- Unstable VPN connection
- Unpleasant UX
- Export crashes on larger than 50MB files

**Technical Needs:**

1. **Remote-Access & Stability:** Uninterrupted service/connection has to be guaranteed.
2. **UI / UX:** The Userinterface could use a refresh.
3. **Export-Performance:** Implement the limit correctly to avoid crashes, also consider higher limit.

---

### M2: List 3 open-ended question types used in professional stakeholder interviews. (K1)

1. **Descriptive:** "Could you describe the project in more detail?"
2. **Problem-oriented:** "Where do you see the biggest problems in your day-to-day work?"
3. **Expectation-oriented:** "What would the optimal process look like to you?"

---

### M3: Describe the difference between a stakeholder's personal wish and a hard technical requirement. (K2)

A **personal wish** is something **subjective** and often **not** measurable/testable. E.g. “The app has to look nice.”

A **hard technical requirement** on the other hand definitive, **objective** and first and foremost **measurable/testable**. E.g. “The measured user retention value is X.”

---

### M4: Formulate 2 open-ended interview questions designed to uncover hidden quality expectations. (K3)

1. "Imagine the system fails for two hours on a Monday morning - what would be the worst consequence for your team?"
2. "Did you use similar software in the past? What were your satisfactions and frustrations using it?"

---

### M5: Summarize a chaotic paragraph of your choice (e.g., from a news article about a failed IT project) into a 3-point bulleted list. (K2)

[**LIDL’s SAP Debacle:**](https://www.henricodolfing.ch/en/case-study-12-lidls-e500-million-sap-debacle/)

> The core failure of the Lidl SAP programme lay in the collision between two different logics of operation, as the standardized assumptions of the software conflicted with the specific practices that defined Lidl’s business model. This conflict was not limited to a single process, but affected multiple areas, including inventory management, pricing, and system integration, creating a network of dependencies that amplified complexity across the programme.

- Assumption of standardization conflicted with complexity
- The vastly different aspects couldn’t be handled by a single software product

---

### O1: Analyze the psychological risks of asking leading questions during an interview. (K4)

Leading questions can pose multiple risks:

- The stakeholder is literally being “led” through the discussion and just affirms/follows the interviewer.
- Important requirements for the stakeholder might go unnoticed.
- Missing features, errors in execution and unsatisfactory results might be the symptom of badly phrased/leading questions.

---

### O2: Evaluate a simulated interview transcript for missed critical information regarding data privacy. (K5)

Not doing this task, as I don’t want to waste time creating such an Interview.

BUT, in essence: **NEVER** forget to think about data privacy! It should always be at least at the back of your mind when working with data.

---

### O3: Design a structured interview template for non-technical stakeholders in an initial project meeting. (K6)

# Stakeholder-Interview - Template

**Date:**  
**Interviewpartner:**  
**Interviewer:**

---

## 1: Context & Background

- Could you briefly describe what your day-to-day work looks like?
- What kind of tools and systems do you regularly use?

## 2: Problems

- Where do you think you lose the most amount of time?
- Is there anything that doesn’t work at all?

## 3: Expectations

- What kind of improvement do you expect?
- How would a satisfactory outcome look like?

## 4: Framework & Requirements

- Are there technical or structural requirements that need to be met or considered?
- Who or what presents a paramount/critical role?

## Notes

\[\_-_-\_\]