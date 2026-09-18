The Phase Transition
On platforms, percolation, and why enshittification follows the same arc every time

Last week you searched for a blender on Amazon*.*

Not something exotic. A blender. A thing with reviews and stars and a little badge that says “Amazon’s Choice.” You trusted the badge the way you once trusted the librarian’s recommendation — not because you’d verified the system behind it*,* but because you’d been inside the current long enough that trust felt like the water you were swimming in. You clicked. You bought. It arrived. It was fine.

But something nagged at you. The way a shift in the current nags at a fish before the fish can name what changed.

I’ve spent twenty-three years inside systems like this, not as a consumer, but as the person called in when the system fails. Fraud detection. Network defense. Trust architectures under stress. After twenty-three years, I can tell you: that nag you felt is real. That badge cost someone. Not you. The seller. It cost them their margin, their independence, their ability to price their own product. “Amazon’s Choice” isn’t a quality signal. It’s a ransom receipt. You paid more for worse. The environment was designed to make that invisible.

This is not a story about Amazon. This is a story about what happens when trust has no weight.

Every platform dies the same way. Not all at once. Not from a single decision. The way a river dies when you straighten the channel — gradually, then suddenly, then everyone acts surprised even though the math was visible the whole time.

And I’ve been working on something for the last several months that I didn’t expect to connect to platforms, to Cory Doctorow, to the reason your Instagram feed feels worse every month even though you can’t stop scrolling.

Elinor Ostrom spent her career studying systems that don’t fail. Commons — shared resources governed by communities without central authority. Irrigation systems. Fisheries. Forests. Grazing lands. She found eight design principles consistently present in the ones that last centuries. She won a Nobel Prize for it in 2009.

I’ve been working on a formal proof that her eight principles are percolation maintenance specifications — each one keeps a specific variable in the community’s trust network above the critical threshold where trust propagates. Drop below that threshold and the network fragments. Trust stops traveling. The community fractures into isolated clusters where nobody trusts anyone they haven’t met personally.

That’s a phase transition. Not a gradual decline. A state change. Ice to water. Connected to fragmented. Community to crowd.

Here’s what I didn’t expect to find: every major platform, in the same order, systematically removed all eight of Ostrom’s principles. And the phase transition followed every time.

## The Eight Principles, Inverted

Let me show you what the platforms did. Principle by principle.

**DP1 — Clear Boundaries.** Ostrom: define who’s in the community. Bound the population. The acequia knows its parciantes. The fishing village knows its fishers. Boundaries make the trust network small enough that trust can actually propagate — you can know enough people that indirect trust reaches everyone.

Platforms: no boundaries. Anyone can join. Bots can join. Fake accounts can join. Amazon has 9.7 million sellers. Facebook has 3 billion users. The trust network is so large that no human can maintain enough direct trust relationships for indirect trust to reach across it. The percolation threshold for a network of 3 billion is astronomically higher than what any trust-generating process can maintain. The network is structurally incapable of percolating. It was designed that way. Growth is the metric. Boundaries are the enemy of growth.

**DP2 — Rules Match Local Conditions.** Ostrom: tune the governance to the specific resource system. A fishing community near a coral reef needs different rules than a timber forest in Nepal. The rules work because they fit the topology.

Platforms: uniform global rules. Amazon’s marketplace policies are the same for a small ceramics studio in Oaxaca and a factory in Shenzhen. Facebook’s community standards apply identically to a knitting group in Vermont and a political movement in Myanmar. The rules don’t match local conditions because the platform doesn’t recognize local conditions. There is no local. There is only the platform. The trust weight on every edge, the quality of every relationship, degrades because the rules optimize for the platform’s extraction, not the community’s coherence.

**DP3 — Collective Choice.** Ostrom: the people affected by the rules participate in making them. The parciantes vote. The fishers deliberate. Legitimacy comes from participation. In network terms, this maintains reciprocity — mutual trust, bidirectional edges, the property that lowers the percolation threshold from the harder directed case to the easier undirected case.

Platforms: rules imposed unilaterally. The terms of service are updated without consent. The algorithm changes without notice. Instagram shifted from chronological to algorithmic feed, the most consequential change in how 2 billion people consume information, and nobody voted. Nobody was consulted. The trust edges became one-directional: users trust the platform (because they have no alternative), but the platform’s actions don’t reciprocate that trust. The network shifted from undirected to directed percolation. The threshold rose. The community fragmented.

