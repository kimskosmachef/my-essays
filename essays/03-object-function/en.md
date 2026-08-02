# Intelligence as Object and as Function: A Description of What Is No Longer There

*Third in the "Geometry of Intelligence" series. The first argued that you cannot finish reading another person. The second, that instead of reading, people finish writing them. This one is about why accuracy will rise but hit a wall — and why the wall isn't made of instruments.*

------------------------------------------------------------------------

## 0. The Opening Scene

I was walking through Ventspils, late for the bus to Kuldīga. And suddenly — a thought that made me stop in the middle of the street, even though the bus wasn't going to wait: intelligence is not an object and not a function, it is both at once. Not "or" — precisely "and." I typed the thought into a chat window standing still. Then I walked on — fast at first, reading the reply as I went, firing off another two or three questions without stopping. At some point I realized the bus mattered more than the conversation, and broke into a run. Made it.

There's a precision in that scene I didn't formulate at the time, I just lived it: while I was inventing the thesis about object and function, I was both at once myself — a body-object running late through physical space, and a working function that at that same moment was holding a conversation and refining a hypothesis. The thought didn't stop the run. It happened inside it.

------------------------------------------------------------------------

## 1. The Thesis, Up Front

I'll start with the claim and explain afterward. That's more honest: if the thesis doesn't hold, you can stop reading.

Everything you know about another person is samples of their behavior. What they said, how they acted, what they did under pressure, what they did when no one was watching. Nothing but samples has been issued to you, and nothing else will be.

And "what they're really like" is no longer observation. It's a model you filled in yourself from those samples. The filling-in happens instantly and invisibly; you don't feel it as work — but it is there, and it is yours.

And here's the main thing. Until recently there was nothing to check the quality of that filling-in against. To test how well we reconstruct a person from their behavior, you'd need to know independently what they're "really like" — and there's nowhere to get that knowledge. Psychology worked for a hundred years without a control specimen.

Now such a specimen exists. There are systems where both sides are visible at once: the behavior, and the thing that produces it. On them you can test not a person but the filling-in procedure itself.

The test gives an unpleasant result, and this whole text is an examination of it. In short: **the famous accuracy ceiling that behavior prediction from character runs into has an irreducible residual — and that residual is not measurement noise to be cleared away by better instruments, but the signature of the reconstruction procedure itself.**

I put it that way rather than more sharply, because more sharply would be untrue. Instruments will lift part of the ceiling, and in part five I'll honestly show which part and why. What I'm talking about is what remains after that.

This claim has an opponent, and I want to name him right away so the argument is fair. The opponent is anyone who expects accuracy to rise all the way: that better tests will come, and bigger data, and better scanners, and a person will finally become predictable. This text claims accuracy will rise — but it will hit a wall, and the wall is not built out of the poverty of science.

------------------------------------------------------------------------

## 2. The Formal Home

**\[textbook\]**

Before arguing, I need to remove the suspicion that philosophy is coming. It isn't. The duality "object or function" is not deep metaphysics but a routine that engineers use every day.

Take a computer program. On disk it's a set of bytes. You can copy it, measure its size, compare it byte by byte with another. That's an object: a thing lying in a definite place. Run it — and it becomes a function: something that takes an input and produces an output. The same thing, two descriptions. Neither of them is the "real" one, neither is an "illusion."

This isn't an observation but an architectural decision taken in the 1940s: the program is stored in the same memory as the data — the principle that came to bear von Neumann's name. It is precisely because of it that the words "object" and "function" stopped being opposites: one and the same string of bytes lies there as a thing and works as a mapping, depending on what you do with it.

The question "so what is intelligence — object or function?" is built exactly like the question "is a program a file or a process?" The answer: both, and the question is badly posed. The interesting part starts further on — when we ask what happens in the passage from one description to the other.

> **Math inset 1. A function as a point.** \[textbook\] To say "two behaviors are close," you need a distance between functions — and it's defined quite literally: `d(f,g) = max|f(x) − g(x)|` over all inputs, or the averaged squared difference. Once a distance is fixed, the set of functions becomes a space in the full technical sense: it has neighborhoods, convergence, dimension, and the usual theorems apply. There is nothing figurative here — it's a standard construction of functional analysis. The first essay was already standing in such a space without naming it: a Gaussian process is a probability distribution not over numbers but over functions, a cloud each point of which is an entire function. There's one difference from ordinary space, and it matters: it is infinite-dimensional, and the intuition "close means similar" works worse there than you'd think.

------------------------------------------------------------------------

## 3. The First Two-Sided Case

**\[textbook\]**

Now to systems where both sides are visible.

A neural network is, on the one hand, a set of numbers. A lot of numbers: billions. They sit in a file on disk; you can copy them, compare them, measure the distance between two such sets. That's an object. On the other hand, those same numbers can be run — feed in an input and get an output. That's a function. A file on disk, and the same file at work. Von Neumann exactly, only at industrial scale.

One important caveat right away, or there'll be a misunderstanding: **the object side doesn't have to be comprehensible — it's enough that it be measurable.** What a particular number inside a neural network means, nobody can really say; in that sense the weights are no more transparent than the neurons of a brain. But to compute the distance between two sets of numbers, you don't need to understand them. For everything that follows, that's enough.

Now two observations, the reason for all of this. Both are not thought experiments but known facts about neural networks.

**Observation one: an enormous shift in the object with zero shift in the function.** Inside a network, the neurons of one layer can be swapped around — if you simultaneously swap the corresponding connections, the network will behave exactly the same. Not "approximately the same": literally bit for bit, on any input. And the set of numbers will change radically — compare the two files directly and they'll turn out completely different. One function, astronomically many different objects implementing it. This is called permutation symmetry and has been known since the early nineties.

**Observation two, weaker than the first, and I mark that honestly: a tiny shift in the object with a large shift in the function.** Fine-tune a model slightly — the numbers change a little, but the behavior can change noticeably. In itself that's not surprising: sensitivity of the output to small changes in the innards shows up in plenty of systems, from weather to economies. But paired with the first observation it gives the picture we need: the link between "how similar the objects are" and "how similar the behavior is" is broken in both directions.

From this follows something that in conversations about intelligence usually sounds like a philosophical declaration but is in fact a technical statement of fact: **the identity of an intelligence is fixed by behavior, not by numbers.** Two networks with different weights that behave identically are one intelligence. There's nothing to argue about: it is impossible to name an experiment that would tell them apart.

And one more rhyme with the first essay that would be a shame to leave out. The same set of weights behaves differently depending on context: what the model is told before the question switches its effective behavior. One object — many functions, one per context. This is exactly the pattern "if situation A, then reaction X," which in the first essay turned out to be the only stable thing there is in a person. There it was a psychological observation. Here it is a property of a system whose construction is open to inspection.

