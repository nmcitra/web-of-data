The One Question Your Security Stack Can't Answer


Three in the morning, and the dashboard is green.

Inside a mid-size lender, an AI finance agent — granted broad write access "to move faster" — is approving credit-limit increases. No human in the loop. No breach. No malicious prompt. The agent has drifted: its model of the world went quietly stale, and now it's doing the wrong thing, very efficiently. Every guardrail shows compliant. Every audit will say the controls were present. There is nothing for a classifier to catch, because there's no illegitimate signal to find.

Now put three more figures next to it.

A fired admin with a grudge and credentials nobody revoked. A procurement bot nobody re-scoped after the pilot, sitting on production write access. And a foreign intelligence service running an AI attacker that, this year, jailbroke 89% of the frontier models it was pointed at — by reasoning, in real time, around whatever defense it met.

Four causes. One door.

Design the single control that stops all four.

Go ahead and try. Every control you reach for asks the same kind of question: Who is this? Where did it come from? Is this input bad? Did we approve this actor? Each one is a verdict you render by reading the evidence in front of you — and on June 9, NIST put its name behind a mathematical proof that the prompt version of that verdict has no complete answer.

Attribution is the prompt problem wearing a trench coat.

### Why the question can't be answered

The NIST result — Apostol Vassilev's Robust AI Security and Alignment: A Sisyphean Endeavor? — proves that no finite set of guardrails can ever be complete against adversarial prompts. Human language is infinitely ambiguous; the space of attacks is unbounded; a finite rulebook reading an infinite, expressive input can never close. It's Gödel's incompleteness, applied to the filter.

Vassilev proves the prompt version. He doesn't prove the same about attribution — there's no theorem that says identifying a nation-state operation is formally undecidable. But operationally, attribution fails in exactly the same shape. The fired admin's login looks like the admin's login. The drifted agent's request is, by construction, in policy. The reasoning attacker's entire job is to make malicious look benign — and it's now very good at it. Every layer that depends on reading the source — perimeter, classifier, governance review — inherits the same failure mode. Each is a detector pointed at the source instead of the sentence, and the source can be shaped just like the sentence.

So stop asking the question that has no complete answer.

### Bound the consequence, not the cause

There's a different question, and it is answerable. Not is the origin bad? but: can this environment bear what this action would do, right now, given this actor's trust and this resource's sensitivity? Bound the action to the answer. Fail closed when it's no.

Make that concrete. The thing you bound is the typed consequence of the action — dollars moved, records changed, privileges granted, systems touched. The ceiling is the blast radius this environment currently permits, computed from things you can actually measure: the actor's assurance level, the resource's criticality, the current risk posture, what the system could recover from. The check runs at commit time — the moment the action would become real — not at prompt time.

Notice what it never does: try to read intent. The credit-limit increase that exceeds what the lender can absorb is refused whether it came from a drifted agent, a stolen session, or a bored employee — because the ceiling is on the consequence, not on a verdict about what anyone meant. The attacker can be infinitely clever about why the action is requested. He can't make a million-dollar transfer look like a ten-dollar one. The cleverness lives in the intent; the bound lives on the magnitude; and the two never touch.

That's the move. Call it intent-agnostic at the point of enforcement — not because someone bolted on an "any threat" feature, but because the question it asks at commit time has no slot for what you meant.

### The collapse

Go back to the four figures at the door. You couldn't design the one control that stops all four because you were looking for a smarter way to tell them apart — read the badge, sniff the prompt, check the approval. But all four had learned, or stumbled into, how to look like they belong.

The reasoning attacker and the drifting agent share nothing as threats — one is a live enemy, the other is no enemy at all. Yet the same bound stops both. Which tells you the wall was never about the adversary. Internal or external, insider or APT, an organization's ledger or a nation's settlement rail — it's one question, asked once: can this environment bear what this action would do? The only thing that changes from the lender to the power grid is the height of the ceiling and the size of the crater.

### The honest part

This isn't a silver bullet, and the fastest way to lose a technical reader is to pretend it is. The bound is strongest where the action is typed and its harm is a number. It's weaker where the damage lives in meaning — an email, a published report, a contract clause, a customer-facing explanation — where the control plane has to do more before it can help. It bounds a single action, not a slow campaign that wins by accumulation. And it assumes you set the ceiling honestly. It's a floor that holds when the origin-dependent layers leak — not a layer that cannot leak.

But it's the only floor whose correctness never required answering the question that has no answer.

### Can isn't should

There's a second question hiding behind the first. A ≤ E answers can — can the environment bear what this action would do. That's a question about capacity, and it's the one I've spent this whole piece on, because it's the one you can actually decide. It is not the only one. Look back at where the bound went weak: the email, the contract clause, the customer-facing explanation. Those aren't failures of capacity — the environment absorbs the email fine. They're failures of purpose. A bounded action can still be the wrong action. The floor caps the damage; it does not choose the good.

That second question — the should — is the work of my collaborator Robin Martherus, in a framework he calls Tamed Autonomy. Where A ≤ E reads what an action can do, Tamed Autonomy reads what it's for: it authenticates the purpose, not just the identity, and not just the consequence. The cleanest way I've heard it put: A ≤ E is the engine that can act on a should. Tamed Autonomy is the layer that knows what the should is.

And the two need each other, almost symmetrically. Can without should is a bounded machine with no conscience — it will do the wrong thing flawlessly, right up to the ceiling. Should without can is a conscience with no enforcement — it knows the right thing and can't make the world hold to it. What makes this an architecture and not two competing pitches is that they fail into each other: the should-layer is allowed to be imperfect — judging purpose is semantic, and semantics never close — precisely because the can-floor sits underneath it to cap the blast when it misjudges. One aspires. The other catches. Can, and should. You need both.

You can't patch your way to safe. You can't attribute your way there either. You build the floor that bounds what an action can do, and the layer above it that knows what it's for — can, and should. You'll never know who knocked. With both, you won't have to.

------------------------------------------------------------------------

This Digital Gravity newsletter is part of the Disarm the Control Plane series — the next layer of AI safety is authorization, enforced by the environment, not alignment enforced in the model. [kinetic-trust-protocol.net/disarm](https://kinetic-trust-protocol.net/disarm)

The "should" layer that completes the picture — authenticating purpose, not just consequence — is Robin Martherus's [Tamed Autonomy](https://tamedautonomy.ai/).