**DP4 — Monitoring.** Ostrom: community members can observe each other’s behavior and attest to what they saw. The mayordomo walks the ditch — not from a watchtower, but alongside the parciantes. He sees who showed up. They see him seeing. And both can attest: Ana was here. Beto was here. Carlos was not. Monitoring isn’t detection. It’s alibi-making — creating the conditions under which presence can be verified by anyone in the network. The trust doesn’t come from catching defectors. It comes from the fact that your contribution is witnessed. The community’s record of who showed up is the trust substrate. Monitoring creates induced percolation pathways: I trust you because someone I trust can attest that you cooperated.

Platforms: monitoring is asymmetric and non-attesting. The platform monitors every user. No user monitors the platform. Amazon knows every click, every hover, every abandoned cart. The seller doesn’t know how the algorithm ranks them, what data Amazon collects, or how “Amazon’s Choice” is determined. But the deeper problem isn’t just the asymmetry — it’s that the monitoring produces no alibi. When Amazon watches you browse, nobody can attest to what Amazon did with that data. When the algorithm adjusts your price, no third party witnessed the decision. The platform creates detection without attestation — surveillance without alibi. The monitoring overlay exists, but it runs in one direction and leaves no verifiable record for the people being monitored. The mayordomo can say “Ana showed up.” Can you say “Amazon showed me a fair price”? Can anyone attest to what the algorithm did? The trust that monitoring is supposed to create, “I trust the system because I can see it operating fairly,” doesn’t exist because the system’s operation is opaque and unattested. There’s no alibi for the algorithm.

**DP5 — Graduated Sanctions.** Ostrom: when someone violates the rules, the punishment is proportional. Small violation, small consequence. Repeated violation, escalating consequence. This prevents two failure modes: too-weak sanctions that let free-riders spread, and too-strong sanctions that destroy trust edges unnecessarily.

Platforms: sanctions are binary and asymmetric. A seller on Amazon can be suspended overnight with no explanation, no appeal, no graduated process. A user on Facebook can be banned for a post that an algorithm misclassified. Meanwhile, the platform itself faces no sanctions for degrading search quality, raising marketplace take rates, or manipulating the feed. The sanctions are maximum for the user and zero for the platform. In cascading failure models, this is exactly the condition that produces system-wide collapse — disproportionate edge destruction in one direction while the other direction accumulates damage unchecked.

**DP6 — Conflict Resolution.** Ostrom: accessible, low-cost mechanisms for resolving disputes. When trust is damaged, there’s a way to repair it. The edge gets restored. The network maintains its connectivity.

Platforms: conflict resolution is inaccessible by design. Try reaching a human at Amazon when your seller account is suspended. Try appealing a Facebook moderation decision to a person who can explain it. The repair mechanisms don’t exist because repairing trust edges with 3 billion users is not scalable, and the platform has no economic incentive to repair edges it can replace with new users. Damaged edges stay damaged. The fraction of active trust edges declines monotonically. The network approaches the percolation threshold from above, and there’s no mechanism pulling it back.

**DP7 — Right to Organize.** Ostrom: the community can govern itself without external authorities overriding its structure. The community controls its own topology.

Platforms: the platform controls the topology. It decides what you see. It decides who your content reaches. It decides which edges are active (amplified) and which are suppressed. Two teenagers built an app called OG that restored Instagram’s chronological feed — the community organizing to restore its own information topology. Meta had Apple and Google remove it. Doctorow called it “felony contempt of business model.” In network terms, the community attempted to protect its own topology and the platform used its control of the distribution layer to prevent it. The community has no right to organize because the platform owns the graph.

**DP8 — Nested Enterprise.** Ostrom: when commons are nested (communities of communities), governance operates at multiple levels. Local communities maintain local trust while inter-community bridges maintain federation. Dong et al. proved that these inter-community links function as an external field that lowers the percolation threshold for the whole system.

