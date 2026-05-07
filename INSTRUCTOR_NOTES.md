# Instructor Notes: Real-World Applications of Statistics
### Last Lecture -- Statistics - MAT 177

**Estimated total time:** ~109 minutes
**Format:** RevealJS slideshow, presented fullscreen in a browser
**Controls:** Arrow keys to advance, S for speaker view, F for fullscreen

---

## Pre-Class Setup

- Open `index.html` in Chrome or Firefox and press F for fullscreen before students arrive
- Press S to open speaker view in a second window -- your notes appear there while students see the clean slide
- If the room has a second screen or monitor, RevealJS speaker view shows your notes and the next slide simultaneously
- Have the birthday demo ready for Section 6 -- students enjoy interacting with the slider
- Consider letting a student volunteer operate the billionaire slider in Section 4

---

## Pacing Guide

| Slide | Section | Time |
|-------|---------|------|
| Cover + Agenda | Opening | 3 min |
| Clever Hans story | Section 1 | 5 min |
| Blinding diagram | Section 1 | 4 min |
| Poker | Section 1 | 5 min |
| AI pipeline | Section 1 | 5 min |
| Quiz 1 | Section 1 | 2 min |
| Storks scatter + r and p explained | Section 2 | 7 min |
| Confounding variable | Section 2 | 5 min |
| Quiz 2 | Section 2 | 2 min |
| GDP Growth vs. Unemployment | Section 3 | 6 min |
| Okun time series + lag | Section 3 | 6 min |
| Quiz 3 | Section 3 | 2 min |
| Section 4 header | Section 4 | 1 min |
| The real shape of income | Section 4 | 4 min |
| Mean vs. median | Section 4 | 5 min |
| Income by bracket | Section 4 | 4 min |
| 40-year income trend | Section 4 | 5 min |
| Lorenz curve | Section 4 | 5 min |
| International Gini | Section 4 | 4 min |
| Wealth vs. income | Section 4 | 4 min |
| Billionaire slider | Section 4 | 4 min |
| Quiz 4 | Section 4 | 2 min |
| Survivorship planes | Section 5 | 6 min |
| Funds chart | Section 5 | 4 min |
| Quiz 5 | Section 5 | 2 min |
| Birthday calculator | Section 6 | 4 min |
| Birthday curve + table | Section 6 | 4 min |
| Quiz 6 | Section 6 | 2 min |
| Six questions | Closing | 3 min |
| Final slide | Closing | 1 min |
| **Total** | | **~109 min** |

---

## Section-by-Section Notes

---

### Opening (3 minutes)

Frame this as synthesis, not new content. Students have seen all the tools -- today they see what those tools are actually for.

Open with something like: *"No new formulas today. Everything we cover, you have technically already seen. What we are doing is connecting it to the world you actually live in."*

Do not start with housekeeping. Go straight into the Clever Hans story -- it is immediately engaging and sets the right tone for everything that follows.

---

### Section 1: The Observer Effect (21 minutes -- 6 slides)

**Slide: Clever Hans (1907) -- 5 minutes**

Tell the story as a narrative before the slide appears. Ask students to guess the explanation before you reveal it.

Key beats:
1. Von Osten was completely sincere -- he genuinely believed the horse could reason. He never charged admission. He was not a fraud.
2. Public demonstrations attracted journalists, scientists, and government officials. The 1904 Hans Commission -- thirteen experts -- concluded no trickery was involved.
3. Pfungst's decisive test: vary whether the questioner knows the answer.
4. Result: 89% correct when questioner knows, 6% when they do not.

Pause after the 89%/6% numbers. Let it land. Then ask: "So what was Hans actually doing?" Students usually land on "reading body language" quickly.

The micro-cue detail -- a barely perceptible head dip at the moment the questioner's tension released -- is worth describing vividly. It was not conscious. Von Osten had no idea he was doing it.

**Slide: Blinding diagram -- 4 minutes**

Walk through it left to right:
- Left panel: questioner knows the answer, cue is transmitted, Hans performs
- Right panel: questioner does not know, no cue, Hans at chance

Connect to research design explicitly: this is why drug trials use double-blind protocols. The doctor's behavior -- how encouraging they are, how they interpret borderline results -- shifts when they know which patient received the real drug.

**Slide: Poker -- 5 minutes**

The key insight: professional poker players have independently arrived at the same solution as experimental scientists -- eliminate the observable signal that leaks from one party to another.

The slide now includes citations for each claim. Walk through them with context:

