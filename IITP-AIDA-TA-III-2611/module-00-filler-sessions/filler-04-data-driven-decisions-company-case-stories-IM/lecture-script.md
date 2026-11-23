# <font color='#1d4ed8'>Lecture Script: Data-Driven Decisions — Company Case Stories</font>

---

## <font color='blue'>Agenda</font>

The lecture runs as four topics. Each topic ends with a quiz.

| Topic | What we do | Learning objectives covered | Minutes |
|:-:|:--|:--|:-:|
| 1 | Hear three company stories | Recall real examples of data-driven business decisions and their outcomes. | 25 |
| 2 | Link each insight to an action | Explain how a data insight led to a specific business action. | 25 |
| 3 | Count the cost of ignoring or misreading data | Discuss risks of ignoring or misreading data signals. | 25 |
| 4 | Take a side on a dilemma | Form and defend an opinion on a business dilemma using narrative evidence. | 30 |
| — | Closing: Outcome & Summary | | 15 |
| | **Total** | | **120** |

> <font color="red">**🎯 Instructor Note**</font> Pace: this is a story-and-discussion session with no software. Spend the time on the dilemma round in Topic 4. Keep each story to about 6 minutes.
> Story 1 uses facts that Netflix has shared in public. Stories 2 and 3 are invented for teaching. You can replace them with a documented case you have verified.

---

## <font color='blue'>Scenario</font>

**Three stories, one pattern.** A business-news podcast runs a segment called "What did the data say?" This week it tells three stories.

| Story | Company | The decision |
|:-:|:--|:--|
| 1 | Netflix | Which ideas to keep from a famous prediction contest |
| 2 | A Zomato-style food app (invented) | What to do about late deliveries in the rain |
| 3 | A neighbourhood supermarket (invented) | How much stock to hold before the monsoon |

> <font color="red">**🎯 Instructor Note**</font> Zomato is only the setting for Story 2. Do not claim it did any of this. The numbers in Stories 2 and 3 are invented for teaching.

---

## <font color='blue'>Problem Statement</font>

A new analyst, Karan, joins a food-app team. In his first meeting, someone says, "The data is clear: raise rain fees." Another says, "The data is clearly the other way." Both quote the same table. Karan cannot say which is right. He also cannot name a single company that made a big call from data, so he has no story to compare with. He stays silent, and the team picks the louder voice.

> <font color='purple'>**What do real data-driven decisions look like, how does an insight become an action, what goes wrong when data is ignored or misread, and how do we argue for a choice with evidence?**</font>

> <font color="red">**🎯 Instructor Note**</font> Poll: "In a business meeting, which is stronger: the loudest voice or a clear data story?" Give learners 30 seconds to respond in chat. Reveal the answer in the Closing.

---

## <font color='blue'>What We Will Use</font>

You have seen what AI is, what it can do for an analyst and how it works. Today is about the human side: decisions. You need no software. You need your opinions and your reasons.

| Topic | Tools | In one line |
|:-:|:--|:--|
| 1 | Story cards | Recall who did what, and what happened |
| 2 | An insight-to-action chain | Link what the data showed to what the company did |
| 3 | A risk table | Name how data gets ignored or misread |
| 4 | A claim, evidence and risk frame | Defend one choice in four sentences |

---

## <font color='blue'>How: Walking Through the Podcast</font>

```mermaid
flowchart LR
    A["Topic 1<br>Three stories"]
    B["Topic 2<br>Insight to action"]
    C["Topic 3<br>Risks"]
    D["Topic 4<br>Your opinion"]
    E["Closing<br>A data story for Karan"]
    A --> B
    B --> C
    C --> D
    D --> E
    style A fill:#dbeafe,stroke:#2563eb
    style B fill:#dcfce7,stroke:#16a34a
    style C fill:#fef3c7,stroke:#d97706
    style D fill:#ede9fe,stroke:#7c3aed
    style E fill:#fee2e2,stroke:#dc2626
```