Platforms: no federation. No interoperability. No portability. Your Facebook relationships don’t transfer to Mastodon. Your Amazon seller reputation doesn’t transfer to Shopify. Your Uber rating doesn’t transfer to Lyft. Each platform is a walled garden — a community with no inter-community bridges. The external-field effect that federation provides is zero. Every platform operates at its own percolation threshold without the resilience benefit that nested enterprise creates. When one platform degrades, users can’t migrate their trust network. They can only start over. The switching cost is the cost of rebuilding every trust edge from scratch.

## What Removing the Maintenance Functions Feels Like

That’s the architecture. Now let me show you what it produces.

Suppose you wanted to exploit a coal miner in 1890. You’d need an army of Pinkertons to surveil their finances. You’d need clerks to annotate each miner’s pay ledger individually. You’d need informants in the company store tracking who was desperate and who wasn’t. The cost of exploitation was proportional to the exploitation attempted. Not because coal bosses were moral — they were among the cruelest employers in American history. Because physics pushed back. Friction existed. Mass was real. Exploitation had weight.

Now update the story. In America, hospitals increasingly hire nurses through contractor apps. The apps buy each nurse’s credit history — legal, since the U.S. hasn’t passed a federal consumer privacy law since 1988, when Ronald Reagan signed legislation making it illegal for video store clerks to disclose your VHS rental habits. Every other form of consumer privacy invasion remains lawful. Based on how much debt a nurse carries, how delinquent that debt is, the app adjusts her wage downward. The more desperate she is, the less she’s paid.

The algorithm does what would have required a thousand Pinkertons — instantly, silently, at scale.

That’s all eight principles, absent, in a single transaction. No boundaries on who can buy her data (DP1). No rules tuned to the conditions of her specific labor market (DP2). No collective voice in setting the terms (DP3). Monitoring runs in one direction and nobody can attest to what happened: the app sees her credit score; she doesn’t see the algorithm adjusting her wage, and no third party witnessed the decision (DP4). Sanctions are binary: accept the rate or don’t work (DP5). There is no conflict resolution, no mechanism to contest the price (DP6). She has no right to organize against the system that prices her desperation (DP7). And her situation is not portable. Her reputation, her reliability, her years of competence don’t transfer to a competing platform that might treat her differently (DP8).

The cost of exploitation approaching zero is the absence of gravity. And a system with no gravity is a system where the percolation threshold rises without limit — where trust cannot propagate, because nothing holds the network together long enough for trust to travel.

The coal miner’s exploitation required mass. The nurse’s exploitation requires a server.

That’s the phase transition, felt in a single life.

## The Arc

Every platform follows the same arc because every platform removes the same eight maintenance functions in the same structural order.

**Phase 1 — Accumulation.** The platform is good to users. It appears to maintain some of Ostrom’s principles. Boundaries are loose but the community is small enough that trust propagates. Rules feel fair because the platform is subsidizing everyone. Monitoring appears symmetric because the platform isn’t yet extracting from what it observes. The trust network percolates. Users feel connected. Sellers thrive. The ecosystem is alive.

The platform is not maintaining these principles. It is *simulating* them with subsidized economics. The subsidy is venture capital. The trust is borrowed. The percolation is artificial — funded by below-cost pricing that creates the appearance of a healthy trust network without the substrate to maintain it.

**Phase 2 — Lock-in.** The platform begins removing principles. First DP7 — the right to organize. The API closes. Third-party access is restricted. Data portability disappears. The community can no longer modify its own topology. Then DP8 — federation. Interoperability is blocked. Switching costs become prohibitive. The network effects that made the platform valuable now make it inescapable.

At this point, the trust network is still above the percolation threshold, but the maintenance functions are being stripped. The water table is dropping but the surface looks the same.

**Phase 3 — Extraction.** The remaining principles are removed simultaneously. Boundaries dissolve — growth demands more users, more sellers, more content. Rules stop matching local conditions — uniform policies optimize for platform revenue. Collective choice disappears — algorithm changes are imposed without notice. Monitoring becomes surveillance without attestation — the platform sees everything, no one can verify what the platform did. Sanctions become binary and unilateral. Conflict resolution becomes inaccessible.

The trust network crosses the percolation threshold. The phase transition occurs.

