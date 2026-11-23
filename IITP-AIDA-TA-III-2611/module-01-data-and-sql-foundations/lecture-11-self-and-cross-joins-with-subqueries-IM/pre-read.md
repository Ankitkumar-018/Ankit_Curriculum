## <span style="color:#2F7DDE">Self and Cross Joins with Subqueries</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Self and Cross Joins with Subqueries"]
  Q["<b>The Big Question</b><br/><i>How can a table talk to itself, and why do some totals come out wrong?</i>"]
  CV["<b>Course use case</b><br/>A bank total of Rs 21.09 crore that was really Rs 15.79 crore after repeated rows were found"]
  RL["<b>Real-world example</b><br/>A school bus roster where students name a buddy, with fares, routes and time slots"]

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

Have you ever wondered how a school can print every student's buddy name from a single roster?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Explain**</span> why 3 routes and 4 time slots give 12 pairs.
- <span style="color:#D9660B">**Predict**</span> whether a comparison with a blank buddy answers yes, no or unknown.
- <span style="color:#D9660B">**Use**</span> the roster twice to print each student's buddy name next to the student.
- <span style="color:#D9660B">**Examine**</span> why a fee total doubles when each student has 2 stops.
- <span style="color:#D9660B">**Check**</span> why students with no stop vanish from a list that should keep them.
- <span style="color:#D9660B">**Write**</span> a line that shows each fare beside the average fare.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> self join, cross join, subquery in SELECT, join fan-out, NULL in comparisons, LEFT JOIN turned inner.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Mr. Thomas runs the school bus roster. Each student row names a buddy, who is another student on the same list. Fees are Rs 600 a month. A helper joined the fee list to the stop list. Every student with 2 stops showed a fee of Rs 1,200. The total looked too high by Rs 6,000.

A <span style="color:#D9660B">**fan-out**</span> means a repeat of one row for every match found on the other side.

In this course, you will join a table to itself and check that each total is counted once.

> <span style="color:#2F7DDE">**Think about it:**</span> Why did a student with 2 stops show the fee twice?

---

### <span style="color:#2F7DDE">The School Bus Roster Puzzle</span>

Here is part of the roster.

| Student | Buddy | Route | Fare |
|:----------:|:----------:|:----------:|:----------:|
| Asha | Bilal | Route A | Rs 600 |
| Bilal | Asha | Route A | Rs 600 |
| Chitra | Not named | Route B | Rs 750 |
| Dev | Chitra | Route B | Rs 750 |

<span style="color:#D9660B">**What you want to happen:**</span>

- The school prints each student's buddy name.
- The school lists every route with every time slot.
- The school shows each fare beside the average fare.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What should the list show for Chitra, who has no buddy named?
> - What happens to a fee total if one student appears twice?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The school has 3 routes and 4 time slots. What is the count of route and slot pairs?**
Hint: Pair every route with every slot.

**2. Chitra has no buddy named. Is the sentence 'Chitra's buddy is Asha' true, false or unknown?**
Hint: Think about what an empty entry tells you.

**3. A student with 2 stops shows a fee twice. How could you total fees without repeating a student?**
Hint: Total the fees before you add the stops.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How can we compare rows of one table, and trust a total after joining?**</span>
>
> Which line of Mr. Thomas's roster would you check first for a repeated fee?
