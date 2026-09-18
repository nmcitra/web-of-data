Protecting Your Organization by Measuring “Days at Risk”
A Consensus-Building Framework for Real Alignment Across All Teams

Every day, state, local, tribal governments and schools endure a relentless barrage of cyberattacks designed to infiltrate, exfiltrate and siphon critical information and undermine public trust. Meanwhile, sophisticated adversaries steadily expand their footholds as we contend with inconsistent detection, scattered containment efforts, drawn-out dwell times and unmitigated vulnerabilities. Each passing hour is key.

### Where a Consensus-Building Framework Comes In

To converge on a secure future, we need a Consensus-Building Framework. We need a blueprint for aligning every stakeholder, from front-line analysts to executive leadership. Such a framework:

- Bridges silos: Ensures coders, SOC teams and executives share a common language of risk and urgency.
- Aligns objectives: Connects the day-to-day realities of patch deployment and incident response with top-level strategic goals.
- Cuts through the status quo: Replaces lingering dwell times and inconsistent detection with proactive, coordinated action.

By measuring “Days at Risk,” the critical metric indicating how long any vulnerability or incident remains unmitigated, you create a rallying point. Everyone from the service desk technician to the highest-ranking leader can see exactly how much time you’re granting adversaries. Once you unify around these numbers, you can tighten processes, allocate resources and sharpen your response to secure your systems before attackers have the chance to strike.

It’s time to leave fragmented efforts behind. Let’s forge a consensus that drives us toward collective resilience — a framework that gives the entire organization, at every level, a clear path to outsmart, outmaneuver and outlast the threats that challenge us daily.

### Why ‘Days at Risk’ Is Your Most Important Number

Before we get into why Days at Risk is the most important metric, let’s talk about why all the other metrics don’t move the needle. For one, just look around you. How much disconnection is there, how much marketing FUD (fear, uncertainty and doubt) is out there and how many competing priorities are there? Remember, if everything is a priority, nothing is a priority.

Using a composite metric (i.e., a single metric made or calculated from many others) can be challenging. As with anything complicated, it’s a matter of simplifying it down to the essentials. We’ll see at the end of this article how to simplify our scoring and unify around what can impact the business (for better or worse).

Most organizations track dozens of cybersecurity KPIs (vulnerability counts, patching stats, breach attempts, compliance checks , etc.) but few ask, *“How long do we knowingly let risk stay in our systems?”* By measuring Days at Risk, you’re quantifying exactly how much time elapses from the moment you discover a threat (or vulnerability) to the moment it’s fully resolved. This focus does two things:

1. Promotes urgency
2. Every extra day means a bigger attack window.

Enables clarity  
A single number, like “We have a 10-day lag,” helps align executive teams and frontline analysts on what truly needs fixing.  
Where the Consensus-Building Framework Comes In

> *Unpatched Vulnerability in a Public Benefits Portal*

A state’s Department of Health and Human Services discovers a critical vulnerability in its online benefits portal, a system used daily by millions of residents to apply for or manage social services. The vendor released a fix a week ago, but patching has been delayed due to resource constraints and scheduling conflicts.

The vulnerability is severe enough that, if exploited, personally identifiable information (PII) could be exfiltrated by attackers. Because the portal integrates with several other agencies’ databases (e.g., tax records, driver’s license systems), the potential impact could ripple far beyond just one department.

Without a consensus, any number of reasons can cause the patch to never be deployed. This could be due to something Systems is saying, or the Application team, or perhaps Network is saying to hold off. Using the key metric, ‘Days at Risk,’ it becomes very clear that 1) there’s risk, and 2) something is causing this risk item to not move. Eventually, the calculation will raise the unmitigated risk to the top for remediation because Days at Risk will be incrementing. Hot take: there could be a political situation where the calculation is modified by decrementing Likelihood or Impact, thereby artificially reducing the overall score.

### 9 Key ‘Days at Risk’ Areas