But it doesn’t feel like a transition. It feels like “Instagram got worse” or “Amazon search is garbage now” or “I can’t tell which reviews are real.” The network has fragmented, but the interface masks the fragmentation. The platform still shows you a feed. It still shows you search results. It still shows you ratings. The dashboard is green. The aquifer is dry.

Ezra Klein described his own experience on Instagram: “I like it less, but the feeling of getting pulled into something is much stronger.” That gap, between what you value and what you can’t stop consuming, is the felt experience of a trust network that has fragmented while the attention capture mechanism remains intact. The community has crossed the phase boundary. The trust edges that once connected you to people you chose to follow have been replaced by algorithmic recommendations optimized for engagement. The trust is gone. The pull remains. The platform persists in degraded equilibrium — not because it works, but because the cost of leaving is higher than the cost of staying.

Doctorow calls this enshittification. The percolation framework calls it what it is: a phase transition from connected to fragmented, caused by the systematic removal of the maintenance functions that kept the trust network above its critical threshold.

## Why the Arc Is the Same Every Time

Doctorow says it’s because the same CEOs go to the same giant switch on the wall marked “enshittification” and yank it as hard as they can. He’s right about the behavior. He’s wrong about the explanation.

The arc is the same because the physics is the same. Remove the maintenance functions from a trust network and the percolation threshold rises while the trust level drops. The two lines cross. The network fragments. It doesn’t matter whether the CEO is greedy or generous, whether the platform is Amazon or Airbnb, whether the year is 2010 or 2026.

The physics doesn’t care about intent.

Ostrom’s design principles aren’t moral recommendations. They’re maintenance specifications. An acequia that doesn’t get cleaned in the spring isn’t punished by the universe for laziness. The silt accumulates, the water slows, the channel fails.

The physics is indifferent to the reason.

A platform that removes collective choice isn’t punished for greed. The trust edges become unidirectional, the percolation threshold rises, the community fragments.

Same physics. Same indifference.

This is why policy interventions keep failing. The GDPR didn’t restore the maintenance functions. It added a rule on top of a system that had removed all eight. Antitrust proposals don’t restore the maintenance functions. They attempt to constrain the platform’s behavior without rebuilding the trust substrate. You can fine Amazon $10 billion and the marketplace take will still be above 50% the following quarter because the fine doesn’t restore DP2, DP3, DP4, DP5, or DP6. The trust network is still fragmented. The percolation threshold is still above the trust level. The phase transition already happened.

The fine is a sign posted above a dry riverbed. *Water Was Here.*

## What Restoration Looks Like

If enshittification is a phase transition caused by removing Ostrom’s maintenance functions, then restoration requires rebuilding them.

Not all eight at once. The percolation framework tells you which variable dropped below threshold first, which means it tells you which maintenance function to restore first. The diagnosis names the repair.

**Interoperability is DP8.** Not as a policy mandate that can be litigated for a decade. As a protocol. The way TCP/IP doesn’t belong to any company and HTTP can’t be amended by a CEO. Data portability that allows your trust network, your relationships, your reputation, your behavioral trajectory, to move with you. The inter-community bridges that create the external-field effect, lowering the percolation threshold for the whole ecosystem.

Federation is physics, not policy.

**Algorithmic attestation is DP4.** Not “disclose your algorithm” — a burden shifted to the user who will never read it. Attestation. If the platform adjusts your price, a third party witnesses the decision and can attest to what happened. If the algorithm changes your feed, the change is recorded in a way the community can verify. The mayordomo doesn’t monitor from a watchtower. He walks the ditch alongside the parciantes, and both can say what they saw. Restoration means building the alibi layer the platforms removed — not surveillance of the platform, but witnessed, verifiable records of what the platform did. Trust propagates when behavior is attested.

Opacity is surveillance without alibi. Transparency is its restoration.

**Collective governance is DP3.** Platform cooperativism. Users with genuine voice in rule-making, not advisory boards with no authority. The rules that govern the community are made by the community. This converts the trust network from directed to undirected, lowering the percolation threshold.

It’s not democracy as metaphor. It’s democracy as network physics.

**Graduated sanctions for platforms is DP5.** Not binary — not “break up Amazon” or “do nothing.” Proportional consequences that escalate with the severity and persistence of the violation. A marketplace take that rises 1% triggers a 1% regulatory response. A take that rises 30% triggers a structural intervention.