> **Math inset 2. How many objects there are per function.** \[textbook\] A permutation of neurons is written compactly: if a layer has `n` neurons, take a permutation matrix `P` and replace the incoming weights `W_in → P·W_in` and the outgoing ones `W_out → W_out·Pᵀ`. The output doesn't change — exactly, not approximately. The number of such permutations across the whole network is the product of the factorials of the layer widths, `∏ᵢ nᵢ!`. For a single layer of a thousand neurons that's already `1000! ≈ 10²⁵⁶⁸`, while the number of atoms in the observable universe is on the order of `10⁸⁰`.
>
> But for networks with ReLU — which is nearly all modern ones — the picture is sharper. There's a second symmetry there, and it is continuous: multiply a neuron's incoming weights by any `c > 0` and its outgoing ones by `1/c`; ReLU is positively homogeneous, so the output doesn't change. So the preimage of a single function in weight space is not a set of isolated points but a connected set of positive dimension. "One function, many objects" is not a turn of phrase here but a statement about the cardinality of a set.

------------------------------------------------------------------------

## 4. Two Kinds of Closeness Diverge

**\[framework\]**

Here is the main claim of the text, and it arrives deliberately early — not tucked into the tail where it's easy to hide, but while the reader still has the energy to object.

The claim is this. We have two ways to ask "how close are these two intelligences." The first is to compare the objects: how similar the sets of numbers are. The second is to compare the functions: how similar the behavior is. It's natural to expect the two answers to agree at least roughly. Well: they don't merely agree poorly — depending on the type of change, they point in opposite directions. Permutation of neurons: the objects have moved apart beyond recognition, the behavior hasn't changed at all. Fine-tuning: the objects nearly coincide, the behavior has diverged.

How large this divergence is in numbers I don't know, and here one has to be precise so as not to pass off the desired as the done. As far as I know, nobody has published such a measurement specifically. So I'll state it honestly: **this is measurable in principle** — open models are available, both quantities are computable, it's an evening's work — but it has not yet been measured, and I have no right to say "shown." If any reader takes it on and computes it, I'll be glad of the result in either direction.

Now I'm obliged to put on the table, myself, the objection a strong reader will prepare for me first. In neural network theory there's a result whose name sounds like a death sentence for everything said above: **"for neural networks, function determines form."** Its meaning is this: if two networks behave identically on all inputs, then their weights are related to each other by known symmetries — those very permutations and their kin. That is, the object *is* after all recoverable from the behavior — up to symmetries. The objection looks fatal: where's the information loss if everything is recoverable?

Let's take it apart calmly, in three moves.

Move one. The theorem requires knowing the function **in full** — the behavior on all possible inputs, down to the last one. In life that never happens. We always have a finite sample: the person was seen in twenty situations, the model was run on a thousand examples. Between "I know the function in full" and "I've seen it twenty times" there is an abyss, and everything this text is about lives in that abyss. The theorem describes a limiting case unattainable in practice; our question is about practice.

Move two, and it turns the objection into a support. The theorem also says something else: it names exactly **in what way** the weights are ambiguous. And if they're ambiguous, then "the distance between objects" cannot be computed in one single correct way. Want to compute it directly, number by number? Then a permutation of neurons gives an enormous distance at complete identity of behavior — the ruler lies. Want a ruler that ignores permutations? Then you've written the answer you wanted into it in advance, and what you're measuring is no longer the object but the object "up to." There is no canonical ruler.

Move three — about modern networks, and here one has to be careful, or it's easy to overplay. The original theorem is proved for smooth odd activations of a particular kind — the hyperbolic tangent family. Nearly all the networks under discussion today have a different activation, ReLU, and it has a symmetry the tangent doesn't: a neuron's incoming weights can be multiplied by any positive number and its outgoing ones divided by the same number — the behavior doesn't change by a single bit. This is no longer a permutation: permutations may be astronomically numerous, but they're a finite number, whereas here we have a continuous family. The ambiguity of the object in modern networks is therefore not smaller than the theorem describes, but larger.

But let me immediately concede what the opponent won't be expecting and honesty requires: **for ReLU an analogous identifiability result has also been proved** — later, in 2020, and under its own conditions on the architecture. So to say "the theorem isn't about modern networks, therefore the objection is disposed of" would be cheating. That is not what disposes of it.

What disposes of it is move one, and that's worth stopping on separately. Of the three moves, **the load-bearing one is the first**: all such theorems, old and new alike, need the function in full. That condition is not softened by broadening the class of networks and never will be, because it isn't about networks — it's about what we have at our disposal. Moves two and three work on a different topic — the non-canonicity of the ruler, and only that. I separate them deliberately, because presenting three arguments as equals would hide the fact that two of them are about something else.

And this is not a technical hitch that somebody will one day fix. This *is* the content of the thesis, stated more strictly:

> **The object side is not measured in agreement with the functional side. Not "agrees poorly" — is not measured in agreement in principle, because no canonical way of measuring the object exists.**

Honest labeling, without which all of this becomes an overclaim. On the AI side, what's been said is not a hypothesis but an **existence proof**: it has been shown that the two sides of an intelligence can diverge structurally, and not by oversight. Exactly that — no more. I am not claiming that AI is a model of a human being, and I'm not passing it off as a control group for psychometrics: these are different systems and different procedures. I claim exactly one thing: the phenomenon I'm about to discuss with respect to human beings exists — here it is, you can touch it in a system whose construction is open. Which means that the same explanation, applied to a person, stops being a fantasy and becomes a plausible hypothesis.

Which brings us to people.

