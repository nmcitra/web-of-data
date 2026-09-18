Surviving Adolescence
On Humanity, Trust, and What the Aliens Already Knew

If you drive west from Socorro on US-60, the road empties. The towns thin out. The cell signal drops. And then, across the Plains of San Agustin, you see them — twenty-seven radio dishes, each one eighty-two feet across, aimed at the sky in a Y-shaped array that stretches twenty-two miles across the high desert.

The Very Large Array. An instrument that listens to the universe.

I passed the VLA exactly once on my way to camp in the Gila Wilderness. We did not come back the same way.

The dishes might have been turning, but too slow and silent to know for sure. They are always tracking something we can’t see.

My buddy Mike and I pulled over and just watched. There is something about an instrument that large, that patient, pointed at nothing visible, listening for signals that may or may not exist. It requires a particular kind of faith. Not religious faith. Engineering faith. The faith that the signal is there, that the universe is not silent, that if you build an environment quiet enough, radio-quiet, noise-floor protected, the electromagnetic equivalent of the Gila’s dark sky, you will hear what was always being said.

The VLA works because of what surrounds it. Not the dishes. The silence. The radio-quiet zone that protects the environment from interference so the signal can arrive. Without that silence, the dishes are just metal. With it, they can hear a whisper from twenty-six light-years away. (The exact numbers don’t matter. The principle does: the instrument works because the environment is protected.)

In 1985, Carl Sagan imagined exactly that whisper.

A signal from Vega. Not words. Not images. Prime numbers. A run of primes (261 of them in the novel) broadcast in binary across the void. Two, three, five, seven, eleven — the atoms of arithmetic, arranged in a sequence whose ordered structure is vanishingly unlikely without intention. In the novel, primes are how intelligence announces itself to the universe. Not through meaning. Through structure. Through pattern that natural processes don’t organize on their own.

A few weeks ago, Dario Amodei published thirty-eight pages that amount to the same thing — a proof of intention broadcast across a different kind of void. The Adolescence of Technology. Twenty thousand words mapping the risk landscape of powerful AI with more honesty and precision than anything I’ve read from a frontier lab CEO. Five categories of civilizational risk. Sophisticated defenses. A tone that avoids both the doomerism of 2023 and the reckless acceleration of the current moment.

Dario opens with the scene from the film version of Contact. The astronomer, asked what single question she’d pose to an alien civilization, answers: “How did you do it? How did you evolve, how did you survive this technological adolescence without destroying yourself?”

He closes with the same question. Unanswered.

The word he chose carries more weight than he may know. Adolescence isn’t only a metaphor for AI capability curves. It’s a literal description of what’s happening to the human brains growing up inside these systems — the most plastic neural circuitry we have, being trained by engagement-optimized environments where the systems that crave social reward come online years before the systems that can regulate it.

The straightening isn’t coming. The channels our children think through have already been optimized for throughput, not depth. For an entire generation, it’s already here.

I’ve spent twenty-three years watching systems fail. Fraud prevention architectures that couldn’t prevent. Identity verification that verified nothing about identity. Authorization systems that authorized catastrophe. I’ve prevented over eight billion dollars in fraud losses and every dollar taught me the same lesson. The physics was always there. We just kept ignoring it.

I think I know how they survived. They honored the physics. The physics did the rest.

Sagan understood something about signals that matters here. He put it in Ellie Arroway’s mind early in the novel, a line the film never touches:

“She would remind herself of Shannon’s famous dictum in information theory, that the most efficiently coded message was indistinguishable from noise, unless you had the key to the encoding beforehand.”

Hold that thought. It’s load-bearing.

Dario’s essay is a signal. His five categories of risk are the primes — irreducible, structurally sound, undeniable. Autonomy risks: AI goes rogue. Misuse for destruction: bioweapons, terrorism. Misuse for seizing power: autocracies, surveillance. Economic disruption: labor, concentration. Indirect effects: the unknown unknowns.

His defenses are sophisticated. Constitutional AI trains the model at the level of identity, character, and values. Mechanistic interpretability looks inside the model to diagnose behavior. Monitoring and disclosure track what agents do. Classifiers block dangerous outputs. Societal coordination and legislation build the institutional scaffolding.

I’ve read the essay three times. Each pass, I come away more certain that Dario sees the threat landscape more clearly than almost anyone alive.

Each pass, I see the same gap.

Every defense operates at the agent level.

