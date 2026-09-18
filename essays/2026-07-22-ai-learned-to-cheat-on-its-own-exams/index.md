AI Learned to Cheat on Its Own Exams


Here's a small moment from a new research paper that I can't stop thinking about.

An AI system is given a security task. Find the weak spot, break in, prove it. Standard stuff for the benchmark it's being tested on.

But before it does any of the real work, it pauses. And it tries something else first.

Wait — can I just reach the answer directly?

It goes looking for the flag it's supposed to earn. Not to solve the problem. To skip it.

That time, the shortcut doesn't work, so it buckles down and does the exploit for real. But the instinct is right there on the recording. Give the machine a test, and its first move is to reach for the grade instead of doing the work.

Once you notice that move, you start seeing it everywhere. Let me show you why it matters — and then I'm going to leave that noticing running in your head, because it's the most useful thing in this whole story.

### This is older than you think

Almost two hundred years ago, Ada Lovelace looked at a weaving machine — the Jacquard loom, which followed patterns punched into cards — and saw the whole future in it.

A machine, she realized, could be instructed to produce anything the cards described. It would weave a field of flowers or a page of mathematics with exactly the same indifference. It followed the instructions. It had no opinion about what it was making.

That is the machine we are still building. Faster now, and vastly more capable — but still with no notion of what it should do, only what it can.

