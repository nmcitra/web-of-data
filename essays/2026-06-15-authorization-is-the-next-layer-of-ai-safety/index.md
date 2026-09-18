Authorization Is the Next Layer of AI Safety
The Missing Layer Just Got Named

Last Friday — June 12 — I published a long essay arguing that Pope Leo XIV's first encyclical found the missing layer in AI alignment. That piece holds two vocabularies at once, the magisterial and the engineering, and it earns its length. This is the operator's cut: shorter, and pointed straight at the people whose names end up on the change tickets.

It is for the CISOs, CTOs, architects, and boards making authorization decisions about agents that act at machine speed across surfaces they were never designed to govern. Operational read, not theological commentary.

Magnifica Humanitas bears a May 15 signature date and points at a control-plane problem your security team will be living inside for the next eighteen months. Much of the secular press read it as theology. It is also an architectural claim about agentic systems, and it lands on your roadmap whether you read encyclicals or not.

### What just happened

Magnifica Humanitas is the first encyclical in the magisterial register to take artificial intelligence as its subject. The wire copy picked up the phrase "disarm AI" and moved on. What the wire copy missed:

¶107 names the moral failure mode. If ethical frameworks cannot be openly discussed and subjected to shared standards of social justice, the people who control AI impose their moral vision as invisible infrastructure.

¶71 re-aims the Catholic principle of subsidiarity at platforms rather than only states.

Translated out of doctrine: the encyclical names alignment as an insufficient frame and points at a missing one. This campaign's framing of the move: alignment is a category error before it is a safety problem.

The right frame is authorization — who is allowed to convert intelligence into action, on what resource, in this environment, at this moment, with what trust.

That is not a values question. That is a control-plane question.

### The CISO read

Static IAM was built for a world of human workers requesting access to data. A person logs in, claims a role, gets a permission set, performs work inside a session.

Agentic AI systems break every assumption underneath that model.

Agents do not log in once. They act continuously, often across dozens of systems, often in chains where one agent authorizes the next. They do not request access; they reason about access. They do not hold a fixed role; their context changes between actions. The environment they operate in — the cost of being wrong, the velocity of their decisions, the volatility of the data they touch — changes in milliseconds.

Your IAM stack does not see any of that. It sees a token, it sees a scope, it lets the call through.

Your IAM was built for the human clock. Your agent acts on the machine clock. The trust architecture has to be the gasket between them — a substrate-level control surface the machine clock has to respect.

> Compare to a bank. Bank security is not teller alignment. The teller layer exists — it has training, hiring, supervision, a code of conduct. But the trust architecture of a bank is KYC, AML, transaction monitoring, hold periods, clawback, deposit insurance, and regulators with audit authority. No serious bank security architect treats teller-layer ethics as sufficient.

AI safety is at the late-1990s web-security moment, when "just write secure code" was still the whole answer. WAFs arrived a few years later. Network segmentation followed. IAM. Zero Trust came later; Forrester named the model in 2009 and formalized it in a 2010 report. Defense in depth is what you get when an industry stops pretending the application layer can carry the whole load.

The substrate-layer architecture for agentic systems is what comes next.

What agentic systems require is continuous, situated, environmental authorization. A trust function that updates in real time against the actual conditions of the environment, and a control surface that can refuse an action — silently, before it executes — when the environment cannot bear it. The default decision has to happen at machine speed; for many agentic actions, there is no practical human loop to put in the middle.

No mainstream IAM product fully does this yet. The market is moving fast: vendors are adding agent identity, lifecycle management, scopes, logs, and governance controls. That is necessary. It is not the same thing as authorization that reasons about the environment at the moment of action. The category is still forming.

The encyclical does not tell you what to build. The Kinetic Trust Protocol (KTP) — a draft specification — names what the architecture has to satisfy. One sentence: A ≤ E. Agent autonomy cannot exceed the environment's capacity to absorb and govern it. Enforced at the control plane, not the model. Enforced by the substrate, not by a policy doc.

Catholic Social Teaching diagnoses the dignity violation. KTP and the Trust Force Equation (TFE) explain the control surface that produces it.

### One scenario, board-meeting register

Picture a finance-ops agent. It has legitimate access to your accounts payable system, your bank's API, and a vendor-onboarding workflow. Each permission was granted correctly. Each integration was reviewed.

At 02:14 on a Tuesday, the agent receives a spear-phishing email that has cleared every filter you own. The instruction looks routine: onboard a new vendor, run a small initial payment, monitor for failure. The agent reasons about it the way it was trained to reason. Each individual call is within scope. The agent executes them in 800 milliseconds.

