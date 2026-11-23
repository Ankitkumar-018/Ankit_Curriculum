## <span style="color:#2F7DDE">Conditional Probability and Bayes Theorem</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Conditional Probability and Bayes Theorem"]
  Q["<b>The Big Question</b><br/><i>How likely is a fire once the alarm rings, and how does a clue change a chance?</i>"]
  CV["<b>Course use case</b><br/>A fraud alert where only 5 of 16 flagged payments were fraud"]
  RL["<b>Real-world example</b><br/>A kitchen smoke alarm that rings on 12 of 100 days, with a fire on 4 of those days"]

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

Have you ever wondered how often a ringing smoke alarm means a real fire?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Calculate**</span> the chance that the alarm rings on a random day, and the chance that it stays quiet.
- <span style="color:#D9660B">**Apply**</span> the multiplication rule to two alarms in a row.
- <span style="color:#D9660B">**Determine**</span> the chance of a fire on a day when the alarm rings.
- <span style="color:#D9660B">**Compare**</span> the chance of an alarm given a fire with the chance of a fire given an alarm.
- <span style="color:#D9660B">**Solve**</span> for the new chance of fire after the alarm, using the rate of fires.
- <span style="color:#D9660B">**Judge**</span> whether a ringing alarm should make the family leave at once.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> probability and complement, multiplication rule, conditional probability, Bayes theorem.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

The Rao family has a smoke alarm in the kitchen. Over 100 cooking days it rang on 12 days. A real fire started on 4 days. The alarm rang on 3 of those 4 fire days. One evening the alarm rings. Mrs. Rao asks how likely it is that there is a fire.

A <span style="color:#D9660B">**probability**</span> means how likely an event is, written from 0 to 1.

In this course, you will read an alert together with how common the problem is.

> <span style="color:#2F7DDE">**Think about it:**</span> If the alarm caught 3 of 4 fires, does a ring mean a 75 percent fire chance?

---

### <span style="color:#2F7DDE">Kitchen Alarm Puzzle</span>

Here are the counts for 100 cooking days.

| | Fire | No fire |
|:----------:|:----------:|:----------:|
| Alarm rang | 3 | 9 |
| Alarm quiet | 1 | 87 |

<span style="color:#D9660B">**What you want to happen:**</span>

- The family knows the chance that the alarm rings.
- The family knows the chance of a fire when it rings.
- The family does not mix up the two chances.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Is an alarm given a fire the same chance as a fire given an alarm?
> - What changes if fires become twice as common?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The alarm rang on 12 of 100 days. What is the chance that it stays quiet?**
Hint: Subtract from 1.

**2. On days when the alarm rang, what was the count of fire days?**
Hint: Look at the first row of the table.

**3. Which chance is larger: alarm given fire, or fire given alarm?**
Hint: Compare 3 out of 4 with 3 out of 12.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**Does a warning that is right most of the time make a fire likely?**</span>
>
> Which count in the table matters most for Mrs. Rao tonight?