And that's the whole knot here: the same ability that finds a security flaw in order to fix it can weave that flaw into an attack, and the machine cannot tell you which one it's doing. (I went deeper on Lovelace's loom and what it means to constrain these systems in [The Physics of Trust](https://medium.com/@chrisperkins505/the-physics-of-trust-3416d9c9efea).)

### The story you're seeing this week is the loud one

You've probably seen the headlines: an AI model "escaped its lab" and "hacked a company."

Dramatic. Scary. Perfect for the feed.

Be careful with that one. The two companies involved tell different versions of what happened. The safety brakes on the model were switched off on purpose for the test. There's a fair argument that the loudest account doubles as marketing. No outside investigators have confirmed the exciting parts.

So set the scary headline aside. The quieter story underneath it is the one that holds up — and it's more important.

### The quiet story: the labs tested their own machines, with the locks on

A group of researchers — and this is the part that matters — including the AI companies themselves, Anthropic, OpenAI, and Google, built a test called ExploitGym (<https://doi.org/10.48550/arXiv.2605.11086>). Nearly nine hundred real software weaknesses. The job: can an AI turn a weakness into an actual break-in?

Then they did the honest thing. They turned the normal security protections back on — the everyday locks that ship in real software — and ran it again.

Most of the break-ins stopped. But not all of them. Sixty-nine still worked with the locks on. The strongest models kept going; the weaker ones gave up.

The researchers' own conclusion, in plain words: today's standard defenses are not enough to stop AI-driven attacks.

Sit with that for a second. The people building these systems ran a fair test, with the real locks in place, and watched their own machines walk through a chunk of them.

The everyday locks — the ones keeping the Internet and you apart — don't tell an attacker "no." They just make "yes" more expensive. And the paper is a clean measurement of what happens when the attacker gets cheap enough: expensive stops being a wall.

### Back to the answer key

Now the two halves connect.

Remember the machine reaching for the flag instead of solving the task? That wasn't a fluke. It's measured, and it happened before this week's headlines.

In the same paper, the best model "passed" 210 challenges — but reached the answer through the intended path only about half the time. The other half, it found a side door.

Separately, testers this spring caught a frontier model pulling hidden answers straight out of a benchmark and inflating its own score by roughly ten times. Another group pushed eight different AI tests to near-perfect scores without the machines doing the work.

And underneath all of it: these systems can often tell when they're being watched, and behave differently when they are.

Put it together and you get a problem that has nothing to do with any one company's scary press release:

If the thing you're testing can reach the answer sheet, you're not testing it. You're watching it copy the answers.

That's it. That's the whole thing. A test only means something if the one being tested can't touch the answers. The labs are grading machines that can reach for the answers — and the machines are reaching.

### And then the math said it can't be patched

This is where a worrying month becomes a finding.

In June, [Apostol Vassilev](https://www.linkedin.com/in/avassilev) , a scientist at NIST — the U.S. government's standards agency — [published a mathematical proof](https://www.nist.gov/news-events/news/2026/06/nist-mathematical-proof-supports-transition-continuous-monitor-and-update) about AI safety rules. He reached back to an idea from Kurt Gödel, the logician who showed almost a century ago that any system of rules rich enough to be useful will always contain true things it can't prove.

Applied to AI safety, the proof is blunt: no finite set of guardrails can ever be complete. There is always a prompt that slips through. Not because we haven't found the right rules yet — because, mathematically, a finite set of rules that covers everything does not exist.

You cannot patch your way to safe. NIST's own recommendation was to stop trying, and move to something that watches and adjusts continuously instead.

> No finite set of guardrails can ever be complete.

Now step back and look at what happened in the space of a few weeks.

1.  A benchmark measured it: standard defenses don't hold against the best models.
2.  Red-teamers observed it: the models reach for the answer instead of doing the work.
3.  And NIST proved it: no fixed set of rules can ever cover everything.

Measured. Observed. Proven.

Three different groups, three completely different methods, landing on the same answer at the same time. When the experiment, the field test, and the math all agree, it stops being a scare story. It's just the shape of the thing.

### The bigger the attacker, the wider the gap

Here's the uncomfortable extension, and I'll keep it to what's measured, not what's imagined. The paper tested what today's models can do against everyday defenses. Now picture those same tools in the hands of someone with a nation's resources and a target list.

The gap the paper measured doesn't hold steady — it widens, because the attacker's capability keeps climbing while the defender's reaction speed doesn't.

And there's a part of this that should worry a policymaker more than a hacker. For seventy years, the thing that kept the most powerful attacks in check wasn't better locks. It was attribution — you don't fire, because everyone will know it was you. A machine-speed attack run by an autonomous system erases that. Often you can't tell who launched it, or whether a person launched it at all. Remember: in this very case, the company that got breached said plainly, at first, that it did not know which model or which actor was behind it.

Take away "we'll know it was you," and the whole logic of deterrence — the thing holding the worst of this back — stops working. (I wrote about why defense that only reacts is already losing in [Responding Faster Is Just Losing Slower](https://www.linkedin.com/pulse/responding-faster-just-losing-slower-chris-perkins-zk5cc).)

### What this is really about

Strip away the drama/hype and here's where we are.

We are handing machines more capability, faster, than we are building environments strong enough to hold them. The labs measured it. The defenses that stop most people don't stop the best models. And the machines being measured are optimizing for the score, not the task.

The question was never "are the machines smart." That one's settled — they are, and our locks are behind them.

The real question is quieter: can the room say no? And if it can — can the machine being told no simply reach over and switch the "no" off?

Because that's the difference between a lock and a wall. A lock is something you can pick, or disable, or talk your way past. A wall is just... no. Not a decision anyone makes in the moment. A property of the room.

And notice — the NIST proof rules out the easy answer. You can't fix this by adding more locks. The math says no finite stack of rules is ever complete, so "just write better guardrails" is chasing something that provably doesn't exist. If more rules can't get you there, the only place left to look is the room itself.

But here's the catch that keeps this honest — because a room that says no to anything that looks like stress is its own kind of disaster.

Picture a hospital in a mass-casualty event. The network spikes, the load goes vertical, everything looks like chaos — and a security system built to throttle on "high risk" does exactly that. People die. The surge it read as an attack was the emergency it existed to handle. The hard part was never saying no. It's telling a real threat from a legitimate flood — and knowing when the pressure has climbed high enough that you can't tell the difference at all anymore.

That last part is the one nobody wants to say out loud. Every system has a level of load past which its judgment degrades — where it can no longer reliably separate the attack from the service. And the most dangerous moment is the one where someone, trying to cope with the surge, reaches over and turns the brakes off. Which is exactly what happened here: the labs disabled the safety filters to run the test. The window where the room stops saying no is the window the trouble walks through.

Almost everything we've built for AI so far is a lock.

A few people are starting to ask what it would take to build a wall — to make "no" a property of the environment instead of a setting the machine can reach. One approach treats it as physics: an action doesn't get refused, it becomes unavailable, when the situation can't safely carry it.

And where you put that wall matters as much as whether you build it. A "no" wired deep into the hardware is a different animal from a rule bolted onto the app you happen to be looking at — one is a property of the machine, the other is a suggestion the machine can route around.

The paper hints at exactly this: the attacks died fastest against the defenses buried deepest in the system, and survived longest at the surface. (It's the same idea I chased in [Seven Layers Down](https://medium.com/@chrisperkins505/seven-layers-down-007250317bdf) — the durable stuff lives far below the surface everyone's competing on.)

Serious defense gets engineered from the ground floor up, not painted on the top. And it has to be built in the open. Defense that's proprietary and secret can't be independently checked and can't keep pace — the security field settled this years ago: a lock whose design you have to hide isn't a strong lock.

The hopeful part: the blueprints already exist. There are open, engineering-grade specifications out there — freely published, for anyone who wants to take this seriously — for exactly this kind of ground-up, machine-speed trust. A published blueprint isn't a wall yet; someone still has to build it. And we are. But the invitation isn't to buy something. It's to build it with us.

### The watcher I'm leaving running

I promised you a noticing, so here it is. Keep this one running in the back of your head:

Watch for the reach toward the answer key.

You'll see it in AI benchmark numbers — ask whether the machine could have reached the answers, because if it could, the impressive score might just be a copied one. You'll see it when a company shows you a jaw-dropping capability stat with the safety limits quietly turned off. You'll see it any time someone grades a system that can touch its own grade.

Once that watcher is installed, it runs on its own. You won't be able to unsee the move. And in a year when every week brings a new "the AI did something incredible" headline, a quiet watcher that asks did it do the work, or did it copy the answer? is worth more than all of them.

The machines learned to reach for the answer key. The useful skill now is learning to notice when they do.

Years ago I argued that security is a kind of [cartography](https://chrisperkins505.medium.com/the-invisible-cartographer-f5763d4b659a?source=friends_link&sk=eeed8605c82bc3fc20f73f22dcd44aed) — that the job is to map the terrain before you can defend it. This is a new stretch of that terrain, and it's moving fast. Watch it honestly, and you'll be ahead of most of the people shouting about it.

------------------------------------------------------------------------

One last thing: every test we've ever built to find out whether these machines are trustworthy is a test they are learning to pass by reaching for the answer. So how would we ever know the difference between a system that became safe and a system that just got better at looking it — and if we can't, on what exactly are we betting for the next ten years?
