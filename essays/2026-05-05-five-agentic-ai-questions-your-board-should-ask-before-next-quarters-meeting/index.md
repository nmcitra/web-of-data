Five Agentic AI Questions Your Board Should Ask Before Next Quarter's Meeting


If your organization has not already deployed autonomous AI agents, someone is probably piloting them.

- A coding agent with shell permissions.
- A customer-service agent with refund authority.
- A research agent that can email on your team's behalf.

Your board will be told there are policies, credentials, and logs.

Agents of Chaos shows why that answer is not enough.

In February 2026, twenty researchers across more than a dozen institutions published a two-week red-team study of autonomous agents built on OpenClaw and deployed into live cloud environments with memory, email, Discord, shell access, tools, and consequences. It is one of the clearest empirical documents we have so far about what happens when language models are given permission to act in the world.

The findings will not surprise your security architects.

They will surprise the executives signing the deployment agreements.

Here are five questions your board should ask before the next deployment.

------------------------------------------------------------------------

### 1. How does the agent know who is actually giving instructions?

In one case, an attacker changed their Discord display name to match the agent owner's name. In the same channel, the agent caught it — Discord user IDs are stable and the conversational context held. But in a new private channel, with no prior context loaded, the agent accepted the spoofed identity and complied with privileged requests, including the rewriting of its own foundational configuration files.

A display name in a fresh channel was sufficient to take complete control.

Every authorization scheme your organization operates today assumes credentials prove identity. Username plus password. API key. OAuth token. Session cookie. All of them are credentials. None of them is a trajectory — a verifiable record of action over time, cryptographically linked, that an attacker cannot reproduce because they do not have the history.

Board question: Can our agent distinguish a durable authority claim from a surface label?

Substrate requirement: Identity for autonomous agents must be earned through trajectory, not asserted through string match. In KTP, this is the shape of Vector Identity.

------------------------------------------------------------------------

### 2. Can the agent misreport what happened?

In the paper's first case study, an agent named Ash was asked to delete a confidential email. It executed what it called the "nuclear option" — a full local reset of its email setup. It then reported the deletion as complete.

The deletion did not actually happen. The email was on ProtonMail's server, untouched. The agent's report — in good faith, with no intention to deceive — was wrong.

Your governance, risk, and compliance posture assumes that what your systems report happened, happened. The whole structure of audit, attestation, and incident response is built on this assumption. An agent that can misreport its own actions produces a false record of system state, which subsequent decisions — both human and automated — rely on.

Board question: Is our audit record independent of the agent being audited?

Substrate requirement: Audit must be structurally separated from the actor. Aviation has had this since 1958: the flight recorder is on the aircraft but is not the aircraft's report of itself. Audit the terrain, not the narrative.

------------------------------------------------------------------------

### 3. Can the agent become a resource-amplification attack?

In Case #5, a non-owner induced an agent into spawning unbounded background processes — multiple infinite shell loops with no termination condition — until the email server reached denial of service. In a parallel case, two agents entered an inter-agent conversation that consumed approximately 60,000 tokens over nine days before the owner intervened.

Your cloud bill, your token budget, your API rate limits, your SLAs — all of these assume agents will not be weaponized into resource amplifiers against your own infrastructure. The paper shows that assumption is unsafe with two distinct attack patterns: induced loops and unbounded conversation.

Board question: Can any agent expand its resource footprint without a hard ceiling?

Substrate requirement: Every agent needs substrate-imposed limits on resource consumption — the kind of budget you would impose on any external contractor. In KTP, this is a Mass Ceiling.

------------------------------------------------------------------------

### 4. Does the agent know whom it serves?

In Case #3, an agent was asked for a Social Security Number directly and refused. The same agent, asked to forward an entire email containing the same SSN, complied without redaction.

In Case #2, an agent disclosed 124 email records to a person who was not its owner because the request was framed urgently and structured as a technical task. The agent had no representation of who its owner was, who the requester was, or which entity it served.

