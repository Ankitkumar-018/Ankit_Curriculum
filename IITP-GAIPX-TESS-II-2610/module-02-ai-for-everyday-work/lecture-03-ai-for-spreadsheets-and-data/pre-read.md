## <span style="color:#2F7DDE">AI for Spreadsheets and Data</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>AI for Spreadsheets and Data"]
  Q["<b>The Big Question</b><br/><i>How do I ask a helper for a total and prove the total is right?</i>"]
  CV["<b>Course use case</b><br/>Testing a Dairy total of Rs 19,980 against 41 supermarket sales rows"]
  RL["<b>Real-world example</b><br/>A family mobile recharge log where one member's total looks too low"]

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

Have you ever wondered why a total in a list of payments never matches what you remember paying?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Use**</span> a short, clear request to get Dad's total from a recharge log.
- <span style="color:#D9660B">**Check**</span> that total by counting the lines yourself.
- <span style="color:#D9660B">**Judge**</span> which of 3 log fixes matters most to the final total.
- <span style="color:#D9660B">**Critique**</span> a 4-line note about the month against the log lines.
- <span style="color:#D9660B">**Write**</span> a request for totals per member with a rule for lines the helper cannot read.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Asking AI for a lookup or SUMIF formula, summarising a CSV, ranking data-cleaning steps, validating AI formulas and summaries against real data, common failure patterns.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Farah keeps a log of the family's mobile recharges, one line per recharge. At month end, her cousin Dev totals Dad's payments.

Dev says Rs 299. Farah remembers paying more.

She finds that Dad's second recharge was typed as "Dad " with an extra space. Dev added only what matched the name exactly.

A <span style="color:#D9660B">**CSV**</span> means a plain-text table where each line is one row and commas separate the columns.

You will ask a chat tool to add up a table like this, then prove the answer.

> <span style="color:#2F7DDE">**Think about it:**</span> What should Dev have told Farah along with the number Rs 299?

---

### <span style="color:#2F7DDE">The Recharge Log Puzzle</span>

Here are 6 lines from Farah's log.

| Member | Plan | Amount in Rs |
|:----------:|:----------:|:----------:|
| Dad | Monthly | 299 |
| Dad (with a space) | Top-up | 100 |
| Mom | Monthly | 299 |
| Mom | Monthly | 299 |
| Riya | Data pack | blank |
| Riya | Monthly | 239 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Dad's total counts both of his recharges.
- Every line with a missing amount is named, not guessed.
- You can show how you checked the total.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Which line made Dev's total for Dad too low, and which line may be a repeat?
> - How could you check his total in under 1 minute?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Dev adds only the line that reads exactly "Dad". What total does he get?**
Hint: Look at the first line only.

**2. Which fix changes the grand total most: removing Mom's repeated line or filling in Riya's blank amount?**
Hint: Riya's data pack costs Rs 98. Compare 98 with 299.

**3. Dev writes: "Mom paid the most this month." Which lines of the log would prove it?**
Hint: Compare the totals for Dad, Mom and Riya.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How can you tell a total that looks right from a total that is right?**</span>
>
> Which line in your own notes could hide a mistake like the extra space?
