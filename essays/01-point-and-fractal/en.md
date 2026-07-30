# The Geometry of Intelligence: A Person as a Point, a Person as a Fractal

*An essay on what psychometrics can describe about the differences between people — and why you cannot know a person completely: not for lack of time, but by the construction of the object.*

------------------------------------------------------------------------

## 0. What This Text Is About — and What It Isn't

Let's settle the genre up front, otherwise half the objections will arrive at the wrong address.

This is **not** a text about how intelligence works. There will be no neurons here, no mechanisms of thought, no hypotheses about how the brain produces a mind. It is about something else: how the *description* of intelligence is built — the language in which the differences between people have been discussed for a hundred and twenty years — and about the fact that this same language turns out to describe, unexpectedly well, an entirely different problem: how one person gradually comes to know another.

This is **not** a predictive model. It produces no numerical forecasts of behavior and suggests no optimal communication strategy. It is an optical instrument, not a prediction machine. The instrument shows where we systematically lose information, which questions are badly posed, and which consequences of known facts have never been said out loud. The genre is legitimate: half of applied mathematics began as a way of seeing, not a way of computing.

The material in this text comes in three different grades, and I will mark every piece so the reader never has to guess:

- **\[textbook\]** — settled mathematics and psychometrics. Linear algebra, factor analysis, the general factor *g*. Nothing of mine — pure retelling.
- **\[framework\]** — an existing but niche research approach. Dynamical-systems theory applied to personality psychology: the machinery is rigorous, the application is contested.
- **\[hypothesis\]** — mine. Here I make a substantive claim that I answer for personally, and where possible I show how to refute it.

I consider exactly one thing in this essay original: the thesis of the **fractal nature of knowing a person**, and its operationalization. Everything else is assembly from off-the-shelf parts.

This text grew out of the author's conversation with the model claude-fable-5.

The push to write it came from a correspondence with a friend, in which a question arose: are the people who took part in a certain popular YouTuber's survey dumb? We will return to that question at the very end.

------------------------------------------------------------------------

## 1. The Cloud: People Differ, and It Is Measurable

**\[textbook\]**

Let's start not with mathematics but with a fact. People differ in their abilities; these differences are stable, reproducible, and measurable. They have been measured for over a century, on samples of millions, and however much the meaning of the results is argued over, the fact of the differences themselves is not in doubt.

The moment you start measuring differences, geometry appears — whether the researcher wants it or not.

Picture a questionnaire. Each of its questions is one axis: height, weight, age — three dimensions already. A filled-out questionnaire is a point. A multidimensional space, once you strip away the mystical haze, is simply a questionnaire with many questions, and a point in it is a specific set of answers. There can be as many questions as you like; nothing terrible happens, and nobody needs to draw an eighteen-dimensional picture — it is enough to be able to count.

One subtlety, out of which everything else will later grow. The questions must be genuinely different. If the answer to one can always be computed from another — like "age" and "year of birth" — then that is not two questions but one, written down twice. The number of genuinely independent questions is called the **dimensionality**. The number of names and the number of dimensions are different things, and that difference will come back to haunt us.

Now fill the questionnaire with abilities: words, numbers, spatial imagination, music, working with people. Every person is a filled-out questionnaire — that is, a point. All of humanity is a **cloud of eight billion points**.

There is the object of study. And the main question driving everything that follows is this: **what shape is that cloud?** Every mathematical instrument below appears not for its own sake but as an answer to that question.

Let's mark off the territory at once. By "intelligence" in parts 1–3 I mean **abilities** in the psychometric sense — what tests measure. Not character, not values, not ethics, not taste. This is a narrow reading, and it is temporary: in part 4 the space will have to be widened.

How many axes does this space have? There is no canonical answer, and that has to be admitted honestly. Charles Spearman showed in 1904 that behind all measurable abilities stands one general factor — *g*. Today's mainstream model, CHC (Cattell–Horn–Carroll), builds a hierarchy: *g* at the top, then the broad abilities — fluid intelligence, crystallized intelligence, visual-spatial processing, working memory, processing speed and others: about ten in the standard model, up to sixteen in the current revision (Schneider & McGrew, 2018) — and beneath them the narrow ones, of which more than eighty have been described. Howard Gardner counts eight "multiple intelligences." Robert Sternberg makes do with three: analytical, creative, and practical.

