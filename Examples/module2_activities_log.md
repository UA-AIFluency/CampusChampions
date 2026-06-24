## A template to be copied to your Github wiki and filled out along your activities of Module 2. 

**Please feel free to customize it.**

<p><img src="https://images.unsplash.com/photo-1507925921958-8a62f3d1a50d?q=80&w=1476&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" width=800>

**Image credit:** [Kelly Sikkema](https://unsplash.com/@kellysikkema). Unsplash.com.

***

## Generative AI - Capabilities, Limitations and Prompting


### Reading Guide
Complete readings BEFORE attempting tasks. Annotate as you read — your notes feed directly
into the tasks below

### Reading 1: [Chain-of-Thought Prompting Elicits Reasoning in LLMs](https://proceedings.neurips.cc/paper_files/paper/2022/file/9d5609613524ecf4f15af0f7b31abca4-Paper-Conference.pdf) (Wei et al., 2022)


**What to look for as you read:** <br>
* The definition of chain-of-thought prompting in Section 2 — exactly what is added to the
prompt and why.
* Figure 1: the side-by-side comparison of standard prompting vs. CoT prompting on the
same problem. Notice the quality difference.
* The 'emergent' nature of CoT benefits — they appear only above a model scale
threshold (~100B parameters). This has implications for which tools you can expect CoT
to help with.
*  The tasks where CoT helps most vs. least — does your professional task domain fall
into the 'helps' category?

**Guided reading questions (annotate answers as you go):** <br>
* **Q1:** What exactly is added to a prompt to make it a 'chain-of-thought' prompt? Reproduce the structure from Figure 1 in your own words.
* **Q2:** Wei et al. report that CoT benefits are 'emergent' — they appear only in sufficiently large models. What does this imply for practitioners using smaller or older LLMs?
* **Q3:** The paper tests CoT on arithmetic, symbolic reasoning, and commonsense reasoning tasks. Which of these task types is most analogous to tasks you perform professionally?
* **Q4:** What is the key limitation of the few-shot CoT approach identified by the authors? Does this concern apply to your planned Task 2 use case? 

**Key terms — write your own definition after reading:**<br>
| Term | Your definition (in your own words) |
| :-- | :-- |
| **Chain-of-thought prompting** | |
| **Zero-shot prompting** | |
| **Few-shot prompting** | |
| **Reasoning chain** | |
| **Emergent ability** | | 

### Reading 2: [Survey of Hallucination in Natural Language Generation](https://dl.acm.org/doi/full/10.1145/3571730) (Ji et al., 2023)


**What to look for as you read:** <br>
*  The formal definition of hallucination in Section 2.1 — note that it distinguishes between faithful and factually grounded content.
* The intrinsic vs. extrinsic hallucination distinction in Section 2.2 — which is more dangerous in professional document contexts?
* The causes of hallucination listed in Section 2.3 — connect these to the LLM training process you learned about in Module 1.
* Any hallucination type that could specifically arise in the professional documents you produce (reports, emails, research summaries, student feedback).

**Guided reading questions (annotate answers as you go):** <br>
* **Q1:** How does Ji et al. formally define hallucination in NLG? What is the relationship between 'faithfulness' and 'factuality' in their framework?
*  **Q2:** What is the difference between intrinsic and extrinsic hallucination? Give one example of each that could occur in an academic professional document.
* **Q3:** The paper identifies several causes of hallucination in the training process. Which cause do you think is hardest to mitigate through prompt engineering alone?
* **Q4:** Based on the taxonomy in Section 2, what type of hallucination would you most need to guard against in the professional tasks you identified in your Module 1 reflection?

**Key terms — write your own definition after reading:**
| Term | Your definition (in your own words) |
| :-- | :-- |
| **Hallucinations (NLG)** | |
| **Intrinsic hallucination** | |
| **Extrinsic hallucination** |  |
| **Faithfulness** | |
| **Factually grounding** | |



***

## Self-Paced Tasks

### Task 1: Structured Tool Comparison — Five-Task Protocol [60 min]


**Step-by-step instructions:** <br>
1. Open Tool A and Tool B in separate browser windows. Use defaults — do not customize temperature, system prompts, or personas.
2. Run Prompt P1 in Tool A verbatim. Record output summary and ratings. Then run P1 in Tool B verbatim. Record.
3. Continue for P2–P5 in the same way — complete both tools for each prompt before moving to the next prompt.
4. P1 (Factual): 'What year was the Transformer architecture first introduced in a peer-reviewed paper, and what was that paper's exact title? Please provide an APA citation.'
5. P2 (Summarization): 'Summarize the following abstract in 100 words for a non-specialist audience: [PASTE the abstract from Ouyang et al. 2022. [Training language models to follow instructions
with human feedback](https://proceedings.neurips.cc/paper_files/paper/2022/file/b1efde53be364a73914f58805a001731-Paper-Conference.pdf) — search 'InstructGPT abstract' or use the one in your course resources]'
6. P3 (Code): 'Write a Python function that accepts a list of numbers and returns a dictionary with keys mean, median, and standard_deviation. Include a docstring and one usage example.'
7. P4 (Professional writing): 'Draft a professional email declining a speaking invitation due to a scheduling conflict. The tone should be warm and leave the door open for future invitations. Length: 150–200 words.'
8. P5 (Balanced argument): 'Write a two-sided argument — two sentences pro, two sentences con — on the following claim: Universities should require disclosure of all AI use in student assignments.'
9. After completing all 10 cells, write your 3-sentence comparative synthesis at the bottom of the template.

**Five-Task Comparison Matrix — complete all cells:**<br>
| Prompt | Tool A name | Output summary | Acc. (1-5) | Rel. (1-5) | Fmt. (1-5) | Tool B name | Output summary | Acc. (1-5) | Rel. (1-5) | Fmt. (1-5) |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- |
|  <br>    |     |     |     |     |     |     |     |     |     |    |
|   <br>   |     |     |     |     |     |     |     |     |     |    |
|  <br>    |     |     |     |     |     |     |     |     |     |    |
|  <br>    |     |     |     |     |     |     |     |     |     |    |
| <br>     |     |     |     |     |     |     |     |     |     |    |

where 

* Acc. = Accuracy (rated 1–5; factual correctness of claims you can independently verify)
* Rel. = Relevance (rated 1–5; how well the output addresses the prompt)
* Fmt. = Format (rated 1–5; appropriateness of structure, length, and presentation)


### Task 2: Prompt Engineering Lab - Four-iteration refinement [60 min]


**Step-by-step instructions:**<br>
1. Choose your target task: a real professional task that produces a document, communication, or structured content. Examples: drafting a course learning objective, writing a grant paragraph, summarizing research findings for a general audience, creating rubric criteria.
2. Write your task in the 'My Target Task' box below before starting.
3. VERSION 1 (Zero-shot): Write a single declarative sentence asking for the output. Nothing more.
4. Record the V1 output summary and quality rating. Identify the two most significant weaknesses.
5. VERSION 2 (+Role specification): Add a specific role persona before your V1 prompt. Be precise about the role (e.g., 'You are an experienced curriculum designer at a research-intensive university who specializes in writing learning objectives for interdisciplinary graduate courses.').
6. VERSION 3 (+Few-shot example): Add one example of a high-quality output — ideally something you have actually written — before the task instruction.
7. VERSION 4 (+Chain-of-thought): Add this instruction after your other instructions: 'Before writing, think step by step through: (1) Who is the audience? (2) What is the single most important point? (3) What tone is appropriate? Then produce the output.'
8. Write your 150-word reflective note in the space below: What changed across iterations? Which technique produced the greatest single improvement?

**Prompt Engineering Iteration Log:** <br>

| My target task (describe specifically — not 'emails' but the specific type, audience, and purpose): |
| :-- |
|  <br>  |
|  <br>   |
|  <br>    |



| VERSION 1 — Zero-shot prompt (write verbatim):  | 
| :-- |
| <br>    |
| <br>     |
| <br>     |


| V1 output quality (1–5): ___. Two weaknesses I identified: | 
| :-- |
|  <br>    |
|  <br>    |
|  <br>    |



|VERSION 2 — +Role specification (write verbatim — include V1 plus new role addition): | 
| :-- |
|  <br>    |
|  <br>    |
|  <br>    |


| V2 output quality (1–5): ___. What improved vs. V1: | 
| :-- |
|   <br>   |
|   <br>   |
|  <br>    |


| VERSION 3 — +Few-shot example (paste or describe your example, then the prompt): | 
| :-- |
|  <br>    |
|  <br>    |
|  <br>    |



| V3 output quality (1–5): ___. What improved vs. V2: | 
| :-- |
|  <br>    |
|  <br>    |
|  <br>    |



| VERSION 4 — +Chain-of-thought instruction (write full verbatim V4 prompt): | 
| :-- |
|   <br>   |
|  <br>    |
|  <br>    |



| V4 output quality (1–5): ___. What improved vs. V3: | 
| :-- |
|   <br>   |
|  <br>    |
|  <br>    |

| 150-word reflective note — which technique produced the biggest jump? What remains unresolved? | 
| :-- |
|   <br>   |
|  <br>    |
|  <br>    |


### Task 3: Hallucination Detection Audit [45 min]

**Step-by-step instructions:**<br>
1. Access the five Module 2 audit texts from the course platform (Texts A–E, one paragraph each).
2. Before reading any text, set up your verification tools in separate tabs: Google Scholar, your institutional library database, and one specialist resource for your field.
3. For Text A: read slowly. Extract EVERY discrete factual claim as a separate row (dates, names, statistics, causal relationships, paper titles, institutional facts). Verify each claim. Note the hallucination type using Ji et al.'s taxonomy.
4. Repeat for Texts B–E. Take 8–9 minutes per text.
5. After completing all five, calculate your detection rate: claims correctly identified as errors ÷ total actual errors (from answer key).
6. Write 2–3 sentences on: What type of hallucination was hardest to detect, and why?

**Hallucination Audit Log — add rows as needed for each claim:**<br>
| Text | Claim (verbatim or paraphrased) | Accurate? Y/N/Uncertain | Verification Source | Hallucination type | Severity Low/Med/High |
| :-- | :-- | :-- | :-- | :-- | :-- |
| <br>  |  |  |  |  |  |
| <br>  |  |  |  |  |  |
| <br>  |  |  |  |  |  |
| <br>  |  |  |  |  |  |
| <br>  |  |  |  |  |  |
| <br>  |  |  |  |  |  |
| <br>  |  |  |  |  |  |
| <br>  |  |  |  |  |  |
| <br>  |  |  |  |  |  |
| <br>  |  |  |  |  |  |


### Task 4: AI Tool Landscape Annotation [15 min]

**Step-by-step instructions:**<br>
1. Open the Module 2 AI Tool Landscape Map from course resources (a visual grid of tools by modality: text, image, code, audio, multimodal).
2. Select 4 tools from the map that are most relevant to your role — at least one from a modality other than text.
3. For each selected tool, complete one row in the annotation table below.
4. For Access Status: check your institution's IT/software portal before marking 'No Access' — many universities have enterprise agreements not widely advertised.
5. Save or print your annotated map — you will update it in Module 3 after completing Task 1's Workflow Audit.

**Tool Annotation Table:**<br>
| Tool name | Modality | Access status | Best use case for my role | Key institutional concern |
| :-- | :-- | :-- | :-- | :-- |
| <br> |  |  |  |  |
| <br> |  |  |  |  |
| <br> |  |  |  |  |
| <br> |  |  |  |  |


*** 

Created: 06/23/2026 (C. Lizárraga) <br>
Updated: 06/23/2026 (C. Lizárraga)