- **Sunglasses / pupil dilation:** Backed by peer-reviewed science. Einhäuser, Koch & Carter (2010) published in *Frontiers in Human Neuroscience* that pupil dilation betrays the timing of decisions. The Caltech press release noted explicitly that this may explain why poker players wear sunglasses. Full URL: https://www.frontiersin.org/articles/10.3389/fnhum.2010.00018/full
- **Consistent timing:** Timing tells are one of the most studied aspects of professional poker. A fast bet signals confidence; a slow bet signals uncertainty. Pros use the same deliberate pause on every decision to eliminate the timing channel. Reference: https://poker.academy/blog/post/the-hidden-power-of-timing-tells
- **False tells:** Sourced to Mike Caro's *Book of Poker Tells* (2003), the canonical reference on poker psychology. Caro documents the advanced technique of deliberately planting misleading behavioral signals. Publisher page: https://www.simonandschuster.com/books/Caros-Book-of-Poker-Tells/Mike-Caro/9781580420822
- **Neutral attire:** Jaw tension and neck movements are nearly impossible to consciously suppress. Covering the face eliminates the channel entirely.

Ask: "What other competitive situations require this kind of information control?" Good answers: negotiation, chess (time management as a tell), sports (pitchers hiding grip).

**Slide: Artificial Intelligence -- 5 minutes**

This will resonate most with this generation. Spend time on the feedback loop diagram.

Three mechanisms:
1. **Labeled training data:** If the people who labeled the data had systematic blind spots, the model absorbed those blind spots -- not the underlying truth.
2. **Feedback loops:** A model's output influences what users see; user behavior becomes future training data; bias compounds across training cycles.
3. **Benchmark design:** A model that scores 95% on a benchmark may have learned to pass that benchmark rather than acquired genuine capability.

The discussion question -- "When an AI confidently gives you a wrong answer, what does the Clever Hans story suggest?" -- is worth 2-3 minutes. The answer: the model learned from human-generated text, and humans write confidently even when they are wrong. The model learned the pattern of confidence, not the truth behind it.

**Slide: Quiz 1 -- 2 minutes**

Correct answer: B (doctors may unconsciously treat patients differently).

If students pick A or C: sample size is a separate issue, and drugs absolutely can be tested blind -- that is the entire point of placebo design.

---

### Section 2: Do Storks Deliver Babies? (14 minutes -- 3 slides)

**Slide: A Real Study. A Real Result. -- 7 minutes**

Do not reveal the confounding variable yet. Show the scatter plot and let students absorb it.

This slide now includes plain-English explanations of both the correlation coefficient and the p-value. Walk through them deliberately:

- **r = 0.62:** Explain that r runs from -1 to +1. Zero means no relationship. Positive one means a perfect lockstep increase. At 0.62, storks and births move together moderately strongly -- not perfectly, but consistently enough to show a clear upward trend.
- **p = 0.008:** Explain that this answers the question: if there were truly no relationship, how likely is it that we would see a correlation this strong just by random chance? Less than 1% likely. That makes the result statistically significant -- it is almost certainly a real pattern, not noise.

Then pause and let the punchline land: the result is real, the pattern is not a fluke -- and yet the interpretation "storks cause births" is completely wrong. This is the core lesson. Statistical significance tells you the pattern is real. It tells you nothing about whether the relationship is causal.

**Slide: The Confounding Variable -- 5 minutes**

Walk through the diagram. Larger, more rural countries have more stork habitat and higher birth rates. Both variables are responding to the same underlying factor -- country size. Neither is causing the other.

Ask: "How would you test whether country size is really the explanation?" Answer: hold country size constant. Analyze within groups of similar-sized countries. The correlation disappears.

**Slide: Quiz 2 -- 2 minutes**

Correct answer: C (confounding variable like family income).

Family income, parental involvement, and home stability all correlate with both having breakfast reliably available and with academic performance. This bridges directly from the storks example.

---

### Section 3: Okun's Law (14 minutes -- 3 slides)

**Slide: GDP Growth vs. Unemployment -- 6 minutes**

Before explaining the chart, ask students to read it:
- "What does the direction of the slope tell you?"
- "What does the scatter around the line tell you?"
- "What do the recession arrows show?"

Students can identify the negative correlation themselves. The scatter is an important teaching moment: real economic relationships are never clean. The points off the line represent recessions of different types, different industries, different eras.

Address the common question directly: "Is Okun's Law actually a law?" No -- it is an empirical regularity, a well-supported rule of thumb that has held for six decades but is not a physical law. The coefficient varies across time periods and countries.

**Slide: The Lag: Why It's Messier Than It Looks -- 6 minutes**

Walk through the time series. Students will recognize the 2008 crisis and 2020 COVID recession.

Ask: "Does unemployment peak at the same time GDP hits its lowest point?" No -- it peaks later. That is the lag.

The practical implication: this is why people often feel like a recession is still happening even after economists say it ended. GDP has recovered. The job market, which is what most people feel directly, has not caught up yet. Both descriptions can be accurate simultaneously.

