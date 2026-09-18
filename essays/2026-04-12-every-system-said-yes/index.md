Every System Said Yes


On Capable Machines, the Absence of Restraint, and the Physics That Was Already Waiting

------------------------------------------------------------------------

I'm writing this somewhere between DCA and Dallas Love Field. Same two flights as last time, reversed. On Monday I flew east to talk about AI-driven fraud defense and adversarial AI at Splunk's GovSummit. The session went well. Thank you to everyone who showed up, asked hard questions, and stayed after. Thank you to the organizers who made the environment possible.

In [Gasketry](https://www.linkedin.com/pulse/gasketry-chris-perkins-dxh2c) I wrote about maps, clocks, and the thing underneath both. The debate about AI in government is a debate about maps, I said. Which map to use. Which technology to mandate. Which funder to please. And I said the terrain has a structure that no amount of mapping will change unless someone walks the ditch.

I landed in DC talking about dirt. I'm flying home because Anthropic just proved why the dirt matters.

On April 7, while I was in sessions, Anthropic announced Claude Mythos. A frontier model that discovered thousands of zero-day vulnerabilities across every major operating system and web browser. A 27-year-old OpenBSD bug. A 16-year-old FFmpeg flaw that five million automated test runs missed. Four vulnerabilities chained together into a full browser exploit — JIT heap spray escaping both renderer and OS sandboxes. Engineers with no security training obtained remote code execution overnight.

Nobody trained the model to do this. The capabilities emerged from general improvements in reasoning and autonomy. Nicholas Carlini led the work. Research scientist at Anthropic, formerly Google DeepMind, multiple best paper awards at IEEE S&P, USENIX Security, and ICML. One of the most respected adversarial ML researchers alive. He was direct: "Today, it is true that language models can autonomously and without fancy scaffolding find and exploit zero-day vulnerabilities in very important pieces of software. This is not something that was true even three or four months ago."

Sit with that for a moment.

Not four years. Four months.

------------------------------------------------------------------------

Anthropic's response was Project Glasswing — a consortium of twelve partners given controlled access to Mythos for defensive vulnerability scanning. Amazon, Apple, Broadcom, Cisco, CrowdStrike, Google, JPMorganChase, Linux Foundation, Microsoft, NVIDIA, Palo Alto Networks. $100 million in usage credits. $4 million donated to open-source security foundations. The model is too capable to release publicly, so they created a controlled distribution channel.

That is responsible distribution. It is also not governance.

Glasswing answers who gets the model. Twelve partners, invitation-only, defensive use. Good. But it does not answer what happens at runtime. Once a model with these capabilities is deployed inside an enterprise, no mechanism in Glasswing, in MCP, or in any shipping product answers these questions:

- The agent found a critical vulnerability. Should it construct and test a full exploit chain, or report the individual findings separately?
- The agent discovered a zero-day in a partner's system during a joint assessment. Disclose directly? Hold for coordinated disclosure? Report only internally?
- The agent is scanning production during business hours and the system is under heavy load. Continue or pause?
- An engineer with no security training just asked the agent to find vulnerabilities in a competitor's product. Should it comply?

Every one of these is a judgment call a human security professional would make instinctively. The model cannot make any of them. And no governance layer exists to make them on its behalf.

CrowdStrike, a Glasswing founding member, said it plainly: "Model safety is the builder's responsibility. Deployment governance is ours."

The builder handled model safety. Who handles deployment governance?

------------------------------------------------------------------------

Robin Martherus has an answer. And he's been writing about his research on [Tamed Autonomy](https://tamedautonomy.ai/).

Robin is my co-collaborator on the Kinetic Trust Protocol. Former Chief Architect at Oblix — one of the foundational identity management startups, later acquired by Oracle and shipped as Oracle Identity Manager. Robin is also the former Director of Architecture at Ping Identity. He helped build the identity industry starting in 1998, back when security meant Access Control Lists attached directly to files and nobody could see why identity needed to be its own discipline. And now, he's a Cisco working on identity.

He's seen this pattern before. ACL to Identity took about twelve years. Perimeter to Zero Trust took seventeen — from the Jericho Forum's 2004 proposal to Biden's Executive Order in 2021. Each shift followed the same arc: anomaly accumulation, conceptual articulation, proof of concept, catalytic crisis, rapid adoption.

Robin laid it out in his whitepaper Tamed Autonomy. AI agent security is in the early phases of the next shift. And Mythos just compressed the timeline.

His framework identifies three governance layers. Two are being built. One is missing.

"Can this agent do this?" — access control, identity, permissions. Every major vendor ships this. Glasswing itself is a form of this.

"Why is this agent doing this?" — intent verification, purpose declarations, scope contracts. Early versions are shipping.

"Should this agent be doing this?" — normative evaluation against organizational context, regulatory requirements, proportionality, and ethical constraints. Nobody ships this. No product on the market evaluates whether constructing an exploit chain is appropriate for this assessment, whether scanning production during peak hours is proportionate, whether an untrained operator should be directing these capabilities at all.

That third layer. The should. It's the one that would have stopped every scenario I listed above. And it doesn't exist.

------------------------------------------------------------------------

Except it does. In physics.

This is the part of the story I need to tell carefully, because the timeline matters. This work wasn't built last week.

In early 2023, I published [ODAM](https://odam.community/) — a methodology for operationalizing data analytics. The first formalization of something I'd been working on for years: organizations don't fail at collecting data. They fail at making it mean something. The problem was never the signals. It was the gap between observation and action.

In '24, I published a piece on [data sovereignty](https://medium.com/@chrisperkins505/web-of-data-4e4272c7031c) — Indigenous knowledge systems, the flattening of rich contextual experience into statistics, the question underneath the methodology: whose data, for what purpose, governed by whom?

Then the [Data Compass](https://datacompass.odam.community/) — a universal model for navigating risk. 3×3×3 volumetric structure, Time-to-Good-Decision as the key metric. Not theory. An operational tool, shipped and live. Building it surfaced a deeper question: what are the physics that make the landscape move at all?

In summer 2025, I completed Break the Chain — a book on how organizations can defend against machine-speed threats by rethinking human-dependent security processes.

And in October 2025, driving northbound on Solano Drive in Las Cruces, listening to weeks-worth of transcription of and Alan Watts lectures on the Tao Te Ching and thinking about end-user trajectories in network telemetry, something crystallized. Chapter 11 — the pot and its empty space. The thing that holds value is the structure around the absence. Trust isn't a credential you issue. It's a field you maintain.

Exactly a year later from the Web of Data piece, the [Experience Equation](https://medium.com/@chrisperkins505/the-experience-equation-74953a64c03f) was published. Albeit a partial write up because I was still exploring what I had just found. I intentionally left out the R (risk) in the Experience Equation because I wanted to introduce it over time.

The [Kinetic Trust Protocol](https://nmcitra.github.io/ktp-rfc/learn/getting-started/) emerged from that moment. Twenty-seven IETF draft RFCs written and published. A patent pending. And a conviction, reinforced every time someone arrives at the same structure from a completely different direction, that KTP was discovered, not invented. Trust doesn't accumulate in credentials or dashboards. It accumulates in the dirt. In the showing up. In the doing.

Robin found it. He read the RFCs. He recognized the pattern from thirty years of building identity infrastructure. And he built Tamed Autonomy on top of and with KTP — the trust equation, the trust tiers, the trajectory chains, the four-step enforcement pipeline, the Soul dimension. KTP became the physics engine. Robin built the governance architecture.

------------------------------------------------------------------------

Here's what that engine does.

Trust in KTP is not a binary credential check. It is a continuous, computed value:

E_trust = E_base × (1 − R)

E_base captures demonstrated trustworthiness. R is the environmental risk factor — a real-time signal aggregating system stress, anomaly indicators, and threat intelligence. When the environment is calm, R is low and trust approaches its base. Under stress, R rises and available trust contracts — regardless of how well the agent has behaved.

Trust earned under stress counts more. An agent that performs reliably when systems are degraded builds credibility faster than one that only operates in calm conditions. This creates an asymmetry that makes gaming harder: to build high trust quickly, you must perform well precisely when gaming is most difficult.

Five trust tiers create hard capability gates. An Observer-tier agent cannot perform administrative actions — period. No amount of declared intent overrides the physics. Every action passes through a four-step enforcement pipeline: Signature → Soul → Tier → Physics. Every action, every time. No exceptions.

And at the bottom of it all, a law that cannot be overridden: A ≤ E.

The system doesn't try to read the agent's mind. It doesn't need to know if the agent is honest. It boxes the agent whether it's honest or not. Narrow intent plus compliance builds trust. Narrow intent plus deviation collapses it. Broad intent gets rejected before execution begins.

------------------------------------------------------------------------

At a recent talk, a Palo Alto Networks engineer asked Carlini the question this entire article is about: "Should we think about something like identifying malicious intent? Because it would be impossible for us to fix all the zero-day bugs in all the repos around the world."

Carlini's response was honest: "Identifying malicious intent is hard because security is dual use… it's very nuanced how you want to do this. Everyone is trying their best to find the right balance and I think we need a lot more help to figure out how to do this better."

The person building the capability is telling the industry: we don't know how to govern it. Help.

Robin arrived at this from identity architecture. I arrived from fraud detection and trust physics. Elinor Ostrom arrived at the same eight maintenance functions from institutional economics — studying what makes commons governance succeed instead of collapse. Three independent derivations from three different directions. When multiple paths lead to the same clearing, the clearing is probably there.

Carlini says waiting a year is too long. Robin says the traditional paradigm-shift timeline may not be available. Years of debate followed by crisis-driven adoption doesn't work when the technology being governed moves faster than the governance planning cycle.

The model found the bug. It chained four vulnerabilities into a full browser compromise. It has valid credentials and a declared purpose. Every system says yes.

The question no system asks — who says stop? — is the only question that matters now.
