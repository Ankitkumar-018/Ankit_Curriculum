## <span style="color:#2F7DDE">Where LLMs Work and Fail</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Where LLMs Work and Fail"]
  Q["<b>The Big Question</b><br/><i>Which AI model fits a job, and which answers can you trust alone?</i>"]
  CV["<b>Course use case</b><br/>Choosing a model for 10,000 refund questions at Rs 0.15 or Rs 1.05 per answer"]
  RL["<b>Real-world example</b><br/>Picking a helper for a family quiz night"]

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

Have you ever wondered why a confident quiz-night friend can give a wrong answer?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**List**</span> the 3 kinds of clue a quiz can hold: words, a picture and a sound.
- <span style="color:#D9660B">**Explain**</span> why a sure-sounding friend can be wrong about last week's match.
- <span style="color:#D9660B">**Classify**</span> 6 quiz questions as safe or unsafe for your friend to answer alone.
- <span style="color:#D9660B">**Compare**</span> a friend who answers in 2 seconds with one who thinks for 14 seconds.
- <span style="color:#D9660B">**Judge**</span> whether a helper from a call centre or one living at home suits your budget.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Hosted and open models, reasoning models, multimodal input, fluent but wrong answers, reliable tasks.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Your family plays a quiz on Sunday. You may call a helper from a call centre, or keep a helper at home.

The call-centre helper charges Rs 5 a call. The helper at home costs Rs 2,000 a month. You do not see the call-centre helper's notes, but you see your home helper's notes.

An <span style="color:#D9660B">**LLM**</span> means a large language model, a program that writes text by predicting the next small piece. Different models suit different jobs.

In this course you will choose a model for each job and check its answers.

> <span style="color:#2F7DDE">**Think about it:**</span> Which helper would you pick if you asked 100 questions a month?

---

### <span style="color:#2F7DDE">The Quiz Night Puzzle</span>

Here are 4 questions from Sunday and what each one needs.

| Question | What it needs |
|:----------:|:----------:|
| What is the capital of France? | A quick answer |
| A train leaves at 3 pm at 60 km an hour. When does it reach 150 km? | Time to think |
| What animal is in this photo? | A look at a picture |
| What was today's cricket score? | A live scoreboard |

<span style="color:#D9660B">**What you want to happen:**</span>

- Each question goes to the helper who suits it.
- You know when the helper may give a smooth but wrong reply.
- You keep live facts away from a helper who cannot see them.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Would a helper who thinks for 14 seconds suit the capital question?
> - What would your helper say about the score with no scoreboard nearby?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. You ask 100 questions a month. Which costs less: Rs 5 a call or Rs 2,000 a month?**
Hint: Divide 2,000 by 5 to find where they tie.

**2. The friend answers the cricket score with total confidence. Why should you still doubt it?**
Hint: Ask where he could have seen the score.

**3. You hold up a photo and a voice clip. Which of your helpers can use both?**
Hint: Think about which senses a helper needs.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**Which jobs would you give a smooth talker alone, and which would you check?**</span>
>
> What would you ask a helper to show you before you trust an answer?
