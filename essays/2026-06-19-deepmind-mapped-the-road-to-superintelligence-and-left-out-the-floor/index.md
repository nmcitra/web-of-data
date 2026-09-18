DeepMind Mapped the Road to Superintelligence and Left Out the Floor


Fifteen of the most authoritative people in AI just published the map.

From AGI to ASI ([arXiv:2606.12683](https://arxiv.org/abs/2606.12683)) is signed by Shane Legg, who named modern AGI; Marcus Hutter, who formalized the upper bound of machine intelligence; and Allan Dafoe, DeepMind's own governance lead. It charts every road past human-level AI: four pathways to superintelligence — scaling, paradigm shifts, recursive self-improvement, multi-agent collectives — and a careful catalogue of the frictions that might slow each.

It is the most rigorous capability forecast in existence. And it is exhaustive in exactly one dimension.

Read it closely and you find the map measures, in beautiful detail, how powerful machines could become — and treats the question of what the world is able to bear as a footnote it sets aside on the first page. The sentence is right there in the research agenda:

> "To keep the scope of this report clear, we assume that AI Safety and Alignment will be solved to a sufficient degree, even in a post-AGI world."

That single assumption is the hole. Everything downstream is a map of how autonomy grows given that someone, somewhere, has already solved the question of who is allowed to act. But that question isn't a footnote to the capability story. It's the load rating of the bridge the capability drives across.

Here's the part that should stop a CISO cold.

The report doesn't just leave the floor out — it tells you, in its own governance section, why the floor won't build itself.

Dafoe's "military-economic adaptationism": actors that adopt power-enhancing technology are differentially selected to survive; actors that resist lose influence or disappear. Read the two passages together. The first assumes governance gets solved. The second explains why competition routes around it. The document names its own cliff — and then walks past it.

This is the whole [Disarm](https://kinetic-trust-protocol.net/disarm) thesis, conceded by the people building the thing. Map every road to superintelligence if you like. Forecast the autonomy all the way to the stars. The floor still has to be built before the climb is survivable — and "the floor" is not alignment. It's authorization: a substrate that bounds what an agent may do to what the environment can actually hold. Autonomy ≤ Environment. The report's own formal limit, AIXI, is defined as an optimizer that cannot model its own embedding in the world that must bear it.

Pure autonomy with no floor, in one line, by the people who wrote the bound.

So here's the call.

If you build agent platforms, IAM, or the control plane underneath them: the authorization layer is the work the establishment roadmap just told you it's assuming away. It is buildable now, in the open, and it does not require waiting for alignment to be solved.

Read the full reading — The Missing Floor — at [kinetic-trust-protocol.net/research/agi-to-asi](https://kinetic-trust-protocol.net/research/agi-to-asi), and the draft RFC at [/specs](https://github.com/nmcitra/ktp-rfc/tree/main/rfcs-txt). Then come break it. The bridge gets built by the people who show up before the traffic does.

[Disarm](https://kinetic-trust-protocol.net/disarm) the control plane.
