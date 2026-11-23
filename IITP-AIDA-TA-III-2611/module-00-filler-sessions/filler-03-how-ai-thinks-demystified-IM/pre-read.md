## <span style="color:#2F7DDE">How AI "Thinks" — Demystified</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>How AI "Thinks" — Demystified"]
  Q["<b>The Big Question</b><br/><i>How does a model learn from examples, and why does it still make mistakes?</i>"]
  CV["<b>Course use case</b><br/>A help bot that described a plan that does not exist and read some customers worse than others"]
  RL["<b>Real-world example</b><br/>A fruit seller's apprentice who learns to judge mango ripeness by touching 50 mangoes"]

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

Have you ever wondered how a fruit seller can tell a ripe mango with one squeeze?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Explain**</span> how the apprentice's 50 practice mangoes differ from the one mango a customer hands over.
- <span style="color:#D9660B">**Describe**</span> how the apprentice improves after each wrong guess.
- <span style="color:#D9660B">**Identify**</span> 2 reasons the apprentice fails on a fruit he has never touched.
- <span style="color:#D9660B">**Predict**</span> what the apprentice says about a green raw mango.
- <span style="color:#D9660B">**Check**</span> one answer from the apprentice against what you can see.
- <span style="color:#D9660B">**Critique**</span> an answer that sounds sure and gives a made-up reason.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> training vs inference explained through analogies (no math, no code), how models learn from data (conceptual), why AI makes mistakes (hallucination, bias), instructor-led live demo (students observe, don't operate).
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Ravi is an apprentice at a fruit stall. For 2 weeks he touches 50 mangoes. After each guess his master says ripe or not ripe. Ravi improves each day. Then a customer hands him a green raw mango. Ravi says it is ripe and gives a long reason. The reason is not true.

<span style="color:#D9660B">**Training**</span> means learning from a large set of examples before you face a real case.

In this course, you will judge what an AI answer is made of before you trust it.

> <span style="color:#2F7DDE">**Think about it:**</span> Why did Ravi sound sure about a fruit that he had never touched?

---

### <span style="color:#2F7DDE">Mango Stall Puzzle</span>

Here are 4 of Ravi's practice mangoes.

| Mango | Colour | Feel | Master's answer |
|:----------:|:----------:|:----------:|:----------:|
| 1 | Yellow | Soft | Ripe |
| 2 | Green | Hard | Not ripe |
| 3 | Orange | Soft | Ripe |
| 4 | Green | Hard | Not ripe |

<span style="color:#D9660B">**What you want to happen:**</span>

- Ravi guesses a new mango's state from colour and feel.
- Ravi says when he is not sure.
- The master can check each guess.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What does Ravi do when he has never seen the colour before?
> - Does Ravi keep all 50 mangoes in his head?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Ravi touches a yellow, soft mango. What would he say from the table?**
Hint: Find the closest row.

**2. All 50 practice mangoes were Alphonso. How might he do with a different kind?**
Hint: Think about what he never saw.

**3. Ravi gives a reason that is not true. How can the master check it?**
Hint: Compare the reason with the mango.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How does a learner who only saw examples handle a case it never saw?**</span>
>
> Which part of Ravi's answer would you test first?
