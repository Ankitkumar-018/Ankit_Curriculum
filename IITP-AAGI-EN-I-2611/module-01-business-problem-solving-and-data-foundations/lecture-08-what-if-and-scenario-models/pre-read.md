## <span style="color:#2F7DDE">What-If and Scenario Models</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>What-If and Scenario Models"]
  Q["<b>The Big Question</b><br/><i>How far can I trust a plan if the numbers behind it change?</i>"]
  CV["<b>Course use case</b><br/>A night-bus trip that earns Rs 4,880 at 80% full and loses money below 65.5%"]
  RL["<b>Real-world example</b><br/>A cricket club planning its annual dinner around 60 guests"]

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

Have you ever wondered how a club knows the number of guests it needs before it books the hall?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Calculate**</span> the club's profit when 60 guests come at Rs 400 each.
- <span style="color:#D9660B">**Determine**</span> the number of guests the club needs to earn Rs 5,000.
- <span style="color:#D9660B">**Compare**</span> a lucky evening, a usual evening and a poor evening.
- <span style="color:#D9660B">**Examine**</span> which of three numbers moves the profit most.
- <span style="color:#D9660B">**Build**</span> a small table of profit for 5 different guest counts.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> What-if scenario table across input values, goal seek, best base and worst case comparison, which assumption the result is most sensitive to, asking an AI tool to review your scenario assumptions.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Imran is the treasurer of a cricket club. He plans the annual dinner for 60 guests.

He tells the committee, "We will earn Rs 3,000 for new kit." Then it rains, and only 45 guests come.

The club loses Rs 750. Nobody had asked what would happen with fewer guests.

A <span style="color:#D9660B">**scenario**</span> means a "what if" version of a plan, with its own set of numbers.

In this course, you will test a plan under three scenarios before you present it.

> <span style="color:#2F7DDE">**Think about it:**</span> What single question could have warned Imran about the rain?

---

### <span style="color:#2F7DDE">The Club Dinner Puzzle</span>

Imran writes down the numbers for the evening.

| Item | Value |
|:----------:|:----------:|
| Hall rent, paid once | Rs 12,000 |
| Caterer cost for each guest | Rs 150 |
| Ticket price for each guest | Rs 400 |
| Guests expected | 60 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Imran sees the profit for 40, 50, 60, 70 and 80 guests.
- Imran finds the guest count that earns Rs 5,000.
- Imran knows which number to watch most closely.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What number of guests would cover the hall rent and nothing more?
> - Would a Rs 50 change in ticket price matter more than 5 guests?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Each guest brings Rs 400 and costs Rs 150. How much does one more guest add to the club's money?**
Hint: Subtract the cost from the ticket price.

**2. Each guest adds Rs 250 after the caterer. What number of guests covers the Rs 12,000 hall?**
Hint: Divide the hall rent by the amount each guest adds.

**3. Which number is hardest to be sure of: hall rent, ticket price or guest count?**
Hint: Think about which one the weather can change.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**Which number in a plan should you test first?**</span>
>
> What would you tell the committee about a poor evening?
