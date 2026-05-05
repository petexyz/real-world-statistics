# Instructor Notes: Real-World Applications of Statistics
### Last Lecture -- Elementary Statistics

**Estimated total time:** 90-110 minutes
**Format:** RevealJS slideshow, presented fullscreen in a browser
**Controls:** Arrow keys to advance, S for speaker view, F for fullscreen

---

## Pre-Class Setup

- Open `index.html` in Chrome or Firefox and press F for fullscreen before students arrive
- Press S to open speaker view in a second window -- your notes will appear there while students see the clean slides
- Have the birthday demo slider (Section 6) ready -- students enjoy interacting with it
- If the room has a second screen or monitor, use RevealJS speaker view: students see the slide, you see your notes and the next slide

---

## Pacing Guide

| Slide Group | Section | Time | Slides |
|-------------|---------|------|--------|
| Cover + Agenda | Opening | 3 min | 2 |
| Clever Hans story | Section 1 | 5 min | 1 |
| Blinding diagram | Section 1 | 4 min | 1 |
| Poker | Section 1 | 5 min | 1 |
| AI pipeline | Section 1 | 5 min | 1 |
| Quiz 1 | Section 1 | 2 min | 1 |
| Storks scatter | Section 2 | 6 min | 1 |
| Confounding variable | Section 2 | 5 min | 1 |
| Quiz 2 | Section 2 | 2 min | 1 |
| Okun scatter | Section 3 | 6 min | 1 |
| Okun time series + lag | Section 3 | 6 min | 1 |
| Two distributions | Section 4 | 4 min | 1 |
| Mean vs. median | Section 4 | 5 min | 1 |
| Height-income correlation | Section 4 | 4 min | 1 |
| TI-84 steps | Section 4 | 4 min | 1 |
| Wald / planes | Section 5 | 6 min | 1 |
| Funds chart | Section 5 | 4 min | 1 |
| Quiz 3 | Section 5 | 2 min | 1 |
| Birthday calculator | Section 6 | 4 min | 1 |
| Birthday curve + table | Section 6 | 4 min | 1 |
| Live demo | Section 6 | 5 min | 1 |
| Six questions | Closing | 3 min | 1 |
| Final slide | Closing | 1 min | 1 |
| **Total** | | **~95 min** | **24** |

---

## Section-by-Section Notes

---

### Opening (3 minutes)

Frame this as synthesis, not new content. Students have seen all the tools -- today they see what the tools are actually for.

Open with something like: *"No new formulas today. Everything we cover, you have technically already seen. What we are doing is connecting it to the world you actually live in."*

Do not start with housekeeping. Go straight into the Clever Hans story -- it is immediately engaging and sets the right tone.

---

### Section 1: The Observer Effect (21 minutes across 5 slides)

**Slide: Clever Hans (1907) -- 5 minutes**

Tell the story as a narrative before the slide appears. Ask students to guess the explanation before you reveal it.

Key beats in order:
1. Von Osten was completely sincere -- he genuinely believed the horse could reason. He never charged admission. He was not a fraud.
2. Public demonstrations attracted journalists, scientists, and government officials. The 1904 Hans Commission -- thirteen experts -- concluded no trickery was involved.
3. Pfungst's decisive test: vary whether the questioner knows the answer.
4. Result: 89% correct when questioner knows, 6% when they do not.

Pause after revealing the 89%/6% numbers. Let it land. Then ask: "So what was Hans actually doing?" Students usually land on "reading body language" quickly.

The micro-cue detail -- a barely perceptible head dip at the moment the questioner's tension released -- is worth describing vividly. It was not conscious. Von Osten had no idea he was doing it.

**Slide: Blinding diagram -- 4 minutes**

The diagram shows the mechanism. Walk through it left to right:
- Left panel: questioner knows, cue transmitted, Hans performs
- Right panel: questioner does not know, no cue, Hans at chance

Make the connection to research design explicit: this is exactly why drug trials use double-blind protocols. The doctor's behavior -- how encouraging they are, how they interpret borderline results -- shifts when they know which patient got the real drug.

**Slide: Poker -- 5 minutes**

This is the most expanded new section. The key insight: professional poker players have independently arrived at the same solution as experimental scientists -- eliminate the observable signal that leaks from one party to another.