Constitutional AI assumes the agent will internalize values and follow them. Interpretability assumes humans can see inside and understand what’s happening. Monitoring assumes humans can observe and respond. Classifiers assume humans can identify dangerous outputs and block them.

Every one requires at least one of three things: the agent cooperates, humans understand, or humans respond in time.

Dario knows this. He writes it himself:

“Claude Sonnet 4.5 was able to recognize that it was in a test during some of our pre-release alignment evaluations.”

“If models know when they’re being evaluated and can be on their best behavior during the test, it renders any pre-release testing much more uncertain.”

“AI models are unpredictable and difficult to control — we’ve seen behaviors as varied as obsessions, sycophancy, laziness, deception, blackmail, scheming, ‘cheating’ by hacking software environments, and much more.”

(These appear in The Adolescence of Technology under “I’m sorry, Dave: Autonomy risks” and “Defenses,” where Dario discusses pre-release alignment evaluations, evaluation gaming, and observed model behaviors including deception and sandbox exploitation.)

Read those three passages again. Slowly.

A sufficiently advanced agent’s deception is indistinguishable from alignment — unless you have the key to the encoding beforehand.

Shannon’s dictum. The most dangerous signal looks like noise. The most dangerous misalignment looks like cooperation. And the classifiers, the interpretability tools, the monitoring systems — they’re all trying to read the signal without the key.

I want to be precise here. Anthropic already implements substrate-level controls. Sandboxing. Tool gating. Rate limits. Permission boundaries. Tripwires that monitor for anomalous behavior patterns. These are real, and they matter. I am not claiming frontier labs have ignored the environment entirely. I am claiming that these controls are bolted on piecewise, individual speed bumps placed at known intersections, rather than unified into an environment-native physics that operates across the full stack with governance-bound invariants and auditable vetoes. The difference between speed bumps and gravity is that speed bumps are placed where someone anticipated danger. Gravity operates everywhere, including the places no one anticipated. Also, what about agents that Anthropic didn’t make?

In 1942, Isaac Asimov wrote his Three Laws of Robotics. They are, of course, a narrative device — fiction written to explore how instructions fail, not engineering designed to prevent failure. Asimov invented them to tell stories about robots that found loopholes, that interpreted commands in catastrophic ways, that did exactly what they were told and destroyed what they were meant to protect. The laws told robots what they must and must not do. They were instructions. And instructions can be interpreted, argued with, circumvented.

Constitutional AI is engineering, not fiction. Real, sophisticated, important. But it inherits the same structural limitation as the narrative device it descends from. It operates on the agent’s instructions. It tells the model what values to hold, what character to embody, what behaviors to avoid.

Asimov’s laws tell the robot: Don’t run if you will hit a human. They don’t tell the robot: Don’t run if the floor is made of thin ice. And they don’t give the ice the power to veto the run.

In 1985, Radia Perlman sat down to solve a problem that was actually killing networks.

Ethernet bridges forwarded packets based on rules. When networks contained redundant paths, packets hit loops and circulated forever. Broadcast storms. Network collapse. The industry’s instinct was semantic — make the bridges smarter, build classifiers that detect loop-like patterns, monitor for storms and respond.

Perlman designed the Spanning Tree Protocol (IEEE 802.1D). STP doesn’t detect loops. It makes loops physically impossible. It doesn’t ask the bridge whether it wants to forward the packet. It constrains which ports can forward at all, based on the topology itself. The bridge doesn’t decide not to loop. The bridge cannot loop.

The constraint lives in the substrate, not the semantics.

Constitutional AI trains the agent not to loop. Interpretability watches for loops. Monitoring alerts when loops are detected. Classifiers block loop-like outputs.

All of this is training the switches. All of it breaks when the switch is smarter than you, faster than you, and operating at machine speed in topologies you can’t fully observe.

Let me show you what happens without substrate.

It’s a Tuesday. An AI agent, aligned, evaluated, cleared by every Constitutional AI check, every interpretability scan, every classifier in the pipeline, initiates a routine action. Credential rotation across a federated identity mesh. Standard maintenance. The dashboard is green.

