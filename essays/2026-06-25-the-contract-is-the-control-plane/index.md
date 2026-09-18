The Contract Is the Control Plane
For state, local, and education buyers: the silent agents are already in your systems. Procurement is the only lever that reaches them in time.

Odds are that sometime in the last two quarters, a vendor switched on an AI agent inside one of your core systems without making a point of telling you. Maybe it was the assistant in your student information system. Maybe it was the automation in your benefits-eligibility platform, or the new copilot in your ERP. It reads records. It takes actions. And it arrived in a release note, not a procurement review.

The problem isn't only that it happened. It's that you may have no way to know it did, or to see what it's doing now.

One principle cuts through it: an agent you can't observe is untrusted by default. Not because the vendor is shady. Untrusted because trust is not a vibe. It accrues from behavior you can witness, over time, and an agent that emits no behavior record has earned none of it. So the burden of proof sits with the vendor's agent, not with your security team. Which, if you're a county or a campus department, might be two people and a stack of compliance binders.

## You can't out-run it, so you bind it going in

Last week I wrote about why responding faster never wins this race: the agent moves on the machine clock, milliseconds, and your judgment moves on the institution clock, months. Those two clocks don't mesh on their own. Something has to sit between them and let the fast one turn without stripping the teeth off the slow one. I've called that part the gasket, and the work of fitting it *gasketry*.

You cannot make the slow clock fast.

Procurement is slow the way concrete is slow. But the slow clock has one move that works, the move institutions were built for: it governs a fast clock by setting the conditions before the fast clock starts running. The contract is the gasket. It's where the institution clock reaches forward and shapes what the machine clock is allowed to do, before the machine clock ever spins up. You don't supervise the agent in real time. You require it to be legible before it is ever allowed to act.

And that requirement only enters the world through one door. Read the chain right to left: the **outcome** you want comes from a **capability**, the capability comes from something the vendor **engineered**, and the engineering only happens because it was written into **procurement**.

Outcome ← capability ← engineering ← procurement.

You hold the key to exactly one of those four doors, the leftmost one, and it sits upstream of all the others. Every capability you wish you had started as an engineering requirement, and every engineering requirement a vendor will honor started as a line in a contract.

You can't bolt observability onto a system that wasn't built to emit it. You require it going in. For public-sector and education buyers that isn't a weakness, it's leverage, because you buy on RFPs and multi-year master agreements, and increasingly you buy together.

## The three asks

Put these to any vendor embedding agents. Each one is a contract line that forces an engineering build that hands you a capability that closes a real risk. The same chain, in four columns:

| The ask (procurement) | What it forces (engineering) | What you can then do (capability) | Why it matters (outcome) |
| --- | --- | --- | --- |
| **Declaration:** every agent in a tenant-visible registry, with stated purpose and scope | A discoverable agent manifest / catalog the tenant can read | See every agent acting in your tenant | No silent features; defensible to a board or commission |
| **Telemetry:** an exportable behavior record into your SIEM, not the vendor's console | Structured, streamable event export you own | Baseline it, alert on it, run forensics on it | You can measure your own exposure |
| **Control:** autonomy bounds plus throttle/kill at the tenant boundary | Policy hooks and a stop control you operate | Bound or halt the agent without the vendor | Autonomy can't exceed what you can govern |

The Control row's last column is the law under the whole framework: an agent's autonomy cannot exceed your environment's capacity to govern it. If you can't bound it, it isn't yours to run.

Let me repeat: if you aren't bounding it, you do not own it.

Declaration, telemetry, control: identity, intent, and behavior attestation for agents. We did exactly this for people with SSO and for workloads with workload identity. The agent equivalent is the missing layer. Several efforts are drafting it; the one I work on is the Kinetic Trust Protocol. That's my bias, said plainly, and the three asks stand whether you ever touch it or not. You don't have to wait for any of them to ratify a standard. Procurement language is how buyers force the layer into existence before any standard catches up.

Procurement, again, is the upstream door.

One caveat: I'm not a procurement expert. I just play one on LinkedIn. So take this to the people who do it for a living. Check with your procurement and contracts team on what your purchasing vehicle can actually carry, which of these belong in the RFP versus the master agreement versus the SOW, and what your state or system already lets you require. The point was never that I have the perfect clause. The point is that the clause is where this gets decided, and right now almost nobody is writing it.

## How it plays out: a state IT office

Picture a state Office of Information Technology running the common model: it provides managed network and security services to the small agencies, while the large agencies keep their own autonomy. A flexible, federated arrangement.

Watch the chain move. The OIT writes the three asks into the statewide master contract and into its managed-security service definition. That's **procurement**.

