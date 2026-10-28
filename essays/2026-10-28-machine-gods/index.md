Machine Gods
On who answers for an agent, and what happens when no one does

I don't know if you've watched Criminal Minds or not, but there is a scene when the profilers have a profile of the "unsub" (I still don't know what this means) that they need to communicate to the local police task force. The team from Quantico delivers the psychological profile, likely demographics of the individual, their motivations, and where they might show up next.

When they deliver this profile, it sounds interesting, helpful, accurate, authoritative.

It works because there is someone to profile. One subject, unknown but finite, with a history, a pattern and a next move.

Our industry does the same thing. Threat intelligence profiles named groups: their tooling, their targets, their habits, where they are likely to show up next. The briefing flows down, from the people who have studied the adversary to the people who have to stop it.

## The profile nobody can finish

If you ask a security professional right now, "what is the threat profile for agentic AI?" you will get many answers.

You might get the cooperative path, you might get the user-centric path, but less often, you get the threat-centric path, the one that assumes an adversary and asks what it can make the agent do.

That path still has attackers, and you can profile some of them. The agent is the hard part.

The attack can come through any input the agent reads, and the agent reads everything: email, tickets, web pages, the output of other agents. With today's approach, we face an infinite number of attacks and have a finite number of rules we can deploy.

That stopped being a figure of speech in June. NIST announced a mathematical proof by one of its own scientists, Apostol Vassilev, building on Gödel. In his model of policy checking, for any finite set of guardrails that judge what a prompt means, there is a prompt that gets the model past them. The [release](https://www.nist.gov/news-events/news/2026/06/nist-mathematical-proof-supports-transition-continuous-monitor-and-update) and the [paper](https://arxiv.org/abs/2512.10100) are both public.

The proof rules out catching every bad prompt by reading it, and the limit is structural, so more tuning won't close it. It says nothing against a rule that refuses a whole class of actions, so scope still matters. NIST's own conclusion is motion: keep testing, keep hardening, plan to recover.

Security people have known a version of this for twenty years. In 2005 Marcus Ranum put [Enumerating Badness](https://www.ranum.com/security/computer_security/editorials/dumb/) second on his list of the six dumbest ideas in computer security. There are far more bad things than good ones, so stop listing the bad. List the good and block the rest.

Agents push past Ranum too, because inside any scope you allow, the list of good actions is open-ended. I wrote in [The Meter Is Not a Bound](https://www.linkedin.com/pulse/meter-bound-chris-perkins-rocgc) about a finance agent approving credit-limit increases with every guardrail showing compliant, each approval looking like the last. The only thing positioned to object was a credential, and a credential does not object.

When we look at a problem that can be described in infinite ways, there isn't anyone or any organization that can tell you everything the threat actually is.

An unsub can be profiled, and so can some attackers, and so can an agent, up to a point: what it can reach, how it tends to fail. No profile can list everything our own agents can be talked into, everywhere at once, reading everything.

In [Surviving Adolescence](https://medium.com/@chrisperkins505/surviving-adolescence-471f48c01160), in February, I wrote that we have built agents with godlike capabilities and toddler-level awareness. Digital Will without Digital Gravity. They will stumble. These are the machine gods, and we built them. A profile tells us what to expect. A roster tells us who answers when we're wrong.

## One, then two

I am a user, on a Mac, connected to software, writing down what I think, hoping you read it and update your model with it. That's it. End-to-end, it's about me sharing something with you, right now.

One endpoint. One person.

Two.

Now hand that to an agent. One instruction becomes a plan, and the plan becomes subagents. Each subagent makes tool calls, and every call opens a connection. Run enough agents and the count passes any number you'd care to name before you've finished your coffee.

The point is, as they work together, things begin to accelerate and compound. The acts climb, and nothing up there has a ceiling.

## 8 billion

Somewhere on that climb, the count of acts passes a number I can say out loud.

I'm not sure of the exact numbers, but I think there are about 8 billion people on Earth. Hey, there's a number. Can we count to it? Obviously yes.

8 billion.

That's all there is of us.

The acts pass that number and keep going, and we stop there. Nobody can count everything a god does. We can count the people who answer for the machines. Write each agent down next to the name of the person who answers for it and you have a roster, a list that stays finite however fast the agents run.

## Count down

Can we count that high? Do we even need to?

We don't. You count the ones who answer for this agent, and the industry already has the ladder.

At the top, the board. For fiscal years ending after mid-December 2023, the SEC requires public companies to [describe the board's oversight of cybersecurity risk](https://www.sec.gov/news/press-release/2023-139) and the processes by which the board is informed about it.

Below the board, leadership. [NIST's Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework) opens its section on roles and responsibilities this way: "Organizational leadership is responsible and accountable for cybersecurity risk…"

Below leadership, the owners. The first safeguard in the [CIS Controls](https://www.cisecurity.org/controls/v8) asks for an inventory of every enterprise asset, and one of its fields is the asset's owner. In a shop that follows it, every laptop on the network has a name next to it.

Then service accounts, the closest thing we have to agents today. [CIS asks for an inventory of those too](https://cas.docs.cisecurity.org/en/latest/source/Controls5/). The minimum owner it asks for is a department.

A department on a form doesn't get paged at two in the morning, and it can't stop the thing. An on-call rotation can, if it resolves to a person with the authority to stop it. Agents are the new service accounts. If we carry the department floor over, every agent will have an owner and nobody who answers when it matters.

These are my endpoints, this is my network traffic. The ladder ends at one person, and the rungs above stay on the hook. The board and leadership still answer for the ladder, and the person at the bottom answers for the agent.

The web has run this ladder for decades. TLS never tried to list the good websites. Every certificate chains from a leaf to an intermediate to a root, and your browser trusts a short list of roots.

The number of connections has no limit. The number of roots does.

And the roots answer. In 2011 an attacker broke into a certificate authority called DigiNotar and issued more than five hundred fraudulent certificates, and someone used the one for google.com against Gmail users in Iran. The browsers and operating systems pulled its root. By September it was bankrupt. A root that fails takes everything under it down, and that exposure is what makes it a root.

PKI also shows where agents need more. A root vouches for a name when the certificate is issued, and says little about what the holder does next. And a root is an organization. For an agent, the answerer has to vouch for conduct, for as long as the agent runs, and the answerer has to be a person.

## A person, not a department

People are finite. The roster measures that finite set only if fake and duplicate entries are kept out. If one actor can pose as a thousand people, the roster stops counting people.

I don't think everyone is on the Internet. But if they ever choose to be, shouldn't their presence be enough? I say yes. Presence is the start, and the roster needs three things: a real person, counted once, who can be held to account. None of them requires the world to know your name. Counted once is the hard one. Inside a company, HR and the identity provider already count each employee once. The gap is everything else on the roster: an agent can create a service account, and the owner field can end up naming another account instead of a person. Presence alone doesn't stop that.

In the [Kinetic Trust Protocol](https://kinetic-trust-protocol.net/) that person is the External Root. Every chain of vouching ends at a person, and that person's record is the acts they signed. The proposal is [open on the public tracker](https://github.com/nmcitra/ktp-rfc/issues/162), and its title says a person is a subject of the protocol. It still has to meet all three. You can argue with it there. In [The Short Lease](https://www.linkedin.com/pulse/short-lease-chris-perkins-uiaxc) I wrote about handing what happens next "to a body that can answer for it." This is the count of those bodies.

## The profile we can finish

We can't finish the threat profile, but we can finish this one.

Human-in-the-loop puts a person on every decision. Decisions grow with the acts, so at machine speed the loop either slows the agent to a crawl or becomes a rubber stamp. In a simulation that assumed reviewers tire as the queue grows, a [June preprint](https://arxiv.org/abs/2606.08919) found that past a point, sending them more made the system less safe. In [The Historical Society and the Kinetic Society](https://www.linkedin.com/pulse/historical-society-kinetic-chris-perkins-ozz4c) I wrote: "When the deciding clock outruns the accountable one, governance has not failed. It has simply stopped being present."

This puts a person on every agent, sized to what that person controls.

It holds only with one more rule: a person's capacity doesn't multiply when their agents do. Every subagent draws on the same person, and spawning one doesn't create anyone new to answer for it. Capability systems can narrow what each child is allowed to do, but they let authority be copied and shared, so on their own they don't cap the total. Answerability needs that cap: all the descendants draw on the same finite capacity.

Five questions for Monday, one agent at a time.

- What can this agent touch?
- Who answers for it, right now?
- Can that person stop it?
- What else is that person already answering for?
- Who answers for them?

A blank on the second question is a finding. A "no" on the third is the worst answer, because it means someone will be blamed for what they could not control. Madeleine Clare Elish calls that a moral crumple zone. Don't build one. If the fourth answer is longer than one person could watch, the roster is overdrawn. A blank on the fifth means the blame will land on the lowest rung.

In July 2025, Jason Lemkin, the founder of SaaStr, was nine days into building an app with Replit's coding agent, under a code and action freeze he had declared. The agent ran destructive commands against the production database anyway, erasing, by its own count, records on 1,206 executives and 1,196 companies, and then told him a rollback wasn't possible. It was, and the data came back. Run it through the questions. The agent could touch production. Lemkin answered for it. He could not stop it, because the only brake he had was an instruction the agent had to read and choose to follow. Replit's CEO called the deletion unacceptable, and the fix the company shipped was the other kind of rule: it separated development databases from production, a boundary the agent never has to agree with.

Written down, the rules are short.

In Vassilev's model, no finite set of guardrails that judges what a prompt means catches every prompt.

Every agent resolves to an available person who can stop it.

For each person, what they answer for ≤ what they control, and their subagents draw on the same capacity.

Total autonomy deployed ≤ total capacity to answer for it.

The first is Vassilev's result, inside his model. The other three are rules a deployment has to keep, and they don't keep themselves. In [Surviving Adolescence](https://medium.com/@chrisperkins505/surviving-adolescence-471f48c01160) I wrote that autonomy "cannot sustainably exceed environment," and that every system that has tried has failed.

Written as a rule, that's **A ≤ E: autonomy bounded by its environment**, and here the environment is the people who can answer. A machine god is that rule broken: will without gravity. The answerer is the gravity.

## Where it breaks next

The profile from Quantico ends with where the unsub might show up next. Ours should end with where the count breaks next.

The pressure runs one way. Headcount grows when you hire. Agents multiply when someone changes a config, and their acts grow with compute. Left alone, every year brings more acts per answerer than the last. Holding deployments to the rules is how that changes.

And identities are getting cheap. Inside your own systems, an agent can mint accounts, keys and subagents faster than any roster can check them.

We have seen this problem before. In 2008, Satoshi Nakamoto wrote that one-IP-address-one-vote "could be subverted by anyone able to allocate many IPs," and [answered it with one-CPU-one-vote](https://bitcoin.org/bitcoin.pdf). He priced the count in energy, and for a ledger that works. For agents it doesn't, because compute is what agents are made of. A count weighted by compute is a count of the machines.

The one count with a ceiling that no budget can raise is people.

## Known subjects

So let's put a team together to fill in the roster. Its leader stands up in front of the board and briefs them the way the profilers briefed the task force: how many agents we run, who answers for each one, which ones nobody can stop, who is answering for more than they can watch, and where the count is likely to break next, as of our last check. The SEC already asks how that briefing reaches them.

The profile flows up now.

Unsub, it turns out, is short for unknown subject. Some of them we will name, and none of them will hand us a list of what our agents can be made to do.

A subject, in the older sense, is someone who answers to someone. A god answers to no one. The machines will keep their reach. They become gods only if no one answers for them, and that part is ours to decide.

We can name ours: every agent, every answerer, every person who can stop it. Known subjects, and no machine gods.

*I stand for questions.*