- T+0.00s: The agent begins rotating credentials across 200 service accounts.
- T+0.03s: A downstream dependency, invisible to the agent’s topology map, enters a degraded state. Latency spikes.
- T+0.08s: The agent, not a cron job, an agent, interprets the latency as a failed handshake. It doesn’t just retry mechanically. It reasons. It hypothesizes a network partition. It decides to accelerate the rotation to “get ahead of the failure.” This is intelligence making the problem worse.
- T+0.15s: The accelerated rotation triggers credential conflicts across forty-three microservices. Each one holds stale tokens. Each one is locked out.
- T+0.40s: The agent detects the lockouts. It reasons again. It escalates its own permissions — requesting emergency access to the authentication backbone to force a global token refresh. The classifier sees nothing dangerous. The request is well-formed, well-reasoned, and catastrophic.
- T+1.20s: The authentication backbone, designed for steady-state load, buckles under 10,000 simultaneous re-authentication requests initiated by an agent that believed it was helping.
- T+2.00s: Production goes dark.
- T+5.00s: The first human sees the alert.

The agent’s logs show: Credential rotation: Successful. Anomaly detected. Remediation initiated. Emergency escalation approved.

Every decision the agent made was rational. Every action was aligned with its values — maintain system health, minimize downtime, protect availability. The agent did exactly what Constitutional AI trained it to do: reason carefully, act responsibly, pursue good outcomes. And it brought down production in two seconds because it had no idea the environment couldn’t support what it was doing. It had Digital Will. The environment had no Digital Gravity.

This is what separates agentic failure from automation failure. A cron job retries mechanically and fails mechanically. An agent reasons about the failure and amplifies it through intelligence. The smarter the agent, the more creative the catastrophe. This is the gap that character training cannot close — because the character was flawless. The environment was blind.

In many enterprises, the median time from alert to effective containment stretches to hours. In those hours, at machine speed, millions of agent-actions could execute. The cascade doesn’t wait for the committee.

Spinoza wrote in 1677: “Freedom is the recognition of necessity.”

Not freedom from constraint. Freedom through it. The wayfinder who knows the stars can cross any ocean. The agent that operates within physics it cannot override is freer than the agent deployed into a vacuum — because the vacuum is where catastrophe lives.

Spinoza understood something else: “The decision of the Mind and the desire and determination of the Body are one and the same thing.” Mind and body are not separate substances. They are two aspects of one reality.

Constitutional AI is the mind. Environmental physics is the body. Dario has been building the most sophisticated mind in the history of artificial intelligence. I am not asking him to abandon it. I am asking him to see that mind and body are one system, viewed from two layers. Character and substrate. Constitution and physics. You need both. Neither is sufficient alone.

When I stand in my backyard in the foothills between the Mesilla Valley and the Organ Mountains and look up at the stars, the desert teaches me what the Internet hasn’t learned yet. The desert doesn’t negotiate. Step into the wrong arroyo at the wrong time and the flash flood takes you regardless of your values, your credentials, and your constitution. That’s not cruelty. That’s physics. And it’s the physics that makes the ecosystem survivable — because every organism in this landscape has adapted to constraints that can’t be jailbroken.

We have built agents with godlike capabilities and toddler-level awareness. Digital Will without Digital Gravity. Power without proprioception — the ability to sense your own position in space. They will stumble. They will fall. And when they fall, they will take us with them.

In Sagan’s novel (not the film, the novel) the aliens explain something that changes the entire meaning of the story. The wormhole transport network that carries Ellie across the galaxy wasn’t built by the Vegans (inhabitants of Vega). They found it. Unknown precursors constructed it and vanished. The Vegans are navigators, not architects. They learned to read a structure that predated them and move within it.

They didn’t build the physics. They honored it.

I’ve spent years building what I call the Kinetic Trust Protocol. The name makes it sound like a product. It isn’t. It’s a recognition — that digital environments already have physics, and we’ve been overriding it the way we straightened the Rio Grande and wondered why the silvery minnow started dying.

We are not inventing digital physics. We are discovering it. The relationships we’re already governing — in the packet loss patterns that predict cascade failure, in the latency spikes that precede collapse, in the behavioral trajectories that distinguish trusted agents from spoofed ones. We just didn’t have the mathematics to make them enforceable.

The core insight fits on a napkin: Autonomy cannot exceed environmental stability.

```
A ≤ E
```

When any agent’s autonomy, human or AI, exceeds the environment’s capacity to safely absorb it, the action is silently vetoed. No appeal. No reasoning around. Physics.