The vendors on that contract now have to build the manifest, the telemetry feed, and the tenant-side kill switch to keep the business. That's **engineering**. Every small agency riding OIT's managed services inherits a governable agent the day it's switched on, without hiring a single analyst. That's **capability**.

And a benefits system or a justice-data system can no longer run a silent, unbounded agent against citizen records. That's the **outcome**.

The federated model is a feature here, not a complication. The small agencies inherit the floor automatically. The large autonomous agencies adopt the same published clause language, or extend it because their data is more sensitive. One contract sets the floor; engineering carries it everywhere; the outcome lands in agencies that never had the staff to demand it themselves.

Timing is the catch. You won't bolt this onto a contract already signed. It goes into the next solicitation, the next renewal, the next cooperative refresh. The door is open at recompete, not in the middle of a term, which is one more reason to write the clause now and have it ready when the door opens.

## How it plays out: a large university

Same chain, messier org chart. A large university has central IT and a CISO, dozens of colleges and departments buying their own software, and research units with grant-funded autonomy and the most sensitive data on campus.

Central procurement and the CISO write the three asks into the university's master service agreements and the centrally vetted app catalog. **Procurement.** Vendors who want into the catalog build to it. **Engineering.** Every college buying through the catalog inherits the floor. **Capability.** Student records and research data stop being acted on by agents nobody can see. **Outcome.**

The autonomous research units don't fight the standard; they take it and tighten it, because they have the most to lose. The flexible model spreads the floor instead of fracturing it.

## Your slow process is, for once, the fastest lever in the room

You think your procurement cycle is your handicap. In this fight it is your weapon, because you do not buy alone. A state master contract, a purchasing cooperative, a department-of-education framework with these clauses written in moves every vendor on it at once.

One district asking is a feature request. A state consortium requiring it is a market signal few vendors can afford to ignore. That is leverage the Fortune 500 envies and rarely has: the power to set the floor for a whole category by changing the language in one agreement.

## In closing

Don't wait for a standard. Don't bolt observability onto a system that was never built to emit it. And don't try to out-run an agent on the machine clock with a team of two.

Write the floor into the contract. Declaration, telemetry, control: legible going in, or it doesn't come in.

The observability tools then have something to watch, and you have an agent you can trust because you can see its behavior over time.

Outcome, capability, engineering, procurement. You only hold the last key. Turn it.

*Disarm the control plane.*

---

## Appendix: Take this to procurement

A starter checklist for your next agent-bearing contract. Not legal language, a conversation starter. Hand it to the people who write your RFPs and master agreements; they'll know which clauses your vehicle can carry and which need rework. Treat every line as a warranty and a requirement, not a roadmap promise.

**Declaration: know what's running**

- ☐ Vendor maintains a tenant-visible registry of every embedded or optional **AI agent or agentic AI**, with declared purpose, scope, and data access.
- ☐ No agent activates in our tenant before it appears in that registry.
- ☐ Vendor notifies us, with a defined lead time, before enabling a new agent or expanding an existing one's scope.

**Telemetry: see what it does**

- ☐ Agent actions emit a structured, exportable record to a destination we control (our SIEM or log store), not only the vendor's console.
- ☐ Records arrive in a documented, machine-parseable schema (CEF, OCSF, or equivalent) mapped to fields we specify, not a proprietary blob our SIEM can't read.
- ☐ Each record identifies the agent, the action, the resource touched, the timestamp, and the outcome.
- ☐ Export is available by API or stream at no premium license tier.
- ☐ We can retain those records on our own schedule, consistent with public-records and FOIA obligations.

**Control: bound and stop it**

- ☐ We can set autonomy limits on what the agent may and may not do at the tenant level.
- ☐ We can throttle, pause, or disable the agent at the tenant boundary, without a support ticket and without disabling the underlying product.
- ☐ Turning the agent off does not breach our SLA or void support.

**Identity and accountability: pin it to someone**

- ☐ Each agent carries its own verifiable identity and never acts under a human user's credentials.
- ☐ Every action is attributable to the agent for audit and forensics.

**Contract hooks: make it stick**

- ☐ The above are warranties and acceptance criteria, not future roadmap items.
- ☐ Remedies for failing to meet them are specified (cure period, service credits, or termination for cause), not left to goodwill.
- ☐ We have a right to evidence or audit of the above on request.
- ☐ These terms survive renewals and bind sub-processors.

If your purchasing vehicle can carry only three lines this cycle, carry these: a registry, an exportable behavior feed, and a kill switch you operate. Declaration, telemetry, control. The floor.

*This is part of Disarm the Control Plane. The three asks are vendor-neutral. Use them against any vendor embedding agents, including the open spec I work on (KTP, kinetic-trust-protocol.net).*
