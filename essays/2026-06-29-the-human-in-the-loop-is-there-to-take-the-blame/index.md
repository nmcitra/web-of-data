The Human in the Loop Is There to Take the Blame
They can't catch the machine, and were never meant to. Real accountability lives where the stake is, not where you parked a person to absorb it.

Every conversation about risky AI ends the same way. Someone raises the failure case (the wrong benefits denial, the bad flag, the hallucinated record) and someone else says the magic words: "We'll put a human in the loop." The room relaxes. A person will be there to catch the machine when it's wrong. Decision made.

I want to take that reassurance seriously, because it's load-bearing for a lot of deployments, and then tell you what the research shows. It doesn't work. Not "works with caveats." It has been tested, in peer-reviewed and replicated studies, and the theory behind it is wrong.

## What the evidence says

Ben Green's 2022 review in *Computer Law & Security Review* went through the human-oversight policies governments wrote and the assumptions underneath them, and found each one falsified in practice:

- **Automation bias.** People defer to the machine even against their own expertise. In one study, police judged a facial-recognition system to be roughly three times more accurate than it really was. The human isn't a check on the machine. The human believes the machine.
- **Deskilling.** Hand a reviewer conclusions instead of problems and they lose the practiced facility to judge them. Checking the last step of a decision without doing the work that leads to it is harder, not easier.
- **Transparency backfires.** Show the reviewer the system's reasoning and they get *more* deferential, not less. More sub-conclusions to nod along to.
- **Discretion brings back the bias.** When humans do override, they often re-inject the bias the system was supposed to remove, overriding more readily for some groups than others.

These effects persist even when people know about them, are trained against them, and are told explicitly to resist. That is the finding that ends the debate. You cannot train your way out of a structural problem.

## What the human in the loop is actually for

If the reviewer can't catch the machine, why is the position there at all? Dan Davies has the answer in one phrase: an **accountability sink**. The human in the loop isn't positioned to catch the error. They're positioned to catch the blame. The institution gets to deploy a high-stakes system, point to "human oversight" when challenged, and when something goes wrong, the failure lands on the operator who, per all the evidence above, never had a real chance to stop it.

Madeleine Clare Elish named the role exactly: a **moral crumple zone**. In a car, the crumple zone is the part engineered to absorb the impact so the occupants survive. In an automated system, the human operator is the part positioned to absorb the moral and legal impact so the system, and the people who deployed it, survive. The caseworker. The clerk. The cop who signed off because the screen said so.

## Why it fails, in one line

The principle underneath it is the same physics this newsletter keeps coming back to. You cannot hold a person accountable beyond their capacity to control the outcome. Assign answerability and deny real control, and you don't get oversight. You get a scapegoat. Accountability has to sit inside the boundary of what someone can govern, or it isn't accountability at all. It's just where the blame is parked.

That's the Zeroth Law of this whole framework, turned to face a person instead of a machine: authority can't exceed the environment that has to carry it. A human handed responsibility for a system they can't realistically override is over that line by design.

One caution, because this principle can be misread into an excuse. The remedy runs one direction only: bring control up to meet the accountability, or don't deploy. Lowering what we ask of a person to fit what they can't do is how the institution slips the hook, not how the operator does. Answerability stays. You make it real by giving it teeth, not by filing them down.

## This isn't accountability. It's a costume.

Notice the swap that just happened. We started out trying to make a system safe, and we slid into deciding who to blame. Those are different projects, and the human in the loop only ever served the second one.

Real accountability follows stake. The party answerable for an action is the one that had something on the line when it was taken: that authorized it, put their name or their capital or their standing behind it, and carries the cost when it goes wrong. Skin in the game isn't a figure of speech here. It is the thing that makes accountability mean anything. A reviewer who staked nothing and controlled nothing is not accountable for the outcome. They are standing where the blame was aimed.

So the real question was never "which human do we hold responsible." It is "what had a stake in this action." Today, for most AI systems, the answer is nobody. The agent acts under a service account or a borrowed credential, with no identity and no stake of its own, so when it misfires the blame rolls downhill to the nearest human. That is the current state, and the crumple zone is its direct product.

Built right, the answer is different. The agent that takes the action is sponsored: a principal authorizes it and binds their identity to it, so the action carries a name and a stake instead of a service account and a shrug. That binding does one thing on its own. It attributes. Making the principal bear the cost is the work of contract and law, which is exactly why the contract matters as much as the code. It's where a signature becomes a liability, and it's the argument the last issue of this newsletter was making.

The binding itself is a job for an open protocol, the kind of plumbing that already runs everything you depend on. SMTP moves mail. TCP delivers packets. Spanning-tree keeps switches from looping. None of them is owned by anyone, and that is the shape agent authorization needs: an open rule, owned by no one, that ties every consequential action to a sponsoring identity. It's early, and the one I work on, KTP, is one attempt at that shape, not the anointed standard. The point is the form, not the name. Get the form in place and "who is accountable" stops being a hunt for a human to blame. It becomes a structural fact, anchored where the contract makes the stake real: the principal who staked the action. The stake and the control sit in the same place, which is the only place accountability can live.

Follow the stake. If the person you would blame had neither stake nor control, you didn't build accountability. You built a crumple zone and put a costume on it.

## The fix is not a better reviewer

So stop trying to repair the human. The research is unambiguous that you can't: training doesn't fix it, transparency makes it worse, and good intentions are not a control. A better reviewer is the wrong category of answer.

The answer is to bound the action instead of reviewing the decision. Don't position a person to catch a harmful output after the model produces it. Constrain the system so the harmful action can't be taken in the first place. A benefits system that cannot auto-deny without a second structural condition met. An agent that physically cannot touch a record outside its declared scope. A model whose output can't become an action the environment isn't built to absorb. That's authorization, and it works while everyone is looking away, which is exactly when oversight doesn't.

One honest distinction, because it's the whole game. This is not "add a human checkpoint." A checkpoint is the thing that just failed every test above. A bound is structural: the system cannot do the thing, with or without a human watching. Get that wrong and you've rebuilt the crumple zone with extra steps.

## Where the human actually belongs

Keep humans in the loop. Just put them where humans are good: setting the bounds, writing the policy, hearing the appeal, owning the decision to deploy at all. Those are judgment at human speed, on human time, with real authority. What no human can do is sit at machine speed and reliably overrule a confident machine a few hundred times an hour. Stop staffing that seat and calling it safety.

If you're a public-sector buyer, this lands in your contracts, not your org chart. Last week I argued the contract is the control plane. This is the sharpest case for it: if your vendor's entire safety story is "a human reviews the output," you have bought a crumple zone, not a safeguard. The thing to require is the bound, not the reviewer.

The loop was never going to catch the machine, and the person in it was never the one with stake. Don't make them absorb the impact for a system you could have bounded and an action someone else authorized. Bound the action so the harm can't happen. Put the accountability where the stake is. Then the human in the loop can go back to being a person with judgment, instead of the part you positioned to crumple.

*Disarm the control plane.*

---

*This builds on work by Ben Green (Computer Law & Security Review, 2022), Dan Davies (the accountability sink), and Madeleine Clare Elish (moral crumple zones), synthesized in Cory Doctorow's "AI's 'human in the loop' isn't." The diagnosis is theirs. The fix (bound the action, don't review the decision) is where this newsletter has been heading for two issues.*
