## <span style="color:#2F7DDE">Your AI Toolkit: What to Use When</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Your AI Toolkit: What to Use When"]
  Q["<b>The Big Question</b><br/><i>How do you pick the right AI tool for a task, and know when to trust its answer?</i>"]
  CV["<b>Course use case</b><br/>Sorting 5 Monday work tasks into 5 tool categories and running 1 prompt in 3 tools"]
  RL["<b>Real-world example</b><br/>A neighbourhood market where each shop does one job"]

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

Have you ever wondered how you know which shop in the market to visit for a torn shirt?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Identify**</span> which of 3 shared items, such as your phone PIN, you should never hand to a shopkeeper.
- <span style="color:#D9660B">**Classify**</span> 5 errands by the shop type that suits each one.
- <span style="color:#D9660B">**Differentiate**</span> a signboard that gives proof from a signboard that only boasts.
- <span style="color:#D9660B">**Compare**</span> what 3 tailors do with the same torn shirt, and name each one's trade-off.
- <span style="color:#D9660B">**Examine**</span> a stranger's directions to find a shop that does not exist.
- <span style="color:#D9660B">**Judge**</span> when to give a shopkeeper no sample and when to show 2 samples.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Tool categories, task matching, four-tool comparison, vendor claims, zero-shot and few-shot, hallucinations, unsafe data.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

On Saturday you walk through your market with 5 errands. A vegetable seller, a tailor and a cobbler each do one job.

You would never ask the cobbler to hem trousers. You also check a shop before you trust it.

A <span style="color:#D9660B">**prompt**</span> means the instruction you type into an AI tool. Each AI tool is like a shop, because each one suits certain jobs.

In this course you will use free AI tools every week.

> <span style="color:#2F7DDE">**Think about it:**</span> If a signboard says "Best tailor in town", what would make you believe it?

---

### <span style="color:#2F7DDE">The Market Errands Puzzle</span>

Here are your 4 errands for Saturday and the shops that might help.

| Errand | Shop 1 | Shop 2 | Shop 3 |
|:----------:|:----------:|:----------:|:----------:|
| Hem a torn shirt | Tailor | Cobbler | Grocer |
| Fix a sandal strap | Cobbler | Tailor | Florist |
| Buy 2 kg of tomatoes | Grocer | Tailor | Cobbler |
| Print a birthday photo | Photo studio | Grocer | Tailor |

<span style="color:#D9660B">**What you want to happen:**</span>

- Each errand goes to the shop that fits it.
- You trust a shop for a reason, not a loud signboard.
- You never hand over private details.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Would 3 tailors stitch the same shirt in the same way?
> - What would you do if a stranger sent you to a shop that is not there?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. A signboard reads "Number 1 in the whole city". A second reads "Open since 1998, 40 reviews posted on the wall". Which one can you check?**
Hint: Look for something you can count or visit.

**2. You tell a tailor "make it look like my old shirt". Would 2 sample hems on the counter change the result?**
Hint: Think about words versus showing.

**3. A stranger says the best tailor is in "Rose Lane, shop 14". You walk there and find a wall. What should you do before asking him again?**
Hint: Think about how you could have checked first.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do you choose a helper for a job and check its work before you rely on it?**</span>
>
> Which of your own details would you never hand to a new helper?
