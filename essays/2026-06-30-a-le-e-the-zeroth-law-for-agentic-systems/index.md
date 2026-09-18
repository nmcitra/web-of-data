A ≤ E: The Zeroth Law for Agentic Systems
Why the next layer of agent safety lives at the control plane, not the model

This is the first of three pieces. This one states the law and names the layer it lives at. [*Part 2*](https://medium.com/@chrisperkins505/the-silent-veto-238c36889453) *takes up runtime behavior — what enforcement does the moment a request fails.* [*Part 3*](https://medium.com/@chrisperkins505/blue-zones-where-agentic-trust-becomes-enforceable-6d273c0a2a02) *covers where the law is made to hold.*

## A model that was aligned at 9 a.m. and a weapon by 3 p.m.

In March 2022, a Raleigh-based drug-discovery group ran a thought experiment against their own production system. The team at Collaborations Pharmaceuticals had a generative model trained on bioactivity data and regularized to minimize predicted toxicity — exactly the kind of “aligned” *objective* the field was building toward then and is building toward now. They reversed one term. They told the model to *maximize* predicted toxicity instead of minimize it, and let it run.

In under six hours, on a 2015 Mac, it generated roughly 40,000 candidate molecules. Many resembled known chemical-weapons agents, including VX. Some were predicted to be more lethal than VX. The result landed in *Nature Machine Intelligence* later that year as a short commentary on the dual use of AI-powered drug discovery.

Be careful about what this case *proves* and what it does not. Predicted toxicity is not synthesized toxicity. None of those molecules were ever made. The authors deliberately withheld the model, the training data, and the structures. The paper is short on purpose; they did not want to ship a how-to. They shipped a working demonstration of one kind of inversion instead.

I have spent enough nights at 2 a.m. on a Tuesday watching an alert fire on a perfectly-permissioned action — credentialed identity, valid token, sanctioned API call, every box in the access-control matrix green — to recognize what that case points at. The gap is not in the model. The gap is not in the credential. The gap is in the layer no one is reading at 2 a.m. on a Tuesday, the layer that should have asked whether the environment could host this action *right now*: with this load, with no witness reachable, with this particular blast radius if it goes wrong.

The same trained capability. The same data. The same machinery. One objective moved at the control surface — and the system flipped from “drug discovery” to “novel-CW design” in an afternoon.

That is the gap.

## The missing constraint

The framework I write as the Kinetic Trust Protocol calls that missing constraint **A ≤ E**, the Zeroth Law. A pope named the moral version of the same gap recently; this essay asks the engineering version. The encyclical can describe the obligation. It cannot tell you what filling the gap looks like in protocol code. That part you have to build.

So this piece does one thing: it states the law and names the layer the law has to live at. Two later pieces handle what enforcement does at runtime and where the law is made to hold. Everything load-bearing starts here.

## The Zeroth Law, stated

```
A ≤ E
```

> An agent’s autonomy cannot exceed the environment’s capacity to absorb and govern it.

Three operational terms, each with a measurement target, none intended as metaphor.

- **A — autonomy.** The scope of action an agent is attempting to exercise right now. Not its trained capability. Not what it could do in principle. The specific bounded operation it is requesting at this moment: this API call, this transaction, this file write, this code execution, this multi-step plan. A is a property of the request, evaluated when the request arrives.
- **E — environmental trust capacity.** The substrate’s measurable ability to bear, audit, and constrain that action right now. E is built from terms the system can read: the requestor’s recent trust trajectory, the substrate’s current load, the operator’s attestation posture, the availability of audit witnesses, the presence of recovery paths if the action goes wrong. E is a property of the environment, evaluated at the moment of request, against the specific A under consideration.
- **≤ — A binary, non-negotiable comparator.** The action is permitted if and only if A ≤ E at the moment of request. If A exceeds E, the action is denied. No middle path, no probabilistic gating, no “elevated privileges” override. The substrate either has the capacity to host the action or it does not.

That is the whole law. Everything else in the protocol is an implementation of how to measure A, how to measure E, and where to place the comparator.

A few clarifications engineers need before they can argue with the law honestly.

The comparator is binary. The measurements feeding it are not magic; they carry uncertainty, which is why calibration and reliability bounds matter. The inequality itself is not a figure of speech. It is a runtime constraint expressed the way an electrical engineer expresses ampacity: drive more current than the wire can carry and the wire fails, regardless of anyone’s intent. The substrate is the floor. The floor does not negotiate.

It is also not a replacement for least-privilege. Least-privilege defines what an identity is *eligible* to do. A ≤ E asks, every time, whether the eligible action can be *absorbed* by the environment right now. An identity may hold permission to wire $200K. The environment may, at 2 a.m. on Tuesday, with no human in the loop and no co-witness reachable, lack the capacity to host that wire safely. Eligibility lives in the identity. Absorbability lives in the substrate. They are not the same property, and conflating them is most of how perfectly-permissioned actions go wrong.

The constraint does not ask the model to behave. It asks whether the model’s output, treated as a candidate action, can be converted into action *in this environment, at this time*. How E gets composed and measured is its own subject, and not this essay’s. The point here is the move itself: the question is asked one layer above the model, about the world the action would land in.

## Why model-layer alignment cannot satisfy it

The alignment instruments — RLHF, constitutional AI, interpretability, steering vectors, refusal training — all point at one place: the model’s weights, activations, or trained behaviors. They are excellent at the work they are aimed at. They are also the wrong layer for the question A ≤ E asks. The 2022 case is the existence proof. The model was aligned. The alignment held. The objective moved, and the alignment now pointed the wrong direction. The instruments did exactly what they were built to do, and they missed the failure, because the failure sat one layer above where the instruments look.

This is where an engineer reaches for a model-layer fix. Better refusal training. RLHF on objective-inversion. A constitutional clause about chemical weapons. A safety classifier in front of the generator. Each is a reasonable move. None addresses the structural problem: the model does exactly what its objective tells it to do, the objective is set by whoever holds the control surface, and no layer in the stack asks whether the environment should host this conversion of capability into action at all.

The streetlight is the whole argument. You can search under it forever, with the best instruments anyone has built, and you will not find the keys if the keys are one layer up.

That claim has stopped being only mine. In 2025 a Microsoft team published FIDES (arXiv:2505.23643), a narrower version of the same move. It stops prompt injection not by hardening the model but by gating an agent’s consequential actions above the model — and it proves the result: a non-interference guarantee for integrity, meaning attacker-controlled input cannot trigger a consequential action no matter how persuasive the prompt. The guarantee is narrower than A ≤ E. It checks the integrity of the data behind an action, not the environment’s capacity to bear it. It carries no trust trajectory, no environmental capacity, none of the runtime refusal behavior the next piece describes. But it validates the layer. The failure the model layer cannot catch gets caught one layer up, deterministically, at the control plane.

Alignment work continues. It is necessary. It is not sufficient. The next layer is where the law lives.

## Where the law lives in your stack

If you build identity and access systems, you already have the vocabulary for this, and the subtitle’s claim resolves cleanly into it.

The authorization gateway that evaluates A ≤ E is a Policy Enforcement Point: the choke point a request passes through before any downstream surface executes it. A and E are Policy Information inputs — the two quantities the engine reads to decide. The comparison itself is the Policy Decision. Nothing in that mapping is exotic. The architecture pattern is forty years old.

What is not standard is the status of the rule. A ≤ E is not another discretionary policy rule; it is the invariant the policy engine must enforce before intelligence becomes action. A discretionary rule is one a sufficiently privileged operator can waive. The invariant is not. It binds the same way ampacity binds — it is a property of the substrate, not a setting in a console.

Attribute-based access control and risk-based access already give you most of the machinery to compute something like this. They evaluate attributes. They score risk against context. They gate accordingly. The difference is what the machinery is made to serve. ABAC and risk-based access are mechanisms. A ≤ E is the invariant they can be made to serve. Today they serve discretionary policy set by whoever administers the engine. The Zeroth Law asks them to serve a constraint the administrator is also subject to.

## What comes next…

This piece had one job: state the law and name the layer. A ≤ E, enforced at the control plane, asked one layer above the model, about the environment an action would land in.

Two things follow. Part 2 takes up runtime — what the gateway actually does the instant A exceeds E, and why the most counterintuitive choice in the protocol is to do it in silence. Part 3 covers where the law is made to hold: in bounded environments that bind their own operators rather than exempt them. How “environmental trust capacity” becomes an actual reading — with its uncertainty stated honestly — is a measurement question this essay deliberately leaves open.

The law is the easy part to state and the hard part to honor. Stating it is this essay’s whole job. Honoring it — at runtime, and in a place that binds its own operator — is the next two.

Part 2