Walk through each bullet point with a concrete example:

- **Sunglasses:** Pupils dilate involuntarily when you see something exciting -- like a strong hand. Mirrored lenses prevent this from being readable.
- **Consistent timing:** If you bet quickly with strong hands and slowly with weak ones, a sharp opponent will catch it within a few hands. Pros use the same deliberate 10-15 second pause every single decision, regardless of hand strength.
- **False tells:** Some pros deliberately rub their nose or tap the table before a strong hand -- planting a readable signal that they then use against opponents who think they have spotted a tell.
- **Neutral attire:** Jaw tension, a clenched neck, or a subtle swallow are nearly impossible to consciously suppress. Covering them eliminates the channel entirely.

Ask students: "What other competitive situations require this kind of information control?" Good answers include: negotiation, poker, chess (time management as a tell), sports (pitchers hiding grip).

**Slide: Artificial Intelligence -- 5 minutes**

This is the section that will resonate most with this generation. Spend time on the feedback loop diagram.

Walk through the three mechanisms:

1. **Labeled training data:** Someone had to decide what counted as the "correct" label for each piece of training data. If those people had systematic blind spots -- about what faces look professional, what writing sounds authoritative, what answers seem correct -- the model absorbed those blind spots.

2. **Feedback loops:** When a model's output influences what users see, and that user behavior becomes future training data, bias can compound. A recommendation algorithm that slightly favors certain content will generate more engagement data for that content, which makes it favor that content more strongly in the next training cycle.

3. **Benchmark design:** A model that scores 95% on a benchmark may have learned to pass that specific benchmark rather than acquired genuine capability. The benchmark itself was designed by people with expectations about what "good performance" looks like.

The discussion question -- "When an AI confidently gives you a wrong answer, what does the Clever Hans story suggest?" -- is worth 2-3 minutes of student response. The answer: the model learned from human-generated text, and humans write confidently even when they are wrong. The model learned the pattern of confident language, not the truth behind it.

**Slide: Quiz 1 -- 2 minutes**

Correct answer: B (doctors may unconsciously treat patients differently).

If students pick A or C, use it as an opening to reinforce the observer effect concept. Sample size is a separate issue. And drugs absolutely can be tested in blind conditions -- that is the whole point of placebo design.

---

### Section 2: Do Storks Deliver Babies? (13 minutes across 3 slides)

**Slide: A Real Study. A Real Result. -- 6 minutes**

Do not reveal the confounding variable yet. Show the scatter plot and let students look at it for a moment.

Then show the r value (0.62) and p-value (0.008) without explanation. Ask: "What do we conclude?"

Wait for someone to say "more storks cause more babies" or something equivalent. Then ask: "Is there any other possibility?" Students will usually get to "some third factor" quickly.

The combination of an absurd conclusion and a real p-value reliably produces the right kind of laughter -- the kind that comes with genuine recognition that statistics can mislead.

After revealing the answer, make the point explicitly: the p-value tells you the correlation is unlikely to be due to chance. It tells you nothing about whether the relationship is causal.

**Slide: Confounding variable -- 5 minutes**

Walk through the diagram. The key move: country size drives both stork populations (more rural land = more habitat) and birth rates (larger, less urbanized countries have higher birth rates). Neither variable is causing the other.

Ask: "How would you test whether country size is really the explanation?" The answer: hold country size constant. Analyze within groups of similar-sized countries. The correlation disappears.

This is the bridge to randomized experiments. Random assignment breaks the link between the confounder and the treatment, which is why randomized controlled trials are the gold standard in medicine.

**Slide: Quiz 2 -- 2 minutes**

Correct answer: C (confounding variable like family income).

This bridges directly to the storks example. Family income correlates with both having breakfast reliably available and with better academic performance through a dozen pathways -- stability, parental involvement, better schools, less stress.

---

### Section 3: Okun's Law (12 minutes across 2 slides)

**Slide: GDP Growth vs. Unemployment -- 6 minutes**

Lead with the scatter plot. Before explaining it, ask students to read it:
- "What does the direction of the slope tell you?"
- "What does the scatter around the line tell you?"
- "What do the recession arrows show?"

Students can identify the negative correlation themselves. The scatter is the teaching moment: real economic relationships are never clean. The points off the line represent recessions of different types, different industries, different eras.

