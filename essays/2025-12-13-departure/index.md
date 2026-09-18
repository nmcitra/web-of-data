Departure
The Voyage, I — Why the old harbor fails us

This is Day 1 of [*The Voyage*](https://medium.com/@chrisperkins505/the-voyage-12-days-of-digital-physics-724ca6f63b44), a 12-part series on building an Internet governed by physics instead of policy.

> “A ship in harbor is safe, but that is not what ships are built for.” — **John A. Shedd**

The Internet is a physical, humming machine that spans from the silicon in a server rack to the fiber-optic cables resting on the ocean floor.

### 1. The Physical Footprint: Data Centers

In the American Southwest, the “Cloud” is actually millions of square feet of concrete, copper, and cooling systems. For example:

- **Phoenix Metro Area (The Hub):** Phoenix has become a primary node for the Western Hemisphere due to its stable geology and power infrastructure. Key facilities include:
- **Dona Ana County, New Mexico (An Emerging Node) — Project Jupiter:** A planned high-efficiency data center campus near Santa Teresa. It represents the next generation of infrastructure designed to leverage the region’s solar capacity and stable land, bridging the gap between the Texas interconnect and Western grids.

### 2. The Physics of the Machine

When you peel back the screen, the Internet is just energy and physics.

- **Voltage:** Inside the data center, power is stepped down from massive 800VDC distribution lines to the precise voltage needed by silicon. A modern CPU core or GPU operates at a surprisingly low **0.7V to 1.2V**, but it draws massive current — up to **700 Watts** for a single GPU. This low voltage at high amperage creates intense heat, requiring liquid cooling loops.

**Copper vs. Fiber:**

- **Copper (The Last Inch):** Used inside the rack (DAC cables) or the walls of your home. It moves electrons. It has high resistance and is subject to “crosstalk,” effectively capping its useful distance to 100 meters for high speeds.
- **Fiber (The Long Haul):** Used for everything else. It moves photons (light). Unlike copper, it has almost zero resistance and immune to electromagnetic interference.
- **Seabone (The Backbone):** The Internet has a spine. Networks like **Sparkle’s Seabone** are Tier-1 backbones — massive fiber pipes that carry traffic between continents.
- **RF Activity (The Air):** The “last mile” is often invisible. This is the 2.4GHz and 5GHz hum of Wi-Fi, the licensed bands of 5G towers, and the microwave backhaul links connecting remote towers.
- **Weather as a Component:** The Internet is tethered to the climate. A cloudy week in New Mexico drops solar generation, forcing data centers to switch to grid backup or natural gas. High heat reduces the efficiency of cooling towers, literally slowing down the ability to process data (thermal throttling).

### 3. The Pulse: Daily Internet Vital Signs

If the Internet were a single organism, here is what its daily metabolism would look like:

- **Daily Users:** ~5.4 Billion people (roughly 67% of humanity).
- **Websites & Apps:** There are 1.1 billion websites, but only about 193 million are active.
- **Protocols:** The world speaks TCP/IP. Roughly 80% of traffic is video (UDP/QUIC), but HTTP/HTTPS (port 443) is the universal dialect for web pages.

**Communication Volume:**

- **Emails:** ~361 Billion sent daily.
- **Web Calls:** Over 620 Million daily meeting participants across Zoom and Teams alone.
- **DNS Requests:** Trillions per day globally. A single major provider handles ~124 Billion daily.

### 4. The Volume: Internet as Water

We generate approximately **402 million Terabytes** of data every single day. The human brain cannot visualize a “Terabyte.” Let’s use water instead.

- **The Conversion:** 1 Gigabyte (GB) = 1 Gallon of water.
- **Daily Generation:** 402 million TB = **412 Billion Gallons**.

**What does 412 Billion Gallons look like?**

- It is more than the entire United States consumes in fresh water every day (322 billion gallons).
- It would fill 623,000 Olympic-sized swimming pools every 24 hours.
- If you poured it into Lake Tahoe, it would take about 3 months to fill the entire lake from empty.

We are not just surfing a “web.” We are navigating a daily flood that rivals the consumption of a superpower nation.

**This is the harbor we built.**

And it’s not just failing. It’s sinking under its own weight.

We designed today’s Internet around a single question: *Who are you?*

Present your username. Present your password. Present your token, your certificate, your API key. The system checks the list. If your name is on it, you’re in. If it’s not, you’re out. Binary. Clean. Simple.

Simple — and catastrophically broken.

A credential stolen is a credential used. The system cannot tell the difference between you and someone holding your keys. It wasn’t designed to. It asks for the password. It gets the password. It opens the door. This is not a flaw in implementation. It’s a flaw in premise.

We call it the **Passport Fallacy**: the belief that possession equals identity. But a passport can be forged. A key can be copied. A token can be harvested from a phishing email at 2 AM and replayed against your production systems by sunrise.

Every major breach of the last decade walked through the front door carrying valid credentials. We didn’t fail to build walls. We built walls that can’t tell friend from imposter.

The second weakness is temporal — permissions frozen at the moment of asking.

The Passport Fallacy is about identity. This one is about time. We call it the **Snapshot Fallacy**: the belief that what was true at login stays true.

The Internet checks your permissions once — at login, at the start of the session, at the moment you ask. If you’re allowed to do something at 9:00 AM, you’re allowed to do it at 9:01, at 9:02, and at 10:42. And midnight. The system took a snapshot and assumed the picture wouldn’t change.

But everything changes.

The network congests. Disk I/O spikes. An attacker begins probing the perimeter and finds a zero day. Or, perhaps a vulnerability is disclosed in software you’re running. A colleague with the same access level is terminated for cause. An insider is coerced.

The threat landscape at 9:00 AM is not the threat landscape at 9:01. Sixty seconds is an unbridgeable chasm.

Even legitimate users, with legitimate credentials, doing legitimate work, should sometimes be told: not right now. Not because they’ve done anything wrong. Because the environment shifted. Because the system is under stress. Because what was safe an hour ago isn’t safe anymore.

We froze authorization in time. But time doesn’t freeze. The Internet we built can’t feel the difference between calm seas and a gathering storm — so it grants the same access in both.

And beneath it all — the oldest rot.

We built the Internet as if it floats in a vacuum. Abstraction upon abstraction. Cloud upon cloud. We pretend that code is weightless, that data has no location, that our systems exist somewhere outside the physical world.

But they don’t.

Code runs on servers that draw power, generate heat, sit in buildings, in cities, in nations with laws and treaties and histories. Data crosses oceans through cables laid on the seafloor. It touches sovereignty. It touches culture. It touches sacred ground.

The digital world has weight. We just built an Internet that can’t feel it.

We call it the **Vacuum Fallacy**: the belief that the digital world floats free of the physical one.

This is the harbor we’re standing in.

Not a shelter. A structure so heavy with decades of patches and exceptions and workarounds that we’ve forgotten what the original pilings looked like. Barnacles on every surface. Technical debt so thick the water can’t move. We’re not just at risk of collapse. We’re at risk of never moving at all, sinking in place.

The harbor isn’t just unsafe. It’s anchoring us to a past that no longer works.

The age of autonomous agents is here. Billions of AI systems making real-time decisions without human oversight, at speeds no guard can match. The harbor was built for human traffic, human pace, human judgment. It was never designed for this.

We don’t need higher walls. We don’t need faster guards. We need to leave.

What if the Internet could feel its own weather? What if trust wasn’t a key you hold but a weight you carry — earned through behavior, tested under stress, adjusted in real time? What if authorization wasn’t a question asked once at the door, but a continuous negotiation between what an agent wants to do and what the environment can safely bear?

*What if we built an Internet with physics?*

By “physics,” we mean continuous, environment-aware trust. Not credentials checked once at the door, but authorization that responds to real-time conditions — network congestion, attack patterns, system load, who’s watching, and so many other variables. Trust that contracts when risk rises and expands when conditions improve. An Internet that can feel its own weather and adjust accordingly.

A ship in harbor is safe.

But this harbor can’t hold.

**The crossing begins.**

## **In Practice**

**For CISOs:** The three fallacies (Passport, Static, Vacuum) are the root causes of your major incidents. Stolen credentials, stale permissions, and context-blind authorization are not edge cases — they’re the architecture.

**For Infrastructure Engineers:** Your observability stack is already collecting environmental data. The question is: are you using it to inform authorization decisions in real time?

**For AI/ML Teams:** Autonomous agents will expose every weakness in static authorization. If your AI can’t adapt its behavior to environmental conditions, it will either be too constrained to be useful or too dangerous to deploy.

Tomorrow: [Vessel](https://medium.com/@chrisperkins505/vessel-32bb759ebda2) — The Voyage, II

Next: Day 2 — Vessel
