## <span style="color:#2F7DDE">AI for Documents and Research</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>AI for Documents and Research"]
  Q["<b>The Big Question</b><br/><i>How do I make a helper answer only from the page in front of us?</i>"]
  CV["<b>Course use case</b><br/>Checking 6 claims in an AI summary of a 6-paragraph circular"]
  RL["<b>Real-world example</b><br/>A school trip notice read aloud by a neighbour who remembers last year"]

  CUR ==> Q
  Q ==>|&nbsp;Used in the course&nbsp;| CV
  Q ==>|&nbsp;Seen in real life&nbsp;| RL

  classDef currSes fill:#ffe0b2,stroke:#ef6c00,color:#4e342e,stroke-width:3px
  classDef ask fill:#e3f2fd,stroke:#1565c0,color:#0d47a1,stroke-width:3px
  classDef val fill:#e8f5e9,stroke:#2e7d32,color:#1b5e20

  class CUR currSes
  class Q ask
  class CV,RL val

  linkStyle default stroke-width:3px
```

---

### <span style="color:#2F7DDE">What You'll Learn</span>

Have you ever wondered which part of a neighbour's advice came from the notice and which from memory?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Identify**</span> the situations in which you must tell the school that a friend helped you fill a form.
- <span style="color:#D9660B">**Describe**</span> why last year's trip details miss a change the school made in March.
- <span style="color:#D9660B">**Classify**</span> 6 lines of your neighbour's advice as backed by the notice or not backed by it.
- <span style="color:#D9660B">**Write**</span> an instruction that tells a helper to answer only from the notice.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Uploading and summarising a document, grounding a prompt, knowledge cutoff, fact-checking claims against the source, disclosing AI assistance.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Tara receives a notice for her son's school trip. Her neighbour Mr Joshi sent his own child on the same trip last year.

She asks him the departure time. He says 7:00 am, then adds "fee is Rs 400". He sounds sure.

The notice says 7:30 am and Rs 450. The school changed both details this year.

A <span style="color:#D9660B">**source**</span> means the page or file where a fact can be found and checked.

In this course, you will give a chat tool a document and make it answer from that source.

> <span style="color:#2F7DDE">**Think about it:**</span> What should Tara have asked Mr Joshi before she wrote "7:00 am" on her calendar?

---

### <span style="color:#2F7DDE">The School Trip Notice Puzzle</span>

Here are 4 answers from Mr Joshi and what the notice says.

| Question | Mr Joshi said | The notice says |
|:----------:|:----------:|:----------:|
| 1. Departure time | 7:00 am | 7:30 am |
| 2. Fee | Rs 400 | Rs 450 |
| 3. Return time | 5:00 pm | 5:00 pm |
| 4. Packed lunch | Bring your own | Not mentioned |

<span style="color:#D9660B">**What you want to happen:**</span>

- Every answer points to a line of the notice.
- A missing answer says "not in the notice".
- The school knows which help you used.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Which of the 4 answers can Tara defend with a line of the notice?
> - Should Tara tell the school that Mr Joshi helped?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Which answer of Mr Joshi's matches the notice exactly?**
Hint: Compare each time and each fee.

**2. Why did last year's memory give the wrong fee?**
Hint: Think about when he heard it and when the school changed it.

**3. Question 4 is not in the notice. What is the safest sentence for Tara to write?**
Hint: The sentence should name the notice, not his memory.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How can you prove that an answer came from the page and not from memory?**</span>
>
> Who needs to know when you used help to write it?