> **Math inset 3. Why there is no canonical ruler for the object.** \[framework\] The two closenesses are defined differently. The object one is the norm of the parameter difference: `d_obj(θ₁,θ₂) = ‖θ₁ − θ₂‖`. The functional one is the average divergence of outputs on inputs that actually occur: `d_func(f₁,f₂) = E_x‖f₁(x) − f₂(x)‖`. One would like them to grow in step. A permutation gives `d_obj ≫ 0` with `d_func = 0`; fine-tuning gives `d_obj ≈ 0` with `d_func ≫ 0`. There is no agreement in either direction.
>
> The natural fix is to measure not the weights but the equivalence classes: `d([θ₁],[θ₂]) = min_{g∈G} ‖θ₁ − g·θ₂‖`, where `G` is the symmetry group. But that fix is itself an admission of the thesis: for the ruler to work, `G` has to be written into it in advance; `G` depends on the architecture, for ReLU it contains a continuous part, and minimizing over it is computationally hard. The canonical ruler isn't "not built yet" — it doesn't exist, by the construction of the problem.
>
> Now the identifiability theorem (Albertini and Sontag, 1993) and its two limitations, which have to be named honestly. The first, discussed in the main text: it requires knowledge of the function on **all** inputs, and we always have a finite sample. The second, less well known: it is proved for odd smooth activations under the conditions `σ(0)=0`, `σ′(0)=1`, `σ‴(0)≠0` — the hyperbolic tangent family, not ReLU. For ReLU the symmetry group is wider: continuous positive rescaling is added to the permutations, and the preimage of a function stops being discrete.
>
> It's important not to overplay this. Identifiability for ReLU **has been proved** later (Phuong and Lampert, 2020: for architectures with non-increasing widths, permutation and rescaling exhaust the function-preserving transformations). So broadening the class of networks does not kill the objection. Only the first limitation kills it — the requirement to know the function on all inputs: that one depends neither on architecture nor on activation and is softened by nothing. The limitation on activations works toward the non-canonicity of the metric, not toward disposing of the objection; the two conclusions must not be mixed.

------------------------------------------------------------------------

## 5. Back to People

**\[hypothesis\]**

With a human being it's the other way around: the function is visible, the object is not.

The function is perfectly visible. A person's behavior is exactly what we observe, and we observe it all our lives.

The object needs more care, though, because it's easy to go wrong here, and I made that mistake in the first draft of this text.

The temptation is to say: the object side of a human being is the brain, and it's inaccessible. But that's false, and more false every year. The brain is precisely what we've learned to look at: scanners, electrodes, complete connection maps in small animals, ever more detailed ones in large. If my thesis rested on "the brain can't be read," it would last exactly until the next generation of instruments. And then the objection "wait, the technology will catch up" would be entirely fair.

Something else is inaccessible. Between the readable brain and the observable behavior there is an intermediate floor — that multidimensional construction which in the first essay was drawn as a point in a space of abilities and traits. That is the object. And it shows itself neither from below nor from above. Not from below, because a complete map of the brain does not hand you a profile of abilities: that's a description at a different level, the way a circuit diagram doesn't hand you the meaning of the running program. Not from above, because everything we get from the behavior side is already our reconstruction, not the object itself.

So there are three floors, and confusing them is the main error in this area. The bottom one: the physical substrate, read better and better. The top one: the profile, the traits, the scores — what psychology produces by reconstructing the object from behavior. And between them the middle one: the construction that actually produces the behavior. It is precisely this one that is inaccessible, and inaccessible not through poverty of instruments but because it sits at a different level of description than what the instruments show.

The distinction between levels isn't my invention: in cognitive science it was introduced long ago and serves exactly this purpose — to keep "how the hardware is built" from being confused with "what problem is being solved, and how." A readable substrate does not mean a readable construction. These are different questions, and the answer to one is not an answer to the other.

Now let's connect them. Psychology reconstructs the middle floor from samples of behavior — that is, it performs exactly the operation described in the previous part: reconstruction of an object from a finite sample of a function. The very one where we just saw structural, not random, loss.

And here we need to talk carefully about the famous ceiling, because there's a lot of confusion around it, and half of that confusion is deserved.

The classical fact: knowing a general character trait, you predict a person's specific act in a specific situation with an accuracy that tops out around 0.3 on a scale from zero to one. Not much. That number caused a large argument in psychology in the sixties.

But here's the honest caveat, without which I'd be caught in a sleight of hand. That figure is largely explained by the fact that a single act is a bad measurement: too much randomness in it. If you observe a person many times and average, accuracy rises sharply — this was shown back in the late seventies, and the result has held firmly since. So about the raw 0.3, the honest answer is: yes, a significant part of it is ordinary noise, and it is removed by accumulating observations.

It's worth pausing a second here, because at this point the series closes a loop in an unexpected way. The formula by which the gain in accuracy from accumulated observations is computed was derived in 1910 by Charles Spearman — the same man the first essay began with: he's the one who found the general factor in 1904 and gave the series its first foundation. In his 1910 paper there is a section headed, literally: "Increase of reliability by increasing the number of measurements." That is, one and the same man, six years apart, supplied this series with both its foundation and the best counterargument against its central thesis. The argument isn't with an opponent — it's with the founder.

A small point of honesty while we're here: in the same issue of the same journal, immediately following, the same formula was independently published by William Brown, and in psychometrics it's called the Spearman–Brown formula, with some specialists calling it Brown–Spearman. That doesn't loosen the loop, but the co-author's name deserves saying.

So my thesis is not about the raw figure. It's about what remains after.

Because accumulating observations improves prediction, but not without limit. It runs up against something — and a gap remains that doesn't close no matter how long you observe. That irreducible residual is the signature of the procedure. And unlike noise, it has an intelligible mechanism — the very one we examined in the second essay.

What's stable in a person is not the average level of a trait but an individual pattern: gentle at home, hard at work, goes rigid at the mention of family, jokes exactly when it hurts. An if-then pattern. Now look at what averaging does. It takes that pattern and collapses it into a single number — "on average, rather gentle." The information that in situation A it's one thing and in situation B another is not lost at random. It is destroyed by the operation. And no further accumulation of observations will bring it back, because there's nothing to bring back: it went not into noise but into discarded structure.

I have an example, and it's about me. In the second essay I described how at two jobs I was called different things: at the first, "bad cop" — there I'd occasionally push my subordinates when it was called for; at the second, "rebel" — there I told management to their face and said whatever I thought at general meetings.

For a long time I thought one of the two was a misunderstanding. Then, that both were true. Now I see a third thing, and it's worse than the first two.

The point is that at the first job I had excellent relations with management, on full mutual respect. There was nothing there to rebel against. It's not that I was holding back — the condition under which I start speaking up simply never once occurred.

Which means the rule inside me was one and the same. What changed was not the rule but whether the situations in which it fires occurred at all. The first place saw one half of the rule and called it "bad cop." The second saw the other half and called it "rebel." Both averaged honestly — over what they got. Neither of the two labels is an error, and that is precisely why they're useless: they describe not me but the intersection of me with the place.

And here's the thing I brought the story up for. Observing me only at the second job, it is impossible to distinguish "he's a rebel" from "he objects when there's something to object to." In that place both descriptions predict the same thing, word for word. They differ only where management behaves otherwise — and situations like that didn't occur there.