---

## <font color='blue'>Topic 1: Hear three company stories</font> `25 min`

> <font color='purple'>**What did each company do, and what happened?**</font>

### <font color='green'>Example: Story 1, the Netflix Prize</font>

> <font color='purple'>**What was the prize, who won, and what did Netflix do with the winning idea?**</font>

In October 2006, Netflix announced the Netflix Prize: US$1 million for any team that could improve the accuracy of its movie-rating predictions (its system was called Cinematch) by 10 percent. In September 2009, the team BellKor's Pragmatic Chaos won. Netflix later wrote publicly (in 2012) that it did not roll out the final winning solution. The extra accuracy did not justify the engineering work, and the business had moved to streaming, where what people actually watch matters more than the stars they give.

**Predict before you read on: What will happen?**

> <font color="red">**🎯 Instructor Note**</font> Ask learners whether Netflix used the winning solution. Expected: many say yes. The public account is that it did not deploy the final solution, and used ideas from earlier prize work.

> <font color='green'>**Result**</font> A prize-winning model was not automatically a business win. The company weighed the cost and the new data (viewing behaviour) and acted on that.

### <font color='green'>Extending it: Stories 2 and 3 (invented)</font>

> <font color='purple'>**What did the other two companies see in their data, and what did they do?**</font>

> <font color="red">**🎯 Instructor Note**</font> Read each story aloud. The numbers are invented for teaching.

| | Story 2: food app in the rain | Story 3: supermarket before the monsoon |
|:--|:--|:--|
| What the data showed | 30 of every 100 rainy-evening orders arrived late, against 8 of every 100 on dry evenings | Umbrellas sold out within 2 days in the first rainy week for 3 years in a row |
| What the company did | Added riders in the rain slots and showed a longer arrival time | Ordered umbrellas 3 weeks before the forecast monsoon date |
| What happened | Late orders on rainy evenings fell from 30 to 18 per 100 | No empty shelf in the first rainy week |

> <font color='green'>**Result**</font> In each story, the company saw a pattern in its own numbers and chose a specific action. The first story is a documented case. The other two are teaching cases.

### <font color='purple'>Quiz 1</font>

**Question:** In the Netflix Prize, what did the winning team have to achieve?

**Options:**
- A) Build a new streaming service
- B) Cut Netflix's costs by 10 percent
- C) Write a new movie script
- D) Improve the accuracy of Netflix's rating predictions by 10 percent

**Correct Answer:** D

**Explanation:**
- **A)** The prize was about prediction accuracy, not a new service.
- **B)** Cost was not the target.
- **C)** Scripts had nothing to do with it.
- **D)** The goal was a 10 percent improvement over the Cinematch predictions.

---

## <font color='blue'>Topic 2: Link each insight to an action</font> `25 min`

> <font color='purple'>**A table of numbers does nothing by itself. What turns an insight into an action?**</font>

### <font color='green'>Example: The insight-to-action chain</font>

> <font color='purple'>**What are the four links between data and a decision?**</font>

| Link | Question | Story 2 (food app) |
|:-:|:--|:--|
| 1. Insight | What did the data show? | Rainy evenings: 30 late per 100 orders. Dry evenings: 8 per 100 |
| 2. Reason | Why might it happen? | Orders rise and fewer riders are on the road |
| 3. Action | What will we do? | Add riders in rain slots, show a longer arrival time |
| 4. Measure | How will we know it worked? | Late orders per 100 in the next rainy week |

**Predict before you read on: What will happen?**

> <font color="red">**🎯 Instructor Note**</font> Cover links 3 and 4. Ask learners to guess an action and a measure from the insight and reason. Expected: add capacity, and track late orders per 100.

> <font color='green'>**Result**</font> A good decision has all four links. An insight with no action wastes the data. An action with no measure cannot be judged.

### <font color='green'>Extending it: Build the chain for Story 3</font>

> <font color='purple'>**Fill in the four links for the supermarket.**</font>

