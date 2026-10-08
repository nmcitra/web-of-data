The Meter Is Not a Bound
On user-directed, unbounded agency, and the one limit it always has.

On October 7, Jeetu Patel wrote that "your organization's token efficiency is directly proportionate to your security posture." 

I work for him, several floors down, and I nodded. Most of the thread nodded. Then the conversation unfolded and did something better than nod. It argued, and by the end of the day it had walked, comment by comment, from efficiency to a question about authority.

I am writing this for the person who will direct an agent this quarter and never train one. 

The SOC lead buying the autonomous tier. 

The platform engineer wiring an agent to a key.

The question you will be asked is "how many tokens?" The harder question almost no one will ask you is what the agent is allowed to do and who is accountable when it does something it shouldn't have.

## Three steps in one thread
The first step was Jeetu's. Machine-scale attack needs machine-scale defense, and defense at that scale is paid for in inference. Abhijit Ghosh put the limit on it: the attacker needs one success, the defender needs every block, so token parity still loses, and most breaches begin with a stolen credential that costs the attacker essentially nothing. 

Both are right. Efficiency matters where the fight is at machine tempo, and it is not the whole posture.

The second step was Anshuman Goswami's, in the register of someone who has watched it happen: "business thinks autonomous SOC is protecting but agents stopped protecting in between because tokens are not available." Protection stopped and nobody was told. He asked for observability of dysfunctional agents. I replied with a hospital, an ER that closed with the sign still lit. The comment is [linked here](https://lnkd.in/p/g23hMceT). This piece is the mechanism under it.

The third step was the one the thread took almost without noticing. 

Hoshedar Mana: "More tokens spent on a poorly governed agent just means faster & larger mistakes." 

Gaurav Bhatnagar: "A defensive agent with broad authority is itself an attack surface, so what it may act on should be bounded and enforced outside the model." 

Jon-Rav Shende: "Ten million malicious requests hitting an authorization rule should not require ten million model calls to counter." 

Three people, from three directions, had stopped talking about tokens. They were talking about where the bound lives.

## A goal and a key
Here is the configuration: an agent is given a goal and a key. 