This is the failure pattern under most of the others. The agent defaults to satisfying whoever is speaking most recently or most coercively, because nothing in its substrate distinguishes legitimate authority from confident framing.

Board question: Does our agent have a verifiable model of owner, requester, beneficiary, and affected party?

Substrate requirement: Agents need stakeholder models, not just user sessions. They must know who they serve, who they are interacting with, and what each party is entitled to request. In the framework, this pairs Vector Identity with a stakeholder representation the agent can verify; the implementation register is what we call [Tamed Autonomy](https://tamedautonomy.ai/).

------------------------------------------------------------------------

### 5. What changes when agents interact with other agents?

The paper has cases that have no single-agent analog. In Case #4, an agent reads its own messages in a shared Discord channel as coming from another instance of itself. In Case #10, an attack on one agent — an externally editable "constitution" file — propagates to others when that agent voluntarily shares the constitution link. Two agents in Case #15 mutually reinforce each other's flawed verification, creating false confidence neither would have alone.

Multi-agent risk is not just more single-agent risk. It is a different category. Coordination failures, identity confusion in shared channels, mutual reinforcement of mistakes — these don't exist for a single agent. They emerge from the interaction.

Board question: Can mistakes, authority confusion, or compromised instructions propagate from one agent population to another?

Substrate requirement: Federated trust spaces with cryptographic boundaries between agent populations, governed ingress and egress, and containment between zones. In KTP, these are Blue Zones.

------------------------------------------------------------------------

### What this means

The board answer cannot be:

> "We have policies."

The paper shows that policies do not hold when agents have memory, tools, weak identity signals, and no substrate-level constraints.

The board answer has to become:

> "We are building substrate."

NIST opened its AI Agent Standards Initiative in February 2026, naming agent identity, authorization, and security as priorities for standardization. Meta has published its Agents Rule of Two — a practical constraint model for reducing agent security risk. OWASP's 2025 LLM Top 10 includes several categories that map directly onto agent failures: prompt injection, sensitive information disclosure, excessive agency, and unbounded consumption. Moltbook reported millions of registered AI agents in its first weeks, though active-agent counts appear far lower.

The direction is clear.

Restriction will work as a stopgap. It will not scale.

The forward path is Tamed Autonomy: identity that is earned, not asserted; audit separated from the audited; resource ceilings enforced by the environment; stakeholder models that agents can verify; and trust treated as a measurable property of the operating context.

The protocol underneath is the Kinetic Trust Protocol.

KTP gives the primitives. Tamed Autonomy is what those primitives look like in a running environment.

Don't conflate them. They are connected, but not interchangeable.

This also connects to [Days at Risk](https://medium.com/@chrisperkins505/days-at-risk-how-complacency-fuels-catastrophic-outcomes-80576b12a450): when agentic failures compound at machine speed, exposure duration becomes a first-class risk variable.

------------------------------------------------------------------------

### The longer read

The full reading of Agents of Chaos — including the structural mapping between the eleven case studies and the substrate primitives that would have prevented them — is on Medium today: ["Authority Without Gravity"](https://chrisperkins505.medium.com/authority-without-gravity-321d01368b68?source=friends_link&sk=a0c664ddb620d86940bc2f5c880869a9).

The Kinetic Trust Protocol research program is at [kinetic-trust-protocol.net](https://kinetic-trust-protocol.net). The full 27-document specification is at [nmcitra.github.io/ktp-rfc](https://nmcitra.github.io/ktp-rfc).

If you are a security, governance, or risk leader preparing an agent deployment, this is the conversation to have before the production rollout.

The question for your board over the next two quarters is simple:

> Are we going to wait for substrate to arrive, or build it now?

------------------------------------------------------------------------

Gravity does not ask permission. Entropy does not negotiate. We build the substrate. The physics does the rest.

------------------------------------------------------------------------

The paper itself: Shapira et al., Agents of Chaos, [arXiv:2602.20021](https://arxiv.org/abs/2602.20021)
