## <span style="color:#2F7DDE">Sampling and Confidence Intervals</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Sampling and Confidence Intervals"]
  Q["<b>The Big Question</b><br/><i>How sure can I be about everyone after asking only a few?</i>"]
  CV["<b>Course use case</b><br/>120 of 5,000 viewers give 39.13 minutes a day, with a range of 34.5 to 43.7"]
  RL["<b>Real-world example</b><br/>A school asking 60 of its 1,200 students how long they travel"]

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

Have you ever wondered how a school can learn about 1,200 students by asking only 60?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Classify**</span> the 1,200 students, the class list and the 60 students who were asked.
- <span style="color:#D9660B">**Describe**</span> a bell shape by its centre and its spread.
- <span style="color:#D9660B">**Summarise**</span> why the averages of repeated surveys settle into that bell.
- <span style="color:#D9660B">**Calculate**</span> how far one survey average is likely to sit from the truth.
- <span style="color:#D9660B">**Determine**</span> a range of travel times that likely holds the school's true average.
- <span style="color:#D9660B">**Judge**</span> which sentence about "95% sure" is right.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Population frame and sample, the normal distribution, standard error, central limit theorem, confidence interval for a mean, reading a confidence interval, asking an AI tool to explain a confidence interval in plain words.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Mrs. Iyer, the principal, wants to set new school bus timings. She needs the average time students travel to school.

Her clerk, Mr. Nair, asks 60 students and gets 25 minutes. Mrs. Iyer asks, "Is it exactly 25 for all 1,200 students?"

Mr. Nair has no answer. A second clerk asks another 60 students and gets 27 minutes.

A <span style="color:#D9660B">**sample**</span> means the small group you ask or measure to learn about a larger group.

In this course, you will report sample results with a range, so readers know how far to trust them.

> <span style="color:#2F7DDE">**Think about it:**</span> Do 25 and 27 disagree, or do they say the same thing?

---

### <span style="color:#2F7DDE">The School Travel Survey Puzzle</span>

Mr. Nair writes down what he knows.

| Fact | Value |
|:----------:|:----------:|
| Students in the school | 1,200 |
| Students asked | 60 |
| Average travel time of the 60 | 25 minutes |
| Spread of the 60 times | 12 minutes |

<span style="color:#D9660B">**What you want to happen:**</span>

- Mr. Nair says who the 60 students stand for.
- Mr. Nair gives a range, not one number.
- Mrs. Iyer knows how much to trust that range.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Would 240 students give a steadier answer than 60?
> - What would a range of 22 to 28 minutes tell Mrs. Iyer?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The 60 students are the first ones through the gate. Do they stand for all 1,200?**
Hint: Think about who arrives first.

**2. Another group of 60 gives 27 minutes. Does that make 25 wrong?**
Hint: Think about picking different students each time.

**3. Mr. Nair asks 240 students instead of 60. Will his average be steadier?**
Hint: Think about how a larger group evens out odd answers.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do you say something about everyone after asking only a few?**</span>
>
> What would you add to "25 minutes" so Mrs. Iyer knows how far to trust it?
