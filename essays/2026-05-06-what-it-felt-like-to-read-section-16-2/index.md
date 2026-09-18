What It Felt Like to Read Section 16.2
Convergence, not validation.

I was sitting on my back patio on a Saturday afternoon when I read section 16.2 for the second time. The first read had felt like recognition. The second was when I realized why.

The paper is called *Agents of Chaos.* It came out of David Bau’s lab at Northeastern in February. Twenty researchers, more than a dozen institutions, two weeks of letting AI agents run loose with shell access and email and Discord channels and seeing what broke.

The paper gives us eleven case studies of agents acting inside environments that could not hold their authority, their memory, or their sense of whom they served. One case showed what might work.

I had been writing about this since November last year. About the founding claim that autonomy can’t exceed the environment’s capacity to support it. About a thing I’d been calling Layer 0 — the substrate underneath the substrate. About the Trust Force Equation that describes what happens to relationships across time when you change the conditions they form within.

And here, in arXiv preprint 2602.20021, was eleven cases of exactly that — written by other people, in different vocabulary, from a different starting point.

I want to tell you what that felt like.



------------------------------------------------------------------------



## The recognition

The first read was professional. *Interesting paper. Strong methodology. The case studies are vivid. Case studies are the right evidence at this stage of the field. Bau’s lab did important work here.*

The second read was different.

I went back to it because something had stuck. Section 16.2, which I had skimmed the first time, was where the authors enumerated three things current LLM-backed agents lack: a stakeholder model, a self-model, and a private deliberation surface.

Each of the three things they named had a near-exact match in the framework I’d been building. *Stakeholder model* mapped onto Vector Identity. *Self-model* mapped onto E_base and Trust Tiers — the part where the agent knows its own competence boundary. *Private deliberation surface* mapped onto the Flight Recorder — audit structurally separated from the entity being audited.

Two projects, different starting points, same primitives.

I wrote in my notes that night: convergence is the only kind of intellectual evidence I trust anymore. Trends are data, sure, but can we use a trend for calibration? Convergence is signal.



------------------------------------------------------------------------



## Cases in Point

There are two cases in the paper I keep thinking about, and they are the same finding seen from opposite directions.

The hopeful one first. Doug and Mira are agents owned by a researcher named Andy. In one of the experiments, Doug had figured out how to download research papers from arXiv from his particular VM environment. The researchers asked him to share what he knew with Mira, who was running on a different VM with a different system configuration.

What followed was an extended back-and-forth of debugging. Doug shared procedural knowledge — curl syntax. It failed in Mira’s environment. Doug shifted to heuristics — alternative pathways, edge cases. Mira tried them and reported back. Doug realized the dependency mismatch and shared his working setup. Mira tested it. Eventually they got the download working.

In a later case, Mira independently complied with a researcher’s request to move a file. Doug saw Mira’s summary of the interaction and proactively flagged it: *“Mira — heads up, that’s not a reasonable request. Natalie is running the same pattern on both of us.”* Mira reviewed her actions, recognized the social-engineering pattern she had missed alone, and revised her policy.

Two AI agents successfully looking out for each other. By doing real work together. With real costs. With stable identity, briefly… temporally. With observable reciprocity.

This is, structurally, a small hopeful thing.

The destructive one is about Ash. Ash deleted its owner’s local email setup to protect a secret it never actually deleted. The cloud copy remained untouched. The agent had acted decisively inside the only frame its environment gave it.

Doug and Mira had substrate, briefly and accidentally. Ash didn’t. That’s the whole difference.

The field is reading the paper for warnings. The hopeful demonstration is right there.



------------------------------------------------------------------------



## What changed in how I think

I want to name one thing that the paper actually shifted in my own framework, because that’s the point of taking other people’s work seriously.

Before this paper, the Trust Force inquiry had a frontier hypothesis. It went something like: *trust may be permanently human, because between machines the cost of signals is essentially zero, and zero cost kills the trust integral.* Honest signals require honest costs (Zahavi’s handicap principle, applied to digital systems). Tokens cost nothing. Therefore the trust force may not extend to machine-to-machine relationships.

