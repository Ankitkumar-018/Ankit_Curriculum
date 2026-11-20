# <font color='#1d4ed8'>Lecture Script: Careers in AI: Who Does What</font>

---

## <font color='blue'>Agenda</font>

The lecture runs as four topics. Each topic ends with a quiz.

| Topic | What we do | Learning objectives covered | Minutes |
|:-:|:--|:--|:-:|
| 1 | See how AI moved from hand-written rules to learning from examples | Explain how AI moved from following hand-written rules to learning from examples | 30 |
| 2 | Meet the people who build an AI product | List the roles that build and run an AI product and what each does | 25 |
| 3 | Find where non-technical people fit | The same roles list, applied to the roles that need no coding | 20 |
| 4 | Read a job posting in plain language | Rewrite an AI job posting as a plain-language list of requirements | 30 |
| — | Closing: Outcome & Summary | | 15 |
| | **Total** | | **120** |

> <font color="red">**🎯 Instructor Note**</font> Pace: Topic 3 extends the roles list from Topic 2, so keep it brisk. Spend the extra minutes on the rule-versus-learned example in Topic 1 and on the posting rewrite in Topic 4.
> No software is needed. Learners need paper or a notes app. All messages, postings and counts are invented for teaching.

---

## <font color='blue'>Scenario</font>

**A conversation at lunch.** Neha works on the trust team of a Dream11-style fantasy cricket app. The team is building a filter that catches scam messages in match chats. At a family lunch, her cousin Aditya, a commerce student, asks her two questions: "Is AI just millions of rules that someone typed?" and "Do I need to code to work on a team like yours?" He also holds up his phone with a posting for an "AI Product Associate", full of jargon.

> <font color="red">**🎯 Instructor Note**</font> The company is only the setting. Do not claim it works this way. Neha, Aditya, the filter, the chat messages and the posting are invented for teaching. No real job posting or hiring practice is described.

---

## <font color='blue'>Problem Statement</font>

Aditya has two wrong ideas. He thinks AI means programmers typing a rule for every case, and that every AI job needs coding. He closes the posting without reading it and tells Neha, "That is not for people like me." Neha knows that her own team includes people who label examples, check answers and write for users.

Earlier sessions showed how a chat tool predicts text, how to prompt it and where it fails. Today we look at the people behind such tools and at how to read a job posting.

> <font color='purple'>**How did AI move from hand-written rules to learning from examples, who builds and runs an AI product, where does someone like Aditya fit, and what does the posting really ask for?**</font>

> <font color="red">**🎯 Instructor Note**</font> Poll: "Does every job on an AI product team need coding?" Options: yes or no. Give learners 30 seconds to respond in chat. Reveal the answer in the Closing.

---

## <font color='blue'>What We Will Use</font>

No software today. We use tables, one rounded timeline and one small worked example.

| Topic | Ideas | In one line |
|:-:|:--|:--|
| 1 | Hand-written rules, learning from examples | A rule is written by a person. A learned rule is found from labelled examples |
| 2 | Roles that build and run | Product, data, model, application and operations roles |
| 3 | Non-technical roles | Domain, labelling, testing, rules and support roles |
| 4 | A job posting | Turn jargon into a plain list of requirements |

---

## <font color='blue'>How: Walking Through Aditya's Posting</font>

```mermaid
flowchart LR
    A["Topic 1<br>Rules to learning"] --> B["Topic 2<br>Who builds it"]
    B --> C["Topic 3<br>Where non-technical people fit"]
    C --> D["Topic 4<br>Plain-language requirements"]
    D --> E["Closing<br>Aditya's decision"]
    style A fill:#dbeafe,stroke:#2563eb
    style B fill:#dcfce7,stroke:#16a34a
    style C fill:#fef3c7,stroke:#d97706
    style D fill:#ede9fe,stroke:#7c3aed
    style E fill:#fee2e2,stroke:#dc2626
```

---

## <font color='blue'>Topic 1: See how AI moved from hand-written rules to learning from examples</font> `30 min`

> <font color='purple'>**Aditya thinks AI is millions of rules typed by hand. Was it always built that way?**</font>

### <font color='green'>Example: A rounded timeline</font>

> <font color='purple'>**What changed between the first AI programs and today's chat tools?**</font>

Early AI programs followed **hand-written rules**: a person wrote each if-this-then-that step. Later systems used **machine learning**: they found their own rules from labelled **examples**. The years below are rounded.

<p align="center"><img src="images/01_ai_timeline.png" alt="Timeline: 1956 AI named at a summer workshop, 1980 expert systems with hand-written rules, 2000 machine learning from examples spreads, 2012 deep learning wins an image contest, 2017 the transformer model, 2022 public chat tools reach millions" width="900"></p>

