Who Gets to Set the Clock?
On pacing the frontier, from well behind it.

You will never train a frontier model.

Neither will I.

Nobody reading this will sit in the room where somebody decides whether the next training run starts in March or in June. And yet for the past week that room has been the only thing anyone wants to talk about, because on September 12 the chief executive of Anthropic published an essay saying the industry must slow down, and by Saturday night the replies had sorted themselves into the usual two piles. He's right. He's selling something. [We Must Pace the Frontier](https://darioamodei.com/post/we-must-pace-the-frontier)

I want to write about that essay for the rest of us.

The people who will deploy the models, not build them. The school district's IT lead with four agents in production by Christmas break. The credit union with a hundred helping agents. The ops engineer whose pager goes off when one of them does something nobody wrote down.

Start with the dates, because the dates are where the story is.

The incident the essay cites happened in July. The public account of it is still contested and we are not going to settle it here. A confidential registration statement was filed on June 1. A new model shipped on September 1. The essay landed on the 12th. The waiver it asks for, the one that would let frontier labs coordinate on tempo without an antitrust case, does not exist and has no date.

Five events. Not one of them happened on your clock.

There are several meanings of now in this story, and they belong to different people. When the thing happened. When it could be described. When a company had a decision to make. When a government might.

> Two dates close together are a lead to follow, not a verdict to announce. Most of what you read this week skipped the following and went straight to the verdict.

### What is committed

Sort the essay's three steps by one question. Does this change a release date?

Step one is a team of outside evaluators. METR or someone like them. "Desks in our offices, access badges, and company laptops," employee-like access, and the right to publish what they find without Anthropic's editorial control.

That is real, and it is more than any other lab has offered.

It also changes no release date, and the essay says so: pacing "does not mean halting model training or technical progress." Evaluators verify. They report. They publish. Nothing about that person at a desk slows a training run or changes any date.

Step two is where the slowing lives. Limits on the rate of progress, agreed among labs, which the essay's own footnote says needs the government to mediate for antitrust reasons. Read the threat side of that sentence. Nobody has agreed to slow down. The step is a proposal about a meeting that has not been called.

Step three is agreements with China, in four levels ordered by how hard each is to verify. The essay concedes the hard case itself: "secret models which they don't test but may deploy in secret."

> The one committed act sits in the one step that does not pace. The pacing sits in the steps that are not yet acts.

Not a trick. It is the shape any candid version of this plan has to take. A company can hire evaluators by itself. It cannot slow its rivals by itself, and slowing only itself hands the lead to whoever didn't. Every step that touches the clock needs a government or a rival to agree, and so far neither has.

Which brings me to the question in the title.

A lab can set its own clock, and the essay opens by asking labs to compete on safety, "a race to the top." It closes by asking permission to stop competing on speed. Both in one document. That is not confusion. It is a man standing in a trap and describing it.

### Two sides

Here is the part that reaches you.

The rule underneath this publication is one inequality. Autonomy cannot exceed Environment.

    A ≤ E

An action is safe to let through when what it can do is bounded by what the place it lands in can absorb, refuse, or repair.

Two sides. You can satisfy it from either one.

- Lower A. Slower models, fewer capabilities per release, a cap on self-improvement, a checkpoint that holds a model at capability X until it clears test Y. That is pacing. Every proposal in this week's conversation is a proposal about the agent. A-side, all of it.
- Or raise E. Build the environment so that at the moment an action commits, something that is not the agent checks whether the action exceeds its ceiling and refuses it if it does. Identity that is a trajectory, not a badge. Permissions that expire. A record of what the agent touched that does not depend on the agent narrating it.

A Cisco executive wrote this version on Sunday in plain words: "An agent can decide what it wants to do. The infrastructure decides what it is actually allowed to do." [Liz Centoni](https://lnkd.in/p/gjBT558D)

Same inequality. Opposite side.

And here is why the side matters to someone who lives behind the frontier.

Pacing is a rate. It acts on how fast A grows over calendar time, on the frontier's clock.

A breach is a level. It happens when A exceeds E at an instant, at the point where an action commits, on your clock.

> A slower model that still exceeds your environment at commit time still breaches. Nothing about the rate protects the instant.

You could pace the frontier to a crawl and still be running every agent you own with permissions granted one at a time while the agent operates over everything those grants can be combined into. That is not a speed problem. It is a measurement problem, and it only runs one way. The environment is always overestimated, because grants are written singly and the agent does not act singly.

The essay's own stated use of the time it wants to buy is alignment, interpretability, testing. Understanding the agent. All A-side.

There is no line item in it for the environment, and the environment is the only part of this you will ever own.

### Where I stand

I should say where I am in this, because it colors the reading.

For a year I have been trying to find the doors where the people on the frontier sit. Find them, open them, walk in.

I have not been given the time of day.

The work might be getting out there but I am not. And that's ok! That is not a complaint about anyone in particular. It is what the incentive structure does. The A-side is where the models are, and the money, and the registration statements, so the A-side is where the attention goes. Havel's greengrocer hangs the sign in the window because the structure asks for it. You do not need to know what he believes to predict the sign.

The E-side is infrastructure, and working infrastructure is invisible by design.

I wrote in May that if the framework works, I will be the last to know. [If the Framework Works, You'll Be the Last to Know](https://open.substack.com/pub/kinetictrust/p/if-the-framework-works-youll-be-the) The parciantes on an acequia don't credit the founders. They show up with shovels.

The work is open. Someone will change the words.

> They can change the words. They can't change the math.

If it gets adopted the way it is supposed to, nobody will have an obligation to tell me. I'll know because I'll see the math. So when I say the E-side is the only part of this you will ever own, I am not selling you a door I got through. I am telling you which side of the inequality nobody is working on.

### What the evaluators are

One more thing on the committed step, because it will be sold to you as safety.

Elinor Ostrom's rules for a commons that survives include monitoring, graduated sanctions, and a cheap way to settle disputes. The plan, as proposed, supplies monitoring. Nothing else.

The evaluators will measure how far A has run past E and publish the gap. Publishing is a penalty only if someone else makes it one. A published finding is a record. A penalty is a turn. That is [the difference between a Historical Society and a Kinetic Society](https://www.linkedin.com/pulse/historical-society-kinetic-chris-perkins-ozz4c).

There is one clause that pushes back, and it is the only line in the plan that costs the company anything. Findings publish without editorial control. Redaction only for security, privilege, commercial sensitivity, third-party confidentiality. The reviewers can say out loud when a redaction "removed something important."

Commercial sensitivity is the widest door on that list.

So file the test now. The first unfavorable finding that ships unredacted proves the clause was expensive. The first redaction the reviewers flag in public proves the backstop works. A year with neither proves nothing.

Brian Roemmele laid out the financing calendar the same day and called the essay a pitch. [The Cure Is the Pitch](https://x.com/brianroemmele/status/2098786071522021642) His dates are real. They are evidence about motive, and motive is not the variable. A sincere lab and a cynical one publishing this plan give you the same structure, and the structure is what I just described.

> What the calendar tells you is where to look. If it is a pitch, its commitments are cheap signals. Go find the expensive signals.

### Your clock

[Kinetic Trust Protocol](https://kinetic-trust-protocol.net) is the E-side. Governance in motion.

It does not slow the agent and it does not read its mind. It checks the inequality where the action commits, using only what can be proven about the actor, the resource, and the state of the world at that instant. An action that exceeds its environment fails to execute instead of getting caught afterward. Regardless of what the agent wanted to do or was approved to do.

It runs at the tempo the agent runs at, because a boundary evaluated slower than the actions crossing it is not a boundary. It is a report.

Imagine your environment had wherewithal of its own. It could refuse an agent's update to the ticket-scanning system in the middle of the opening ceremony, however correct the change looked, because it knew what moment it was.

And when an action gets close to the line, the environment can turn the machine down before it turns it off. I call that deautomation. Take the automation out of the step, put a person in, and the chain of machine judgment breaks at the link where yours goes in.

No amount of alignment puts the opening ceremony inside the model. That knowledge lives in the environment, and the environment is yours. E is the commons.

The frontier will set its clock, or the government will, or nobody will. You were never going to hold that lever.

You hold this one.

And there is a second thing you hold, which this week's debate never names.

Amodei's evaluators are a lab paying, in desks and badges, to have someone attend. That is the scarce thing. I know what it costs. I have spent a year asking for it. Proof of work costs energy. Proof of stake costs capital.

> Proof of attention costs time on a human clock, and it is the only proof the frontier cannot manufacture faster by training harder.

It is not a signature. A signature says someone was there. That is a receipt.

Proof of attention says someone looked at this case, under a stated rule, before the action went through, and left a record a stranger could check. Arrive after the action and you have a report, not a gate.

That is the record I am building in the open, with others, under the name Open Trust Commons. Nobody grades their own homework there. The windows open on the calendar, not when someone feels like it, and when nobody shows up, the record says nobody showed up.

More on that soon.

What would your environment need to know, at the moment an action lands, to say no? And who would be able to prove they were paying attention when it did?

I stand for questions.

------------------------------------------------------------------------

Where the work lives

- This newsletter, Digital Gravity, on LinkedIn.
- A [Substack](https://kinetictrust.substack.com/) by the same name, with more.
- [My Medium page](https://medium.com/@chrisperkins505), with dozens of technical and philosophical explorations of these topics.
- Break the Chain, my first book, written before Kinetic Trust Protocol existed.
- The Physics of Intelligence research site: <https://kinetic-trust-protocol.net>
