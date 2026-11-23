## <span style="color:#2F7DDE">Lookup Functions and Conditional Aggregation</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Lookup Functions and Conditional Aggregation"]
  Q["<b>The Big Question</b><br/><i>How do we fetch a value from another table, and what do we do when it cannot be found?</i>"]
  CV["<b>Course use case</b><br/>A store report where 9 manager lookups failed because of a hidden space"]
  RL["<b>Real-world example</b><br/>A tuition centre fee sheet with a batch fee table and a marks-to-grade table"]

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

Have you ever wondered how a tuition centre finds each student's fee from a batch code?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Name**</span> the batch code that links a student to the fee table.
- <span style="color:#D9660B">**Explain**</span> why 'B2 ' with a space finds no fee.
- <span style="color:#D9660B">**Examine**</span> a fee lookup that shows #N/A for the student of batch 'B2 '.
- <span style="color:#D9660B">**Calculate**</span> the total fee collected for batch B2 in March.
- <span style="color:#D9660B">**Determine**</span> the grade for marks of 74 using the grade table.
- <span style="color:#D9660B">**Write**</span> a message that appears when a batch code is missing.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> VLOOKUP, XLOOKUP, fixing #N/A in lookups, IFERROR, SUMIFS and COUNTIFS, banding with a lookup.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Nisha manages a tuition centre. A fee table lists each batch code and its fee. Her student sheet lists a batch code for each student. For 5 students the fee shows #N/A. The codes look the same. One code has a space after it. Nisha also needs a grade for each student from their marks.

A <span style="color:#D9660B">**lookup**</span> means finding a value in one table by matching a key from another table.

In this course, you will fetch values by key and check why a lookup fails.

> <span style="color:#2F7DDE">**Think about it:**</span> Why does a code that looks the same find no fee?

---

### <span style="color:#2F7DDE">Tuition Centre Puzzle</span>

Here are the two small tables.

| Batch | Fee | | Marks from | Grade |
|:----------:|:----------:|:----------:|:----------:|:----------:|
| B1 | Rs 1,200 | | 0 | C |
| B2 | Rs 1,500 | | 50 | B |
| B3 | Rs 1,800 | | 70 | A |

<span style="color:#D9660B">**What you want to happen:**</span>

- Each student gets the fee of their batch.
- A missing batch shows a clear message.
- Marks of 74 get a grade without a long rule.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Why would 'B2' and 'B2 ' not match?
> - Which grade does a mark of exactly 70 get?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. A student is in batch B3. What fee should the lookup return?**
Hint: Find B3 in the first table.

**2. Marks of 74 fall between 70 and the next limit. Which grade is it?**
Hint: Pick the highest limit that 74 has reached.

**3. Two students pay in March for batch B2 at Rs 1,500 each. What is the total?**
Hint: Multiply the fee by the count.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**What can go wrong when two tables should match and look the same?**</span>
>
> Which key in Nisha's sheet would you check first for a hidden space?
