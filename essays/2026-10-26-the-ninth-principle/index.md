The Ninth Principle
On repair that runs on a calendar, not a complaint

Every spring, before the snowmelt comes down, the people who share a ditch walk it together. They carry shovels. They clear the winter out of the channel. The silt. The branches. The bank that slumped in a February freeze. They call it la limpia. The cleaning.

The ditch is an acequia. About seven hundred of them still run in New Mexico. Stanley Crawford was mayordomo of one, the Acequia de la Jara, and wrote a year of it down in a book called *Mayordomo*. Two dozen or more families shared his ditch. The mayordomo walks it, knows where it seeps, and calls the work.

The work is owed. It was owed by custom long before any legislature wrote it down. New Mexico has counted the ditch as a unit of government since 1965, and under current law the commissioners can assign each owner a share of the work. You can do it. You can send someone in your place. You can pay the price they set instead. What you cannot do is make the work disappear. Every share puts a body in that channel, yours or one you sent or paid for.

Everyone can see who came.

Centuries of this. The tradition came north with the Spanish settlers in 1598. Spain had it from the Arabs. Acequia is an Arabic word. People were already irrigating these valleys when the Spanish arrived. The cleaning came with the tradition, and so did the meeting where neighbors divide a shortage. Nobody legislated either. The ditch got cleaned every spring because the people on it agreed it would be, and kept agreeing, one generation handing the shovel to the next. When Elinor Ostrom went looking for commons that had lasted, the irrigation communities she found in Spain were this tradition's cousins.

Then in 1907 the Territory of New Mexico wrote a water code that let a right be severed from the land, with the owner's consent, and moved somewhere else without losing its place in line. After that, the water could leave the ditch. Whoever held it would never need a shovel.

The ditch is still here. So is the market. In 2024 a City of Santa Fe water memo valued transferable rights in the middle Rio Grande at more than thirty thousand dollars an acre-foot. A water market would price a communal ditch out the way a housing market prices out a family. Not by breaking a rule. By outbidding a body.

I have written about this ditch before. This is the first time I have written it as a test.

---

## What the ditch does

Last time I wrote about two of the things trust runs on. A signal that costs the sender something, and a reservoir that can run dry. The model I have built over the years, the trust force equation, names the rest. The ditch makes every one of them visible.

- Somebody has to be available. The mayordomo can be found.
- There has to be capacity left to trust with. A ditch with nobody left to walk it has none.
- The cost has to be paid where others can see it. Everyone sees who came.
- The two sides have to be present to each other, not one watching the other. The mayordomo walks the same channel.
- Both have to carry part of the cost. No share is exempt.
- There has to be a horizon, a next spring worth keeping faith for. Your children will need this water. So will theirs.
- Against all of it runs betrayal, the kind people saw and the kind nobody did. Trust breaks like glass and mends like bone. Fast one way, slow the other. And the bone remembers.

In the model, take any one of the others away and the rest cannot make up for it. A costly signal nobody is present to see is a letter dropped in an empty room. Presence without shared cost is surveillance. Shared cost with no future is a hostage exchange.

The ditch is not wise. It is built so that none of them goes missing.

---

## Eight principles, eight tests

