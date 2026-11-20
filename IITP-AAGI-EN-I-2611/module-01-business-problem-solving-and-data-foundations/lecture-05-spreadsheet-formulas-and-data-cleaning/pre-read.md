## <span style="color:#2F7DDE">Spreadsheet Formulas and Data Cleaning</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Spreadsheet Formulas and Data Cleaning"]
  Q["<b>The Big Question</b><br/><i>How do I make a sheet add up the right total?</i>"]
  CV["<b>Course use case</b><br/>Cleaning a 120-row order file so March revenue falls from Rs 260,315 to Rs 247,064"]
  RL["<b>Real-world example</b><br/>A housing society's Diwali donation register with repeats and messy names"]

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

Have you ever wondered why a register total looks different from the money in the tin?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Identify**</span> which lines in a 4-line register are repeats of the same payment.
- <span style="color:#D9660B">**Calculate**</span> the total and the average of the donations on a short list.
- <span style="color:#D9660B">**Apply**</span> one fixed 5% fee to every line without the fee drifting away.
- <span style="color:#D9660B">**Use**</span> three clean-up moves to fix spaces, capitals and stray letters in names.
- <span style="color:#D9660B">**Demonstrate**</span> how "Rs 500" becomes a number that can be added.
- <span style="color:#D9660B">**Write**</span> the one fact that tells you two lines are the same entry.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Formulas, absolute vs relative references, SUM AVERAGE COUNT MIN and MAX, TRIM PROPER and SUBSTITUTE, text to numbers and dates, remove duplicates.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Sunita volunteers to total the Diwali party donations in her housing society.

She types each line as the neighbours wrote it. Her total says Rs 3,000.

The tin holds Rs 2,000. Flat A-102 appears twice, and the treasurer is upset.

A <span style="color:#D9660B">**formula**</span> means a rule typed into a sheet cell that works out a value from other cells.

In this course, you will build formulas and clean files before you trust any total.

> <span style="color:#2F7DDE">**Think about it:**</span> Where would you look first to find the Rs 1,000 gap?

---

### <span style="color:#2F7DDE">The Society Register Puzzle</span>

Sunita copies four lines from the register.

| Flat | Name as written | Amount as written |
|:----------:|:----------:|:----------:|
| A-101 | "  sunita rao " | Rs 500 |
| A-102 | "RAVI KUMAR" | Rs 1,000 |
| B-201 | "meena shah" | Rs 500 |
| A-102 | "Ravi Kumar" | Rs 1,000 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Every name looks the same way.
- Every amount can be added by the sheet.
- Each flat is counted once.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Which two lines are the same payment?
> - Why would a sheet refuse to add "Rs 500"?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Sunita adds a 5% hall fee in one cell and copies the line down. Why might line 3 lose the fee?**
Hint: Think about what moves when you copy a line.

**2. "Rs 500" sits beside "500". Which one can a sheet add?**
Hint: Look at the letters.

**3. Which fact tells you flat A-102 paid once and not twice?**
Hint: Look for a detail that names one payment.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**What can quietly make a sheet add up wrong?**</span>
>
> Which of the four lines would you fix first, and why?