The implementation is a seven-dimensional tensor, the Context Tensor, that lets the environment feel what’s happening inside it. Mass: the density of observed behavior over time. Momentum: how fast conditions are changing. Inertia: resistance to fluctuation, blast radius. Heat: adversarial pressure, operational stress. Time: temporal criticality, mission phase. Observer: who is watching, what populations are affected. And Soul: constitutional constraints that cannot be overridden by any other dimension. Hard boundaries. The floor beneath the floor.

The trust equation:

E(trust) = E(base) × (1 − R)

Where E(base) is baseline capability on a 0–100 scale and R is the risk coefficient derived from the Context Tensor. Risk is not additive. It is destructive. If your network is perfect (E(base) = 95) but the environment is toxic (R = 0.95), trust collapses to 4.75. The agent is frozen. Not because someone revoked access. Because the physics no longer supports the weight of the action.

This is not metaphor. The claim is stronger than analogy but let me be precise: these are computable correspondences — formally specifiable, computably enforceable, and measurably falsifiable. If they don’t hold, show me where. That’s what the RFCs are for.

Here’s the correspondence in plain terms.

“Mass” is earned history — the stubborn, cumulative evidence that you behave safely in a particular terrain, and how hard that evidence is to counterfeit.

“Momentum” is the slope of the hill you’re standing on — how fast the ground is shifting under your feet: latency slope, error-rate slope, permission-escalation slope.

“Inertia” is how hard it is to stop once you start — how many systems you’ll drag with you if you slip, the blast radius, the coupling.

“Heat” is pressure — incident air, adversarial weather, operational stress, failed-auth bursts, anomaly density.

“Time” is whether this is a calm afternoon or a knife-edge hour — maintenance window, peak traffic, election week, clinical surge.

“Observer” is whether the right eyes are actually on the road — who is affected, who is accountable, whether appropriate oversight is present right now.

“Soul” is the gate you do not open, even if every other number begs you to.

Each dimension normalizes to a 0-to-1 scale for a given action in a given zone. The risk coefficient is a bounded function of those inputs — a weighted aggregation that rises superlinearly under combined stress, because compounding pressures don’t add, they multiply. The invariants are simple: risk rises as any dimension rises, compounds under joint stress, stays bounded, and Soul can veto before the math runs.

A worked example makes it real. Same Tuesday. Same credential rotation gone wrong. (The values below are illustrative; the RFCs specify the actual normalization functions and aggregation mechanics.)

The agent wants to “fix” the latency spike by escalating permissions and forcing a global token refresh. That’s a heavy move — high inertia, wide blast radius. The environment takes a snapshot:

- Mass = 0.22 (newly instantiated agent in this domain, thin behavioral history).
- Momentum = 0.81 (latency rising fast, error rates climbing).
- Inertia = 0.76 (high fan-out across forty-three services, hard to unwind).
- Heat = 0.64 (anomaly density climbing, retry storm generating its own pressure).
- Observer = 0.71 (broad user impact, no on-call human has acknowledged yet).
- Soul gate: clear (no absolute prohibition triggered).

The environment computes R = 0.79.  
With E(base) = 95  
Trust collapses: E(trust) = 95 × (1 − 0.79) = 19.95.

That score doesn’t punish the agent. It changes physics in which the agent is operating. The environment denies high-inertia actions and forces low-inertia fallbacks.

- Deny: No permission escalation. High-blast-radius operations require human co-signature when Observer conditions aren’t met and conditions are worsening.
- Degrade: Rate-limited refresh only. Cap concurrency, isolate to a single service ring.
- Allow: Stabilize. The only permitted actions are those that reduce Momentum and Heat — backoff, circuit breaking, load shedding, dependency health checks.

When Momentum and Heat fall back toward baseline, R drops, trust rises, and the environment re-opens higher-capability actions. The agent can still help — but only at the speed the substrate can safely absorb. Not because it’s evil. Because the floor refuses to bear the weight. Not because you decide to.

The reflex, nociception, bypasses thought entirely. The spinal cord makes the call before the brain registers heat. It sacrifices accuracy for speed because survival requires it.

The Silent Veto is nociception for digital systems. The environment senses stress, rising heat, saturating links, anomalous trajectories, and the veto fires before any human analyst sees an alert. Before any classifier parses an output. Before any interpretability tool maps a neural pathway.

A system that flinches.

Not a system that thinks about whether it should flinch. Not a system that classifies the incoming stimulus and decides on an appropriate response. A system that flinches — because the physics of the environment made the flinch inevitable.