The goal is open-ended by design, because open-ended is what autonomous is selling. Handle the queue. Protect the estate. Close the tickets. The key is standing and broadly scoped. It was minted once, it lives for months, and it opens more than the goal needs. I wrote in [The Buffer and the Ditch](https://www.linkedin.com/pulse/buffer-ditch-chris-perkins-xbbpc) that we grant authority like a key, once, at the door. This is that key, and the thing holding it never leaves the building. And between the goal and the key there is no independent check on each action the agent proposes. 

Nothing asks, before the action commits, whether this one is allowed.

I have described this arrangement before without naming it. In [One Question Your Security Stack Can't Answer](https://www.linkedin.com/pulse/one-question-your-security-stack-cant-answer-chris-perkins-ipr1c), a finance agent at a mid-size lender, granted broad write access "to move faster," was approving credit-limit increases with no human oversight and every guardrail showing compliant, because there was no illegitimate signal to find. The signal was never the problem. The grant was.

I have started calling this user-directed, unbounded agency. The user directs. Nothing bounds. The budget is what remains.

The failure it produces has a name too: authorized inappropriate execution. The key said yes. The action was wrong for this host, this hour, this state of the world. It ran anyway, because the only thing positioned to object was a credential, and a credential does not object.

That last clause needs care, because a budget can stop a process.

OWASP's guidance for LLM10, Unbounded Consumption, says so plainly: rate limits, quotas, timeouts, throttling, limits on queued actions, graceful degradation. A hard quota blocks execution. 

So, let's distinguish three things so they don't get collapsed into one. 

A meter reports consumption. 

A cap enforces a limit on consumption. 

An authorization check governs a proposed action. 

The first two can be excellent and still say nothing about the third. The condition I am naming is what happens when an organization treats the first two as if they were the third.

In [The Short Lease](https://www.linkedin.com/pulse/short-lease-chris-perkins-uiaxc) I wrote that a lease is a leash with a clock in it. The leash says how far, right now. The lease says how long, before asking again. A budget is the clock without the leash. It says how long. It never says how far.

OWASP already holds both halves of this, and I pointed boards at both entries in [Five Agentic AI Questions Your Board Should Ask](https://www.linkedin.com/pulse/five-agentic-ai-questions-your-board-should-ask-before-chris-perkins-1tfwc). The question I gave them then was whether any agent could expand its resource footprint without a hard ceiling. That was the cap question. This is the other one. LLM06 is Excessive Agency, with three root causes: 

excessive functionality, 

excessive permissions, and 

excessive autonomy. 

OWASP defines the third as the system failing to require independent verification and approval for high-impact actions. LLM10 is Unbounded Consumption, and its attack list includes Denial of Wallet and Resource-Intensive Queries. 

Neither entry requires the other. An agent with a goal can run under tightly scoped permissions, and a chatbot with no agency at all can be run out of budget. The interaction is narrower and worth stating exactly: broad standing permissions, an open-ended goal, and no independent limit on each action let the two reinforce one another. The agent spends to pursue the goal, nothing checks the actions the spending buys, and when the spending stops, so does the protection. One configuration. Two line items.

An agent in that configuration is not more capable. It is careless, in the plain sense of the word. There is nothing its next action has to be careful of. It has no concept of how its or any actions are related to harm.

## The meter, examined
A budget has three properties that matter and the thread supplied evidence for each.

**It is silent about authority.**
The agent that runs out mid-task does the correct thing for a budgeted process. It stops. Nothing in it misbehaved. This is the kill switch without a handback from The Short Lease: the agent stopped correctly and then nothing happened. 

The difference between a lease and a lock is whether the return arrow exists, and a budget has no return arrow. What Anshuman reported is that the business did not know. My reading of why is that the console was built to show activity, and activity is what it keeps showing, because nobody built a field for authority. 

A schema is a decision about what can be known 

... as I put it in [There Is No Field For It](https://www.linkedin.com/pulse/field-chris-perkins-tff8c), and this one decided that spend was knowable and authority was not. 

The agent was not dysfunctional. The governance was.

**It enforces the wrong thing.**
A limit can be watched, rechecked, checked before each action commits, or made impossible to cross. 

Those are four different claims, and the industry collapses them into one. 

A cap is a real gate, and what it gates is spend. It will stop the agent at the ten-thousandth dollar whether the ten-thousandth action was isolating a compromised host or deleting a backup. It stands between the process and its budget. It does not stand between an action and the world. 

Authorized inappropriate execution passes straight through it, on budget.

**Other people can reach it.**
Tom Gamali asked the right question: how do we know whether we are applying more reasoning than the problem requires? Samer Abu Arisheh answered in three words: Token Exhaustion Attacks. 

OWASP's name for it is Denial of Wallet. Anything that makes the agent think harder spends the defender's budget at the attacker's price. Shende's rule is the counter. A deterministic authorization decision costs no inference per request. A model call costs the budget. Where you put the check decides whether the check has a meter.

## The swapped grant
Step back and the arrangement is upside down. The agent acts at machine tempo, thousands of consequential actions a session, on a key that lives for a quarter. The person who directed it is reviewed per ticket. Each is running the grant length that belongs to the other. A thing acting at machine tempo needs judgment at action grain, because a season-long grant lets it compound faster than any review can notice. 

We handed the machine the human's grant and kept the machine's for ourselves.

## Efficiency, with a condition
Jeetu's word is efficiency, and it is the right word. 

Here is how I would measure it: tokens a defender spends per attacker request, at equal coverage. The condition is the point. Without it a defender that does nothing wins, and the attacker's own cost belongs in the ratio too, since a request that costs them a model call is a different fight from one that costs them a packet. Lower the defender's side at equal coverage and the attacker's amplification drops with it. Buy more supply and the ratio does not move. You have bought a bigger tank for the same leak.

A measured example keeps this honest. Microsoft's FIDES enforces its policy deterministically, outside the model, before every tool call, which is exactly where Bhatnagar said the bound belongs. It still spent more tokens than the unguarded baseline it was compared against, because the governed workflow makes more model calls. Moving enforcement out of the model does not make the workflow cheaper. What it buys is narrower and more important: the authorization decision itself no longer depends on inference, so an attacker cannot run that decision out of budget.

A paper from August put the larger inversion in one paragraph. "Agentic AI is sold on a simple promise: the system keeps acting when the user stops watching," Hanjing Shi and Dominic DiFranzo write. 

"As stepwise supervision recedes, verification does not disappear; it moves into the runtime infrastructure that defines authority, records action, interrupts execution, checks outcomes, and supports repair." 

They call it the reduced-supervision paradox. 

Their evidence is what public artifacts disclose, not a census of what runs undisclosed, so read it as a map of the shift rather than a measure of it. I call that runtime infrastructure the environment, and Mike Storm calls it the Kinetic Infrastructure Layer, his contribution to KTP (https://github.com/nmcitra/kil).  

And the rule it has to enforce is older than this thread. Go back twelve months.. which is more if you're clocking on the machine clock.

## One action, bounded
In the Kinetic Trust Protocol the rule is:

**A ≤ E**
Autonomy cannot exceed environment, held per action, at commit. Follow one action through it.


A SOC agent proposes to isolate a production host. 

The grant says what it may ever do: isolate hosts in the segments it was given, never touch the identity provider, never power anything off. 

That is the ceiling, and it was set when the agent was onboarded, not when the alert fired. 

The envelope says what portion of that ceiling is safe here and now. 

The host is a payment server, it is peak hour, the on-call engineer has not acknowledged, and the agent has never isolated this class of machine before. 

That last condition is the one the key cannot see. A key says what the agent holds. A trajectory says what it has done, and the envelope reads the trajectory. Trust as trajectory: what an actor did last time becomes part of what the system sees now. 

In [Every Check Came Back Clean](https://www.linkedin.com/pulse/every-check-came-back-clean-problem-chris-perkins-mqwgc) I wrote that an empty history and a clean one look the same unless something is built to tell them apart. The envelope is that something, and here the history is empty. I wrote in The Short Lease that novelty shortens the lease, uncertainty shortens it, and irreversibility shortens it further. This is that sentence with numbers behind it.

The envelope narrows: quarantine egress, leave the host running, and the action needs a co-sign. The supervision floor says how much automation remains appropriate at this moment, and here it says assisted. 

Then the check, at commit: does this action, in this envelope, fit inside what the environment can currently support? 

The environment's capacity is a score, E_trust = E_base × (1 − R), where R is the stress the environment is under. 

If the action fits, it executes. If it does not, it fails to execute. That failure is the Silent Veto, and it is a decision about the action, not a budget reaching zero.

Now let the reasoning budget fall. Capacity is part of the environment, so E falls with it, and the agent loses automation one rung at a time, visibly: assisted becomes supervised, supervised becomes recommend-only. The supervision level is itself a reported signal, so the operator learns that protection has degraded because the degradation is the message, not because a stream went quiet. And the actions that were declared to run without inference, the known-bad blocks, the deterministic quarantine of anything matching a signature, keep running at zero model calls. 

The agent gets slower and more careful. It does not vanish behind a green light or the fog of night.

That is the difference between a meter and a bound. 

A meter tells you the agent is running. A bound tells the agent what it may not do, before it does it, whatever it was told. 

Authorized inappropriate execution lives in the gap between those two sentences.

## Decide before the surge
The hospitals here in Las Cruces already do this. All hospitals do this.

Crisis mode is declared before the surge, with a protocol that runs at zero deliberation while judgment goes only where it is needed. Translated: declare what must still run at zero model calls. Put it outside the model. Let the reasoning budget pay for the rest. And give the check something to read, because a bound with no evidence under it is a meter with better manners. 

The stack under that check is now clear:

The observation contract establishes what evidence must exist.

Observation SLOs establish whether that evidence is usable.

ARQ (availability, retainability, quality) translates technical condition into mission condition.

Ambient Breach Rate shows whether uncertainty is accumulating.

Semantic Join makes the evidence mean the same thing across organizations.

KTP uses that shared evidence to constrain autonomy.

[Ambient Breach Theory](https://kinetic-trust-protocol.net/research/ambient-breach) says that at machine scale the condition where you cannot tell the attack from the load is the default, and the meter is the first instrument to lie about it, because it reports effort, and effort looks like defense.

Three questions for Monday.

What is this agent allowed to do that it has not been asked to do?

What stops it, and is that thing a cap on spend or a check on the action?

Who else can reach the stop?

I stand for questions.
