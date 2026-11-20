## <span style="color:#2F7DDE">AI for Spreadsheets and Data</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>AI for Spreadsheets and Data"]
  Q["<b>The Big Question</b><br/><i>How do you know a total from an AI tool is the right total?</i>"]
  CV["<b>Course use case</b><br/>Testing a formula on 5 rows, then on a 120-row dairy sales sheet"]
  RL["<b>Real-world example</b><br/>A cycle repair shop's weekly job book"]

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

Have you ever wondered why two people adding the same job-book page can reach two different totals?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Summarise**</span> a week of repair jobs in 2 lines, using only the job-book page.
- <span style="color:#D9660B">**Calculate**</span> the total puncture repairs done, and test your sum on 3 rows first.
- <span style="color:#D9660B">**Examine**</span> 3 messy entries to find which one changes the weekly total the most.
- <span style="color:#D9660B">**Check**</span> 5 sentences in a helper's note against the numbers on the page.
- <span style="color:#D9660B">**Write**</span> a clear request that asks a helper for a total and says how you will test it.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> CSV summaries, lookup and SUMIF formulas, cleaning plans, checking formulas, checking claims.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

A cycle repair shop keeps a job book. On Friday the owner adds up the puncture repairs done that week.

His helper adds the same page and gets a different total. One entry was written twice, and one number was written as a word.

A <span style="color:#D9660B">**formula**</span> means a rule in a spreadsheet cell that works out a number from other cells. A formula can run without an error and still give a wrong total.

In this course you will ask AI tools for formulas, then prove them.

> <span style="color:#2F7DDE">**Think about it:**</span> How would you decide which of the two totals is right?

---

### <span style="color:#2F7DDE">The Repair Shop Puzzle</span>

Here is one week of the job book.

| Day | Job | Count | Price per job |
|:----------:|:----------:|:----------:|:----------:|
| Monday | Puncture repair | 20 | Rs 30 |
| Monday | Puncture repair | 20 | Rs 30 |
| Tuesday | Chain oiling | ten | Rs 20 |
| Wednesday | Puncture repair | 15 | Rs 30 |
| Thursday | Chain oiling | 30 | Rs 20 |

<span style="color:#D9660B">**What you want to happen:**</span>

- The puncture total matches the jobs the shop finished.
- You know which messy entry to fix first.
- You can say why a helper's total is right or wrong.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Is the second Monday row a real sale or a copy?
> - What would a sum do with the word "ten"?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Add the puncture repairs twice: once with the second Monday row and once without. Which total do you trust?**
Hint: Ask whether two identical rows can be two real sales.

**2. A helper says, "Chain oiling earned Rs 150." What would you check on the page?**
Hint: Multiply the count by the price for each oiling row.

**3. You can fix only one messy entry before 5 pm. Which one, and why?**
Hint: Pick the entry that moves the weekly total most.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**What would you test on 3 rows before you trust a total on 300 rows?**</span>
>
> Which entry in your own records could be counted twice?
