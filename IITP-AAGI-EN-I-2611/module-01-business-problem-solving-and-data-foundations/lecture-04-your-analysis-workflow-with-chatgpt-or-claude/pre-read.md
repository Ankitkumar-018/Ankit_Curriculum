## <span style="color:#2F7DDE">Your Analysis Workflow with ChatGPT or Claude</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Your Analysis Workflow with ChatGPT or Claude"]
  Q["<b>The Big Question</b><br/><i>How do I give an AI helper clear rules and a clear list, then trust the total?</i>"]
  CV["<b>Course use case</b><br/>Asking a chat tool for city totals from a 120-row file, then checking Rs 227,410 by hand"]
  RL["<b>Real-world example</b><br/>A wedding caterer whose helper totals dish orders from a paper list"]

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

Have you ever wondered why a helper gives you a different answer when you ask a loose question?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Classify**</span> four caterer jobs by whether a helper can do them or a person must.
- <span style="color:#D9660B">**Check**</span> a helper's total of 290 plates by adding the lines yourself.
- <span style="color:#D9660B">**Write**</span> 3 standing rules for a helper: the job, the limits and the do-nots.
- <span style="color:#D9660B">**Design**</span> a request that asks for dish totals from a list of 4 dishes.
- <span style="color:#D9660B">**Build**</span> a table layout where one row stands for one dish, with 3 named columns.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Where AI helps at each stage of an analysis, standing instructions for your analysis assistant, a summary from a CSV in a chat tool, prompts that return a table in the layout you need.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Mrs. Nair runs a catering business. For a wedding of 120 guests, she hires a helper, Kabir, for the week.

She says, "Do the lists." Kabir adds up the plates, but he counts cancelled plates too.

He also writes one line for every guest, so the list has 120 lines. Mrs. Nair cannot read it, and she orders 15 plates more than needed.

A <span style="color:#D9660B">**system prompt**</span> means standing instructions that tell an AI tool its job and limits before you ask anything.

In this course, you will give chat tools clear instructions and check every total they return.

> <span style="color:#2F7DDE">**Think about it:**</span> What three sentences would you say to Kabir on his first morning?

---

### <span style="color:#2F7DDE">The Wedding Caterer Puzzle</span>

Mrs. Nair keeps a short list of dish orders.

| Dish | Plates ordered | Plates cancelled |
|:----------:|:----------:|:----------:|
| Paneer Butter Masala | 60 | 5 |
| Dal Makhani | 55 | 0 |
| Veg Biryani | 70 | 10 |
| Gulab Jamun | 120 | 0 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Kabir knows his job and his limits before he starts.
- Kabir counts only the plates that are not cancelled.
- The final list has one row for each dish.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Which plates should Kabir count for each dish?
> - What would the list look like with one row for each guest?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Which job should Mrs. Nair keep for herself: choosing the menu or adding the plates?**
Hint: Think about who answers for the choice.

**2. Kabir hears "total the orders". Which three facts would make that request clearer?**
Hint: Think about which rows, what to add and how to group.

**3. The list covers 120 guests and 4 dishes. What is the row count of a list with one row per dish?**
Hint: Count what one row stands for.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do you give a helper rules and a clear request, and still check the answer?**</span>
>
> Which line of Mrs. Nair's list would you add up first to test Kabir?