| Period | How the system got its rules |
|:--|:--|
| Around 1980 | Experts and programmers wrote the rules by hand |
| From around 2000 | Programs learned rules from many labelled examples |
| After 2012 | Larger learned models, called deep learning, handled images and speech well |
| After 2017 | The transformer design led to the language models behind chat tools |

> <font color='green'>**Result**</font> The shift is from "a person writes every rule" to "a program finds the rule from examples". The examples became the new raw material.

### <font color='green'>Extending it: A rule versus a learned rule</font>

> <font color='purple'>**Which sorts scam chat messages better, a hand-written rule or a rule found from examples?**</font>

> <font color="red">**🎯 Instructor Note**</font> All 20 messages are invented for teaching. The counts were worked out by a separate check. Ask learners to predict which side wins before you show the result. Give learners 30 seconds to respond in chat.

The **hand-written rule** says: a message is a scam if it contains the word "free". The **learned rule** comes from 10 training messages (5 scam, 5 fine). It keeps each word that appears in at least 2 scam messages and in no fine message. The words it found are: click, now, offer, otp, send, your.

Both rules face 10 new messages. S means scam and H means fine.

| # | New message | True | Hand-written rule | Learned rule |
|:-:|:--|:-:|:-:|:-:|
| 1 | Free coins claim now | S | S, right | S, right |
| 2 | Send OTP to get your prize | S | H, wrong | S, right |
| 3 | Win cash prize click link | S | H, wrong | S, right |
| 4 | Offer for you send OTP now | S | H, wrong | S, right |
| 5 | Free gift click here | S | S, right | S, right |
| 6 | Free tips for tonight match | H | S, wrong | H, right |
| 7 | Is the match at 7 pm | H | H, right | H, right |
| 8 | Good luck with your team | H | H, right | S, wrong |
| 9 | Will you win today | H | H, right | H, right |
| 10 | Send me your team name | H | H, right | S, wrong |

$$\text{hand-written: } \frac{6}{10} = 60\% \qquad \text{learned: } \frac{8}{10} = 80\%$$

<p align="center"><img src="images/02_rule_vs_learned_accuracy.png" alt="Bar chart: the hand-written rule sorts 6 of 10 new messages correctly and the learned rule sorts 8 of 10" width="900"></p>

> <font color='green'>**Result**</font> The learned rule did better on these 10 messages, but it also made two mistakes. It treated "your" as a scam word, because "your" appeared in two scam messages and no fine ones. Learned rules are only as good as their examples.

> <font color='#b45309'>**Common mistake**</font> Thinking that a learned rule is always right. Fix: it reflects its examples, so people check it on new messages.

### <font color='purple'>Quiz 1</font>

**Question:** Which statement describes the move from hand-written rules to learning from examples?

**Options:**
- A) Programmers stopped writing any code
- B) The program finds its own rules from labelled examples instead of a person writing every rule
- C) Computers started using electricity
- D) The rules became longer, but a person still wrote each one

**Correct Answer:** B

**Explanation:**
- **A)** People still write the code that trains and runs the systems.
- **B)** Correct. The rules come from patterns in labelled examples.
- **C)** Computers always used electricity. That is not the shift.
- **D)** The point is that the rule was found from data, not typed by a person.

---

## <font color='blue'>Topic 2: Meet the people who build an AI product</font> `25 min`

> <font color='purple'>**A filter like this needs examples, models, an app and someone to keep it running. Who does each job?**</font>

### <font color='green'>Example: Roles on the scam-filter team</font>

> <font color='purple'>**Which roles build and run an AI product, and what does each do?**</font>

Job titles differ between companies. The work below is what matters.

| Role | What the role does | In the scam filter |
|:--|:--|:--|
| Product manager | Decides what to build, for whom, and how success is measured | Sets the goal: fewer scam messages reach users |
| Data engineer | Builds the pipelines that collect, clean and store data | Gathers chat messages safely |
| Data scientist or analyst | Explores the data, chooses measures and tests ideas | Checks which words signal a scam |
| Machine learning engineer | Trains, tests and packages models | Trains the learned rule from labelled examples |
| AI application engineer | Builds the app around the model, calls model services and writes prompts | Connects the filter to the chat screen |
| MLOps or platform engineer | Deploys the model, watches it and keeps it running | Alerts the team when accuracy drops |

> <font color="red">**🎯 Instructor Note**</font> Ask learners which role they would ask when the filter flags a fine message as a scam. Give learners 30 seconds to respond in chat. Expected: the data scientist or the machine learning engineer, then the product manager.

> <font color='green'>**Result**</font> Six roles cover the build and the run: set the goal, collect data, study it, train the model, build the app and keep it running.

