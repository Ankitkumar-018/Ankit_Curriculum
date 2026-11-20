## <span style="color:#2F7DDE">AI for Documents and Research</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>AI for Documents and Research"]
  Q["<b>The Big Question</b><br/><i>How can you make an AI tool answer only from your document and check every claim?</i>"]
  CV["<b>Course use case</b><br/>Checking 6 claims about a 6-clause insurance policy against the policy text"]
  RL["<b>Real-world example</b><br/>An open-book exam with a printed school rulebook"]

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

Have you ever wondered how an open-book exam stops you from answering with whatever you half remember?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Identify**</span> when you must tell the examiner that you had help.
- <span style="color:#D9660B">**Describe**</span> why a rulebook printed in 2019 can give a wrong answer about 2026.
- <span style="color:#D9660B">**Classify**</span> 3 answers as backed by the rulebook page or not backed by it.
- <span style="color:#D9660B">**Write**</span> an instruction that tells a helper to answer only from page 4.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Uploading and summarising a document, grounding, knowledge cutoff, fact-checking, disclosing AI help.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Your school allows an open-book exam. You bring the library rulebook, printed in 2019.

One question asks for the late fine per day. You remember a notice about Rs 5. The book says Rs 2.

Which answer should you write? The exam says: use the book, and say where you found it.

A <span style="color:#D9660B">**source**</span> means the document an answer comes from. In this course you will make AI tools answer from a source you supply.

> <span style="color:#2F7DDE">**Think about it:**</span> What could go wrong if you answer from memory instead of the page?

---

### <span style="color:#2F7DDE">The Library Rulebook Puzzle</span>

Here are 3 rules, as printed in 2019 and as shown on the school notice board in 2026.

| Rule | Printed rulebook (2019) | Notice board (2026) |
|:----------:|:----------:|:----------:|
| Loan period | 14 days | 10 days |
| Late fine per day | Rs 2 | Rs 5 |
| Books per student | 3 | 3 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Every answer comes from the page you were told to use.
- You notice when the book is out of date.
- You tell the examiner how you found each answer.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - If a friend whispers "the fine is Rs 5", is that answer backed by the page?
> - How would the examiner know that you used the book rather than guessing?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The book says 14 days and the notice says 10. Which answer fits the question "According to the book"?**
Hint: Read the question word by word.

**2. A friend says, "Books per student is 5." Is that backed by the page?**
Hint: Look at the third row of the table.

**3. You used a tutor's notes to write 2 answers. Should the examiner be told?**
Hint: Think about what the exam rules ask.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do you know an answer comes from the page and not from memory?**</span>
>
> When would you tell a reader that you had help?