The spread from three to several dozen is not a sign of an immature science but a consequence of that same subtlety about independence. A pretty name is not yet a dimension.

------------------------------------------------------------------------

## 2. The Shape of the Cloud

**\[textbook\]**

There is one empirical fact around which all of psychometrics revolves, and it is counterintuitive to the general public.

**All measurable abilities correlate positively.** A person who does well on tasks of one kind, on average — I stress, on average — does decently on tasks of another kind. This is called the positive manifold, and it replicates in any sample, on any battery of tests, in any culture.

This fact has a direct geometric consequence. If the axes correlate, they are not perpendicular. Which means the cloud of humanity is **not round but elongated**, like an airship. And it has a principal axis — the direction along which the spread is greatest.

That principal axis *is* *g*, general intelligence.

It is worth pausing here, because *g* is usually presented as a philosophical assumption — "scientists decided there is some general intelligence." Nothing of the kind. *g* is a **geometric property of the data**: the principal axis of the ellipsoid. Spearman arrived at it not by reasoning but by computation: he noticed that school grades in all subjects correlate, and devised a procedure for extracting the principal direction from that correlational porridge. The procedure is called factor analysis, a close relative of principal component analysis, and geometrically it is a **rotation of the coordinate system onto the cloud's principal axes**.

From this follow four consequences, all of them direct.

### Weights: Not All Axes Matter Equally — and Weights Are Computed, Not Assigned

A reader of the draft who did mathematical modeling half a century ago (Boris Tsilevich) asked me a question that strikes at the very foundation: when building a model, the first step is to separate the essential parameters from the inessential and discard the latter. If you are computing the frequency of vertical oscillations of a maglev train car, the car's color does not enter the model. So are all the questionnaire's axes equally important? Shouldn't they be given weights?

They should. But — and here lies the beauty of the method — the weights are **not assigned by an expert; they are extracted from the data**. The measure of an axis's importance is its contribution to the cloud's spread: in the language of linear algebra, factor loadings, the eigenvalues of the covariance matrix. Axes with little spread are discarded, because they barely distinguish anything.

The question's author had, without knowing it, reinvented principal component analysis on the example of a train car. "The car's color doesn't matter for the oscillation frequency" is exactly the discarding of low-variance axes. The mechanism of importance is built into the model from the start; it is simply computed rather than postulated.

### IQ Is a Shadow

If *g* is one axis, then **IQ is the projection of a person's multidimensional vector onto that single axis**. One number instead of the whole questionnaire.

A projection is useful: an object's shadow tells you a lot about the object. But the shadow is not the object. Two people with entirely different ability profiles cast the same shadow, and by the shadow you cannot tell them apart. All arguments about IQ are, at bottom, arguments about how much information we agree to lose for the convenience of a single number.

The same logic applies to height. Measuring height is useful. Describing a person by their height is meaningless.

### Geniuses Are the Vertices of the Hull

Stretch a rubber band around the point cloud and you get the convex hull — the minimal wrapper containing every point. The shape of that wrapper is held **only by the extreme points**; everything inside affects the shape not at all.

Geniuses, in this picture, get a rigorous definition: they are the **vertices of humanity's convex hull** — the ones whose vector sticks out in at least one direction. Not "those who are above average at everything," but those who hold up the rubber band.

### The Trade-Off Myth Does Not Exist

Folk wisdom holds: strong at math means wooden in conversation. Nature supposedly deals out a fixed ration, and what it gave you in one place it took away in another.

The statistics do not support this. Correlations between abilities are **positive on average**, not inverse. The cloud is stretched along the "everything at once" diagonal, not across it. The brilliant mathematician who cannot say hello is not a pattern but a memorable exception — and it is memorable precisely because it is rare.

### Two Obligatory Caveats