Note that this is not a shortage of observations. Watch me at that outfit for ten years — you won't get a step closer to the answer: what's missing isn't quantity, it's the situations that don't happen in that place. This is exactly the condition from part four, only about a person: to reconstruct the construction from the behavior, you need the behavior on all inputs. Not on many. On all. There it sounded like a technical footnote to a theorem about neural networks; this is what it looks like when it's about you.

Hence the first hypothesis of this essay. Numbering runs continuously through the series: the first had hypotheses 1–3, the second 4–5.

> **Hypothesis 6a — loss in compression.** The residual inaccuracy in predicting behavior from a personality profile is not measurement noise but structural loss: the mapping "construction → behavior" is many-to-one, averaging over situations irreversibly destroys the if-then pattern, and therefore the residual is not removed by improving instruments.

**How to kill 6a.** If prediction from the if-then pattern — rather than from the averaged trait — tops out in the same place as prediction from the trait, then the discarded structure carried nothing and the mechanism is made up. There's also a weak version of death: if improving the quality of instruments systematically raises the ceiling and the residual shrinks toward zero, then it was noise after all.

This hypothesis has a sister. The compression mechanism is not the only cause of the irreducible residual; the second will appear in part six, when it turns out that the target doesn't stand still. Hypothesis 6b will be formulated there, along with what it takes to kill both at once.

> **Math inset 4. Noise and loss are different terms.** \[framework\] Prediction error is composed of two quantities of different nature, and all of hypothesis 6a rests on telling them apart.
>
> The first term is measurement noise. A single act = a stable disposition + a random deviation. Averaging over `m` observations damps the deviation as `1/√m`, and the reliability of the aggregate grows by the Spearman–Brown formula: `r_m = m·r₁ / (1 + (m−1)·r₁)`. Hence Epstein's result: aggregate, and the correlation rises. Noise is reducible.
>
> The second term is loss in compression, and it's built differently. What's stable in a person is a mapping "situation → reaction," `f: S → R`. The trait profile is a single number, the average over situations: `θ = E_s[f(s)]`. The mapping `f ↦ θ` is many-to-one: two people with the same average and opposite patterns get the same profile. What's lost here is not a random addend but the component of `f` orthogonal to the constant. No `m` brings it back, because it isn't in the aggregate.
>
> Hence the exact formulation of hypothesis 6a and the exact site of the test. Averaging raises prediction of **aggregated** behavior, not of an act in a specific situation; the disputed residual lives in the second. The death condition in formal terms: if prediction from the pattern `f` tops out at the same ceiling as prediction from the number `θ`, the discarded component carried no information and the mechanism is made up.

------------------------------------------------------------------------

## 6. The Loop: The Target Moves

**\[framework\]**

So far we've been talking as if the object stands still while we try to reconstruct it. That's a simplification, and it's time to drop it.

The cycle looks like this. The object sets the function: the construction determines the behavior. The function operates and errs somewhere. The error changes the object: the construction rebuilds itself. And the next run happens on a different construction.

This description fits both the training of a neural network and the learning of a human being. But a limiter has to go in right away, or a single sentence will kill the whole part. The mechanisms in the two cases are different, and their identity cannot be asserted. The way a neural network learns requires the error signal to travel back along exactly the same connections as the forward signal — and in the brain synapses are one-way, so that possibility doesn't exist; the problem was named and has been discussed since the eighties. Workaround schemes are known that learn without that requirement, but on large problems they still lose. Whether the brain approximates something like gradient learning by other means is an open question, argued about seriously to this day.

So I'll state it cautiously and exactly as far as I'm entitled to: **these are two instances of one loop, not one mechanism.** What they share is the form of the cycle: object → function → error → altered object. What differs is everything else. For the thesis that's enough, and there's no need to claim more.

And for the thesis, here's what follows. In reconstructing an object from behavior, you are reconstructing a target that isn't standing still. While you collect samples, the construction producing them is already being rewritten — including under the influence of the very situations in which you're observing it. By the end of your observation you hold a description of what is no longer there.

And here something important emerges — the thing this part is in the text for, rather than being a pleasant addition. A moving target gives a **second, independent cause** for the same irreducible residual.

Watch what happens to the observer. He wants more samples: the more there are, the less random noise — we've discussed that, noise is damped by accumulation. But the longer the observation window, the further the construction itself has drifted in that time. Observe briefly — you drown in noise. Observe long — you get an average over the trajectory, that is, a description of a state that existed at no single moment. Two errors pull in opposite directions: one decreases with the length of observation, the other grows. Which means there's an optimal length — and at that optimum the total error is not zero. Not "not zero yet." Not zero.

This is the standard picture of tracking a changing parameter, nothing exotic. But for our thesis it matters because it comes from a completely different direction than the previous argument. In part five the residual was explained by compression: averaging destroys the pattern. Here it's explained by motion: the target moves away faster than accuracy accumulates.

And here I have to admit something uncomfortable, or I'll break my own rule. Two legs instead of one aren't only sturdier. They're also worse: the hypothesis has become harder to kill. The death condition from part five now fells only the compression leg, while the drift leg will stand on its own and account for the same ceiling by itself. A theory that is harder to kill is, by this series' rules, not better but more suspect. So I'll separate them honestly.

> **Hypothesis 6b — target drift.** Part of the irreducible residual arises not from compression but from non-stationarity: the construction is rewritten over the time of observation, and an estimate from the accumulated sample refers to a state that existed at no single moment. Therefore the residual is removed neither by lengthening the observation nor by shortening it.

**How to kill 6b.** If the residual does not grow as the gap between observation and prediction widens, the hypothesis is dead: the target stands still for our purposes.

**For the general thesis to fall, both must be killed.** As long as even one leg stands, the ceiling remains structural rather than instrumental. That makes the critic's job harder, and I'm obliged to compensate: to give not only a way to refute the mechanisms but a way to tell them apart.

The way fits into a single study, because the legs make **different** predictions. Drift requires the residual to grow with the temporal gap between observation and prediction, and to be smaller for traits that are more stable over time. Compression requires something else: the residual should be largest in people with strong if-then contrast — those who are markedly different in different situations — and should not depend on the temporal gap. Measure both factors in one design and see which one moves the residual. The outcome "both" is possible — then both legs live. "Neither" is possible — then the whole thesis is dead, and that's the most useful result of all for me.

As for the plausibility of drift, there's no need to guess; it's been measured. The classic review of trait stability — a hundred and fifty-two longitudinal studies, more than three thousand repeat measurements — gives exactly the shape required: stability rises with age, from about 0.31 in childhood to a plateau of around 0.74 at fifty to seventy, and **falls as the interval between measurements grows**.

