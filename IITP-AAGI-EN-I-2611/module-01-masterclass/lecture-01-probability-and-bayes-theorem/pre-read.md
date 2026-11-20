## <span style="color:#2F7DDE">Probability and Bayes Theorem</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Probability and Bayes Theorem"]
  Q["<b>The Big Question</b><br/><i>When an alert goes off, how likely is the danger to be real?</i>"]
  CV["<b>Course use case</b><br/>A fraud detector that catches 75% of frauds, yet only 9 of its 18 flags are fraud"]
  RL["<b>Real-world example</b><br/>A kitchen smoke alarm that rings for burnt toast as well as real fires"]

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

Have you ever wondered why you roll your eyes when the smoke alarm rings during breakfast?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Explain**</span> why "the alarm rings for most fires" differs from "most rings are fires".
- <span style="color:#D9660B">**Calculate**</span> the chance that the alarm rings on a random day, and the chance it stays silent.
- <span style="color:#D9660B">**Estimate**</span> the chance that the alarm rings two days in a row.
- <span style="color:#D9660B">**Determine**</span> the chance of a real fire when the alarm rings, using a table of 100 days.
- <span style="color:#D9660B">**Judge**</span> whether to leave the house when fires become 10 times rarer.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Probability and complement, multiplication rule, conditional probability from a count table, Bayes' theorem.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Anaya has a smoke alarm in her kitchen. Last year it rang for 2 of the 3 real fires.

It also rang on 8 mornings of burnt toast. When it rings today, Anaya grabs her bag and runs.

Her brother laughs. "The alarm catches most fires, but most of its rings are toast."

A <span style="color:#D9660B">**probability**</span> means a number from 0 to 1 that says how likely something is.

In this course, you will turn counts into probabilities before you trust any alert or test.

> <span style="color:#2F7DDE">**Think about it:**</span> Is Anaya's brother right that a ring usually means toast?

---

### <span style="color:#2F7DDE">The Kitchen Alarm Puzzle</span>

Anaya keeps a note of 100 mornings.

| Type of morning | Number of mornings |
|:----------:|:----------:|
| Alarm rang, real fire | 2 |
| Alarm rang, burnt toast only | 8 |
| Alarm silent, real fire | 1 |
| Alarm silent, nothing happened | 89 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Anaya finds how often the alarm rings.
- Anaya finds how likely a fire is once it rings.
- Anaya sees what changes if fires become rarer.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Which total do you divide by to find the chance of fire after a ring?
> - Would a ring mean more or less danger if toast burned twice as often?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The alarm rang on 10 of the 100 mornings. What is the chance it stays silent on a random morning?**
Hint: The two chances add up to 1.

**2. The alarm rings on 2 of the 3 fire mornings. Is that the same as 2 of the 10 ringing mornings being fires?**
Hint: Look at the number you divide by.

**3. Fires become 10 times rarer and toast stays the same. Does a ring now mean fire more often or less often?**
Hint: Think about the number of toast mornings that remain.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**What do you divide by when an alert has already gone off?**</span>
>
> Would you run out of the kitchen every time the alarm rings? Why?