First: **the axes are constructs**. They are not given by nature; they are derived from specific test batteries. Change the set of tasks and the axes will turn slightly. This is exactly what psychometricians criticize Gardner for: his eight intelligences sound beautiful, but in the data they separate poorly and behave more like talents and fields of activity than independent dimensions. An empirical test of the eight domains yielded one large *g* factor (Visser, Ashton & Vernon, 2006); Gardner's reply to his critics appeared in the same issue of *Intelligence* — the exchange is worth reading whole.

Second, and more important: **all of this is statistics of the cloud, not a verdict on the point**. Correlation describes the shape of the crowd. To an individual person, it prescribes nothing.

------------------------------------------------------------------------

## 3. The Point Is Alive

**\[textbook\]**

The model laid out above has a defect, and it was pointed out to me quickly and fairly: in it, **intelligence is static**. A person is a point, and the point stands still. But a person does not stand still: they learn and forget, progress and degrade, and count worse in the evening than in the morning.

The defect is fixed not by rewriting but by layering. The questionnaire's axes are heterogeneous in nature, and they have to be split into two layers.

The **slow layer** changes over years. Crystallized intelligence — accumulated knowledge and practiced techniques — grows into deep old age. Fluid intelligence — the ability to solve the new without leaning on the learned — declines with age, and declines early. This is the classic Cattell–Horn distinction, and it means that a person's point **drifts** through the space for decades: one way along some axes, the other way along others.

More than that: the whole cloud drifts too. Across the twentieth century, measured scores rose from generation to generation — the Flynn effect; and since the mid-1990s, in a number of countries, the rise has stalled and gone into reverse, with both the climb and the decline reproducing within families — that is, environment, not the changing composition of generations (Bratsberg & Rogeberg, 2018). Not only the point moves — the frame of reference moves, and it moves in both directions.

The **fast layer** dances within a single day: fatigue, mood, stress, coffee, time of day, quality of sleep. Same tests, same person — a noticeable spread.

Hence the corrected formulation, which will carry the rest of the essay:

> **A person is not a point but a trajectory. What we call their "level" is the slow average of a fast dance.**

In psychology this is an old distinction: **trait** versus **state**. A trait is a stable position; a state is a momentary deviation from it. Mixing them in one table is a category error — the one that makes any static model of personality fall apart on first contact with reality.

------------------------------------------------------------------------

## 4. The Second Space: From Abilities to Personality

**\[textbook\]**

Now I have to acknowledge a seam that the draft had taped over — and acknowledge it loudly, because this is exactly where the text nearly tore.

Parts 1–3 speak of **abilities**. But when one person perceives another, they do not perceive a test score. They perceive a person: their values, decency, taste, humor, temperament, their readiness to offer you a shoulder or a shove. Not one of these axes is an ability, and not one is measured by an intelligence test.

So there are two spaces, and they are nested.

The **narrow space** is abilities. Its empirical map is the CHC hierarchy; its principal axis is *g*.