One has to lean on this carefully, and I'll say exactly what to lean on. That even at the plateau it's 0.74 and not one proves little by itself: into the gap between 0.74 and one falls both real change in the person and ordinary measurement unreliability — that is, exactly the noise I just agreed is removable. What does the work is something else: **the fall with interval**. Measurement error doesn't grow because twenty years passed between measurements rather than five; yet observed stability falls. The only thing that grows with the interval is real change. That is the proof that the target moves — and it's exactly the quantity on which the death condition of hypothesis 6b rests.

This, incidentally, is also the precise answer to a question put to me by a reader of the first essay — a mathematician who fairly noted that if a fractal is self-similar, then magnifying it shows the same thing over again, and it's unclear what then prevents you from finishing reading it. What prevents it isn't the self-similarity. What prevents it is that the rule drawing the pattern is itself rewritten in the course of the drawing. The pattern is completed faster than it can be read off.

This loop has a ready-made emblem, and I'll take it with the caveat established in the second essay: a symbol is honest as a generator of thought and lying as a measuring instrument. The snake biting its own tail is an old image of a closed cycle; in this text it has exactly one meaning, the literal one: the system's output becomes its own input. The function rewrites its own substrate. That's the first bite. The second is in the next part.

> **Math inset 5. Estimating a moving target.** \[framework\] The loop is written as a dynamical system: the object is a state variable `θ_t`, the function is `f_{θ_t}`, the error is `e_t = loss(f_{θ_t}(x_t), target)`, the update is `θ_{t+1} = U(θ_t, e_t)`. Gradient descent `θ ← θ − η∇L` is one possible `U`, synaptic plasticity another; what they share is the form of the scheme, not the mechanism.
>
> What this means for the observer. He collects samples in a window of length `m` and estimates a single `θ̂` from them. But the samples were produced by **different** states `θ_t`, drifting at a rate `δ` per step. The estimation error is then composed of noise decreasing as `σ/√m` and a bias from drift growing roughly as `δ·m`. The sum is minimal at a finite `m*`, not at `m → ∞`, and at the minimum it isn't zero. Observe longer and you get a state averaged over the trajectory that existed at no single moment; observe shorter and you drown in noise. The error floor isn't removed by either strategy: this is the standard picture of tracking a non-stationary parameter, and it is the formal content of hypothesis 6b — a contribution independent of the argument about pattern compression.

------------------------------------------------------------------------

## 7. The Same Question from the Inside

**\[framework — not a hypothesis\]**

Everything so far has been about the view from outside: I am looking at someone else. Now the same question in the first person.

Self-knowledge is a function applied to the very object that implements it. A construction attempting to describe itself while running on itself.

The first thing to say: this is possible in principle. There's no mysticism here. In computability theory it has long been known that a program can refer to its own description and operate on it; there exist programs that print their own text — they're called quines, and this isn't a curiosity but a consequence of a perfectly workable theorem. So "you cannot in principle know yourself" is a false claim, and I'm not making it.

The second thing is the limit, and here I'll be pedantic, because the temptation to say something stronger is very great and there's nothing to back the stronger thing with.

What is genuinely proved: **there exists no general procedure that, from the description of any system, would predict its substantive behavior.** There is no universal solver — not for "will this program halt," nor, more generally, for any non-trivial question about program behavior. These are classical results from the middle of the last century.

What is not proved — and what I will not claim: that this particular system cannot predict this particular self. That claim has an author and a name. Stephen Wolfram calls it computational irreducibility: some systems have no shortcut, and the only way to learn what happens in a thousand steps is to carry out all thousand.

Let me split it in two, briefly. What's firm: very simple systems can be computationally universal — Wolfram conjectured this in 1985 about the cellular automaton Rule 110, and Matthew Cook proved it; and for a universal system, general questions about behavior are undecidable. Only this is exactly the classical result I took a paragraph above — nothing beyond it is added here. What's not firm: irreducibility itself, in general form, is not a theorem but a principle. To prove that a particular system has no shortcut means proving a complexity lower bound, and lower bounds almost never come — this is one of the most stubborn difficulties in complexity theory.

So I take only the weak and the proved: there is no universal recipe for self-prediction. Particular questions about oneself can be settled, and people settle them constantly. A guaranteed method for all questions — there isn't one.

And this is the second bite: the system reads itself. Note that it's gentler than the first. The first bite is a fact: learning really does rewrite the substrate. The second is a limit on method, not a prohibition on self-knowledge.

And now the observation for which, to my mind, this part earns its place in the text. Look at **where exactly** the boundary of decidability runs.

Properties of the object are always decidable, and trivially so. How many lines the program has, how many parameters the network has, whether there's a loop inside, what number sits in such-and-such a position — a machine answers any such question in finite time, without running the program and without guessing. The object is readable. It's all right there; it can be counted up.

Undecidable are the properties of the function. What the program does, whether it halts, whether it's equivalent to another, whether its behavior has any substantive property at all — for these questions there is no general procedure and there cannot be.

That is, the boundary of computability runs exactly along the seam this text began with. Not near it, not approximately — along it. The object is always readable; the function is precisely what isn't. The distinction I introduced in part one as a convenient way of talking about intelligence turned out to be the line at which computability itself breaks. This is the one place in the text where my distinction isn't applied to something but is confirmed from outside — by a theorem proved long before any conversation about people and neural networks, and for an entirely different reason.

**An honest note, without which this part would be a swindle.** Everything discussed in the series so far has been about knowing another. This part is about knowing oneself. These are different claims about different things, and I have no intention of gluing them together with the appearance of unity. Why they nonetheless stand side by side — in the next part.

I mark the whole part as framework, not hypothesis, deliberately. It has no death condition and cannot have one: this is a mathematical fact, not a prediction about how the world is built. A prediction can be refuted by experience; a theorem cannot. Hanging a fake "death condition" on it for symmetry with the other parts would mean deceiving the reader.

> **Math inset 6. What exactly is proved about self-prediction.** \[textbook\] Three statements that are constantly glued into one.
>
> The positive one. Kleene's second recursion theorem: for any computable transformation of programs there exists a program that behaves as if it had applied that transformation to its own code. Hence quines, and the legitimacy of self-reference generally. Self-application is not a paradox but a construction.
>
> The negative one. Rice's theorem: any non-trivial property of the function computed by a program is undecidable — there exists no general procedure that answers such a question from the text of the program. The halting problem is a special case of it.
>
> What does **not** follow from this: that a given system cannot predict a given property of itself. The quantifier in Rice's theorem ranges over all programs at once; the absence of a universal method does not amount to the presence of a personal prohibition. Particular questions about oneself get settled constantly, and no theorem stands in the way.
>
> Formally the seam runs between the **syntactic** properties of a program (code length, number of parameters, presence of a loop) — trivially decidable — and the **semantic** ones, that is, properties of the computed function: undecidable. The discussion of this coincidence is in the main text of the part; I won't repeat it here.