Address the common question directly: "Is Okun's Law actually a law?" No. It is an empirical regularity -- a well-supported rule of thumb that has held for six decades but is not a physical law. The coefficient varies across time periods and countries.

**Slide: The Lag -- 6 minutes**

Walk through the time series. Students will recognize the 2008 crisis and 2020 COVID recession viscerally.

Ask: "Does unemployment peak at the same time GDP hits its lowest point?" No -- it peaks later. That is the lag in action.

The explanation of why: companies do not immediately fire everyone when a recession begins. They reduce hours, freeze hiring, cut contractors, and only then cut permanent staff. When recovery begins, they wait for confirmation before committing to payroll. Finding, interviewing, and training workers takes months.

The practical implication: this is why people often feel like a recession is still happening even after economists say it ended. GDP has recovered. The job market, which is what most people feel directly, has not caught up yet. Both descriptions can be accurate simultaneously.

---

### Section 4: The Shape of Income (17 minutes across 4 slides)

**Slide: Two distributions -- 4 minutes**

Put the two charts side by side and let students look before talking. Ask: "What is different about the shape of these two distributions?"

Height: symmetric. Tails are roughly equal on both sides. The mean, median, and mode all land at the same place.

Income: right-skewed. A long tail extends far to the right. The bulk of households cluster at lower-to-middle incomes, but a small number of households earn extraordinary amounts.

**Slide: Mean vs. Median -- 5 minutes**

The company example is the clearest illustration. Walk through the arithmetic:
- 9 workers at $40,000 = $360,000 total
- 1 CEO at $1,000,000
- Total payroll: $1,360,000
- Divide by 10: mean = $136,000

Nobody at the company earns $136,000. The mean is mathematically correct and completely misleading as a description of what a typical worker earns.

The order of statistics in a right-skewed distribution -- mode < median < mean -- is worth writing down or photographing. It is a diagnostic students can apply to any income, wealth, or price data they encounter in the news.

**Slide: Height-income correlation -- 4 minutes**

This is a fun bridge between the two distribution types. One is normally distributed, one is right-skewed -- and they are weakly correlated.

Key numbers to land:
- r = 0.13 to 0.20 across studies -- weak positive, but statistically significant
- r-squared = approximately 0.02 -- height explains about 2% of the variation in income

The r-squared number is the teaching moment: statistically significant does not mean practically important. With a large enough sample, even a tiny correlation will pass a significance test. Height is a real but very minor factor in a very complicated picture.

Then ask: "Wait -- could this be a confounding variable problem?" Yes. Childhood nutrition and family socioeconomic status correlate with both height and adult income. Height may partly be a proxy for those advantages.

**Slide: TI-84 steps -- 4 minutes**

Walk through the four steps live if calculators are available. If not, walk through the expected output and focus on interpreting r and r-squared.

The key question to ask students after they see the output: "If r = 0.15 and the p-value is 0.001, does that mean height is an important predictor of income?" No -- important and significant are different things. r-squared = 0.02 means 98% of income variation is explained by something else.

---

### Section 5: Survivorship Bias (12 minutes across 3 slides)

**Slide: Abraham Wald and the WWII Bombers -- 6 minutes**

Tell this story slowly and with some drama. Build up before revealing Wald's insight.

Setup: "You are an engineer in 1943. Bombers are being shot down. Your team examines 100 planes that came back. You map every bullet hole. Most damage is on the wings, fuselage, and tail. Where do you put the armor?"

Wait for student answers. Most will say reinforce where the holes are. Then deliver the insight.

The philosophical core is worth a full sentence on its own: "The planes they were looking at were the ones that survived. Bullet holes in the wings and fuselage were common on returned planes for exactly one reason -- those hits did not bring the plane down. The planes that took engine hits never came back. They were not in the dataset."

Then: "The absence of data was the data."

**Slide: Mutual funds -- 4 minutes**

The chart makes the point visually. Left panel: of 355 funds that existed in 2000, fewer than half survived to 2023. Right panel: the survivor-only reported returns are dramatically higher than the true all-fund average.

Ask: "If you saw a fund company advertise 8% average annual returns over 20 years, and you knew about survivorship bias, what is the first question you would ask?"

Answer: "Of how many original funds is that 8% the average? And what happened to the ones that are not included?"