The **wide space** is the personality as a whole. Abilities enter it as a subspace, but alongside them live character traits (best developed empirically as the "Big Five"; the canonical review is John, Naumann & Soto, 2008), values (the working map is Schwartz's theory of basic values, 1992), ethical and aesthetic preferences.

**The geometry of the two spaces is one and the same. The empirics are different.** Axes, cloud, principal directions, convex hull — the entire apparatus of parts 1–3 carries over verbatim; only the data that fill it change.

Emotional intelligence lives exactly on the seam between the spaces, and that is where all the confusion around it comes from. As a measurable ability (to understand emotions, distinguish them, manage them) it exists and fits structurally into the hierarchy of abilities as a full second-stratum factor, on equal footing with working memory or processing speed (MacCann et al., 2014) — that is, it belongs to the narrow space. As the fashionable "EQ" of corporate trainings, it is a loose mix of character traits and motivation — that is, it lives in the wide one.

From here on, "a person" means **a point in the wide space**.

------------------------------------------------------------------------

## 5. Three Stages of Knowing

This is the core of the essay.

The question is posed like this: **how does the image of one person gradually take shape inside another person's head?** Not "what is this person really like," but precisely: what happens to the *model* of a person in someone else's head as acquaintance deepens.

The answer unfolds in three stages, and each next stage reveals that the previous one was too coarse.

### Stage 1. The Shrinking Body of Uncertainty

**\[textbook\]**

A first impression is not a point but a **region**: a pencil outline drawn with an enormous margin — "the person is somewhere in here." In the language of mathematics — a prior distribution, a wide cloud of guesses.

Every session of contact is a **noisy measurement**. It does not deliver the truth; it narrows the region. Bayes' rule describes this contraction exactly, and the engineering version of the same thing is the Kalman filter: the idea of a person is stored as a center (the best guess) plus an ellipsoid of spread, and with every observation the ellipsoid shrinks and turns slightly.

The metaphor here is simple and exact: **bringing into focus**. First a blurry patch, then a contour, then features.

How coarse is the initial outline? Indecently coarse. The data on social perception say that a first impression is almost **two-dimensional**: people instantly rate a stranger on two axes — warmth and competence (Fiske, Cuddy & Glick, 2007): "friend or foe," "strong or weak" — and everything else is filled in later, over months.

Here is a detail for those who love geometry. The cheapest body of full dimension is the **simplex**: a triangle in two dimensions, a tetrahedron in three, in N dimensions a figure of N+1 vertices. Minimum anchor points, maximum coverage. A first impression is built exactly that way: the coarsest possible wrapper stretched over a minimum of data.

### Stage 2. A Person Is Not a Point but a Function

**\[textbook → framework\]**

Then something unpleasant comes to light: you can shrink the ellipsoid as long as you like, but it will not converge to a point. Because the target is not a point.

A person is **different in different situations**. Gentle at home and hard at work. Brave in an argument and timid at the doctor's. This is not inconsistency and not hypocrisy — this is the design. In personality psychology the structure is known as **if-then signatures** (Mischel & Shoda, 1995): what is stable in a person is not the average level of a trait but an individual pattern — "if situation A, then reaction X; if situation B, then reaction Y."

So the object being estimated is not a point but a **function**: a mapping from situation to reaction.

The machinery for estimating a function from a finite number of observations exists, and it is called a Gaussian process. Its main property is exactly the one we need: **the band of uncertainty is narrow where we have observed, and wide where we have not**.

And from this follows an explanation of surprise — a rigorous one, not a household one. We know a person well in the contexts where we have seen them, and **not at all** in all the rest. But the head does not tolerate a vacuum: it silently fills in what it never observed, extrapolating from what it did. That is why people "suddenly reveal themselves" — in trouble, around money, in power, in a foreign country. There is nothing sudden about it: we have simply looked, for the first time, into a context where our uncertainty band was as wide as a barn gate — and we had been taking it for a line.

Hence the first testable hypothesis. **The accuracy of predicting a person's behavior grows with the number of distinct *contexts* in which we have observed them, not with the total length of acquaintance.** Ten years in one context give less than two years in five. This claim can be tested experimentally, and it may turn out to be false.

### Stage 3. The Fractal

**\[framework + hypothesis\]**

Here the "new" part begins, and here too is the essay's main fork.

An observation anyone can make for themselves. The closer you look at a person, **the more detail there is** — and it does not run out. An acquaintance is "a harsh man." A buddy is "harsh, but quick to cool." A friend is "harsh with strangers, soft with his own, turns to stone when family is touched, and jokes exactly when he is hurting." Twenty years later — a new pattern that was not visible before.

This is **coastline** behavior. On a globe — a smooth arc. On a map — bays. On the ground — rocks in every bay. And so on without end: at every scale, structure appears that did not exist at the previous one. Objects with this property are called **fractals**, and their key characteristic is not "prettiness" but **fractional dimension**: the number of significant details grows as a power law as the scale shrinks, and never plateaus. Formally it is measured by the box-counting procedure.

**The hypothesis: the image of a person in another person's head behaves like a fractal.** Not "complex," not "multifaceted" — precisely this: it does not saturate under refinement.

And here we are obliged to produce not a metaphor but a way to test it, otherwise everything above is pretty words.

**Operationalization.** Take a measure of the model's detail: the number of distinguishable **if-then rules** that one person can formulate about another ("if his work is criticized in front of him — he goes quiet and leaves"). This quantity is measurable: the rules can be collected by interview and counted after weeding out synonyms. Now watch how it grows with depth of acquaintance.

- If the curve **reaches a plateau** — the image is finite, the hypothesis is false, knowing converges, and sooner or later a person is "fully studied."
- If the curve grows **as a power law and does not saturate** — the image is fractal, and that is fractional dimension itself, only in units not of space but of knowledge.

This claim is falsifiable. That is what distinguishes a model from a metaphor.

**The second, stronger version is dynamical. \[framework\]** Since a person is not a point but a trajectory (see part 3), a person is a **process**, and processes are described by the theory of dynamical systems. The trajectories of complex nonlinear systems wind themselves, over time, onto an **attractor** — a stable motif of behavior, the place the system is inevitably pulled toward. And here is the key fact: **the attractors of chaotic systems are, as a rule, fractal** — they are called strange attractors for a reason; the classic Lorenz attractor has a fractional dimension of about 2.06.

In this optic, deep knowledge of a person is not "refined the coordinates" but **learned the shape of their attractor**: where they get pulled, which loops they run, where their breaking points are and how long before they return to them.

**A correction worth stating honestly.** The coastline comparison captures endless detail, but not the part that matters, and one careful reader of the draft caught it exactly. Take the clean version of a coastline — the **Koch snowflake**: the same generating rule runs at every step, and it never changes. There are infinitely many details, but nothing about them is unpredictable: knowing the rule, you can compute any scale in advance. A person is not that kind of object, and if the fractal comparison stops here, it promises more than the model can deliver.

The difference is two properties Koch lacks and a strange attractor has.

First: **sensitive dependence on initial conditions**. A strange attractor has a positive Lyapunov exponent, and nearby trajectories diverge exponentially. At the same time, the shape of the attractor — the character, the recognizable "how it's built" — stays stable and learnable: the fact that the Lorenz attractor looks like the Lorenz attractor does not change from trajectory to trajectory. But where the trajectory goes next is unpredictable in principle — not for want of data, but because any uncertainty at the input is amplified exponentially. That is what actually changes with depth of acquaintance: not the picture, and not its statistics — but the **continuation**.

Second, and it matters more than the first. Koch's generating rule is never edited. A person's is: **the rule gets rewritten by its own execution**. Every experience — including the very fact of being known — edits the function that produces the next behavior. So while the observer is dutifully tracing the lower scales of the image, the upper scale has already moved. We are not reading a fixed infinite object — we are reading an object that **rewrites itself faster than we can finish reading it**.

Hence a corrected grounding for the metaphor, sharper than before. The claim isn't "infinitely many details on a fixed pattern" — taken literally, that version is either false or trivial for any sufficiently complex object. The claim is that **the pattern rewrites itself faster than it can be read**. The emphasis on self-similarity was a mistake, and the objection to it was exactly right. The operationalization above (the count of if-then rules) isn't hurt by this correction — it still honestly measures the non-convergence of knowing; what changes is the answer to "why," not the testable hypothesis itself.

And one last honest caveat, the kind a careful reader would find without the author's help. Sensitive dependence gives unpredictability **forward in time** — where the trajectory will go. The question this stage opened with was arguably about the unknowability of **structure** — what's inside. Those are two different claims, and read dynamically, the fractal metaphor strictly earns only the second: a person is unknowable because they are a generating process, not because they are a static object with endless nested rooms. The metaphor does not license the "structure" version, and it is more honest to say so than to stretch it further than it can carry.

And the cherry the whole essay was worth starting for. **Takens' theorem** (1981) states: by observing just one variable of a system for long enough, you can reconstruct the geometry of its entire hidden attractor — up to a smooth deformation, but the whole of it. One variable. For example — nothing but conversations with a person.

If this is right, then closeness has a mathematical justification: a long series of observations through one single channel is, in principle, enough to reconstruct the shape of the whole. We are not hopeless in our attempts to know another — we are simply doing attractor reconstruction from a one-dimensional series, without knowing that is what it is called.

**Honest labeling.** The bricks here are rigorous: Bayes, Gaussian processes, box-counting, sensitive dependence on initial conditions and the Lyapunov exponent, Takens — all of it proven mathematics. Applying dynamical-systems theory to personality is **a niche research direction, not a textbook**. The idea of a self-rewriting generating rule is no longer mathematics but a hypothesis on top of it — the boldest claim in the whole stage. And the fractality of the image is our hypothesis, together with the procedure for testing it.

### The Conclusion of Part 5

The model yields a claim that I consider the main one in the whole essay:

> **Knowing a person does not converge. Not for lack of time — by the construction of the object.**

At any scale of magnification a new bend is waiting, as on a coastline. "I know him like the back of my hand" is a statement not about the person, but about the speaker's resolving power.

Mathematics here turns out, unexpectedly, to be on the side of the romantics.

------------------------------------------------------------------------

## 6. What the Model Gives — and What It Does Not

The section I was too lazy to write in the draft — and I got what I deserved for it.

**It gives — a vocabulary.** A profile instead of a score. A body of uncertainty instead of "I know him." A trajectory instead of a characterization. An extrapolation band instead of "he surprised me." These are not ornaments: each term cuts off a specific, widespread error of thought.

**It gives — explanations of the familiar.** Why IQ loses information (projection). Why first impressions are coarse (a two-dimensional wrapper). Why the people closest to us surprise us (extrapolation into unobserved contexts). Why "he has changed" most often means "I saw him in a new context for the first time."

**It gives — three falsifiable hypotheses:**

1. The accuracy of predicting behavior grows with the number of distinct contexts of observation, not with the total length of acquaintance.
2. The number of distinguishable if-then rules one can formulate about a close person grows without saturation as acquaintance deepens.
3. The dimensionality of the image grows with acquaintance: it starts near two (warmth, competence) and increases as observations accumulate.

Each can be tested. Each may turn out to be false. That is the price of admission to the conversation.

**It does not give — a mechanism.** Not a word about *how* the brain produces intelligence. Neurophysiological objections fly past: that is a different floor of description.

**It does not give — forecasts.** No "this person will act thus-and-so 73% of the time."

**It does not give — a communication strategy.** The model describes; it does not advise.

**And it does not settle the old argument about the number of intelligences** — but it reformulates it so that it stops being rhetorical. In this language, the question "how many intelligences are there" becomes a question about the **rank of a data matrix**. The question "can a person be known completely" becomes a question about the **convergence of a refinement procedure**. Both answers are obtained by computation, not by argument.

------------------------------------------------------------------------

## 7. Objections That Have Already Been Raised

I posted a draft of this text on social media and received a takedown — harsh, in places caustic, and very useful. I answer the main points here and preempt the rest.

**"These are all metaphors; there is nothing to discuss."**

The difference between a metaphor and a model is real and important. A metaphor decorates and commits to nothing; a model takes on obligations — it specifies correspondences, names what is measurable, and admits refutation. By this criterion, parts 1–3 are not metaphorical at all: factor analysis does literally what is described there, and has since Spearman's day, while "the cloud is elongated" is a testable claim about the sign of correlations, tested on mountains of data. What is metaphorical there is the language of exposition, not the model.

As for the fractal hypothesis — see part 5: it has an operationalization and a condition of refutation. A metaphor that comes with instructions for how to kill it is called a hypothesis.

**"The real level of description is neuronal, and your whole inner theater is an illusion."**

A category error. The objection arrives from a different floor. I describe the psychological level — how people perceive people; the objector describes the neurophysiological one — how neurons fire. From the existence of the neuronal floor it does not follow that the psychological one is unreal. Otherwise you would have to explain the love of a novel's characters by typographic ink: formally true, and zero answer to the question.

What is amusing is something else: the neural scheme presented to me as a refutation — patterns tagged with labels and loaded on demand — is a hardware implementation of exactly what part 1 describes. Points in a feature space. That is not a refutation of the model; that is its lower floor.

**"Where is the part about how intelligence actually works?"**

Nowhere. See part 0. No promises were made — at least not in this edition of the title.

And the piece of self-criticism best spoken by oneself. The whole picture is linear: axes, projections, rotations. This is a first approximation. The real space of abilities may turn out to be curved — a manifold rather than a flat space — and then the "principal axis" becomes a principal curve, and distances stop obeying Pythagoras. Nothing catastrophic: the linear approximation has lived a hundred and twenty years precisely because it works. But it has to be kept in mind.

------------------------------------------------------------------------

## 8. Repaying the Debt

One debt from the opening paragraph remains. The text began with a question from a correspondence: are the people who took part in a certain popular YouTuber's survey dumb?

Now that question can be answered with instruments rather than intonation. A survey is one noisy measurement of one projection in one context. The word "dumb" is a verdict on a point along a single axis, passed from a shadow. The model in this essay does not forbid such a verdict — it shows its price: an object that does not converge even under twenty years of closeness has been sentenced on a single reading.

So the honest answer to my friend's question is: unknown. And there is no politeness in that "unknown" — it is technical. From one survey you know about as much about a person as you know about a coastline from orbit: that it exists, and that it is somewhere around here.

After that — as you wish. You can look closer. There is enough detail for everyone: as we have established, it does not run out.

------------------------------------------------------------------------

## Acknowledgments

Boris Tsilevich — for the question about axis weights, out of which half of part 2 grew. Andrei Baulinsh, Sasha Erashoff, Lev Lisagor — for a harsh and useful takedown of the draft: part 7 exists because of them.

------------------------------------------------------------------------

## Sources

1. Spearman, C. (1904). "General Intelligence," Objectively Determined and Measured. *The American Journal of Psychology*, 15(2), 201–292. Full text: [archive.org/details/jstor-1412107](https://archive.org/details/jstor-1412107)
2. Schneider, W. J., & McGrew, K. S. (2018). The Cattell–Horn–Carroll theory of cognitive abilities. In: *Contemporary Intellectual Assessment* (4th ed.). Guilford Press, 73–163.
3. Visser, B. A., Ashton, M. C., & Vernon, P. A. (2006). Beyond *g*: Putting multiple intelligences theory to the test. *Intelligence*, 34(5), 487–502. Reply: Gardner, H. (2006). On failing to grasp the core of MI theory. *Intelligence*, 34, 503–505.
4. Bratsberg, B., & Rogeberg, O. (2018). Flynn effect and its reversal are both environmentally caused. *PNAS*, 115(26), 6674–6678. [doi.org/10.1073/pnas.1718793115](https://doi.org/10.1073/pnas.1718793115)
5. John, O. P., Naumann, L. P., & Soto, C. J. (2008). Paradigm shift to the integrative Big Five trait taxonomy. In: *Handbook of Personality* (3rd ed.). Guilford Press.
6. Schwartz, S. H. (1992). Universals in the content and structure of values. *Advances in Experimental Social Psychology*, 25, 1–65.
7. MacCann, C., Joseph, D. L., Newman, D. A., & Roberts, R. D. (2014). Emotional intelligence is a second-stratum factor of intelligence. *Emotion*, 14(2), 358–374. [doi.org/10.1037/a0034755](https://doi.org/10.1037/a0034755)
8. Fiske, S. T., Cuddy, A. J. C., & Glick, P. (2007). Universal dimensions of social cognition: Warmth and competence. *Trends in Cognitive Sciences*, 11(2), 77–83.
9. Mischel, W., & Shoda, Y. (1995). A cognitive-affective system theory of personality. *Psychological Review*, 102(2), 246–268. [doi.org/10.1037/0033-295X.102.2.246](https://doi.org/10.1037/0033-295X.102.2.246)
10. Takens, F. (1981). Detecting strange attractors in turbulence. In: *Dynamical Systems and Turbulence, Warwick 1980*. Lecture Notes in Mathematics, 898. Springer, 366–381.
11. Dimension of the Lorenz attractor (D ≈ 2.06): [sprott.physics.wisc.edu/chaos/lorenzle.htm](https://sprott.physics.wisc.edu/chaos/lorenzle.htm)
12. Lorenz, E. N. (1963). Deterministic Nonperiodic Flow. *Journal of the Atmospheric Sciences*, 20(2), 130–141. — sensitive dependence on initial conditions, the Lyapunov exponent.