Elinor Ostrom won the Nobel Prize in economics in 2009. The committee cited her for showing how common property can be managed by the people who use it. She studied commons that had lasted from a century to more than a thousand years. The huertas of Valencia and Murcia. The zanjera irrigation societies of the Philippines. From them she drew [eight design principles](https://kinetic-trust-protocol.net/writing/phase-transition).

She was careful about what she had found. "This list of design principles is still quite speculative," she wrote. She would not yet call them necessary. Twenty years later a review of ninety-one studies found them well supported. The care is part of the lesson.

A value is something you hope a system has. A requirement is something you can test for. The test has to be able to fail. Most values never get one.

The next major version of the Kinetic Trust Protocol is named for her. The protocol is a set of rules I write for how software agents, and the people behind them, are given authority, lose it, and get it back. The new version is proposed, not released. The [release proposal](https://github.com/nmcitra/ktp-rfc/issues/182) is public. It maps each of her eight to a requirement with a test vector. The release waits until every one has its vector. No implementation has passed them in public yet. That is the honest state of it.

Here is what that looks like, one principle at a time. The ditch first. Then what the proposal asks.

Boundaries. A ditch knows whose water it carries. The proposal asks each system to [write its boundary down](https://github.com/nmcitra/ktp-rfc/issues/189): the resource, who is entitled to it, who outside it is affected, and what the authority may not do.

Local fit. The rules on a ditch fit that slope, that soil, that snowpack. The proposal makes every claim of conformance [name the ground it was made on](https://github.com/nmcitra/ktp-rfc/issues/183).

Collective choice. Ostrom's third principle reads, "Most individuals affected by the operational rules can participate in modifying the operational rules." On the ditch that is not abstract. Every other year the parciantes elect the mayordomo and three commissioners. The person walking beside you holds the job because you gave it to them. The proposal says the people a rule binds [may open it for amendment](https://github.com/nmcitra/ktp-rfc/issues/175), and the amendment has to cite the records that moved it.

I thought there might be a need for a commons online, so I wrote out some ideas and kept working on them. It became a public registry called the [Open Trust Commons](https://www.opentrustcommons.org). I maintain it, and I wrote [its succession plan](https://github.com/open-trust-commons/otcs-registry/blob/main/CHARTER.md#7-stewardship-and-succession). On September 25 it merged its first change from an outside contributor. Maksim Barziankou builds an open ledger of admissions and executions called [NC25OL](https://github.com/petronushowcore-mx/NC25OL). He had [objected in public](https://github.com/open-trust-commons/otcs-registry/blob/main/proposals/OTCS-0004/objections/objection-001-two-relations-one-field.md) to how a proposed rule handled rights. Then he [wrote the repair](https://github.com/open-trust-commons/otcs-registry/pull/67). That is her third principle, working.

Monitoring. Everyone sees who came. The mayordomo and the parciante can see each other. That is not surveillance, which runs one way. The proposal says a decision with no receipt that it was carried out [is unverified](https://github.com/nmcitra/ktp-rfc/issues/187), and may not be reported as if it never ran.

Graduated sanctions. Miss the work and you owe it. Send someone, or pay, or pay the fine. The price fits the miss. The ditch is not trying to get rid of you. It wants the channel clear and you back next spring. The proposal's version is [a ceiling](https://github.com/nmcitra/ktp-rfc/blob/e331c9c31f7a907b20773e8c1358466843ebc659/rfcs-md/ktp-repair.md#the-cost), and I will come back to it.

Conflict resolution. Ostrom wanted a cheap local place to bring a dispute. The proposal requires every system to [publish where a dispute goes](https://github.com/nmcitra/ktp-rfc/blob/e331c9c31f7a907b20773e8c1358466843ebc659/rfcs-md/ktp-repair.md#required-not-invoked) and keep the record open. Nobody is abandoned in silence. A system may not stop someone [without saying where that leads](https://github.com/nmcitra/ktp-rfc/issues/191).

Recognition. Her seventh principle reads, "The rights of appropriators to devise their own institutions are not challenged by external governmental authorities." Since 2004 a New Mexico acequia that adopts the rule can refuse a transfer of water that would harm it. It has to say why in writing, and a court can review it. The proposal says recognizing a local rule [creates no obligation anywhere else](https://github.com/nmcitra/ktp-rfc/issues/185). Recognition never hardens into a requirement.

Nested enterprises. No ditch is alone. Upstream and down, other ditches take from the same stream, and in a dry year the acequias on one river divide the shortage among themselves. They call it the reparto. On the Río Lucero near Taos the shares were set by a court in 1893 and renegotiated as recently as 2013. So there are layers. Each ditch runs its own channel. The ditches on a stream settle what they share. Above them, the state adjudicates the river. Each layer decides only what it can see, and none of them runs the one below it. The proposal [nests its systems the same way](https://github.com/nmcitra/ktp-rfc/issues/159). Trouble outside a system can raise the guard inside it. Calm outside cannot lower it. And [what crosses](https://github.com/nmcitra/ktp-rfc/issues/177) from one system to the next is a record, never a score.

Eight tests. Then a ninth.

---

## Where the sixth stops

Her sixth principle is the one I keep circling. It is real. A commons without a place to bring a dispute fractures. But notice when it fires. Somebody has to carry the grievance to the arena first. Until then, the arena does nothing.

La limpia does not wait. Nobody files a complaint to start the spring cleaning. The calendar starts it. The snowpack starts it.

> ***Her sixth principle fires when someone complains. The ninth fires when the snow melts.***

Rules are not the only thing that breaks a commons. Relationships break too. Two families stop speaking after the water runs short one dry August. Nobody broke a rule. Every rule held. The grievance hardens anyway. Neither family will be the first to name it. A dispute arena cannot hear a silence.

The ditch puts them in the same channel in spring regardless. It cannot tell you whether they heal. Water arriving downstream proves the channel is open, not the families. But it keeps them close enough, often enough, that something else becomes possible.

The proposal draws half of that line. A grievance invokes conflict resolution. [Reconciliation is required before re-entry](https://github.com/nmcitra/ktp-rfc/blob/e331c9c31f7a907b20773e8c1358466843ebc659/rfcs-md/ktp-repair.md#required-not-invoked), whether anyone complained or not. The other half is the ditch's alone. The proposal has no snowmelt. It has a door.

A platform keeps the enforcing half of Ostrom's list. Boundaries. Monitoring. Sanctions. All of it at a scale no mayordomo could reach. It can ban you, flag you, throttle you, remove you. It dropped the half that lets the governed change the rules. And it has nothing like la limpia. It can remove the violator. It cannot repair the violated.

In September I wrote that [a system without structural repair](https://www.linkedin.com/pulse/architecture-presence-chris-perkins-ossoc) "isn't a loop. It's a cascade with good posture."

---

## The ninth, written down

I first wrote the ninth principle down in [March](https://kinetic-trust-protocol.net/writing/other-exponential). I called it forgiveness. I wrote it again in April, when I said [it runs in dirt](https://medium.com/@chrisperkins505/the-cost-of-free-maps-c2c611a5b659). Again in May, and again in September. This is the fifth time. It is the first time it is a specification. The specification taught me that forgiveness was the wrong word. The word is repair.

Forgiveness is something the harmed person does. A requirement cannot ask that of them. So the proposed document, [KTP-REPAIR](https://github.com/nmcitra/ktp-rfc/pull/172), puts the whole weight on the other side.

It starts with a door. ["A system that can stop an actor and cannot return it has a door that only closes."](https://github.com/nmcitra/ktp-rfc/blob/e331c9c31f7a907b20773e8c1358466843ebc659/rfcs-md/ktp-repair.md#introduction) Every other part of the protocol says how authority is withdrawn. This one says how it comes back.

It comes back on a condition. Standing lost in a breach does not return because time passed. Or because the system restarted. Or because nobody complained, or a new sponsor vouched. It returns when a reconciliation record is written into the system's audit chain. And it returns "to a ceiling below where it stood." For a serious breach, the ceiling sits at least a tenth below the standing it had. In the document's words, ["what was lost is earned again, not returned."](https://github.com/nmcitra/ktp-rfc/blob/e331c9c31f7a907b20773e8c1358466843ebc659/rfcs-md/ktp-repair.md#the-cost) The bone remembers.

That is the graduated sanction. The repair is built in.

The record is spare on purpose. It ["carries no account of what was said."](https://github.com/nmcitra/ktp-rfc/blob/e331c9c31f7a907b20773e8c1358466843ebc659/rfcs-md/ktp-repair.md#the-record) It states "that the parties were present, who confirmed it, and what remains." What remains can be harm that cannot be repaired. The record is allowed to say so, and the obligation can close while the harm stands.

Last time I asked who stands where the rule lands, with the authority to lift it and the duty to say why. Here there are two answers. The system must publish its route, so anyone can find it. And the record must be confirmed by a verifier who is independent of every party.

Then the part I had wrong in March. The duty to seek reconciliation rests with the side that caused the breach. Never with the side that was harmed. A harmed person's attendance is voluntary. ["A person is never required to attend."](https://github.com/nmcitra/ktp-rfc/blob/e331c9c31f7a907b20773e8c1358466843ebc659/rfcs-md/ktp-repair.md#required-not-invoked) If they decline, that is not a veto, and it closes nothing. The record stays open to them.

That is where the ditch and the specification part ways. The ditch takes a body for every share. It will take a substitute, or a check. Repair will not. A new sponsor does not close a breach. A bond does not close it. The one who caused it has to come. The one who was harmed never has to.

The record and the cleaning do different jobs. The record keeps the last turn honest. La limpia governs the next one. I have called these [the historical society and the kinetic society](https://www.linkedin.com/pulse/historical-society-kinetic-chris-perkins-ozz4c). A commons needs both.

My own commons [says it in its code](https://github.com/open-trust-commons/otcs-registry/blob/main/src/standing.ts#L33-L34). "The machine lowers standing. Only a person raises it, by appending a record saying they looked." I have said it shorter. A number can say no. Only a person can say come home.

---

## Peace in the valley

That line near the start of KTP-REPAIR is about a door that only closes. We have built rooms like that for people.

Thomas Dorsey played blues piano as Georgia Tom before he wrote gospel. In 1932 his wife died in childbirth, and their newborn son died soon after. Grief gave him "Take My Hand, Precious Lord." A few years later he wrote "Peace in the Valley."

The title is the whole argument. Not peace after you leave the valley. Peace in it. The ground you are standing on can be made to hold you.

Johnny Cash carried gospel into prison rooms. At Folsom in January 1968 he closed the show with a song written by a man sitting in the audience. A year later, at San Quentin, he sang "Peace in the Valley" to a room the outside had already filed under done. Not made the same. Not made innocent. Held long enough to sing.

Different, and held.

Forgiveness isn't soft. It's load-bearing. That is exactly why no system gets to require it. The song can offer it. The specification can only keep the door from closing for good.

---

## Repair has a capacity

Stephen Hanmer D'Elía read la limpia more sharply than I had. I [quoted him in May](https://kinetic-trust-protocol.net/writing/govern-the-sand). "The limpia is not an update mechanism. The rules don't change. What changes is the community's capacity to carry those rules into another season of scarcity and conflict."

Capacity is the right word. Capacity runs out.

The New Mexico Acequia Association has a name for what is happening on the ditches. The Mayordomo Crisis. The mayordomos are aging. Fewer young parciantes will take a job that is often unpaid and never ends. After one meeting at Medanales, a member put it plainly. "Nobody can afford to give up their time to be Mayordomo."

Repair is work. Work takes people. The specification counts it the way a ditch would if a ditch kept books. Breaches arrive. Reconciliations close them. Whatever has not been reconciled sits in an open stock. Nothing leaves that stock with time, or a restart, or a new sponsor. [Only an anchored record takes one out.](https://github.com/nmcitra/ktp-rfc/blob/e331c9c31f7a907b20773e8c1358466843ebc659/rfcs-md/ktp-repair.md#declared-repair-capacity)

Last time it was Donella Meadows' bathtub. Same tub. Now the drain has a name. If breaches arrive faster than a system can repair them, [the stock has no ceiling](https://github.com/nmcitra/ktp-rfc/blob/e331c9c31f7a907b20773e8c1358466843ebc659/rfcs-md/ktp-repair.md#ambient-breach). It grows for as long as the gap holds. People who study queues have known this for a century. A line that fills faster than it is served never settles.

So a system's capacity to repair is a design number, like the height of a levee. Set it too low and every other safeguard is borrowed time. Prevention without repair is a system that can only degrade. Given enough years, it will.

---

## Repair to the rule

The clause in KTP-REPAIR called [The Rule](https://github.com/nmcitra/ktp-rfc/blob/e331c9c31f7a907b20773e8c1358466843ebc659/rfcs-md/ktp-repair.md#the-rule) is the one I am least sure the world is ready for. "Repair applies to the rule as it applies to the actor."

If the same breach keeps happening under a rule, past a rate the system declared in advance, the rule is in breach. And "the governing authority that set it is the breaching party." That is a choice the proposal makes, not a fact recurrence proves. Attackers can hammer a sound rule all year. The proposal puts the pattern on the authority that set the rule anyway. The people it bound are the harmed. Its reconciliation record is the amendment. The amendment must cite the records that drove it. "An amendment that cites no reconciliation record is not repair."

A computer in Michigan's unemployment system accused tens of thousands of people of fraud, and when the state went back through the verdicts it could not stand behind nine in ten. Michigan had a rule that kept breaching. So does every system that keeps producing the same harm and files each one as an exception.

So somebody has to be allowed to open the rule.

That brings me back to the ditch, and to something I walked past for years. The channel runs where it runs because somebody set its course. Long before anyone now living picked up a shovel, somebody read the slope and decided where the water would go, and every spring since, the parciantes have cleaned a line they did not draw.

Donella Meadows said to watch the rules, and who has power over them. The ninth principle keeps a commons whole. It does not tell you who drew the line.

The spring is coming. The snow will be on the mountains soon. In March every share will put a body in the channel, whether or not anyone complained.

A country has a spring too. Every other November, on a calendar, whether or not anyone complained, every share can put a body at the polls. Can, not will. Look around. It isn't going so well, and you're likely worried, like me. The vote is the ninth principle applied to the rule. The governed change who governs, on a schedule, without filing anything. The platforms threw that part away. It cannot repair the violated. Two families who stopped speaking in August are not reconciled by November. Everything we have for them runs on a complaint. The court. The file.

In October 2026 a judge in Santa Fe ordered Meta to pay this state twenty-five billion dollars for misleading people about their privacy, more than a decade after the fact. The file at its largest is still the file. The complaint came first, the money comes last, and nobody stood in a channel.

The ditch does it the other way. Everyone comes, the harmed and the one who did the harm, in the same channel, close enough and often enough that something else becomes possible. We have a spring for the rule. We do not have one for the people under it. The harm does not wait for November. It piles up between elections, in a stock nothing drains. The one who was harmed can stay home from the record. There is a place for them in the line either way.

Somewhere a question is waiting that no shovel answers. Who gets to decide that what we keep repairing should continue?