#### <font color='#c2410c'>Logic Explanation</font>

- The work moves in a line: goal, data, model, app, running system.
- In a small team, one person may hold two of these roles. In a large team, each role has several people.

### <font color='green'>Extending it: Match the task to the role</font>

> <font color='purple'>**Who owns each task?**</font>

> <font color="red">**🎯 Instructor Note**</font> Ask learners to type a role for each task before you reveal the column.

| Task | Role |
|:--|:--|
| "Decide that the goal is to cut scam chats by half" | Product manager |
| "Remove duplicate messages from the stored data" | Data engineer |
| "Train the model on 1,000 labelled messages" | Machine learning engineer |
| "Page the team at 2 am when the filter stops working" | MLOps or platform engineer |

> <font color='green'>**Result**</font> A task belongs to the role whose work it is, not to whoever is available.

### <font color='purple'>Quiz 2</font>

**Question:** Which role trains, tests and packages the model?

**Options:**
- A) Product manager
- B) Data engineer
- C) Support agent
- D) Machine learning engineer

**Correct Answer:** D

**Explanation:**
- **A)** The product manager sets the goal and the measure of success.
- **B)** The data engineer builds the data pipelines.
- **C)** A support agent helps users and escalates problems.
- **D)** Correct. This role trains, tests and packages models.

---

## <font color='blue'>Topic 3: Find where non-technical people fit</font> `20 min`

> <font color='purple'>**Aditya cannot code. Which parts of the filter's team need no coding at all?**</font>

### <font color='green'>Example: Roles that need no coding</font>

> <font color='purple'>**Which roles on the same team are not built on programming skills?**</font>

The roles below continue the list from Topic 2. Each is part of building and running the same product.

| Role | What the role does | In the scam filter |
|:--|:--|:--|
| Domain expert | Knows the business and its rules | Says what a real scam looks like in fantasy cricket |
| Data labeller | Marks each example with the right answer | Tags 1,000 messages as scam or fine |
| Tester or evaluator | Checks outputs against a checklist | Reviews 100 filter decisions a week |
| Legal, privacy and compliance | Makes sure data use follows the rules | Checks that chats are used lawfully |
| Support and operations | Helps users and escalates problems | Handles users whose messages were wrongly blocked |

> <font color='green'>**Result**</font> Five roles need judgement and care, not code. Without labellers and evaluators, the learned rule has no examples to learn from and no check.

### <font color='green'>Extending it: Where would Aditya's skills fit?</font>

> <font color='purple'>**Which role fits a commerce student who writes clearly and checks details?**</font>

> <font color="red">**🎯 Instructor Note**</font> Ask learners to type one role that fits Aditya and one skill that supports it. Give learners 30 seconds to respond in chat. Several answers are valid.

| Aditya's strength | Roles that fit |
|:--|:--|
| Checks details and finds errors | Tester or evaluator |
| Understands money and rules | Domain expert, compliance |
| Writes clearly for users | Support, product assistant |
| Organises work and explains progress | Product assistant or associate |

> <font color='green'>**Result**</font> A non-coder can hold a real role on an AI team. The test is what the role needs, not whether it has "AI" in the name.

> <font color='#b45309'>**Common mistake**</font> Assuming that no coding means no technical understanding. Fix: these roles still need to know what the model can and cannot do.

### <font color='purple'>Quiz 3</font>

**Question:** Which role on an AI product team marks each example with the right answer so a model can learn from it?

**Options:**
- A) Data labeller
- B) MLOps engineer
- C) Legal and compliance officer
- D) Support agent

**Correct Answer:** A

**Explanation:**
- **A)** Correct. A labeller tags examples, and no coding is needed.
- **B)** The MLOps engineer deploys and monitors the system.
- **C)** Legal and compliance check that data use follows the rules.
- **D)** Support helps users and escalates problems.

---

## <font color='blue'>Topic 4: Read a job posting in plain language</font> `30 min`

> <font color='purple'>**Aditya stopped at the jargon. What does the posting actually ask for?**</font>

### <font color='green'>Example: Decode the posting</font>

> <font color='purple'>**How do we turn jargon into a plain list of requirements?**</font>

> <font color="red">**🎯 Instructor Note**</font> The posting below is invented for teaching. Do not present it as a real company's ad. Ask learners to circle the 3 phrases they find hardest.

> **AI Product Associate.** Leverage LLM capabilities to drive cross-functional roadmaps. Define evaluation harnesses and KPIs for generative AI features. Partner with engineers to iterate on prompts. Synthesise stakeholder requirements. **Requirements:** 2+ years in product or analytics; familiarity with Python and SQL; excellent communication; exposure to responsible AI.

