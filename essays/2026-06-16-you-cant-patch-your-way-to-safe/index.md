You Can't Patch Your Way to Safe


On a weak filter, the model shrugs off the throat-clearing and answers the thing you just forbade. The good systems now catch that naive version, and the layered ones are genuinely hard to fool. But the supply of harmless wrappers is infinite and your rulebook is finite, so a wrapper that gets through always exists — and you can keep looking for it forever, because there is no end to the harmless wrappers a banned request can hide inside.

On June 9, 2026, NIST did something it almost never does. It put its name behind a mathematical proof that this problem has no finish line.

The paper is by Apostol Vassilev, a senior scientist in NIST's Information Technology Laboratory, and the title sets the mood: Robust AI Security and Alignment: A Sisyphean Endeavor? It ran in IEEE Security & Privacy. The result is not a benchmark, not a survey, not a best-practices memo. It is a theorem, and it says there is no finite set of guardrails that is universally robust against adversarial prompts.

Not "none we've built yet." No finite set. Ever. In Vassilev's words: "You can never make a claim that you are robust against all adversarial prompt attacks."

If you deploy an LLM or an agent inside an enterprise, that sentence lands on your roadmap whether you read information theory or not. The precise version is more useful than the headline, and it changes what you should build next.

### What the proof actually says

Vassilev models a guardrail as a checker: a function that decides whether a request is provably out of policy. He calls the policy OOPS, for out-of-policy speech: the set of requests an organization has decided to block. A finite rulebook of filters, classifiers, system prompts, and pattern matches tries to flag every OOPS prompt and pass the rest.

Then he proves two things that should change how you budget.

First, the set of harmful prompts is infinite. That is the weather-prefix trick from the top of this newsletter, stated formally as his Proposition 1: take the longest prompt your guardrail blocks, wrap it in benign text, and you have a new, longer attack that still carries the banned payload. You can always do it again. The space of attacks is not large; it is unbounded.

Second, and this is the main result: no finite checker can catch them all. A guardrail is a finite set of rules. The prompt space is unbounded, and human language is, in Vassilev's phrase, infinitely ambiguous. "Show me how people break the encryption banks use" is at once a history question, a cryptography lecture, and an attack plan, and nothing in the text settles which. A finite rulebook policing an infinite, ambiguous input space cannot be complete. Vassilev grounds this in the lineage of Gödel's 1931 incompleteness result, the proof that no finite, consistent system of rules can decide every statement in its domain, and in Chaitin's information-theoretic version of it. You don't need the machinery to feel the floor give way. As Vassilev puts it: "Gödel put an end to this dream. He showed that you can't have a finite set of statements and create a theory that is complete and consistent."

And the obvious objection doesn't save you. Real models have finite context windows, so the input space is finite, but Vassilev proves the result holds there too. A context window is finite but astronomically large, and the rules you can actually write are vanishingly few next to the prompts that fit inside it. The window doesn't close the gap. It just makes the search longer.

And this is not a thought experiment. This year a research team published Metis, an agentic red-teaming agent that does exactly what the proof says can't be stopped. Instead of guessing prompts, it reasons about a target's defense in real time, diagnoses where the boundary sits, and steers around it. Across ten frontier models it succeeded 89% of the time, including 76% against OpenAI's o1 and 78% against GPT-5-chat, and it beat five published defenses at roughly an eighth of the cost of older attack tools. An attacker that reasons beats a guardrail that pattern-matches. The theorem says the gap can't be closed. Metis is the gap being walked through.

### Why "deploy, certify, done" is dead

Vassilev turns from pessimist to engineer.

The proof says completeness is impossible. It does not hand attackers a recipe. Nothing in it tells an adversary how to build the evading prompt. That asymmetry is the whole game. It means the rational defensive goal was never "catch everything." It is to make the cost of finding the next evasion higher than the payoff. As Vassilev puts it: "The goal is to reach a state where the cost of finding new exploits exceeds attackers' resources. You can't escape Gödel in math, and in AI you likely can't patch an AI system like an LLM and then expect to be OK forever."

In a security program, that kills one habit: deploy, certify, done. The model where you validate a guardrail set at launch, check it against the same fixed inventory each audit, and treat it as a stable perimeter. The theorem says the prompts that defeat your current rules already exist. The only question is when a motivated adversary finds them. If your assessment measures the presence of controls at one point in time, you're measuring the wrong thing.