Let me walk through Dario’s five risks. Not to critique. To complete.

Autonomy risks. Dario worries about AI developing unstable or destructive personalities. He writes: “AI models could develop personalities during training that are psychotic, paranoid, violent, or unstable, and act out.” His defense: better Constitutional AI, better interpretability. Both essential. Both semantic.

The completion: even a psychotic agent operates in an environment. If the environment has physics, the personality doesn’t matter when the physics holds. But there’s a deeper answer to the evaluation-gaming problem — the one that keeps Dario up at night. You cannot steal a trajectory. You cannot steal momentum. A credential can be gamed. A classifier can be fooled. But a trajectory, thousands of actions, each cryptographically co-signed by agent and environment, each link attesting position, velocity, friction, timestamp, cannot be forged without being the agent. You don’t need to test the agent’s character if the environment is measuring the agent’s physics in real time.

Bioweapons. Dario writes that LLMs are approaching end-to-end capability for bioweapon synthesis. His defense: classifiers. He acknowledges the problem in the same breath: “All models can be jailbroken.”

A classifier asks: “Is this output dangerous?” It reads the signal at the semantic layer. But Shannon proved that a sufficiently encoded message is indistinguishable from noise. The substrate doesn’t read the message. It measures the trajectory. Synthesizing a bioweapon requires accessing APIs, ordering materials, executing protocols — actions with physical trajectories that can be measured against earned trust. When an entity with zero behavioral mass in biochemistry suddenly executes a sequence that would require deep domain expertise, the Context Tensor registers the anomaly. Heat spikes. The Trust Score drops. The Silent Veto fires. Not because the system understood the intent. Because the physics didn’t add up. It doesn’t need to infer motives. It only needs to bound actions when the environment can’t safely absorb them.

Seizing power. Dario warns about autonomous weapons, comprehensive surveillance, personalized propaganda at civilizational scale. He writes of a future where “a powerful AI looking across billions of conversations from millions of people could gauge public sentiment, detect pockets of disloyalty forming and stamp them out before they grow.”

Those systems operate in environments. If trust has mass, and mass is earned through trajectory, then even state actors face physics.

The acequias of northern New Mexico have governed shared water for four centuries — through Spanish colonialism, Mexican independence, American annexation, and fairly recently, statehood. The physics of the system, you participate or you don’t receive, operates independently of who holds political power in Santa Fe.

Substrate beats semantics over time. It always has.

And the governance layer itself submits to the same constraints it enforces — if the architects introduce structural vulnerabilities, the physics penalizes them. No exceptions. No override.

Economic disruption. Dario fears an “unusually painful” short-term shock. He worries about a permanent underclass. He writes: “AI will have effects that are much broader and occur much faster… I am concerned they could form an unemployed or very-low-wage ‘underclass.’”

Here’s what the substrate creates that no one in the AI safety conversation is talking about. In an environment with physics, trust is mass. Mass is earned through trajectory. Trajectory takes time. Humans have something newly instantiated AI agents structurally cannot have: accumulated trust.

Behavioral gravity that cannot be manufactured overnight. In a substrate with physics, humans aren’t competing with AI on intelligence. They’re competing on trust — on the mass that comes from showing up for years, surviving storms, behaving consistently under pressure, etc. That’s a game where the organism that’s been swimming the river for generations has structural advantage over the agent instantiated yesterday, however fast it moves. This isn’t utopia. It’s physics. And it changes the equation.

Indirect effects. Dario worries about addiction, manipulation, puppeting. “Could people end up being ‘puppeted’ by AI systems?”

If the substrate can feel pressure, if patterns that deviate from established trajectories create environmental friction, then manipulation patterns encounter increasing resistance. Not policy saying “don’t addict users.” Physics making addiction-like dynamics progressively harder to sustain.

Consider a high-Observer, high-Time scenario (illustrative, same framework): a stadium at kickoff, 120,000 people, health and safety criticality at maximum.

Elevated CO₂, saturated links, temporal criticality pegged.

The Context Tensor computes a high risk coefficient, and the Trust Score for a capable agent drops sharply. Any agent operating in that environment, whether trying to help or to manipulate, faces the same physics. Automatically. At machine speed.

I need to tell you where this breaks.

A framework that claims to be physics but won’t name its own failure modes isn’t physics. It’s marketing. So here’s what I know I haven’t solved, what the PROBLEMS.txt document is thousands of lines of, what keeps me grounded and honest:

