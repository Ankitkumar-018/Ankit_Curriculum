## <span style="color:#2F7DDE">CTEs and Views with Indexes</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>CTEs and Views with Indexes"]
  Q["<b>The Big Question</b><br/><i>How can we name a step, save a search and find one record without opening every file?</i>"]
  CV["<b>Course use case</b><br/>A payments table where a search for one phone number read 150 rows to find 11"]
  RL["<b>Real-world example</b><br/>A clinic file cabinet with a working note, a saved list for today and a phone card list"]

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

Have you ever wondered how a clinic front desk finds all files of one phone number without opening every drawer?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Describe**</span> how a working note can hold the March fee average of Rs 312.50 for one job.
- <span style="color:#D9660B">**Explain**</span> why a saved list for today shows a new file the moment it is added.
- <span style="color:#D9660B">**Interpret**</span> a search note you did not write, and say in one sentence what it finds.
- <span style="color:#D9660B">**Judge**</span> why a card list sorted by phone cannot help a search by the day of the month.
- <span style="color:#D9660B">**Plan**</span> a phone card list that lets the desk jump to the 11 files of one phone number.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> CTE (WITH), view, what an index does, create an index, index skipped by a function, explaining what an unfamiliar query returns.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Nisha works at a clinic front desk. The cabinet holds 150 patient files in drawers sorted by surname. A caller gives a phone number. Nisha opens every drawer to find the 11 matching files. The same weekly search note is copied on three desks. One copy has a typo, so that desk finds nothing.

An <span style="color:#D9660B">**index**</span> means a sorted list of one detail, such as a phone number, that points to the files.

In this course, you will name steps, save shared searches and add sorted lists to make lookups quick.

> <span style="color:#2F7DDE">**Think about it:**</span> Why does Nisha open all 150 files to find the 11 she needs?

---

### <span style="color:#2F7DDE">Clinic Cabinet Puzzle</span>

Here are 4 files from the cabinet.

| Patient | Phone | Last visit | Fee |
|:----------:|:----------:|:----------:|:----------:|
| Rao | 9810012000 | 2 March | Rs 300 |
| Iyer | 9810012007 | 5 March | Rs 450 |
| Khan | 9810012000 | 7 March | Rs 200 |
| Das | 9810012011 | 5 March | Rs 300 |

<span style="color:#D9660B">**What you want to happen:**</span>

- The desk finds every file of one phone number without opening all 150.
- All three desks use one saved search note.
- A new colleague can read a search note and say what it finds.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Would a card list sorted by phone help a search for visits on the 5th?
> - What happens to a saved list when a new file arrives?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The 4 fees add up to Rs 1,250. What is the average fee?**
Hint: Divide the total by the number of files.

**2. Rao and Khan share one phone number. What is the count of files a phone search finds for it in this table?**
Hint: Count the rows with the same number.

**3. A card list is sorted by phone number. Can it help find every visit that happened on the 5th?**
Hint: Think about what the cards are sorted by.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How can we ask a question once, save it and still get an answer fast?**</span>
>
> Which of the 4 files would your phone card list point to for 9810012000?
