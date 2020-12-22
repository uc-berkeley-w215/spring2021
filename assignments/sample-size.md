# Assignment: Calculate an experiment's sample-size requirement

[<span class="underline">Sample size determination</span>](https://en.wikipedia.org/wiki/Sample_size_determination) (AKA power analysis) is the process of calculating the number of participants an experiment will require to reach statistical significance under assumptions (guesses) about size of the effect that will be observed.

For this assignment, imagine that students in W215 propose a course project to test whether users will be more likely to comply with a warning if a popular 80s adjective is used to highlight which option is safe (e.g. not installing unsafe software the user has just downloaded) and which option is unsafe (e.g. installing the software).

The student researchers choose four possible words that describe the safe option: “bodacious”, “righteous”, “tight”, and a control (no adjective). They choose three variants for the adjective attached to the unsafe option: “gnarly”, “grody”, or a control (no adjective). This yields a between-subjects 4x3 design: four treatments for different adjectives for the safe option x 3 treatments for the unsafe option. This yields a total of 12 treatment groups to cover all possible combinations of positive and negative adjectives.

Using online participants and gratuities, the students are able to run the study at a cost of $5 per participant.

Assume that 50% of participants will typically choose the safe option, and our student researchers believe a really great pair of adjectives could improve the proportion who choose the safe option to 60% (an impressive 10% increase over the 50 percentage point baseline).

How many participants and what budget would be required for the student researchers to have a 50% chance of seeing an effect that yields p\<=0.05 using a chi-square test, if they indeed are correct that there is an adjective that cause 60% of participants to take the safe option? (The simplest case is a single adjective having an impact and all of the others having no impact, as you don’t need to make any assumptions about the two individual contributions combined.)

The simplest way to determine this is through numerical analysis: build a 12x4 contingency table of hypothetical observed and expected results for a chi square test where one adjective has a 60% compliance rate and all other treatments have a 50% warning compliance rate. Increase the absolute numbers of participants (keeping the ratios the same) until you reach the point where the chi square test produces a p value \<= 0.05. (You can use the CHITEST function in excel or GoogleSheets to run a chi square test. There are also online chi square test calculators that you can use if you’re not familiar with any other statistical software.)

Since the CHITEST function requires an expected value, the example in [<span class="underline">https://en.wikipedia.org/wiki/Chi-squared\_test</span>](https://en.wikipedia.org/wiki/Chi-squared_test) in the section titled “Example chi-squared test for categorical data” may be helpful for you.
