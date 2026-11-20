## <span style="color:#2F7DDE">Prompt Chaining with Critique and Personas</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Prompt Chaining with Critique and Personas"]
  Q["<b>The Big Question</b><br/><i>How do I get a helper to match my need, check its own work and reuse the recipe?</i>"]
  CV["<b>Course use case</b><br/>Turning one supplier email into a 3-step chain with a 6-blank template"]
  RL["<b>Real-world example</b><br/>Asking a dietitian friend to plan a week of tiffins for a grandfather"]

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

Have you ever wondered why the same friend gives a different menu when you say who will eat it?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**List**</span> the 4 parts of a clear request to your dietitian friend.
- <span style="color:#D9660B">**Apply**</span> a "plan it like a dietitian for a 78-year-old" line to change the words and depth of her answer.
- <span style="color:#D9660B">**Demonstrate**</span> how you ask her to check her own menu against 3 rules and fix it.
- <span style="color:#D9660B">**Use**</span> one answer, the 5-day menu, as the start of the next request, a shopping list.
- <span style="color:#D9660B">**Build**</span> a request card with 5 blanks you fill in for each new week.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> A full prompt with role, context, constraints and format, role-based prompting, self-critique, prompt chaining, reusable prompt templates, worked examples for email, research and planning.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Anaya wants a week of tiffin menus for her grandfather. He is 78 and eats soft food with little salt.

She texts her friend Neel, a dietitian: "Plan his tiffins." Neel sends 5 days of menus. Two items are fried and one roti is hard.

A short text hides the rules. A clear request names the person, the limits and the shape of the plan.

A <span style="color:#D9660B">**prompt chain**</span> means a set of small requests where the answer to one becomes the start of the next.

You will ask a chat tool for email, research and planning work in the same way.

> <span style="color:#2F7DDE">**Think about it:**</span> Which 2 rules about grandfather's food were missing from Anaya's first text?

---

### <span style="color:#2F7DDE">The Tiffin Menu Puzzle</span>

Here is Anaya's week, with what each request needs.

| Request | What Anaya tells Neel | What she gets |
|:----------:|:----------:|:----------:|
| 1. Plan 5 days | Eater: age 78, soft food | A day-by-day menu |
| 2. Check the menu | Rules: low salt, no fried food, soft | A marked list |
| 3. Shop for the menu | Use the menu from request 1 | A shopping list |

<span style="color:#D9660B">**What you want to happen:**</span>

- Neel writes in words a family member can follow.
- Neel spots a dish that breaks one of your 3 rules.
- You can reuse the same request card for next week.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What would change if Anaya asked for a menu for a 10-year-old cousin?
> - Why ask Neel to check the menu before you buy any food?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Which 2 facts would you add to "Plan his tiffins" so Neel cannot send fried items?**
Hint: Think about who eats and what he must avoid.

**2. Anaya asks Neel to check the menu against the 3 rules. How can she tell the check was honest?**
Hint: Pick one dish and test it yourself.

**3. Next month Anaya plans tiffins for her cousin. Which 3 parts of her request card change?**
Hint: Look at the person, the days and the rules.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do small, checked requests beat one big request?**</span>
>
> Which parts of your own weekly requests could become blanks on a card?
