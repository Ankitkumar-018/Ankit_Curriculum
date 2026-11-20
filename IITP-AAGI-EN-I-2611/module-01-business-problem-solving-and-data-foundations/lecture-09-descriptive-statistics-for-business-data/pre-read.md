## <span style="color:#2F7DDE">Descriptive Statistics for Business Data</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Descriptive Statistics for Business Data"]
  Q["<b>The Big Question</b><br/><i>Which few numbers describe a long list fairly?</i>"]
  CV["<b>Course use case</b><br/>Describing 120 parcel delivery times: median 27 hours, middle half from 23 to 33"]
  RL["<b>Real-world example</b><br/>A commuter's bus wait on 6 mornings, with one 45-minute morning"]

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

Have you ever wondered how one bad morning can change what a commuter says about her bus?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Identify**</span> the wait that appears most often in a week of 6 mornings.
- <span style="color:#D9660B">**Describe**</span> how one 45-minute morning stretches the picture to one side.
- <span style="color:#D9660B">**Interpret**</span> how far a usual morning sits from the middle, in minutes.
- <span style="color:#D9660B">**Calculate**</span> the total divided by 6 and the middle wait of the sorted list.
- <span style="color:#D9660B">**Determine**</span> how far the 45-minute morning sits from the rest of the week.
- <span style="color:#D9660B">**Judge**</span> which middle number to tell a friend about a usual morning.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Mean median and mode, skew and shape, mean or median, range variance and standard deviation, quartiles and IQR, reading standard deviation, z-score, asking an AI tool to explain a statistic in plain words.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Kiran catches the 8:15 bus to work. She notes her wait each morning for a week.

On Friday she waited 45 minutes. At lunch she tells a friend, "My average wait is about 15 minutes."

Her friend frowns. "You wait about 10 minutes on most days." Both of them are right, and both are describing the same week.

A <span style="color:#D9660B">**statistic**</span> means one number that describes a whole list of numbers.

In this course, you will pick the right statistic before you describe any business data.

> <span style="color:#2F7DDE">**Think about it:**</span> Which of the two numbers would you tell a new neighbour?

---

### <span style="color:#2F7DDE">The Bus Stop Wait Puzzle</span>

Kiran writes down her wait on each of 6 mornings.

| Morning | Wait in minutes |
|:----------:|:----------:|
| Monday | 8 |
| Tuesday | 10 |
| Wednesday | 9 |
| Thursday | 12 |
| Friday | 45 |
| Saturday | 8 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Kiran finds the wait that happens most often.
- Kiran finds the middle wait and the total divided by 6.
- Kiran says how unusual the 45-minute morning was.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Which number moves more when Friday changes from 45 to 12?
> - How far from the usual morning is a wait of 45 minutes?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Which wait on the list appears twice?**
Hint: Scan the list for a repeated number.

**2. Friday changes from 45 minutes to 12. Which moves more: the total divided by 6, or the middle wait?**
Hint: Think about which number listens to every value.

**3. Most waits sit between 8 and 12 minutes. Is a 45-minute wait close to usual or far from it?**
Hint: Compare 45 with the usual range of waits.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**Which number tells the truth about a usual morning?**</span>
>
> What would you add so a friend also knows about the bad Friday?