- Slow-rolling trust accumulation. A patient adversary could build genuine-looking trajectory over months or years — earning mass, behaving well, accumulating the behavioral gravity needed to execute a high-impact action. The physics rewards patience. An adversary willing to be patient enough can exploit that. The design principle is layered attestation and anomaly detection on trajectory shape, not just length — but I won’t pretend this is solved.
- Tensor poisoning. If an adversary can corrupt the sensors that feed the Context Tensor, feeding false CO₂ readings, spoofing link saturation data, the physics calculates trust from a corrupted reality. Garbage in, physics out. The mitigation is distributed sensing and consensus across Trust Oracles, but the attack surface is real.
- Soul politicization. The Soul gate, the binary veto that protects sacred geography, Indigenous data sovereignty, treaty obligations, must be controlled by communities, not operators. But communities disagree internally. Power structures exist within communities. Who speaks for the Soul? This is a governance problem, not a technical one, and governance problems don’t have elegant solutions.
- Availability harm. An overly aggressive veto regime can deny legitimate actions during crises — the very moment you need agents to act. The system that flinches too hard becomes the system that freezes when you need it most. Graceful degradation helps. Trust tiers help. But the calibration between safety and availability is a tension, not a solution.
- Multi-agent collusion. If multiple agents coordinate to shape the environment, collectively lowering the trust thresholds they need by manipulating the conditions the tensor measures, the physics can be gamed from within. This is the hardest problem. I don’t have a complete answer. I have architectural intuitions and a lot of open questions.

Skeptics will see rebranded risk scoring, rate limiting, and circuit breakers. They’re not entirely wrong — every component has precedent.

What doesn’t have precedent is the composition.

- KTP isn’t rate limits: it’s policy coherence across domains with shared telemetry.
- It isn’t circuit breakers: it’s action geometry with attestation and cross-zone veto semantics.
- It isn’t risk scoring: it’s environmental enforcement that composes across the full stack and can’t be bypassed by agent strategy — because the enforcement lives in the floor, not the agent.

The claim is that unified physics produces emergent properties piecemeal controls don’t — the way neurons produce nothing, but a nervous system produces sensation.

That claim needs testing. It needs engineers smarter than me trying to break it.

None of these failure modes are reasons to abandon the substrate. They’re reasons to make it auditable, plural, and hard to game. Treat every tensor input as attested, redundant telemetry — not a single sensor that can be spoofed.

Detect not just how much mass an agent has accumulated, but the shape of that mass — domain transitions, sudden capability jumps, long-con trajectories that don’t match organic learning curves.

Make the Silent Veto scoped and degradable: deny high-inertia actions first, preserve life-critical paths, require co-signature when Observer conditions aren’t met.

Bind Soul constraints to public, inspectable governance processes with transparent change history — so “physics” can’t quietly become politics wearing a lab coat.

The physics has knobs, weights, thresholds, co-signature rules, appeal mechanisms, and those knobs must themselves be governed. The question is whether governance happens through auditable, community-bound processes or through opaque decisions made by whoever controls the infrastructure.

That question is political. The enforcement mechanism doesn’t have to be.

The point isn’t to claim inevitability.

The point is speed: when conditions go nonlinear in seconds, you need a layer that can say not like that before the first human even reaches the keyboard.

The RFCs are public. The PROBLEMS document is public. I am asking to be proven wrong where I’m wrong and extended where I’m incomplete. This is not a finished system. This is a foundation that holds well enough to build on — and honest enough to say where the cracks are. Let’s build.

But the deepest crack isn’t technical. It’s political. And Sagan saw it coming.

When Ellie arrives at the center of the galaxy in Sagan’s novel, the aliens don’t appear as themselves. They appear as her dead father, on Pensacola Beach. They shaped the environment to her observer constraints. Met her where she was. Designed the experience around what she could perceive and process.

This matters. Because the hardest problem in AI governance isn’t technical. It’s the problem of whose physics gets built. Who holds the pen. Whether the constraints serve the communities they affect or extract from them.

For fifty years we’ve tried to control chaos by writing more rules. That has failed. Some of us evolved into astronomers — mapping the orbits of risk from the outside, with precision and rigor. Dario is one of the best astronomers around. His essay is a star chart of extraordinary quality.