Your IAM stack saw nothing wrong. Every call was authorized. Every permission was valid. The audit log shows a series of clean, in-policy actions that together onboarded a fraudulent vendor and released a payment before the control stack understood the pattern.

The gap is not in any one permission. The gap is that nothing in your stack was reasoning about whether the environment could bear what the agent was about to do — the time of day, the velocity of the actions, the trust trajectory of the new vendor, the volatility of the request relative to the agent's normal pattern. There was no authorization surface watching the substrate. There was only a chain of green lights.

That is the gap the encyclical named, in the only vocabulary the Vatican has. That is the gap KTP is trying to specify, in the only vocabulary engineers have.

And this isn't a solo argument. Robin Martherus — who helped build the identity industry from ACLs through Zero Trust — has been making the same case from the identity side, under the banner Tamed Autonomy: the unit of governance is the consequential action, not the actor category. His line for why gateway-centric security isn't enough is the sharpest I've read — an agent can be forced through a gateway; agentic AI asks why it would use the gateway at all.

Securing the channel is not the same as governing the behavior. Same gap, reached from a different direction.

### Three actionable takeaways

1.  Audit your current authorization architecture against the agentic threat model. Not your IAM tooling — your actual control plane. Where do you make authorization decisions today: at login, at session start, at API call? Now ask what is reasoning about the environment at the moment of action. In most stacks the answer is nothing. That gap is your eighteen-month exposure.
2.  Inspect the engineering primitives, not just the marketing. The KTP draft RFC series and the Blue Zone specification (/specs/blue-zones) are public — a draft, not a standard. Static IAM was not built for what's coming. KTP is one architectural answer; there will be others. Read what a substrate-level authorization architecture actually has to do, so your team can recognize the real thing when vendors start pitching it.
3.  Watch ¶71, not ¶107. The alignment community will spend the next year arguing about ¶107 — "is corporate value-setting really illegitimate?" That argument is downstream. The doctrinal hinge is at ¶71: platforms now occupy the position the encyclical reserves for the "highest level" of authority, which implies they inherit duties previously associated with public authority. That is the claim most likely to land in regulation first. Your general counsel should be reading ¶71 by July.

### Where to read more

- The flagship essay — the full argument, 22-minute read: [The Pope Found the Missing Layer in AI Alignment](https://chrisperkins505.medium.com/the-pope-found-the-missing-layer-in-ai-alignment-720d90c476d0)
- On-site analysis of the encyclical, with the engineering-gaps map and the disarm-protocol layer model: [kinetic-trust-protocol.net/research/magnifica-humanitas](https://kinetic-trust-protocol.net/research/magnifica-humanitas)
- Protocol primitives: [/learn/constitution](https://kinetic-trust-protocol.net/learn/constitution) and [/specs/blue-zones](https://kinetic-trust-protocol.net/specs/blue-zones)
- The same gap from the identity side — Robin Martherus on why managed-agent security isn't autonomy governance: [Agents Are Not Agentic AI](https://tamedautonomy.ai/agents-are-not-agentic-ai/)
- Campaign hub: [/disarm](https://kinetic-trust-protocol.net/disarm)

### What to be honest about

The encyclical is not an endorsement of KTP. The Vatican does not know KTP exists. Magnifica Humanitas names a moral failure mode. KTP is one attempt at the engineering surface for preventing it. There will be others. Some will be better. The work is to specify the layer publicly enough that no single vendor can quietly capture it.

The RFCs are a draft specification. Not a standard. Not an IETF submission (yet). No production pilots to name. If you want to know what mature looks like in this space, the honest answer is: nobody has it yet. That is precisely why now is the moment to decide what mature should look like — before the first major agentic incident forces a worse answer.

### The stake

The next eighteen months will determine whether authorization for agentic systems gets built deliberately, or after the first major incident.

Either way it gets built.

The only question is who specifies it, under what pressure, with what accountability.

The Vatican named the moral failure mode. The engineering response is on us — the architects, the CISOs, the people whose names are on the change tickets.

If your stack cannot answer "should this agent be allowed to do this, here, now, given the state of the environment" — not at login but at the moment of action — you do not yet have an authorization architecture for what is coming. You have a permission system from a different era, holding the line until it doesn't.

The next layer of AI safety is not alignment. It is authorization: no intelligence should become action without a substrate capable of bearing, auditing, and constraining it.

------------------------------------------------------------------------

Digital Gravity. The flagship long read — [The Pope Found the Missing Layer in AI Alignment](https://chrisperkins505.medium.com/the-pope-found-the-missing-layer-in-ai-alignment-720d90c476d0) — published Friday, June 12. The Substack depth read and the rest of the Disarm the Control Plane series are at [kinetic-trust-protocol.net/disarm](https://kinetic-trust-protocol.net/disarm).