Use three steps. First, find each action word. Second, replace each jargon phrase with plain words. Third, split the list into must have and nice to have.

| Jargon in the posting | In plain words |
|:--|:--|
| Leverage LLM capabilities | Use a chat-style AI tool to do the work |
| Cross-functional roadmaps | Plans that involve several teams |
| Evaluation harnesses and KPIs | Tests and numbers that show whether the feature works |
| Iterate on prompts | Try, check and improve the instructions given to the AI |
| Synthesise stakeholder requirements | Collect what each team needs and summarise it |
| Exposure to responsible AI | Knows about privacy and fairness basics |

> <font color='green'>**Result**</font> The posting is mostly: plan work with other teams, test AI features, improve prompts and summarise needs.

### <font color='green'>Extending it: The plain-language requirements list</font>

> <font color='purple'>**What is the list of requirements after the rewrite?**</font>

| Must have | Nice to have |
|:--|:--|
| 2 or more years in product or data analysis work | Basic Python |
| Can write a clear prompt and check an AI answer | Basic SQL |
| Can explain progress to people who are not technical | Knowledge of privacy and fairness basics |
| Can plan work with several teams | |

> <font color="red">**🎯 Instructor Note**</font> Learners now rewrite one real posting of their own choice, from a public job site, using the three steps. They bring back one jargon phrase and its plain version. Give learners 30 seconds to respond in chat.

> <font color='green'>**Result**</font> A plain list lets you compare your skills with the role. Aditya can tick the must-haves he already meets and plan to learn the nice-to-haves.

> <font color='#b45309'>**Common mistake**</font> Reading "familiarity with" as "expert in". Fix: ask which items are must have and which are nice to have, and apply anyway if you meet most.

### <font color='purple'>Quiz 4</font>

**Question:** Which line is the best plain-language rewrite of "Iterate on prompts"?

**Options:**
- A) Write code to train models
- B) Run the company
- C) Try, check and improve the instructions given to the AI
- D) Read research papers

**Correct Answer:** C

**Explanation:**
- **A)** Training models is a different job.
- **B)** The phrase does not mean running the company.
- **C)** Correct. A prompt is the instruction given to the AI, and iterating means trying, checking and improving it.
- **D)** The phrase does not mention research papers.

---

## <font color='blue'>Closing: Outcome & Summary</font> `15 min`

Back to Aditya. We answer the Problem Statement using each topic once.

> <font color='purple'>**1. How did AI get here? (Topic 1)**</font>

It moved from rules typed by hand around 1980 to rules learned from labelled examples. On our 10 test messages, the learned rule got 8 right against 6 for the hand-written rule, and it still made 2 mistakes.

> <font color='purple'>**2. Who builds and runs it? (Topic 2)**</font>

A product manager, data engineer, data scientist or analyst, machine learning engineer, AI application engineer and MLOps engineer.

> <font color='purple'>**3. Where does he fit? (Topic 3)**</font>

Domain expert, data labeller, tester or evaluator, legal and compliance, and support roles need judgement and care, not code.

> <font color='purple'>**4. What does the posting ask? (Topic 4)**</font>

Four must-haves and three nice-to-haves, once the jargon is rewritten in plain words.

### <font color='green'>Outcome</font>

| | Aditya's first reading | Aditya's reading after today |
|:--|:--|:--|
| What AI is | Millions of hand-typed rules | Rules found from examples, checked by people |
| Who builds it | Programmers only | Technical and non-technical roles |
| The posting | Jargon, so he skips it | 4 must-haves, 3 nice-to-haves |
| Her decision | Do not apply | Apply, and say which must-haves he meets |

> <font color='green'>**Therefore,**</font> AI moved from hand-written rules to rules learned from examples. An AI product needs build roles, run roles and non-technical roles. Rewriting a posting in plain words shows Aditya which requirements he already meets, so he can apply.

> <font color="red">**🎯 Instructor Note**</font> Reveal the poll: no. Labellers, evaluators, domain experts, compliance and support roles need no coding.

### <font color='green'>Summary</font>

| Learning objective | Takeaway |
|:--|:--|
| How AI got here | From rules written by people to rules learned from labelled examples |
| Roles that build and run | Product, data, model, application and operations roles each own part of the work |
| Where non-technical people fit | Domain, labelling, testing, compliance and support roles |
| Plain-language posting | Find the actions, replace jargon, split must have from nice to have |
| **Practical value** | Knowing who does what helps you choose a role and read a posting with confidence |

---

# <font color='red'>Launch the Feedback Poll</font>

> <font color="red">**🎯 Instructor Note**</font> Reminder: launch the feedback poll now to collect learner feedback.
