Swells
The Voyage, IV — Reading what cannot be seen

This is Day 4 of a 12-part series on building an Internet governed by physics instead of policy. Start at [Day 1: Departure](https://medium.com/@chrisperkins505/departure-525049f52c23).

> “The ocean is not silent. We have simply forgotten how to listen.” **— Nainoa Thompson, Polynesian Voyaging Society**

Three days out now. The harbor is behind us.

I catch myself looking back sometimes. Not with regret — with something closer to appreciation and tenderness. We built that harbor. All of us. Generations of engineers, architects, security professionals. They poured their lives into those pilings. Firewalls and access control lists. Role-based permissions and identity providers. It wasn’t nothing. It was the best we knew how to build at the time.

And it worked. For a while. When the traffic was human, when the pace was slow, when you could check a user and ask, “*Are you who you say you are?*”

But I’d be lying if I said the harbor served everyone equally.

The old system had owners. It had gatekeepers. It was built by the few, and the rest of us paid rent. Our money. Our attention. Our habits. Our data, quietly siphoned and sold to the highest bidder while we clicked “agree” on terms no one was meant to read. Security was a product, not a right. Privacy was a premium feature, not a foundation. The people who built the walls also held the keys. They decided who got in, who got watched, and who got monetized.

The harbor kept some of us safe. It made others into the product.

We honor the craft of those who built it.

The destination we’re sailing toward is different — not just more secure, but fairer. Not just faster, but more private. A system w*here* the physics protects everyone, not just those who can afford the best walls.

We keep sailing.

The stars tell us where we’re going. But the stars are distant. Points of light that speak in the language of direction, not condition. They can’t tell us what’s happening here. They can’t feel the water beneath the hull.

To navigate the open ocean, the wayfinders learned to read the swells.

Not waves. **Swells**. Waves are local, chaotic, driven by immediate wind. Swells are deeper. They originate from storms hundreds or thousands of miles away, traveling across the open Pacific in long, rolling patterns. To the untrained eye, the ocean looks the same in every direction. To a wayfinder, it’s full of information. They could feel a swell through the hull of the canoe, sense its direction, its rhythm, its interference with other swells. They built stick charts out of palm ribs and shells to map these invisible patterns.

The ocean is not silent. We had simply forgotten how to listen.

We have built something similar in the digital world. We just don’t recognize it yet.

Data analytics platforms. Security lakes. Telemetry pipelines. Network monitors. Log aggregators. We have instrumented everything. We capture the hum of voltage, the rhythm of packets, the temperature of the attack surface. Every transaction, every latency spike, every failed authentication. Recorded, timestamped, stored.

We have built the greatest sensor network in human history.

And then we turned the volume down.

We collected the data and filed it away for forensics. Something to examine after the breach, after the outage, after the damage is done. We built the nerves of a digital nervous system, and then we never connected them to the muscles.

The sensors are there. The swells are there. What’s missing is the physics to interpret them.

We call it the **Context Tensor.** A way of measuring the environment across multiple dimensions simultaneously. Not a single number. A shape. A reading of the conditions the vessel is moving through.

The first three dimensions are physical. The most tangible, the easiest to sense:

- **Mass (M):** Physical density — the number of active devices in a subnet, the crowd density in a stadium, the RF noise in a spectrum band at the airport. High Mass means high environmental load.
- **Momentum (P):** Data flow velocity — queries per second hitting an API, link saturation on a network segment, the rate of authentication attempts. High Momentum means the system is moving fast.
- **Inertia (I):** Blast radius — how many downstream services depend on this one, how deep the dependency chain goes, what breaks if this component fails. High Inertia means the action has consequences that ripple outward.

Three dimensions. Three ways of feeling the water beneath the hull.

There are more we’ll encounter as we cross. But these three are enough to begin. Enough to turn telemetry into physics. Enough to teach the network to feel its own weather.

[**Splunk**](https://www.splunk.com) gives us the eyes. Physics gives us the sight.

The wayfinders didn’t just see the ocean. They felt it through the hull, through their bodies, through years of accumulated wisdom about what the patterns meant. We are building the same capacity for digital systems. Not just data collection, but data *comprehension*. Not just sensing, but understanding.

The swells are already there. They’ve always been there. We just need to learn to read them again.

The ocean is not silent.

We are learning to listen.

**We are learning to feel.**

## **In Practice**

**For CISOs:** You already have the “nerves” (observability infrastructure). The Context Tensor is about connecting them to authorization decisions. Mass, Momentum, and Inertia are already being measured — start using them.

**For Infrastructure Engineers:** Instrument your systems to expose M, P, I in real time. Number of active devices (Mass), queries per second (Momentum), dependency depth (Inertia). Make these metrics queryable by your authorization layer.

**For AI/ML Teams:** Your agents need to sense their environment to operate safely. The Context Tensor is the sensory input. Without it, your AI is blind to the conditions it’s operating in.

### Tomorrow: [Current](https://medium.com/@chrisperkins505/current-745961b089ae) — The Voyage, V

Previous: Day 3 —Stars | Next: Day 5 — Current