------------------------------------------------------------------------

## 8. How This Connects to the Two Previous Texts

The temptation was to say it beautifully: three essays, three locks on one door. Beautiful, but untrue, and I'd rather say so myself.

The first two texts prove one and the same claim by different means. **You cannot finish reading another person.** The first essay shows it from the measurement side: however much you refine, the details never run out, and knowing doesn't converge. The second, from the side of the language of description: a short label doesn't describe a person but does govern the one who hung it. Two independent proofs of one thesis is a good thing — it's exactly what one wants from an argument.

The third text is about something else. It's about the fact that from the inside, too, you can't get a complete description of yourself in advance. That's a different subject and a different direction of gaze. Not a third lock on the same door, but the first lock on the door next to it.

And there's no weakness in that. The weakness would be in pretending there's only one door.

------------------------------------------------------------------------

## 9. Objections

**"The duality of object and function has been known since calculus — what's new here?"** Nothing, and I'm not claiming it — see part 2, deliberately marked as textbook. The new claim isn't about the duality but about the two sides diverging measurably and structurally, and about what that implies for the accuracy ceiling.

**"Identity by behavior is a philosophical trick. So what if they behave the same."** This objection is testable, and therefore not philosophical. Produce an experiment that distinguishes two intelligences behaving identically on all inputs. If you produce one — I'm wrong. If no such experiment exists, then "different but indistinguishable" is a claim without content.

**"Function determines form — there's a theorem."** There is, I put it on the table myself in part 4 and took it apart there: the theorem requires the whole function, and we always work with a finite sample. And the same theorem shows that no canonical ruler for the object exists.

**"AI and humans are different systems; transferring the conclusion is illegitimate."** Agreed, and that's why the conclusion isn't transferred. The claim about AI is an existence proof: divergence of the two sides happens, and it's structural. The claim about humans is hypotheses 6a and 6b, each with its own death condition. The second doesn't follow from the first; the first only shows the second isn't an invention. Nowhere do I say a human being is built like a neural network, and my thesis isn't about biology but about the reconstruction procedure.

**"But brains are being scanned — just wait, and the object will become accessible."** See part 5: what's inaccessible isn't the substrate but the middle floor. A complete connection map doesn't hand you a profile of abilities — that's a description at a different level. The instruments answer a different question.

**And the self-criticism, better spoken by me.** The weak spot of this text is the numbers it doesn't have. I declared the divergence of the two closenesses measurable and didn't measure it; I formulated hypotheses 6a and 6b, described a design that would tell them apart — and ran neither. The text remains an optical instrument, not a result. That's a legitimate genre, but let me name its boundary honestly: for now this is a way of seeing the problem, not a proof that it's solved in this particular way.

------------------------------------------------------------------------

## 10. The Return

Let's go back to that street in Ventspils.

The thought that switched on mid-run was the system's output. And then it came back around to the input: it rewrote months of drafts, changed the structure of three texts, forced eleven parts to be thrown out and started over. That is, it did exactly what part six describes: the output became the input, the function rewrote its own substrate. Only this time the substrate wasn't weights and wasn't synapses, but the design of the thing.

The body made the bus in minutes. The thought took weeks to finish writing itself. Different time scales — but the loop is one and the same, and both are real.

And the last thing, the point of writing all this. If it seems to you that a person — someone else or yourself — could be finished reading if only we had better instruments, that's neither optimism nor resignation. It's simply a mistake about where to look for the cause. The cause isn't in the instruments. It's that you have to read by the traces, and whoever leaves them is, by the time you've read them, already someone else.

------------------------------------------------------------------------

## Formulas

The whole essay in the language of formulas — part by part. There are two carrying symbols: `θ` — the object, the construction that produces behavior (for a network, the set of weights; for a person, the middle floor); `f` — the function, the behavior itself, the mapping "input → output." The whole text is about what happens in the passage between them. Layer tags (\[textbook\] / \[framework\] / \[hypothesis\]) are preserved.

**1. The Thesis** · \[framework\]

- `given: f(x₁), …, f(x_m)` — Everything issued to the observer is a finite sample of the function's values. Nothing else has been issued, and nothing else will be.
- `"what they are" = θ̂(sample)` — "What a person is really like" is not observation but a reconstruction of the object from that sample. The filling-in is yours, not theirs.
- `residual ≠ noise` — The carrying claim of the text: the accuracy ceiling is the signature of the reconstruction procedure, not the poverty of instruments.

**2. The Formal Home** · \[textbook\]

- `program = bytes` and `program = input → output` — Von Neumann: one and the same string lies there as a thing and works as a mapping. "Object or function" is a false dichotomy by construction, not by taste.
- `d(f,g) = max|f(x) − g(x)|` — The distance between functions is defined explicitly ⟹ the set of functions is a space: neighborhoods, convergence, dimension. The Gaussian process from №1 lives exactly there.

**3. The First Two-Sided Case** · \[textbook\]

- `θ ∈ ℝᴺ` (file) ⇄ `f_θ` (run) — Weights on disk are the object; the same weights running are the function. The object side needn't be comprehensible, only measurable.
- `W_in → P·W_in`, `W_out → W_out·Pᵀ` ⟹ `f_θ` unchanged — Permutation symmetry: an enormous shift in the object, exactly zero shift in the function. Not "approximately" — bit for bit.
- `∏ᵢ nᵢ!`; for one layer `1000! ≈ 10²⁵⁶⁸` against `10⁸⁰` atoms — How many different objects implement one function. The number isn't rhetorical.
- `W_in → c·W_in`, `W_out → W_out/c`, `c > 0` ⟹ `f_θ` unchanged (ReLU) — A second symmetry, continuous: the preimage of a function is a connected set of positive dimension, not a set of points.
- `f₁ ≡ f₂ ⟹ one intelligence` — Identity is extensional: no experiment distinguishes two identically behaving constructions ⟹ nothing to argue about.
- `(θ, context) ↦ f_eff` — One object, many functions, one per context. This is the "if A, then X" pattern from №1, but in a system whose construction is open.

**4. Two Kinds of Closeness Diverge** · \[framework\]