> <font color="red">**🎯 Instructor Note**</font> Take answers in chat first, then show the table.

| Link | Story 3 (supermarket) |
|:-:|:--|
| 1. Insight | Umbrellas sold out within 2 days of the first rain in 3 years |
| 2. Reason | Demand jumps at once, and the usual order arrives late |
| 3. Action | Order umbrellas 3 weeks before the forecast monsoon date |
| 4. Measure | Days with an empty shelf in the first rainy week |

> <font color='green'>**Result**</font> The same four links fit a different business. The action is specific, with a quantity and a date, and the measure can be counted.

### <font color='purple'>Quiz 2</font>

**Question:** Which of these is an action, not an insight?

**Options:**
- A) Add riders in the rain slots
- B) 30 of every 100 rainy-evening orders arrive late
- C) Fewer riders are on the road in the rain
- D) Late orders per 100 in the next rainy week

**Correct Answer:** A

**Explanation:**
- **A)** It is something the company will do.
- **B)** It is a finding in the data, which is an insight.
- **C)** It is a possible reason.
- **D)** It is a measure, used to check the result.

---

## <font color='blue'>Topic 3: Count the cost of ignoring or misreading data</font> `25 min`

> <font color='purple'>**The data was in the room, and the team still got it wrong. How does that happen?**</font>

### <font color='green'>Example: Four ways data goes wrong</font>

> <font color='purple'>**What are the common ways of ignoring or misreading a data signal?**</font>

| Way | What it looks like | Example (invented) |
|:--|:--|:--|
| Ignoring | The signal is there and nobody acts | The supermarket's sell-out pattern sits in a report that nobody reads. Shelves are empty in week 1 |
| Reading too little | A tiny sample is treated as a trend | One rainy evening with 5 late orders leads to a fee change |
| Mixing up cause and effect | Two things move together, and one is blamed for the other | Late orders and rain both rise, and the team blames a rider group |
| Chasing the wrong target | A model that is "more accurate" but cannot be used | A prize-winning model that is too costly to run |

**Predict before you read on: What will happen?**

> <font color="red">**🎯 Instructor Note**</font> Ask which of the four the Netflix story warns about. Expected: the fourth. A better score does not equal a better business result.

> <font color='green'>**Result**</font> Data fails in two ways: people do not act on it, or they read more into it than it holds. Both are about people, not about the numbers.

### <font color='green'>Extending it: Spot the misread</font>

> <font color='purple'>**A store sees that ice-cream sales and drowning news both rise in summer. A manager says, "Ice cream causes accidents, so stop selling it." What went wrong?**</font>

> <font color="red">**🎯 Instructor Note**</font> Take answers in chat. Expected: both rise because of summer heat. One does not cause the other.

> <font color='green'>**Result**</font> Two numbers moving together do not prove that one causes the other. A third factor, the season, explains both.

### <font color='purple'>Quiz 3</font>

**Question:** Ice-cream sales and swimming accidents both rise in summer. What is the best reading?

**Options:**
- A) Ice cream causes accidents
- B) Accidents cause ice-cream sales
- C) A third factor, summer heat, may explain both
- D) The data must be wrong

**Correct Answer:** C

**Explanation:**
- **A)** Moving together does not prove a cause.
- **B)** There is no reason to think accidents drive sales.
- **C)** Summer heat can raise both.
- **D)** The numbers can be right, and the reading wrong.

---

## <font color='blue'>Topic 4: Take a side on a dilemma</font> `30 min`

> <font color='purple'>**Karan's team has two views of the same table. How do we choose, and how do we argue for it?**</font>

### <font color='green'>Example: The rain-fee dilemma</font>

> <font color='purple'>**What would you do?**</font>

The food app's numbers (invented for teaching): on rainy evenings, 1,000 orders came in, and 300 were late. On dry evenings, 1,000 orders came in, and 80 were late. The team has three options.