**Slide: Quiz 3 -- 2 minutes**

Correct answer: B (unemployment can keep rising after GDP turns around due to the lag).

The student in the question is not wrong -- they are describing the lag effect accurately. GDP recovery and labor market recovery are different things that happen on different timelines.

---

### Section 4: The Shape of Income (37 minutes -- 8 slides)

This is the longest section. The interactive slides benefit from letting students engage before you explain.

**Slide: The Real Shape of Income -- 4 minutes**

Let students look at the chart before saying anything. Ask: "Where is the mean relative to the median on this chart?" The mean sits further right -- pulled by the tail. This chart is the foundation for everything that follows in the section.

**Slide: Mean vs. Median - Why It Matters -- 5 minutes**

Walk through the arithmetic of the company example:
- 9 workers at $40,000 = $360,000 total
- 1 CEO at $1,000,000
- Total: $1,360,000 divided by 10 = mean of $136,000
- Nobody earns $136,000. The mean is correct and misleading simultaneously.

The order mode < median < mean in a right-skewed distribution is worth writing on the board. It is a diagnostic students can apply to any income or price data they encounter in the news.

**Slide: Income by Bracket: What the Numbers Actually Look Like -- 4 minutes**

Walk through the bars left to right. Point out where the median line sits -- between the $75k-$100k and $100k-$150k bars. Half of all U.S. households earn less than $83,000.

Ask: "If a politician wanted to make the economy sound like it was doing well, which number -- mean or median -- would they use?"

**Slide: The Growing Gap: 40 Years of Income in America -- 5 minutes**

Ask students to look at all three lines and describe what they see before you explain. They should notice the widening gap between median and mean.

Key question: "If everyone got richer, why does it feel like most people are falling behind?" Because the gains concentrated at the top. The mean grew fast; the median grew slowly. These are both true and they tell very different stories about the same economy.

**Slide: The Lorenz Curve: Making Inequality Visible -- 5 minutes**

Walk through the axes before reading the curve:
- X-axis: cumulative share of population ranked poorest to richest
- Y-axis: cumulative share of total income
- The diagonal: perfect equality

Trace the actual U.S. curve. The two specific callouts to land: the bottom 50% earn about 10% of total income; the bottom 80% earn about 33%.

The Gini coefficient converts the visual bow into one number between 0 and 1. The U.S. Gini is approximately 0.49.

**Slide: How the U.S. Compares: International Gini Coefficients -- 4 minutes**

Students are often surprised the U.S. sits much closer to Mexico and Brazil than to Canada or Germany.

Note: Gini is a summary statistic. Two countries with the same Gini can have very different distributions. As with mean vs. median, a single number always loses information about shape.

**Slide: Income vs. Wealth: Two Different Levels of Skew -- 4 minutes**

Give students a moment to take in both charts. The income picture already looks unequal. The wealth picture is on another level.

The bottom 50% of Americans -- roughly 130 million people -- collectively own about 2.5% of total U.S. wealth. Let that land before moving on.

Clarify the distinction: income is what flows in each year. Wealth is what has accumulated over a lifetime -- savings, home equity, investments, inheritance.

**Slide: The Billionaire Slider: How One Outlier Moves the Mean -- 4 minutes**

Let a student volunteer drag the slider if possible.

Start at the far left -- everyone at $50,000. Mean, median, and mode are identical.

Drag slowly right. Point out at each stage:
- The mode never moves -- $50,000 is still the most common value
- The median never moves -- the middle value of the group is still $50,000
- Only the mean responds to the extreme value

At $1,000,000,000 the class mean exceeds $33,000,000 -- while 29 out of 30 people still earn $50,000.

Ask: "Which of these three numbers best describes what a typical person in this group earns?"

---

### Section 5: Survivorship Bias (12 minutes -- 3 slides)

**Slide: Abraham Wald and the WWII Bombers -- 6 minutes**

The slide uses the canonical Wikipedia survivorship bias diagram -- a top-view B-17 with red dots showing where returning planes were hit (wings, fuselage, tail). Note that the engines show very few hits -- not because they were never struck, but because planes hit in critical engine components (oil cooler, fuel lines, supercharger) were far less likely to survive and return. Wald's data showed a plane survived a single engine hit about 60% of the time, versus ~95% survival for fuselage hits. The underrepresentation of engine damage was the signal.

Build the story before revealing the insight.

Setup: "Engineers mapped bullet holes on returned planes. Most damage: wings, fuselage, and tail. Where do you put the armor?"

Wait for student answers. Most will say reinforce where the holes are. Then deliver the Wald insight.