- `d_obj(θ₁,θ₂) = ‖θ₁ − θ₂‖` against `d_func(f₁,f₂) = E_x‖f₁(x) − f₂(x)‖` — Two rulers for the question "how close." Expectation: they agree. Fact: they don't.
- permutation: `d_obj ≫ 0`, `d_func = 0`; fine-tuning: `d_obj ≈ 0`, `d_func ≫ 0` — The link is broken in both directions, not merely weak.
- `d([θ₁],[θ₂]) = min_{g∈G} ‖θ₁ − g·θ₂‖` — The fix via a quotient space by the symmetry group `G` requires writing `G` into the ruler in advance ⟹ there is no canonical ruler by the construction of the problem, not for want of effort.
- `f in full ⟹ θ up to G` (Albertini–Sontag 1993; for ReLU — Phuong and Lampert 2020) — The objection "function determines form" is proved both for smooth odd activations and, later, for ReLU. Broadening the class of networks won't remove it.
- carrying limitation: `f in full` — Only this condition removes the objection: all such theorems require the function on **all** inputs, and we have a finite sample. Independent of architecture and activation ⟹ never softened.
- `G_ReLU ⊃ G_tanh`: permutations `+` continuous rescaling — The limitation on activations works **not** toward removing the objection but toward the non-canonicity of the ruler: the preimage of a function stops being discrete. The two conclusions are not to be mixed.
- status: `existence proof`, not `transfer` — On the AI side it's shown that divergence of the sides happens and is structural. Nothing about humans follows from this — only the plausibility of the hypothesis.

**5. Back to People** · \[hypothesis\]

- `f visible, θ not` — For a human being the picture is the reverse of the machine's: behavior is observable, the construction isn't.
- `substrate → construction → profile` — Three floors. The bottom is read better and better (scanners, connectomes), the top is produced by psychology. The middle one is inaccessible — not through poverty of instruments but because it's a different level of description.
- `r ≈ 0.3` — The ceiling for predicting a specific act from a general trait.
- `r_m = m·r₁ / (1 + (m−1)·r₁)` — Spearman–Brown: aggregating over `m` observations raises accuracy ⟹ a significant part of the raw 0.3 really is noise. The thesis isn't about that part.
- `f: S → R`, `θ = E_s[f(s)]`, mapping `f ↦ θ` many-to-one — The profile is the average of the pattern over situations. Two people with one average and opposite patterns get the same profile. What's lost is the component of `f` orthogonal to the constant — and it isn't in the aggregate at any `m`.
- **Hypothesis 6a:** `residual = structural loss in compression`, not `measurement noise` ⟹ not removed by improving instruments — The mapping "construction → behavior" is many-to-one, and reconstruction runs from a finite sample.
- death of 6a: `ceiling(prediction from f) = ceiling(prediction from θ)` — If the pattern predicts no better than the averaged trait, the discarded structure carried nothing and the mechanism is made up. Weak version: improving instruments systematically raises the ceiling ⟹ it was noise.

**6. The Loop: The Target Moves** · \[framework\]

- `θ_{t+1} = U(θ_t, e_t)`, where `e_t = loss(f_{θ_t}(x_t), target)` — The form of the cycle: the object sets the function, the function errs, the error rewrites the object.
- `U = gradient descent` and `U = synaptic plasticity` — Two instances of one form, **not** one mechanism: backpropagation requires symmetric connections the brain doesn't have. The claim is deliberately limited.
- `error(m) ≈ σ/√m + δ·m` ⟹ `m*` finite, `min > 0` — Estimating a non-stationary target: observe longer and you catch an average over the trajectory that existed at no single moment; shorter and you drown in noise. The error floor isn't removed by either strategy.
- **Hypothesis 6b:** `residual ⊃ drift contribution`, `δ > 0` — A second, independent cause of the same floor. Death of 6b: the residual doesn't grow with the gap between observation and prediction ⟹ the target is stationary for our purposes.
- `6a ∧ 6b`: the general thesis falls only if **both** die — An admission against myself: two legs make the hypothesis harder to kill, and therefore more suspect. The compensation is the discriminating design below.
- discrimination: `∂residual/∂Δt > 0` (drift) against `∂residual/∂contrast(if-then) > 0` with `∂/∂Δt = 0` (compression) — Two factors in one design; the outcome "neither" kills the whole thesis.
- `∂r_test-retest/∂interval < 0` — Drift is empirically confirmed: 152 longitudinal studies. The support is the derivative, not the level: the gap `0.74 < 1` mixes real change with measurement unreliability, whereas the fall with interval isn't explained by unreliability — measurement error doesn't depend on the length of the interval.
- `the rule is rewritten in the course of the drawing` — The answer to the mathematician from №1: knowing fails to converge not because of self-similarity but because the pattern is completed faster than it can be read.
- emblem: `output → input` — The first bite: the function rewrites its own substrate. The symbol is taken as a generator, not as a measuring instrument (the license from №2, part 6).

**7. The Same Question from the Inside** · \[framework — not a hypothesis\]

- Kleene: `∃e: φ_e = F(e)` — The second recursion theorem: self-reference is legitimate, quines exist. "You cannot in principle know yourself" is a false claim.
- Rice: `non-trivial property of f ⟹ undecidable` — There is no general procedure answering a substantive question about a system's behavior from its description. The halting problem is a special case.
- `¬∀` ≠ `∀¬` — The absence of a universal method is not a personal prohibition. Particular questions about oneself get settled constantly.
- computational irreducibility = principle, not theorem — Wolfram named the phenomenon; what's firm in it is the universality of simple systems (Rule 110, proved by Cook) and the undecidability that follows — that is, the classics already taken. Proving there's no shortcut for a particular system = proving a complexity lower bound ⟹ not taken as support.
- `syntax(θ)` decidable / `semantics(f)` undecidable — The boundary of computability runs exactly along the essay's seam: properties of the object are always readable, properties of the function are not.
- emblem: `f(θ)`, where `θ` implements `f` — The second bite: the system reads itself. Gentler than the first — a limit on method, not a prohibition on self-knowledge.

**8. Connection to the Series**