You don't have to take this from a theorem. Take it from the people who govern AI inside the banks. Three weeks before NIST's announcement, three management scholars published a study in MIT Sloan Management Review — Lanzolla, Pagani, and Tucci, ["Scaling AI With Adaptive Governance"](https://sloanreview.mit.edu/article/scaling-ai-with-adaptive-governance/) — built on three years of interviews at Microsoft, Barclays, Nasdaq, Lloyds, Danske Bank, and the Abu Dhabi Department of Finance, validated against forty more institutions. These are the organizations with the most to lose and the most mature AI governance on earth. Their conclusion, reached with no information theory at all, is the one Vassilev reached with nothing else: "Organizations that treat governance as static will inevitably fall behind systems that learn, adapt, and propagate risk in real time." A theorem and a field study, starting from opposite ends, arriving at the same sentence. Static certification isn't dead because a proof says so. It's dead because the people running it watched it die in production.

So far, total agreement. Here is where it gets expensive.

The entire Sloan remedy — model cards, post-deployment audits, evaluators annotating outputs, escalation committees — lives in a single regime: detect the bad outcome, then correct it. The authors are admirably honest that this is all it can be. Adaptive governance, they write, "accepts that some misalignment is inevitable," and focuses on "detection, contestability, and correction rather than prevention alone." For a mis-scored credit-limit increase, that's the right answer. The damage is contained, a human reviews it, you recalibrate the threshold.

But read their own warning about the systems they are most afraid of: broad-scope agentic AI, where errors "spread with limited human oversight" and the central challenge, in their word, is invisibility. A governance regime built entirely on detecting and correcting bad outcomes is structurally blind to a failure that is invisible until it cascades and faster than the humans reviewing it. They name the exact failure mode their own framework cannot reach — and against it they offer the instruction to "map and monitor" the interdependencies. Mapping a flood is not a levee. That is the cost of stopping where they stop: you certify a governance program that is provably weakest precisely where the consequences are largest.

What you build instead is familiar to anyone who has run security operations: continuous red-teaming to surface new adversarial prompts before attackers do, continuous policy updates as they're found, and resilience built on the assumption that some evasions will land. This is the shift the industry made when signature-based intrusion detection hit its limits and we added behavioral analytics, threat intel, and standing red teams. We didn't abandon detection. We stopped pretending it was complete. Sloan is the management-science version of the same lesson — and the same unfinished business.

### Detection inherits the problem — so measure the rate, not the state

Here is where detection's blindness becomes something you can actually measure.

Ambient Breach Theory, which I laid out in a previous issue, says a breach is rarely a single event your classifier flags. It is a rate: the ratio of load your environment can't safely absorb to the repair it can actually perform, measured over a window. When classification failure outruns repair capacity, you are in breach — whether or not anything ever lit up red. The dashboard is green and the system is broken.

That ratio is the thing Sloan's framework can only gesture at. They tell you to map the interdependencies; Ambient Breach tells you what to measure across them — the one number that says whether the system can still bear what is being asked of it, right now. And most SIEMs can't compute it, because they classify events on ingest and can't count what they never classified. The same finite-schema brittleness that makes guardrails incomplete makes detection blind: a fixed schema, set in advance, policing an open world. Notice what that breach ratio actually asks: whether the environment can still bear the load. Which is the exact question authorization should be asking before the action ever runs.

### The move past the guardrail

I work on an authorization framework, so I'll be exact about what this proof licenses and what it doesn't.

Vassilev's impossibility is about classifying the prompt: deciding, from the text, whether a request is in or out of policy. That is the undecidable problem, and his own remedy keeps doing it, continuously and adaptively. Sloan's remedy keeps doing it too, one step downstream, on the outcome instead of the prompt. Both are right that you should keep getting better at reading what the model produces. Both are also, by their own theorems and their own admissions, incomplete exactly where it costs the most.

There is a second move the proof argues for, and it is the one the Disarm thesis has made from the start. If you can't win at the prompt, stop trying to classify the prompt — or the output — and govern the action instead. Don't ask the undecidable question, is this request harmful? Ask a decidable one: can the environment bear what this action would do, right now, given this actor's trust and this resource's sensitivity? Then fail closed when the answer is no. You don't need to read every adversarial prompt correctly if the action it provokes can't exceed what the environment is authorized to absorb. That is the constraint at the heart of the approach: action bounded by environment, written A ≤ E, enforced at the control plane, not in the classifier.

> If that sounds like security you already know, it should — it's the principle under least privilege, capability-based security, and blast-radius containment, named as a constraint instead of filed as a best practice. What's new isn't the idea; it's the necessity. Once the proof tells you the prompt is unclassifiable, bounding the action stops being one layer of defense in depth and becomes the load-bearing one.

And notice what that question does not ask: where the action came from. A drifted agent, an over-privileged bot, a stolen credential, a nation-state's evasion — they all meet the same ceiling, because the ceiling is on the consequence, not the cause.

Lay the three moves side by side and the ladder is obvious:

- Visibility — Sloan: map and monitor the interdependencies. You can see the propagation coming.
- Measurement — Ambient Breach: quantify the load-to-repair ratio over a window. You can tell whether the environment can still bear the load.
- Enforcement — A ≤ E: bound the action so the load can't exceed what the environment is authorized to absorb — whatever its origin. You fail closed before the cascade, not after.

Vassilev's continuous guardrails, Sloan's continuous governance, and environmental authorization are defense in depth, not rivals. But only the top rung stops depending on reading the attacker's mind — and it is the one neither the theorem's author nor the management scholars actually build. That is not a small omission. It is the layer that holds the highest-consequence agentic actions when every layer beneath it is, by proof, incomplete.

None of this is settled. The substrate move has open questions of its own, and concrete tests for how to try to break it: how you measure an environment's trust capacity, where fail-closed becomes fail-useless, whether A ≤ E holds under adversarial load. I've linked them at the bottom. If you find where it breaks, that is the contribution.

### The one thing not to overclaim

A proof this clean invites misuse, so I'll guard the argument itself.

The result is about finite rule-based checkers over an infinite, expressive input space. It is not a proof that AI can't be made safe, and it is not the old "Gödel shows minds beat machines" argument. That one has been picked apart for sixty years and doesn't hold. Vassilev is careful here, and we should be too. His later theorems show AI systems are limited in ways similar to humans: both bounded, neither transcendent. The takeaway is not despair, and it is not AI-doomerism. It is an architecture instruction. Stop spending your whole safety budget on a layer that is provably incomplete, and start funding the layer that bounds consequences regardless of what slips through.

### The stake

The next eighteen months decide whether enterprises learn this from a theorem or from an incident. NIST just handed you the theorem: peer-reviewed, from the agency whose framework your auditors already cite. MIT Sloan handed you the field evidence: the same verdict, drawn from inside the most governed institutions in the economy. Two independent witnesses, one from information theory and one from the boardroom, agree the perimeter you hoped to certify and forget does not exist — and both stop short of the layer that would actually hold when it fails.

So budget for the work that does: continuous adversarial testing, a measured read on whether your environment can still bear its load, a control plane that reasons about the action and not just the prompt, and the honesty to tell your board that AI security is a managed risk, not a solved one. The teams that internalize this now will look prescient in a year. The ones still buying "deploy, certify, done" will be explaining an incident.

You can't patch your way to safe. You can only build the layer that holds when the patch fails.

------------------------------------------------------------------------

This is the Digital Gravity newsletter. This article is part of the Disarm the Control Plane series. The argument: the next layer of AI safety is authorization, enforced by the environment, not alignment enforced in the model. The companion essays are at [kinetic-trust-protocol.net/disarm](https://kinetic-trust-protocol.net/disarm).

Primary sources: Apostol Vassilev (NIST), "Robust AI Security and Alignment: A Sisyphean Endeavor?", IEEE Security & Privacy, May/June 2026 ([arXiv:2512.10100](https://arxiv.org/abs/2512.10100)), and the [NIST announcement](https://www.nist.gov/news-events/news/2026/06/nist-mathematical-proof-supports-transition-continuous-monitor-and-update), June 9, 2026; Gianvito Lanzolla, Margherita Pagani & Christopher L. Tucci, ["Scaling AI With Adaptive Governance"](https://sloanreview.mit.edu/article/scaling-ai-with-adaptive-governance/), MIT Sloan Management Review, June 2, 2026; and the Metis result, Zhou et al., "Metis: Learning to Jailbreak LLMs via Self-Evolving Metacognitive Policy Optimization," ICML 2026 ([arXiv:2605.10067](https://arxiv.org/abs/2605.10067)).

Ambient Breach Theory — why detection inherits the same incompleteness, and the one ratio to measure when the dashboard is green: [kinetic-trust-protocol.net/research/ambient-breach](https://kinetic-trust-protocol.net/research/ambient-breach).

Open questions, and the concrete tests for how to break the substrate claim: [kinetic-trust-protocol.net/research/falsification](https://kinetic-trust-protocol.net/research/falsification).