| Option | What it does | The story in its favour | The risk |
|:--|:--|:--|:--|
| A. Raise the rain fee | Slows demand and pays riders more | Fewer orders per rider, so fewer late orders | Some customers leave for a rival |
| B. Add riders in rain slots | Adds capacity | Directly attacks the cause (too few riders) | Costs money on days when it does not rain |
| C. Show a longer arrival time | Resets expectations | Cheap and quick | Late orders stay late |

**Predict before you vote: What will happen?**

> <font color="red">**🎯 Instructor Note**</font> Take a poll in chat: A, B or C. Expect a split. There is no single right answer. Look for reasons and for the risk each person names.

### <font color='green'>Extending it: Defend your choice in four sentences</font>

> <font color='purple'>**Use this frame: claim, evidence, risk, what would change my mind.**</font>

> <font color="red">**🎯 Instructor Note**</font> Give learners 3 minutes to write four sentences in chat. Call on 3 learners. Praise a named number in the evidence and an honest risk.

| Part | Example for option B |
|:--|:--|
| Claim | "I would add riders in rain slots." |
| Evidence | "300 of 1,000 rainy orders were late, against 80 of 1,000 dry-evening orders." |
| Risk | "The extra riders cost money on dry days, so I would add them only on forecast rain." |
| What would change my mind | "If late orders stay above 20 per 100 even with more riders, the cause is not rider count." |

> <font color='green'>**Result**</font> A strong opinion names a number, owns a risk and says what evidence would change it. A strong opinion can still be wrong, and it can be tested.

### <font color='purple'>Quiz 4</font>

**Question:** Which is the strongest defence of an option?

**Options:**
- A) "I just feel it will work."
- B) "It names a number from the data, owns a risk and says what would change my mind."
- C) "Our competitor did it."
- D) "The boss prefers it."

**Correct Answer:** B

**Explanation:**
- **A)** A feeling is not evidence.
- **B)** Numbers, an honest risk and a test make an argument that others can check.
- **C)** What a competitor did is not proof that it works here.
- **D)** A boss's preference is not evidence.

---

## <font color='blue'>Closing: Outcome & Summary</font> `15 min`

Back to Karan and his silent meeting. He now has stories and a frame.

> <font color='purple'>**1. What data stories can Karan quote?**</font>

The Netflix Prize: a prize-winning model was not deployed in full because of cost and a change to streaming (Topic 1). The food app: the rainy-evening late rate fell after more riders were added (Topics 1 and 2). The supermarket: a repeated sell-out led to an early order (Topics 1 and 2).

> <font color='purple'>**2. How should Karan speak in the meeting?**</font>

He should give an insight, a reason, an action and a measure (Topic 2). He should name the risk of misreading, such as mixing up cause and effect (Topic 3), and use the four-part defence (Topic 4).

### <font color='green'>Outcome</font>

| | First meeting | Next meeting |
|:--|:--|:--|
| Stories | None | Three company stories |
| Argument | Silence | Claim, evidence, risk and what would change his mind |
| Decision | The louder voice | The option with a testable measure |

> <font color='green'>**Therefore,**</font> data-driven decisions turn an insight into a specific action with a measure. They fail when data is ignored or read too far. A clear opinion names its evidence, its risk and its test.

> <font color="red">**🎯 Instructor Note**</font> Reveal the poll: a clear data story. It names a number, an action and a measure, and others can check it.

### <font color='green'>Summary</font>

| Learning objective | Takeaway |
|:--|:--|
| Real examples | Netflix Prize (documented), and two teaching cases about rain and stock |
| Insight to action | Insight, reason, action, measure |
| Risks | Ignoring a signal, reading too little, mixing cause and effect, chasing the wrong target |
| Defend an opinion | Claim, evidence, risk and what would change my mind |
| **Practical value** | You can walk into a meeting with a story, a number and a test |

---

# <font color='red'>Launch the Feedback Poll</font>

> <font color="red">**🎯 Instructor Note**</font> Reminder: launch the feedback poll now to collect learner feedback.