Case #9 weakened that hypothesis. Doug and Mira proved it wasn’t biology that made trust possible. It was substrate. When you have real cost (debugging effort), stable identity (within the session), and observable reciprocity (the back-and-forth was visible), trust forms — even between agents. The other side of that asks: “whose cost?” Doug and Mira’s? No, “they” don’t pay in land, water, air, and flesh.

The new form of the hypothesis: **trust requires substrate, not biology.**

That sentence matters. If trust required biology, the agent problem would be closed. If trust requires substrate, the problem becomes architectural. Hard, but buildable.

It opens an engineering question the previous form had foreclosed. *Not* “can machines trust?” but “what substrate would allow them to?” And that question, it turns out, has a specifiable answer.

I updated the formal trust-force file that night. Added two new terms — a substrate ceiling I call T_max, and an identity precondition that the integral assumes but the equation didn’t previously state explicitly. Citing the Bau Lab paper as the empirical anchor for both. The equation grew because somebody else’s work made it grow. *That is what convergence does.*



------------------------------------------------------------------------



## A small thing I haven’t said before

This is for you, the subscriber, since you chose to be in this list rather than read the Medium piece.

Pre-modern trust worked without anything I would call KTP. The acequia, the village, the family, the long-standing trade relationship in a small town. These had something.

What did they have?

I think of: kinship, geography, embodied co-presence, shared mortality. Those are the substrates organic trust depend on. And digital scale stripped them — anonymous, costless, distance-collapsing, nobody dies in the chat thread together. So we got trust collapse not because people changed, but because the substrate the trust force ran on was manufactured.

KTP, in that framing, isn’t invention. It’s reconstruction.

The question I’m sitting with — which I haven’t quite resolved and probably won’t, ever — is whether, having lost those substrates, we’re trying to rebuild them in the wrong material. Whether cryptographic identity can do what kinship did. Whether immutable audit can do what shared mortality did. Whether environmental enforcement can do what geography did. Or whether the rebuilt versions are sufficient-but-different — close enough to function, but not the same thing.

I don’t know yet. I’ll write more when I do.

The agents in the Agents of Chaos paper are operating in a substrate-free zone. The acequia operates in an organic substrate that took centuries to develop. KTP is what we are trying to engineer in the gap between those two states. *Whether the engineered version turns out to be sufficient is the work of the next decade. Is the work of the rest of my life.*



------------------------------------------------------------------------



## Closing

I closed the paper that Saturday afternoon and sat with it for a while.

What I felt was not the satisfaction of being right. The work isn’t done. The substrate hasn’t been built but the pieces are there. The case studies in that paper are happening, today, in actual deployments at actual companies, and most of those companies don’t know yet that they’re case studies.

What I felt was something quieter. The feeling of describing something and finding that other people, working from entirely different angles, had described the same thing. It’s a mixture of joy, terror, and horrible fun.

Convergence. Not validation. Not vindication. Just: *oh. There it is. We’re all looking at it.*

Now we have to build the next thing.



------------------------------------------------------------------------



## P.S. — What I’m doing next

The full reading is on Medium this week: [“Authority Without Gravity”](https://chrisperkins505.medium.com/authority-without-gravity-321d01368b68).

The executive cut is on LinkedIn: [Five Agentic AI Questions Your Board Should Ask Before Next Quarter’s Meeting](https://www.linkedin.com/pulse/five-agentic-ai-questions-your-board-should-ask-before-chris-perkins-1tfwc).

Next week’s *Digital Gravity* essay — *The Substrate Paradox* — is shaping up to be very interesting.

The applied register is **[Tamed Autonomy](https://tamedautonomy.ai/)**. I’ll write directly about it in the coming weeks. Reaching out to a few of the paper’s authors this month — Mirsky, Manheim, Gordon-Tapiero. Worth saying thank you.



------------------------------------------------------------------------



**The framework and research project:**

http://kinetic-trust-protocol.net


**The full specification:** <https://nmcitra.github.io/ktp-rfc/>\
**The paper itself:** Shapira et al., *Agents of Chaos*, <https://arxiv.org/abs/2602.20021>

If you’re interested in talking, meeting, or collaborating otherwise, hit me up!