The philosophical core: "The planes they were studying were the ones that survived. Bullet holes in the wings and fuselage were common on returned planes for exactly one reason -- those hits did not bring the plane down. The underrepresentation of engine damage was not because engines were never hit. It was because certain engine hits -- to the oil cooler, fuel lines, supercharger -- were far more likely to bring the plane down entirely."

Then: "The underrepresentation of engine damage was the signal."

**Slide: Mutual funds -- 4 minutes**

Ask: "If you saw a fund company advertise 8% average annual returns over 20 years, and you knew about survivorship bias, what is the first question you would ask?"

Answer: "Of how many original funds is that 8% the average? And what happened to the ones that no longer exist?"

**Slide: Quiz 5 -- 2 minutes**

Correct answer: B (graduates who are unemployed or underemployed and did not respond to the survey).

Graduates who found high-paying jobs are proud to report them. Those who are underemployed or still searching are far less likely to respond. The published figure is a biased sample -- the survivors.

---

### Section 6: The Birthday Problem (10 minutes -- 3 slides)

**Slide: What's Your Guess? -- 4 minutes**

Slider now starts at the leftmost position (2 people, 0.3% probability). Before touching it: "In a room of 30 people, what is the probability that at least two share a birthday? Write down your guess."

Take a few answers aloud. Most will be in the 5-20% range. Then drag to 30 and reveal: 70.6%. Watch the reactions.

Let students interact: "Drag it until it crosses 50%. What number is that?" (23.) "What number hits 99%?" (57.)

**Slide: Why Our Intuition Fails -- 4 minutes**

Walk through the table. The jump from 10 people (12%) to 23 people (50%) is the most surprising.

Explain the intuition failure: "We think about this as 'what is the chance someone shares MY birthday?' That probability is small -- about 8% in a room of 30. But the actual question is: what is the chance any two people share any birthday? With 30 people there are 435 different pairs. Each pair is a separate chance for a match."

**Slide: Quiz 6 -- 2 minutes**

Correct answer: B (they are thinking about one specific match rather than the 435 possible pairs at the party).

The person at the party framed the coincidence as a specific prediction. The birthday problem asks a fundamentally different question about any match across all possible pairs.


---

### Closing (4 minutes across 2 slides)

**Slide: Six Questions You Now Know to Ask**

Read each question slowly. Pause between them. Suggest students write them down or photograph the slide.

These are the transferable product of the course. The formulas will fade. These questions stay useful for the rest of their lives.

**Final slide**

End here. The closing line lands better in silence than with additional commentary. Do not explain it or summarize it. Just let it sit.

---

## Anticipated Student Questions

**"Is Okun's Law still valid after COVID?"**
The 2020 recession and 2021 recovery were exceptional -- unemployment spiked far more sharply than Okun would predict and recovered faster than expected. Most economists believe Okun's Law holds over normal business cycles but that COVID was outside its domain of applicability.

**"Does the stork correlation actually disappear when you control for country size?"**
Yes. When you analyze within groups of countries of similar size and urbanization, the stork-birth relationship is no longer statistically significant. This is the standard test for whether a confounding variable explains a correlation.

**"Why is the U.S. Gini so much higher than other wealthy countries?"**
Multiple factors: weaker redistribution through taxes and transfers, a more polarized labor market, higher returns to education and capital, and historical factors including racial wealth gaps. The U.S. pre-tax Gini is high; the post-tax Gini is somewhat lower but still elevated compared to peer nations.

**"How do we know the mutual fund survivorship bias numbers are right?"**
Studies track all funds from a starting date forward and compare reported performance against the full original cohort. Elton, Gruber, and Blake (1996) is the landmark paper. The methodology is transparent and has been replicated.

**"Why does the birthday probability matter outside of a demonstration?"**
The birthday problem is the mathematical foundation for understanding coincidences generally, hash collisions in cryptography, and DNA database false matches. Any situation where you are asking whether any two items in a large set share a property follows the same logic.

**"What is the difference between income and wealth inequality?"**
Income inequality measures how unequally annual earnings are distributed. Wealth inequality measures how unequally accumulated assets -- savings, property, investments -- are distributed. Wealth is typically far more concentrated because it builds over time and can be passed down across generations.

---

## If You Have Extra Time

- **The Monty Hall Problem** -- similar intuition-defying probability; works well as a follow-on to the birthday problem
- **Publication bias** -- the scientific literature as a survivorship bias problem; connects directly to the replication crisis in psychology and medicine
- **Regression to the mean** -- why exceptional performance tends to be followed by more average performance; relevant to sports, investing, and medicine

---

*Instructor notes by Pete Halbeisen*
*Corresponds to index.html -- RevealJS slideshow, ~33 slides*
*Last updated: Rev 2.2*

