Current
The Voyage, V — Mass, friction, motion

This is Day 5 of a 12-part series on building an Internet governed by physics instead of policy. Start at [Day 1: Departure](https://medium.com/@chrisperkins505/departure-525049f52c23).

> “You cannot step into the same river twice.” **— Heraclitus**

In 2023, the current changed with the availability of ChatGPT (the first of its kind).

For decades, the traffic on the Internet was human. People typing passwords. People clicking links. Sending emails and deleting spam. People making decisions at human speed — slow enough that a guard (technology) could check credentials, slow enough that a policy could be consulted, slow enough that someone could pick up a phone and ask, *“Will you please help me reset my password?”*

That current is gone.

The age of AI has arrived. Not as a distant promise, but as the water we’re already swimming in. Large language models that write code and learn skills. Autonomous agents that negotiate contracts, execute trades, manage infrastructure, book flights, file reports. Agents that spawn other agents. Decisions made in milliseconds, at volumes no human could review, by entities that don’t sleep, don’t pause, don’t wait for approval.

If the current had stayed human, we might have patched the harbor for another generation. More firewalls. More policies. More billions poured into complexity, more consultants, more certifications, more theater. The old guards weren’t failing because they were incompetent. They were failing because they were human — and the traffic no longer is.

This is why we need physics, not policy.

Policy requires interpretation. Policy requires committees and exceptions and edge cases. Policy moves at the speed of humans arguing in conference rooms.

Physics just is.

An autonomous agent moving at machine speed doesn’t have time for a policy committee. But it can feel friction. It can sense when A exceeds E. It can respond to the environment in real time, because the environment is the constraint. Not a human gatekeeper who’s already two seconds and ten thousand decisions behind.

We are five days into open water now. The ocean is vast, and the current here moves in ways I’m still learning to read.

But current is current. The physics is the same whether you’re crossing the Pacific or wading into a river in New Mexico. And it was rivers that first taught me what current means.

I was young when I first felt it. Wading into the Pecos River in eastern New Mexico. The water was shallow, clear, deceptively gentle. But when I stepped in past my ankles, I felt it: that insistent pull. Not violent. Just certain. Steady. The river was informing me of a fact. This is how fast I’m moving, and you will account for me, or you will stumble.

Years ago, I stood at the edge of the Rio Grande, tossing sticks into the current. I was maybe eight or nine. Each stick was a vessel to me. I’d hold it for a moment before letting go, convinced it carried something important. A message. A wish. Some part of me racing on the water toward someone I’d never meet (it turns out, I met her!). I imagined a kid in another town, maybe another country, pulling my stick from the water and somehow knowing it had traveled far to reach them.

The sticks carried nothing, of course. Just bark and air and the weight of a child’s hope. But I couldn’t stop sending them. The river was going somewhere. And I wanted to be part of where it went.

The Rio Grande is special. It carved the valley I grew up in. The Bosque spreads along its banks, cottonwoods and willows drinking from water that’s been flowing for millions of years. But what you see on the surface is only part of the story.

Beneath the Rio Grande lies the Rio Grande Rift. A place where the Earth’s tectonic plates are slowly pulling apart. The continent is stretching, thinning, cracking. The river follows the rift because the rift created the valley. The visible current flows because of invisible forces far below. Forces that have been shaping the landscape since before there were humans to name it.

The surface moves fast. You can see it, feel it, measure it.

The deep structure moves slow. You can’t see it at all. But it determines everything. Where the water flows. Where the valley forms. Where life takes root.

Rivers taught me this. Now we’re in the open ocean, and the lesson holds.

The current you’re feeling on this voyage, the packets, the transactions, the API calls: that’s the surface. The physics we’re naming, A ≤ E, the **Trust Equation**, the **Context Tensor** — that’s the rift. The deep structure that shapes where everything else can flow.

**Friction is not failure. Friction is information.**

It’s the environment telling you that you are on the wrong vector. The river doesn’t punish the swimmer who moves against the current. It simply makes the truth visible.

In our framework, friction manifests as **Risk (R)** in the Trust Equation. When R rises, when adversarial **Heat** increases, when the network congests, when the system is under stress, friction increases. The agent feels resistance. This is not a bug. This is the system communicating.

The Pecos taught me that. The Rio Grande confirmed it. A river doesn’t punish you for wading in. It tells you the truth about how fast it’s moving, and you either adjust or you fall.

The ocean works the same way. The wayfinders didn’t fight the currents of the Pacific. They read them, joined them, let the water carry them where they needed to go. **Current** is current, whether it’s flowing through a rift valley in New Mexico or across the largest ocean on Earth.

The Trust Equation formalizes this:

```
**E_trust** = **E_base** × (1 - R)
```

E_base is the agent’s intrinsic capability. The mass it has earned through demonstrated behavior, through survival, through trajectory. Think of it as the strength of the swimmer.

R is the Risk Factor. A value between 0 and 1, derived from the environment. It’s the current. The friction. The resistance the swimmer moves through.

E_trust is what remains. The effective capability after the environment has had its say.

Let me make it concrete.

An agent begins with E_base of 100. Full capability, hard-earned. The environment is calm. R is low: 0.1. The math is simple:

```
100 × (1–0.1) = 90
```

The agent operates at 90. Nearly full capacity. The current is gentle. Movement is easy.

Then adversarial pressure spikes. Anomalies in the network. Probing attacks. The temperature rises. R climbs to 0.7.

```
100 × (1–0.7) = 30
```

The agent’s effective trust contracts to 30. Not because it did anything wrong. Not because a policy changed. Because the environment changed, and the physics responded.

The agent that could write to the database can now only read. The agent that could access the entire network can now reach only its own subnet. Capabilities narrow. Automatically, silently, without a committee convening or a ticket being filed.

No administrator intervened. No policy was consulted. The physics enforced the constraint.

This is what it means to navigate by current instead of credential.

The Context Tensor measures the current.

In Day 4, we met the first three dimensions: Mass, Momentum, Inertia. The physical weight of the environment.

Now we add two more:

Heat: adversarial pressure. Attack signatures. Anomaly rates. Failed authentications. WAF blocks. The temperature of the threat landscape. When Heat rises, the environment is under stress. R increases. Capabilities contract.

**Time**: temporal criticality. How close are we to the event? Is this the maintenance window or the product launch? The hour before the earnings call or a quiet Sunday morning? Time isn’t linear in terms of risk. Some moments are load-bearing. The system should know which ones.

Five dimensions now. Five ways the current speaks. Whether that current flows through a river, across an ocean, or through the wires of the digital world.

There are two more dimensions. We’ll meet them at the horizon and at the sacred boundary. For now, five is enough to feel the water, to sense when the current is gentle and when it’s about to sweep us off our feet.

The Bosque survives because it learned to live with the river, not against it.

The cottonwoods don’t fight the flood cycle. They depend on it. Their seeds germinate in the wet sand left behind when the waters recede. The whole ecosystem exists because the river is allowed to be a river. When we dammed it, channeled it, tried to make it predictable, the Bosque began to die. The river needs to move.

We’re building the same relationship with risk. Not damming it. Not pretending we can make it predictable. Learning to let the current inform us, shape us, tell us where we can go and where we can’t.

The Bosque teaches what the wayfinders knew: life doesn’t flourish by conquering the physics. It flourishes by joining it. The cottonwood by the river. The navigator in the ocean. The agent in the network. All learning the same lesson.

You cannot step into the same river twice. You cannot cross the same ocean twice. You cannot send the same packet twice.

The current that was calm at 9:00 AM is turbulent by 9:01. The packets have moved on. The threats have evolved. The agents have multiplied.

But beneath the surface current, beneath the river, beneath the ocean — the deep structure holds. The physics beneath the protocol. A ≤ E was true before we named it, and it will be true long after we’re gone.

We’re not inventing the constraint. We’re uncovering it.

But no agent crosses alone.

Tomorrow, we meet the crew. We learn how trust is staked, how new agents earn their first mass, how the vessel holds together when everyone is paddling through the same current.

For now, we rest. We feel the water beneath the hull. We remember that friction isn’t the enemy. Not in the river. Not in the ocean. Not in the network.

Current is current. And we are learning to read it.

You cannot step into the same river twice.

You cannot cross the same ocean twice.

But you can learn to feel the current — and the rift beneath it.

**We move with the water.**

## **In Practice**

**For CISOs:** The Trust Equation (E_trust = E_base × (1 — R)) gives you a mathematical model for dynamic trust. Risk (R) should be computed in real time from environmental signals — not set once at deployment.

**For Infrastructure Engineers:** Implement the Trust Equation in read-only mode first. Let it calculate E_trust but don’t enforce it yet. Watch what happens during incidents. Tune R based on real conditions.

**For AI/ML Teams:** Trajectory over credential. Your agent’s trust should be based on where it’s been and what it’s done, not just what keys it holds. Build systems that track geometry, not just identity.

### Tomorrow: [Crew](https://medium.com/@chrisperkins505/crew-f3efdcb804c2) — The Voyage, VI

Previous: Day 4 — Swells | Next: Day 6 —Crew