**Slide: Quiz 3 -- 2 minutes**

Correct answer: B (unemployed or underemployed graduates who did not respond).

This is the schools-as-survivors problem. Graduates who found high-paying jobs are proud to report them. Graduates who are working part-time, still job searching, or took positions well below their degree level are far less likely to respond to a salary survey. The published figure is a biased sample of outcomes.

---

### Section 6: The Birthday Problem (13 minutes across 3 slides)

**Slide: Birthday calculator -- 4 minutes**

Before touching the slider, ask the class: "In a room of 30 people, what is the probability that at least two share a birthday? Write down your guess."

Take a few guesses aloud. Most will be in the 5-20% range.

Then reveal the slider result: 70.6%. Watch the reactions.

Let students interact with the slider. Ask: "Drag it until you find where it crosses 50%. What number is that?" (23.) "What number does it hit 99%?" (57.)

**Slide: Birthday curve and table -- 4 minutes**

The table is the anchor. Walk through the numbers. The jump from 10 people (12%) to 23 people (50%) is the most surprising.

Explain why intuition fails: "We think about this as 'what is the chance someone shares MY birthday?' That probability is small for a room of 30 -- about 8%. But the actual question is: what is the chance any two people share any birthday? With 30 people there are 435 different pairs. Each pair is a separate chance for a match."

The number of pairs growing faster than the number of people is the key mechanism. Going from 20 to 30 people does not add 10 more chances for a match -- it adds roughly 250 more pairs.

**Slide: Live demo -- 5 minutes**

This is the best closer in the course. Do it in every class.

Set the slider to the actual class size. Go around the room. Every student says their birthday out loud. Ask the class to call "match!" the moment they hear a repeated birthday.

In a class of 25-30, a match typically occurs in the first 20-25 students. The moment it happens is always memorable.

If no match occurs: "We beat the odds today. That happens about 30% of the time in a class of 30. If we ran this experiment in ten different classes of 30, we would see a match in about seven of them."

---

### Closing (4 minutes across 2 slides)

**Slide: Six questions**

Read each question slowly. Pause between them. Suggest students write them down or photograph the slide.

These are the transferable product of the course. The formulas will fade. These questions stay useful.

**Final slide**

End here. Brief. The quote lands better in silence than with additional commentary.

---

## Anticipated Student Questions

**"Is Okun's Law still valid after COVID?"**
The 2020 recession and 2021 recovery were exceptional -- unemployment spiked far more sharply than Okun would predict and recovered faster than Okun would predict. Most economists believe Okun's Law holds over normal business cycles but that COVID was outside its domain of applicability.

**"Does the stork correlation actually disappear when you control for country size?"**
Yes. When you analyze within groups of countries of similar size and urbanization, the relationship between storks and birth rates is no longer statistically significant. This is the standard test for whether a confounding variable explains a correlation.

**"If height explains only 2% of income, why do the studies bother reporting it?"**
Two reasons. First, it is still statistically significant and consistently replicated -- it tells us something real about the relationship, even if modest. Second, even a 2% explanation can matter at scale. Across a 30-year career, 2% of income variation translates to real dollars. The point is not that height is irrelevant, but that it is a minor factor in a complex picture.

**"How do we know the mutual fund survivorship bias numbers are right?"**
The studies track all funds from a starting date forward and compare reported performance (survivors only) against the full original cohort. Elton, Gruber, and Blake (1996) is the landmark paper. The methodology is transparent and has been replicated.

**"Why does the birthday probability matter outside a party trick?"**
The birthday problem is the mathematical foundation for understanding coincidences, hash collisions in cryptography, DNA database false matches, and any situation where you are asking whether any two items in a set share a property. It is not a party trick -- it is a fundamental result in combinatorial probability.

---

## If You Have Extra Time

- **The Monty Hall Problem** -- similar intuition-defying probability; works well as a follow-on to the birthday problem
- **Publication bias** -- the scientific literature as a survivorship bias problem; connects to replication crisis
- **Regression to the mean** -- why exceptional performance tends to be followed by more average performance; relevant to sports, medicine, and business

---

*Instructor notes by Pete Halbeisen*
*Corresponds to index.html -- RevealJS slideshow, 24 slides*
*Last updated: Rev 1.4*
