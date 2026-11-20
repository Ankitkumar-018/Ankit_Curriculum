## <span style="color:#2F7DDE">Prompt Chaining with Critique and Personas</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Prompt Chaining with Critique and Personas"]
  Q["<b>The Big Question</b><br/><i>How do you get a precise answer, improve it, and reuse the recipe?</i>"]
  CV["<b>Course use case</b><br/>Writing a refund-reminder email for 38 bookings, then reusing the prompt for a second hotel"]
  RL["<b>Real-world example</b><br/>Ordering a custom birthday cake from a bakery"]

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

Have you ever wondered why a baker gets your cake order right when you write it on a form?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**List**</span> the 4 details every cake order needs: the job, the facts, the shape and the limits.
- <span style="color:#D9660B">**Demonstrate**</span> how telling the baker to act as a pastry chef changes the words in the reply.
- <span style="color:#D9660B">**Apply**</span> a check, such as "does the slip show 2 kg and Friday 5 pm?", to the baker's order slip.
- <span style="color:#D9660B">**Trace**</span> how a design sketch becomes a price, and the price becomes a pickup message.
- <span style="color:#D9660B">**Design**</span> an order form with blanks that you reuse for a 1 kg or a 3 kg cake.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Full prompt, role prompting, self-critique, prompt chaining, reusable templates.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Your cousin's birthday is on Friday. You call a bakery and say, "I want a cake."

The baker asks 6 questions: the flavour, the weight, the date, the message, the budget and the allergies. You answer, and the order is clean.

A <span style="color:#D9660B">**prompt**</span> means the instruction you give an AI tool. A vague prompt gets the same 6 questions back, or a wrong guess.

In this course you will write prompts that leave no questions open.

> <span style="color:#2F7DDE">**Think about it:**</span> What would the baker make if you only said "a cake"?

---

### <span style="color:#2F7DDE">The Birthday Cake Puzzle</span>

Here is the order for your cousin's cake.

| Detail | Your order |
|:----------:|:----------:|
| Flavour | Mango |
| Weight | 2 kg |
| Message on top | Happy Birthday Tara |
| Pickup | Friday, 5 pm |
| Budget | Rs 1,800 |

<span style="color:#D9660B">**What you want to happen:**</span>

- The baker writes down all 5 details without asking again.
- The baker checks the slip against your list before baking.
- Next month you reuse the same form for a 1 kg cake.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Would the baker bake differently if you said "you are a pastry chef who loves mangoes"?
> - If the baker writes the price on the slip, can that price feed your pickup message?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. You hand over the slip. Which 2 checks would you ask the baker to check before baking?**
Hint: Compare the slip with your 5 details.

**2. The price goes up from Rs 1,800 to Rs 2,200 after a design change. What do you do with the next message?**
Hint: One answer feeds the next question.

**3. Which 2 details of your order stay the same next month, and which 2 change?**
Hint: Weight and date are likely to change.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How can one carefully written order be checked, chained and reused?**</span>
>
> Which of your own weekly tasks would you turn into a fill-in-the-blank form?