Below are nine critical domains where tracking Days at Risk can make a profound difference. Each one highlights how long a known risk remains unresolved and how your organization can reduce that window.

- Mean Time to Detect & Contain (MTTD & MTTC)
- Patch Cadence (Vulnerability Window)
- Phishing Susceptibility & User Behavior
- Control Coverage & Effectiveness
- Incident Response Drills & Exercises
- Third-Party & Supply Chain Risk
- Cost-Benefit of Security Initiatives (Budget/Approval Delay)
- Alignment with Risk Appetite & Governance
- Compliance & Regulatory Alignment

Let’s take a closer look at what these are meant to track and why they matter.

![Days at Risk matrix of priorities.](images/figure-01.png)

Putting it all Together: Simple Risk Calculation  
Raw Score:  
Likelihood = 9  
Impact = 10  
Days at Risk = 9 -> doubled to 18 (because >7)

Risk Factors for Weighting:  
Data sensitivity factor (DSF) = 1.5  
Public exposure factor (PEF) = 1.2  
Active exploit factor (ZDF) = 1

Raw score = 9 x 10 x 18 = 1620  
Weighted score = 1620 x 1.5 x 1.2 = 2916 (off the charts!)

Since 2916 is greater than 1000, we cap it at 1000.

Final score = 1000 -> Drop everything and remediate!

Comments:  
Data Sensitivity Factor (DSF) = 1.0 or 1.5 (e.g., 1.5 for PII, HIPAA data).  
Public Exposure Factor (PEF) = 1.0 or 1.2 (e.g., 1.2 if the system is a public-facing portal).  
Active Exploit Factor (ZDF) = 1.0 or 1.3 (e.g., 1.3 if exploits are actively used by adversaries).  
How to Interpret the Score  
801-1000 Catastrophic  
24/7 escalation, immediate lockdown, ongoing executive oversight.

601-800 Critical  
Rapid mobilization, major service disruption likely if not addressed.

401-600 Significant  
Serious incident but can be contained within 24 hours.

201-400 Moderate  
Some disruption; address in planned maintenance window.

0 - 200 Minor  
Low risk; handle via routine updates or next patch cycle.  
Conclusion & What Comes Next

The “Days at Risk” model does more than highlight our blind spots. It also focuses our entire team on the exact moment when a known threat becomes truly dangerous. Whether it’s patch delays, phishing susceptibility, or budget gridlocks and shortfalls, measuring how many days these issues linger frames cybersecurity risks in undeniable terms: each day of inaction is another day adversaries can exploit.

A Consensus-Building Framework weaves these metrics into a single, transparent process — one that ensures security analysts, risk managers, CISOs, SOC leads, compliance officers and executives share the same view of what “urgent” really means. For instance:

As a Director of Security, I want to track ‘Days at Risk’ for each vulnerability so I can immediately spot overdue patches and prioritize remediation.  
As a CTO, I want to transform raw data (Likelihood, Impact, Days at Risk) into a single composite score, so I have a quick snapshot of enterprise-wide risk.

When everyone reads from the same sheet of music, even complex issues become more manageable.

In future articles, we’ll dive deeper into how to operationalize this framework: setting up your 0–1000 scale, integrating the 2x multiplier for delayed fixes, and factoring in zero-day exploits (ZDF). We’ll also explore how a unified approach to “Days at Risk” not only speeds containment but transforms cybersecurity from a fragmented challenge into a shared, strategic advantage. Until then, remember: the clock is ticking and the less time we give our adversaries, the safer we all become.

I appreciate your feedback and collaboration, Matt Snyder!

Please note: the views and opinions expressed in this post are those of the author (Chris Perkins) and do not necessarily reflect the official policy or position of my employer, or any other agency, organization, person or company. Assumptions made in this post are not reflective of the position of any entity other than the author — and, since we are critically-thinking human beings, these views are always subject to change, revision, and rethinking at any time.