The sanctions prevent cascade by keeping the damage proportional.

Each restoration is a maintenance function returned to the network. Each one lowers the percolation threshold or raises the trust level. Together they move the system back across the phase boundary — from fragmented to connected. From crowd to community.

## The Protocol That Already Exists

There is a technical specification that encodes all eight of Ostrom’s principles as infrastructure. It’s called the Kinetic Trust Protocol. I filed the patent. Here is the mapping:

- DP1 (Boundaries) → Blue Zones: bounded trust regions with defined membership, constraining the graph so percolation is achievable.
- DP2 (Rules match local) → Context Tensor: six dimensions of the local environment, tuning the physics to the specific conditions the way an acequia’s flow rate matches its watershed.
- DP3 (Collective choice) → Federated zone governance: each community sets its own parameters, so the rules that govern the network are made by the people inside it.
- DP4 (Monitoring) → Oracle mesh: distributed attestation across multiple independent sensors, where each oracle can verify what it observed and the community can confirm the record. The alibi layer the platforms removed.
- DP5 (Graduated sanctions) → Digital Gravity: friction proportional to deviation from established behavioral trajectory, graduated and continuous, never binary.
- DP6 (Conflict resolution) → Trust Score recovery: damaged trajectories repaired through demonstrated behavior over time, restoring edges before accumulated damage crosses the percolation threshold.
- DP7 (Right to organize) → Protocol-level sovereignty: no single entity controls the trust layer, the way TCP/IP doesn’t belong to any company and HTTP can’t be amended by a CEO.
- DP8 (Nested enterprise) → Zone-to-zone trust translation: behavioral trajectory carried across community boundaries, creating the inter-community bridges that function as the external field lowering p_c for the whole ecosystem.
- DP9 (Temporal persistence) → Proof of presence: not just co-location, but the full encounter — show up (proximity), attend to each other (attention), build something together (creation), and be witnessed doing it (alibi). Trust that isn’t periodically renewed by actual encounter across all four dimensions decays below the threshold where the network holds. A mandatory roll call wouldn’t work. A Zoom check-in wouldn’t work. The la limpia works because the parciantes show up, see each other, clean the ditch together, and the community can attest to who was there.

The substrate for all nine is the trust environment itself. Not a platform. Not a server. Not a company’s infrastructure. The measured, real-time state of the environment in which agents operate. The physics lives in the substrate the way gravity lives in mass. Remove the substrate and the protocol is policy. Maintain the substrate and the protocol is physics.

KTP is not inspired by Ostrom. It is Ostrom formalized as a network protocol. I derived it from twenty-three years of watching systems break. She derived her principles from decades of watching commons hold. We arrived at the same architecture from opposite directions. She studied what persists. I studied what fails. The answer was the same eight maintenance functions.

The ninth was hiding in the acequias the whole time.

## The Acequia and the Algorithm

There is a ditch is just down the hill from where I’m sitting, face glowing from the laptop, that has been carrying water for four hundred years. The parciantes clean it every spring. They show up. They attend to each other. They build something together. They are witnessed doing it. The mayordomo walks it. The water flows by gravity. All nine principles are present. The trust network percolates. The community holds.

There is an app on my phone that has been carrying attention for fifteen years. No boundaries. No collective choice. No conflict resolution. No right to organize. No federation. The trust network fragmented years ago. The attention capture remains.

The acequia persists because the physics is maintained. The platform degrades because the physics was removed. Same water. Different channels. Same math.

Enshittification is not a business strategy. It is not a moral failure. It is not the inevitable consequence of capitalism or greed or human nature.

It is a phase transition. Predictable. Measurable. Reversible.

If we rebuild the maintenance functions.

Show me your physics.

Chris Perkins writes about cybersecurity, trust, and digital physics from New Mexico. He is a Solutions Engineer at Cisco/Splunk with twenty-three years in fraud detection, network defense, and trust architecture.

This essay draws on a formal proof in development: “Ostrom’s Design Principles as Percolation Maintenance Specifications for Trust Networks” and the Study of Resilient Systems. Previous essays in this series: *“Ditches Are Deadly”*, *“What Was Already Here”*, *“The Speed of Inference and the Depth of Trust”*.