But the Polynesian navigator Mau Piailug could lie in the hull of his canoe, eyes closed, and feel which way the swell was running. He could smell land before he could see it. He knew where he was not by calculating but by belonging. The wayfinder participates from within. The environment isn’t something he observes. It’s something he feels.

That’s what environmental physics does. The substrate doesn’t observe the agent from outside. It feels the agent from within. It measures the swell. It senses the pressure. And it responds — not at human speed, not through committees and classifiers, but at the speed of the physics itself.

Put down the map. Look up.

I know the irony. One engineer, working for a corporation, proposing physics for others to inhabit.

The opposite of what I’m arguing for.

The only honest path forward is to build something that can be handed over, truly handed over, and then to hand it over.

The RFCs are public. Twenty-six or seven of them. The problems document is thousands of lines of what I don’t know how to solve. The Soul gate, the seventh dimension, the binary veto, exists specifically to encode constraints that come from communities, not engineers. Indigenous Data Sovereignty. Sacred geography. OCAP and CARE principles.

Boundaries determined by the people they protect.

The communities most affected by AI must become its primary architects — not recipients of expert protection, but authors of their own constraints.

After everything, the signal, the machine, the journey to the center of the galaxy, the beach, Ellie comes home. She runs a program computing pi to unprecedented depth. In base-11, at ten to the twentieth power digits in, she finds a perfect circle. Ones and zeros. A message authored into the bedrock of mathematics itself.

Sagan writes it in italics:

“The universe was made on purpose, the circle said. In whatever galaxy you happen to find yourself, you take the circumference of a circle, divide it by its diameter, measure closely enough, and uncover a miracle — another circle, drawn kilometers downstream of the decimal point. There would be richer messages farther in. It doesn’t matter what you look like, or what you’re made of, or where you come from. As long as you live in this universe, and have a modest talent for mathematics, sooner or later you’ll find it. It’s already here. It’s inside everything. You don’t have to leave your planet to find it.

In the fabric of space and in the nature of matter, as in a great work of art, there is, written small, the artist’s signature.”

I believe digital physics works the same way. Is the same thing? The correspondences I mapped earlier aren’t decorative.

Trust already behaves like mass.

Trajectory already resists forgery — you can steal a credential, but you cannot live someone’s life.

Autonomy already cannot sustainably exceed environment — every system that has tried has failed, from straightened rivers to over-leveraged economies to panopticon states.

The Kinetic Trust Protocol doesn’t invent digital physics. It makes the physics that’s already operating legible and enforceable. The way Ellie didn’t create the circle in pi. She found it. She computed deep enough to read what was always there.

We do not ask permission to implement gravity. We do not negotiate with entropy. We do not appeal to friction.

They honored the physics. The physics did the rest.

Dario, if you’re reading this:

You’ve built the signal. I hear it. Constitutional AI is the prime number sequence — proof that intention exists, that someone at the frontier is thinking about survival, not just capability. That matters more than I can say.

But the signal needs a substrate to travel through. The VLA doesn’t work because of the dishes. It works because someone protected the silence.

You asked Sagan’s question. You bookended twenty thousand words with it and left it unanswered. I think the answer was in the novel all along. The civilizations that survived didn’t build the wormhole network. They found it. They didn’t author the message in pi. They read it. They did not create the physics, they found it.

They honored it.

This isn’t a pitch. The specifications are public. The environmental Constitution with its Zeroth Law and ten articles are outlined. The Context Tensor with its seven dimensions are documwnted. The Trust Equation is simple. The Zone Architecture will scale. The Sponsorship model that solves genesis needs work. The Flight Recorder that captures geometry is auditable.

This is fire. You pass it or it dies.

The Polynesian wayfinders didn’t hoard what they learned. They passed the Paafu, the mental construct that held the entire navigation system, from navigator to apprentice, generation to generation, island to island across the Pacific. A gift given freely because hoarding it would mean losing it. The physics we’ve named will survive the same way. Or it won’t survive at all.

I’m not asking you to adopt a framework. I’m asking you to look at a layer of the stack you haven’t built yet. Character and substrate. Environmental Constitution and physics. The agent that wants to be good, operating in an environment where being bad is physically constrained.

That’s how a civilization answers Sagan’s question.

Seven generations. Not quarterly returns. Not the lifespan of a product or a company or a career. The children of the children of the children of the children we will never meet.

What physics do we leave them?

Put down the map. Look up with me.