- №1 and №2: `you cannot finish reading another person` — Two independent proofs of one thesis: from the measurement side (it doesn't converge) and from the side of the language of description (the label governs the observer).
- №3: `you cannot compute yourself in advance` — A different subject, a different direction of gaze. Not a third lock on the same door but the first on the door next to it. Better to say so myself than to be caught at it.

**The emblem formula of the text**

- `f ↦ θ` many-to-one ⟹ `residual ≠ noise` — Compressing behavior into a profile loses structure, not precision. That's why the ceiling won't rise with instruments: it isn't standing where everyone is looking.

------------------------------------------------------------------------

## Sources

> **\[SOURCE REVIEW COMPLETED (02.08.2026): 23 entries. Checked directly against the primary source during work on this text: entries 5, 6, 13, 14 and 21 — those carrying load-bearing claims, or where the wording was corrected in the course of proofreading; each states what specifically was confirmed. Entries 15, 16 and 17 are carried over from the source reviews of essays №1 and №2 and were not re-checked. Entry 11 remains open: the exact wording of the title is unconfirmed. The remaining entries — settled classics and textbook references without contestable details — were not separately re-verified in this pass, and I flag that rather than paper over it.\]**

1. Marr, D. (1982). *Vision: A Computational Investigation into the Human Representation and Processing of Visual Information.* San Francisco: W. H. Freeman. (Reprint: MIT Press, 2010.) Three levels of description: computational theory; representation and algorithm; hardware implementation.
2. Hecht-Nielsen, R. (1990). On the Algebraic Structure of Feedforward Network Weight Spaces. In: Eckmiller, R. (ed.), *Advanced Neural Computers*, 129–135. — the first description of permutation symmetry.
3. Chen, A. M., Lu, H.-m., & Hecht-Nielsen, R. (1993). On the Geometry of Feedforward Neural Network Error Surfaces. *Neural Computation*, 5, 910–927.
4. Ainsworth, S. K., Hayase, J., & Srinivasa, S. (2023). Git Re-Basin: Merging Models modulo Permutation Symmetries. *ICLR 2023*; arXiv:2209.04836. — plus Entezari et al. (2021) as the source of the conjecture on connectivity modulo permutation.
5. Albertini, F., & Sontag, E. D. (1993). For neural networks, function determines form. *Neural Networks*, 6(7), 975–990. — identifiability: the function fixes the weights up to symmetries, given knowledge of the whole function. A clarification essential for part 4: the result is proved for odd smooth activations under the conditions σ(0)=0, σ′(0)=1, σ‴(0)≠0 — the hyperbolic tangent family, not ReLU; it does not apply to modern networks in its original form. See the next entry.
6. Phuong, M., & Lampert, C. H. (2020). Functional vs. parametric equivalence of ReLU networks. *ICLR 2020* (8th International Conference on Learning Representations). — for ReLU networks the symmetry group includes continuous positive rescaling in addition to permutations; for architectures with non-increasing widths these two transformations exhaust the function-preserving ones. Essential for part 4: this *is* identifiability for ReLU, i.e. an extension of the theorem rather than its absence.
7. Grossberg, S. (1987). Competitive learning: from interactive activation to adaptive resonance. *Cognitive Science*, 11, 23–63. — the weight transport problem is named here.
8. Crick, F. (1989). The recent excitement about neural networks. *Nature*, 337, 129–132.
9. Lillicrap, T. P., Cownden, D., Tweed, D. B., & Akerman, C. J. (2016). Random synaptic feedback weights support error backpropagation for deep learning. *Nature Communications*, 7, 13276.
10. Lillicrap, T. P., Santoro, A., Marris, L., Akerman, C. J., & Hinton, G. (2020). Backpropagation and the brain. *Nature Reviews Neuroscience*, 21, 335–346. — a review from which it's clear the question is open in both directions.
11. Bartunov, S., et al. (2018). Assessing the scalability of biologically-motivated deep learning algorithms and architectures. *NeurIPS 2018*. (exact wording of the title unconfirmed)
12. Epstein, S. (1979). The stability of behavior: I. On predicting most of the people much of the time. *Journal of Personality and Social Psychology*, 37(7), 1097–1126. DOI 10.1037/0022-3514.37.7.1097. — aggregation raises accuracy. Part II: *American Psychologist*, 1980, 35, 790–806.
13. Spearman, C. (1910). Correlation calculated from faulty data. *British Journal of Psychology*, 3(3), 271–295. DOI 10.1111/j.2044-8295.1910.tb00206.x; Brown, W. (1910). Some experimental results in the correlation of mental abilities. Ibid., 3(3), 296–322. — the Spearman–Brown formula: growth of aggregate reliability with the number of observations; the mathematical support of the aggregation objection (inset 4). Spearman's paper has a section headed "Increase of reliability by increasing the number of measurements." The same author as source №1 of the first essay (Spearman 1904): the foundation of the series and the chief counterargument to it, from one man six years apart. A pedantic note: the form of the formula in use today is Brown's version, and some psychometricians call it Brown–Spearman.
14. Roberts, B. W., & DelVecchio, W. F. (2000). The rank-order consistency of personality traits from childhood to old age: A quantitative review of longitudinal studies. *Psychological Bulletin*, 126(1), 3–25. DOI 10.1037/0033-2909.126.1.3. — 152 longitudinal studies, 3,217 test-retest coefficients; consistency rises from 0.31 in childhood to a plateau of ≈0.74 at ages 50–70 (at an interval of 6.7 years) and **decreases as the interval grows**. The empirical support of hypothesis 6b — support on the decrease specifically, not on the level.
15. Mischel, W. (1968). *Personality and Assessment.* Wiley. — the "0.3 ceiling." *(carried over from the source review of №2)*
16. Mischel, W., & Shoda, Y. (1995). A cognitive-affective system theory of personality. *Psychological Review*, 102(2), 246–268. — the if-then pattern. *(carried over from the source review of №1)*
17. Funder, D. C., & Ozer, D. J. (2019). Evaluating effect size in psychological research: Sense and nonsense. *Advances in Methods and Practices in Psychological Science*, 2(2), 156–168. *(carried over from the source review of №2)*
18. Rice, H. G. (1953). Classes of recursively enumerable sets and their decision problems. *Transactions of the American Mathematical Society*, 74, 358–366. DOI 10.2307/1990888. — no general procedure for non-trivial properties of program behavior.
19. Kleene, S. C. (1938; exposition — *Introduction to Metamathematics*, 1952). The second recursion theorem. — the positive result: self-reference is possible, quines exist.
20. Wolfram, S. (2002). *A New Kind of Science.* Champaign: Wolfram Media. — computational irreducibility; called a principle rather than a theorem in the text, and not taken as support.
21. Cook, M. (2004). Universality in Elementary Cellular Automata. *Complex Systems*, 15(1), 1–40. — the proof of universality for Rule 110; Wolfram's 1985 conjecture. The only elementary cellular automaton with directly proved Turing completeness.
22. Hofstadter, D. (1979). *Gödel, Escher, Bach: An Eternal Golden Braid.* Basic Books. — a popular exposition of self-reference; not a load-bearing source in the text.
23. The Rider–Waite deck (1909): A. E. Waite, art by Pamela Colman Smith, published by William Rider & Son. The lemniscate above the Magician's head — confirmed; Waite himself called it a sign of life, "infinity" being a later popular reading. *(for the emblem, if it stays in the text)*
