# The Five Domains: Govern to Strategize

> **Independent, unofficial study resource.** EC-Council, CCISO, CISSP, CISM,
> CISA, ISO, NIST, ISACA, COBIT, and MITRE ATT&CK names belong to their owners.
> No affiliation, official courseware, or exam dumps. No domain weights, exam
> figures, prices, or CPD numbers are asserted here; verify such details with
> the issuer. This is governance education, **not legal, financial, tax,
> regulatory, or investment advice**. Vendor statistics are marketing claims.

## Learning objectives

After working through this article you should be able to:

1. Explain why the five domains are **decision lenses**, not five departments or
   five sequential phases.
2. For each domain, state its purpose, the decisions it owns, the artefacts it
   produces, a meaningful metric, and a characteristic failure mode.
3. Trace one business risk through all five domains and name the handoff
   artefact at each boundary.
4. Recognise a STOP branch — a point where governance requires a pause, a named
   decision owner, or written authority before work continues.
5. Distinguish governance authority from operational authority during an
   incident or an audit response.
6. Map your own experience to the five domains using evidence rather than job
   titles.
7. Challenge a technical or vendor claim by asking the question the correct
   domain owns.

If you can do items 3, 4, and 7, you are beginning to think like a CISO rather
than a catalogue of topics.

---

## Why domains exist at all

A list of topics helps you study. **Domains** help you decide. A CISO rarely
faces a problem belonging to one specialty: a supplier outage is at once a
third-party dependency, an operational incident, a communication problem, an
architecture question, and a budget decision. Domains ask *who decides, with
what authority, on what evidence, and with what consequence* — a different
skill from knowing which control to deploy.

The five executive domains used by the CCISO body of knowledge are **Govern,
Lead, Operate, Secure, Strategize**. Treat them as overlapping lenses, never as
an organisation chart: one person may span several, and one meeting can move
through all five.

The order used in the flow below is a *logic of dependency*, not a calendar.
You cannot legitimately fund what you cannot govern; you cannot govern what
nobody will lead; you cannot secure what you do not understand; you cannot
operate what you cannot see; and you cannot strategize without operational
evidence. Real work loops backwards constantly.

### The five domains at a glance

| Domain | Question it owns | Decision right it claims | Characteristic artefact | Metric question | Typical failure |
|---|---|---|---|---|---|
| **Govern** | "Who is allowed to decide, and within what limits?" | Authority, risk acceptance, policy exceptions | Decision-rights charter, risk register, exception register | "Are accepted risks current and owned?" | Paper policies with no named owner |
| **Lead** | "Will people understand, trust, and act?" | Mandate, messaging, escalation, culture | Stakeholder map, briefing, decision log | "Did the decision land, and who still disagrees?" | Technically correct advice nobody follows |
| **Secure** | "Do we understand the system well enough to shape it?" | Design posture, control selection, technical challenge | Control catalogue, architecture notes, design review | "Can we explain the exposure in business terms?" | Fluency delegated entirely to vendors |
| **Operate** | "Is the program working today, including when it fails?" | Response command, prioritisation, service continuity | Runbook index, incident record, measurement pack | "Can we detect, respond, and recover predictably?" | Counting activity instead of outcomes |
| **Strategize** | "Where are we going, and what will it cost?" | Funding, sequencing, portfolio and supplier choices | Roadmap, business case, benefit review | "Did the funded work change the risk profile?" | A wish list with no owner or money |

Each domain has a recognisable way of failing, and the failures are
*organisational*, not technical. That is the point of the model.

---

## Governance to strategy: the flow, including the stops

The diagram below is a decision flow, not a procedure. STOP branches are
deliberate: stopping and escalating is often the correct governance answer.

```
              +--------------------------------+
              | Business intent / duty to act  |
              +----------------+---------------+
                               v
              +--------------------------------+
              | GOVERN: owner + limits?        |
              +----+---------------------+----+
                   |NO                   |YES
                   v                     v
            [ STOP:            +--------------------------------+
             no mandate ]      | LEAD: sponsor + message?      |
                               +----+---------------------+----+
                                    |NO                   |YES
                                    v                     v
                            [ STOP:           +--------------------------------+
                             no sponsor ]     | SECURE: fluency to challenge?  |
                                              +----+---------------------+----+
                                                   |NO                   |YES
                                                   v                     v
                                           [ STOP:          +--------------------------------+
                                            get advice ]    | OPERATE: run + recover?        |
                                                            +----+---------------------+----+
                                                                 |NO                   |YES
                                                                 v                     v
                                                         [ HOLD:        +--------------------------------+
                                                          stabilise ]   | STRATEGIZE: funded roadmap?    |
                                                                        +----+---------------------+----+
                                                                             |NO                   |YES
                                                                             v                     v
                                                                     [ STOP:        [ PUBLISH: plan + measures +
                                                                      unfunded       review cadence ]
                                                                      wish ]               |
                                                                                           v
              +----------------------------------------------------------------------------------+
              | FEEDBACK: incidents, audit findings, metrics, law/supplier change -> GOVERN        |
              +----------------------------------------------------------------------------------+
```

### What the gates actually test

| Gate | Evidence required | Who says "go" | If the gate fails |
|---|---|---|---|
| Mandate | Charter with named owner and limits | Executive sponsor | STOP: no authority to spend or compel |
| Alignment | Sponsor repeats the message; leaders consulted | Executive team | STOP: build agreement first |
| Fluency | Design explains exposure in business terms | Security lead + engineers | STOP: get competent advice |
| Operational readiness | Owners, measures, failure path exist | Service and security owners | HOLD: fix the operating model |
| Funding | Money, people, review date committed | Budget owner | STOP: it is an unfunded ambition |

A mature program clears these gates because the artefacts already exist. A weak
one discovers at the funding gate that nobody owned the risk earlier. The loop
matters: feedback never jumps straight to "buy something" — it returns to
authority.

---

## Govern — the right to decide

**Purpose.** Govern converts vague concern into legitimate, traceable
decisions: who owns risk, what authority each role holds, which policies bind
whom, how exceptions are granted. It does not mean "more documents"; it means
a decision can be defended months later by someone who was not in the room.

**Decisions it owns.** Risk appetite and acceptance; policy approval and
exception; control ownership; the boundary between security, IT, legal,
privacy, and the business; when to escalate. An information security management
system (ISMS) — a management structure for governing security — is one
structure for this, not the whole of governance. See the [CSIX ISO 27001 companion](https://siedysoes.github.io/csix-iso27001/).

**Artefacts it produces.** Decision-rights charter; policy register; risk
register with owners; exception register with expiry dates; acceptance record.

**Metrics.** Count decisions *current and owned*: accepted risks past review,
exceptions with no expiry, controls with no owner, time from escalation to
recorded decision. A policy count measures typing.

**Failure modes.** Paper policies nobody finds; a register kept for auditors;
committees that never decide; "the business accepted it" with no name;
governance treated as legal's job rather than line management's.

**Connections.** Govern authorises Lead, constrains Secure and Operate, and
sets Strategize's criteria. It also receives the strongest feedback: incidents
and audits reveal where authority was unclear.

| Decision-rights question | Bad answer | Defensible answer |
|---|---|---|
| Who accepts a residual risk? | "Security said it was fine" | Named business owner, date, rationale, review trigger |
| Who can approve an exception? | "Whoever is closest" | Defined role, documented criteria, recorded decision |
| Who owns a control? | "IT" in general | A named role accountable for operation and evidence |
| Who declares an incident? | The tool, by default | An authorised role with a threshold and a deputy |

---

## Lead — making the decision travel

**Purpose.** Lead turns authority into coordinated behaviour. A CISO who is
technically right but organisationally invisible has not led anything. Framing
the problem so executives, engineers, and teams see what is asked of them —
and can disagree before a decision hardens — is the work.

**Decisions it owns.** Message and audience; when to escalate and to whom; how
to handle dissent; when to say "no" to a request conflicting with agreed risk;
how to protect a team from blame while demanding accountability. Ethics belongs
here: the willingness to state an inconvenient truth early.

**Artefacts it produces.** Stakeholder map; short executive brief with a
decision request; decision log with agreement, dissent, and deferrals; talking
points; named escalation contacts.

**Metrics.** Did the audience make the requested decision; how many decisions
were reopened because the premise was unclear; how fast did bad news reach the
sponsor; do staff feel safe raising a concern? The last is a cultural signal —
gather it carefully and anonymously.

**Failure modes.** Briefing upward only; risk as fear rather than choice;
winning the meeting and losing implementation; commanding engineers; hiding a
red metric until crisis; confusing confidence with credibility.

**Connections.** Lead gives Govern its mandate, gives Operate pause authority,
borrows Secure evidence, and sells Strategize's roadmap to funders. See
[Board Communication & Executive Presence](../career/board-communication.md).

| Audience | What they need from the CISO | Decision you are asking for |
|---|---|---|
| Board or governing body | Exposure in business terms, options, and a clear recommendation | Approve risk position or funding |
| Executive peers | Impact on their objectives and their obligations | Accept ownership or change a plan |
| Engineering teams | Why the control exists and what "done" looks like | Sequence work and report obstacles |
| Legal, privacy, audit | Shared facts and documented boundaries | Agree interpretation or escalate |
| Suppliers | Requirements, evidence expectations, and review cadence | Accept contractual obligations |

---

## Secure — enough depth to challenge

**Purpose.** Secure supplies technical judgement behind executive claims. The
CISO need not configure every control, but must ask questions that expose
whether a design does what a vendor or slide says — and know when the answer
is "we do not know yet". Fluency is a credibility instrument, not a hobby.

**Decisions it owns.** Whether architecture fits the risk position; which
identity, data-protection, and software-supply-chain assumptions are
acceptable; when independent review is needed; what evidence justifies calling
a control effective; where expert advice must be sought. The leader must be
able to interrogate architecture, identity, cloud, applications, data, and
secure development.

**Artefacts it produces.** Control catalogue with purpose; architecture and
trust-boundary notes; design-review records; assumptions with owners; vendor
questions and answers.

**Metrics.** Share of material changes reviewed; high-impact assumptions still
untested; whether a manager-readable explainer exists per critical control.
Tool counts do not measure understanding.

**Failure modes.** Outsourcing judgement; marketing language as architecture;
controls demanded without knowing what they protect; "AI-powered" as a reason
to skip review; inability to explain a control to its funder.

**Connections.** Secure tells Govern whether a risk claim is plausible, gives
Lead defensible evidence, makes Operate's alerts interpretable, and shapes
Strategize's build-versus-buy choices. The CISO owns the *question*, not the
configuration.

| A leader's question | What a weak answer looks like | What to ask next |
|---|---|---|
| What does this control protect? | "It covers everything" | Which asset, which threat, which failure path? |
| Where is the trust boundary? | "It's in the cloud" | Who can cross it, and how is that logged? |
| What does the supplier actually assure? | "They say it's compliant" | Which claim, evidenced by what, reviewed when? |
| What happens when this fails? | "It won't" | Who is called, and what is the fallback path? |

---

## Operate — the program in motion

**Purpose.** Operate makes the program real in ordinary weeks and in bad ones:
service delivery, monitoring, incident management, continuity, awareness, and
the measurement habit that tells you whether anything improved. A program that
exists only in a roadmap is not operating.

**Decisions it owns.** Which findings get worked first; when an event becomes
an incident and who commands it; when to pause a service; how evidence is
preserved; when to involve legal or communications; how remediation is verified.
Operational and governance authority differ: the incident commander directs the
response; the risk owner accepts residual risk afterwards.

**Artefacts it produces.** Service catalogue and runbook index; incident record
with decision points; escalation contacts; measurement pack; remediation
tracker with verification criteria; lessons-learned note.

**Metrics.** Track time to detect and restore, share of incidents with a
decision trail, remediations passing a defined retest, and planned versus
interrupt-driven work. Alert and ticket counts describe activity, not outcome.
Service-management habits from the [CSIX ITIL companion](https://siedysoes.github.io/csix-itil/) can help, but
measures must reflect your own risk position.

**Failure modes.** Heroics as an operating model; ownerless alert queues; fixes
declared complete without verification; post-incident blame hunts; metrics
chosen because they look good; no deputy commander.

**Connections.** Operate supplies evidence for Govern's risk acceptance, gives
Lead the honest story, tests Secure's assumptions, and tells Strategize which
investment changed outcomes. Here feedback becomes data.

| Weak metric | Better question | Why it matters |
|---|---|---|
| Alerts handled this month | Which exposures were actually reduced? | Volume can rise while risk rises |
| Tickets closed | Which remediations passed verification? | Closure is not effectiveness |
| Training completion rate | Can staff describe the action they would take? | Attendance is not behaviour |
| Uptime only | How fast did we restore, and what did we learn? | Resilience needs a recovery measure |

---

## Strategize — turning risk into a funded direction

**Purpose.** Strategize converts the other four domains into a direction that
survives contact with a budget: funded choices with owners, dependencies, and a
way to tell whether they worked.

**Decisions it owns.** Which risks get funded first; roadmap versus operating
commitment; build, buy, or partner; supplier dependency governance; benefit
measures; and what is explicitly *not* done. Saying no is strategic and should
be recorded.

**Artefacts it produces.** Roadmap with review points; business case per
initiative; benefit measures; supplier register; capital versus operating
expenditure framing; deferred-work list.

**Metrics.** Share of roadmap items with owner and benefit measure; delivery
against the agreed sequence; and whether funded work moved the risk indicators
that justified it. Perfect delivery with unchanged exposure is a warning.

**Failure modes.** Tool-first strategy; a catalogue of requests; business cases
with no counterfactual; ignoring running costs; vendor claims as benefit
evidence; forgetting that supplier risk remains your risk.

**Connections.** Strategize receives authority from Govern, narrative from
Lead, design from Secure, and evidence from Operate, then returns a funded plan.
See [Risk, Finance & Vendor Governance](../career/risk-finance.md),
[Frameworks & Tools for the Executive](../exam/frameworks-tools.md), and the [CSIX COBIT companion](https://siedysoes.github.io/csix-cobit/).

| Strategic question | Evidence to bring | Decision recorded |
|---|---|---|
| Why this initiative now? | Current risk and incident evidence | Priority and opportunity cost |
| What changes if we fund it? | Benefit measure with a baseline | Expected outcome, not just output |
| What does it cost to keep? | Operating effort, skills, supplier fees | Whole-life commitment |
| What are we not doing? | Explicit deferred list with reason | Trade-off made visible |

---

## How the domains connect in practice

Each row below is a handoff: one domain finishes a sentence and another picks
it up. Informal handoffs create gaps no single domain can see.

| From → To | Handoff artefact | Decision it enables | What breaks if the handoff fails |
|---|---|---|---|
| Govern → Lead | Decision-rights charter and risk position | Leader knows what they may promise | Public commitment beyond authority |
| Lead → Govern | Decision log including dissent | Policy is revised before it hardens | Silent non-compliance |
| Secure → Govern | Design review and stated assumptions | Risk acceptance rests on reality | Accepted risk based on a marketing claim |
| Govern → Operate | Thresholds, escalation path, owner list | Incident command knows its limits | Nobody knows who may declare or pause |
| Operate → Govern | Incident record and verification result | Residual risk is updated with evidence | Risk register drifts from reality |
| Lead → Operate | Sponsor message and escalation contacts | Teams stop work without fear | Delayed containment and blame culture |
| Secure → Operate | Control purpose and detection expectations | Alerts can be interpreted | Noise that nobody can act on |
| Operate → Strategize | Outcome metrics and lessons learned | Money goes to what changes outcomes | Funding follows the loudest complaint |
| Strategize → Secure | Funded architecture work and constraints | Designs fit the affordable envelope | Elegant plan nobody can maintain |
| Strategize → Govern | Roadmap and deferred-work list | Governance reviews what was traded away | Undocumented risk acceptance by omission |

### One risk, five domains

A fictional firm depends on one outside provider for a critical service.

- **Govern** records who is accountable and what level of disruption is
  acceptable.
- **Lead** ensures executives understand the dependency and the service owner
  accepts it, rather than assuming security owns it.
- **Secure** asks what data crosses the boundary, which identity is trusted,
  and which assumptions need testing.
- **Operate** verifies detection, staff actions, and measured recovery.
- **Strategize** funds an alternative, negotiates terms, or accepts the
  dependency with a review date — recording what was deferred.

Every step is a decision with an owner and an artefact. That is the executive
view of security.

---

## Case study 1 — a startup forming its first security function

**Context.** "Northstar Ledger" is a fictional 45-person company selling a data
product to larger customers. A founder handles security informally, two
engineers share administrative access, and a prospect wants evidence of
security practices before signing. There is no security budget line.

**Constraints.** Engineers expect security to slow delivery. The founder wants
a quick certificate-like answer. The cloud environment changes weekly; there
is no time for a large framework implementation. One customer deadline is fixed.

**Decisions.** The founder appoints a part-time security lead with a written
charter rather than buying a platform first. Govern writes a one-page
decision-rights note: the founder accepts residual risk, the engineering lead
owns access reviews, and the security lead may pause a release only under a
defined high-impact condition. Lead has the founder repeat that security is a
customer requirement, not a police function. Secure reviews how administrative
access is granted and documents three assumptions, without a full architecture
overhaul. Operate chooses three measures — access review completion, recovery
exercise result, time to restore — and records customer-relevant evidence.
Strategize funds only access and recovery this quarter, explicitly deferring a
monitoring platform with reasons. The questionnaire is answered with evidence
that exists; gaps are named, not overstated.

**What this teaches.** The first security function is a governance act, not a
tool purchase. Sequence matters: authority before messaging, fluency before
controls, evidence before assurance claims. Recorded "no" items matter as much
as funded ones.

---

## Case study 2 — a regulated enterprise with an audit finding

**Context.** "Meridian Health Systems" is a fictional large organisation with
legacy clinical platforms, a board risk committee, and an external audit
finding about periodic access reviews. The finding is uncomfortable but not an
immediate service failure.

**Constraints.** The legacy platform cannot be replaced in one planning cycle.
Clinical staff resist extra steps during patient-facing work. The audit
response has a fixed timetable; the board wants assurance. Legal and privacy
interests overlap.

**Decisions.** Govern treats the finding as an ownership and evidence problem
before a tooling problem: a named executive owns residual risk, and an
exception register records the platform with expiry and review trigger. Lead
briefs the board in exposure and options, not control names, and records the
clinical representative's dissent. Secure confirms which account types affect
patient data and states which compensating controls work and which are assumed.
Operate builds the evidence trail, fixes the review workflow, and verifies
completion rather than accepting a signature. Strategize funds an interim
process now, a platform change later, and supplier support. The audit response
states what is remediated, what is accepted, and when each is revisited.

**What this teaches.** In regulated settings, the artefact chain is the
product: evidence lets Govern accept an exception honestly, Lead prevents
panic, and Strategize turns a finding into sequenced investment.

---

## Case study 3 — post-incident restructuring

**Context.** "Aster Logistics" is a fictional distribution company that has
just recovered from a disruptive cyber incident. Services are restored, but the
after-action review shows conflicting accounts of who could authorise a
service pause, who was responsible for external communications, and which
decisions were made on incomplete information.

**Constraints.** Customers are asking for reassurance; insurers have evidence
requirements; the response team is exhausted; several staff fear being blamed.
The executive team wants a quick reorganisation announcement.

**Decisions.** The CISO separates two tracks. Operations closes the incident
with a verified timeline, preserved records, and a no-blame learning session
with clear accountability for fixes. Governance rewrites the decision-rights
charter so incident command, external communication, and residual-risk
acceptance are distinct roles, each with a deputy. Lead states what changed and
what did not, acknowledging uncertainty rather than promising it cannot recur.
Secure identifies failed assumptions and requires design review. Operate
replaces ticket volume with recovery time, decision latency, and recorded
owners. Strategize funds identity and recovery first, deferring other requests
with reasons. A quarterly exercise tests whether the new roles work.

**What this teaches.** An incident is a governance stress test. Moving boxes
leaves ambiguity in place; the durable fix is clearer authority, honest
measures, and a funded path.

---

## Practice by domain

Answer each scenario aloud before opening the key. These rehearse decisions,
not vocabulary. There are 15 scenarios, three per domain.

### Govern

**Q1.** A manager says the team "verbalised acceptance" of a high residual risk
in a meeting. What do you need before treating it as accepted?

**Q2.** An audit finding names "IT" as the control owner. What is your first
governance move?

**Q3.** A policy exception is approved with no expiry date. Why is that a
governance defect rather than a paperwork detail?

<details><summary>Key — Govern</summary>

**A1.** A named owner, decision and date, rationale, review trigger, and a risk
register entry. A conversation proves discussion, not authority.

**A2.** Convert "IT" into a named role accountable for operating the control and
producing evidence; confirm acceptance and record it.

**A3.** Without expiry, the exception becomes permanent by silence. Future
leaders cannot tell a deliberate choice from an oversight.

</details>

### Lead

**Q4.** Engineers say a new control will slow releases. You are sure it is
necessary. What is your next leadership move?

**Q5.** The board asks for a single assurance number. Your metrics are mixed
and some are red. How do you respond?

**Q6.** A respected peer quietly disagrees with the risk position in a meeting.
What do you record?

<details><summary>Key — Lead</summary>

**A4.** Ask which release step is affected, restate the risk in business terms,
and offer sequencing or a pilot. Do not win the argument and lose implementation.

**A5.** Give the decisions and trends behind the numbers, explain the red items
as exposure, and invite a decision. Do not compress an honest picture into a
comforting figure.

**A6.** The dissent, the premise challenged, and what was deferred. Recording
disagreement prevents false consensus.

</details>

### Secure

**Q7.** A vendor says its product is "AI-driven and automatically compliant".
What technical question do you ask first?

**Q8.** A proposed design puts a sensitive dataset in a new service. What must
a leader establish before approving it?

**Q9.** You cannot personally verify a complex cloud configuration. What is the
appropriate executive behaviour?

<details><summary>Key — Secure</summary>

**A7.** Which specific claim is meant, what evidence supports it, who assessed
it, when? Treat the phrase as marketing until it becomes a testable claim.

**A8.** The trust boundary, who accesses the data, identity and logging,
untested assumptions, and the failure path. Record assumptions with owners.

**A9.** Say so, obtain competent independent review, and record the adviser and
basis. Fluency includes knowing its edge.

</details>

### Operate

**Q10.** An incident is contained and the team wants to close it. What evidence
do you require first?

**Q11.** Your dashboard shows 2,000 alerts handled this month. What question
should replace it?

**Q12.** During an incident, a leader asks you to wait before pausing a
service because of a customer launch. Who decides, and how is the decision
recorded?

<details><summary>Key — Operate</summary>

**A10.** Verify against the original criterion: observed fact, verifier, open
items, and risk register update. Closure is a decision, not relief.

**A11.** Which exposure decreased, how fast service was restored, which fixes
passed verification. Volume measures work, not risk.

**A12.** The incident commander owns containment within Govern's thresholds;
the business trade-off escalates to the named authority. Record time, decision,
person, and rationale.

</details>

### Strategize

**Q13.** A roadmap item is fully delivered but the risk indicator it was meant
to improve has not moved. What do you conclude?

**Q14.** A supplier promises large savings but will become critical to
operations. What belongs in the business case?

**Q15.** Your portfolio has more worthwhile initiatives than capacity. What do
you produce, and who needs to see it?

<details><summary>Key — Strategize</summary>

**A13.** Output was mistaken for outcome. Check baseline and measure, then
adapt, stop, or redirect funding. Shipping is not success.

**A14.** Whole-life cost including exit, dependency and concentration risk,
benefit baseline, evidence for the savings claim, review cadence. A price is not
a business case.

**A15.** A sequenced roadmap with deferred list, reasons, owners, and review
points, agreed by Govern and communicated by Lead. Unrecorded "no" is invisible
risk acceptance.

</details>

---

## Common mistakes worth memorising

- **Domain silos.** Govern as paperwork, Lead as slides, Secure as engineering,
  Operate as a help desk, Strategize as a spreadsheet.
- **Tool-first governance.** Buying a platform before naming an owner.
- **Authority by implication.** Seniority mistaken for permission to accept risk.
- **Counting instead of deciding.** Totals reported as risk reduction.
- **Metrics theatre.** Measures chosen to improve the slide.
- **Vendor translation service.** Marketing repeated without asking for evidence.
- **Incident amnesia.** Returning to normal without updating register or rights.
- **Blame as method.** Reviews that punish reporting instead of exposing
  ambiguous authority.
- **Outsourced fluency.** A supplier explaining your own architecture.
- **Unfunded ambition.** A roadmap with no "no", no deferred list, no review date.
- **Wrong advice.** A technical control for a governance question; an incident
  metric for a strategy question.

---

## Reusable templates

Copy these into your notes. They are structures; the value comes from filling
them honestly.

### Domain-mapping worksheet

Record a *specific decision you influenced*, not a job title. If you cannot name
an artefact a reviewer could inspect, you probably observed rather than owned.

| Domain | A decision I influenced | Artefact a reviewer could check | Who benefited | Confidence (high / medium / low) |
|---|---|---|---|---|
| Govern | | | | |
| Lead | | | | |
| Secure | | | | |
| Operate | | | | |
| Strategize | | | | |

### Decision-rights record

```
Decision:          [what was decided, in one sentence]
Domain owner:      [Govern / Lead / Secure / Operate / Strategize]
Accountable role:  [name or role, not "IT" or "the company"]
Consulted:         [roles and their dissent, if any]
Evidence used:     [artefacts and their dates]
Risk accepted:     [what remains, by whom, until when]
Review trigger:    [date or event that reopens the decision]
Communicated to:   [audiences and date]
```

### Domain handoff checklist

| Handoff | Artefact attached | Owner named | Date | Review point |
|---|---|---|---|---|
| Govern → Lead | | | | |
| Lead → Operate | | | | |
| Secure → Govern | | | | |
| Operate → Strategize | | | | |
| Strategize → Govern | | | | |

### Weekly operating rhythm

```
Monday:    Which decisions are blocked, and by which domain?
Wednesday: Which evidence changed a risk position this week?
Friday:    Which metric would make us change the roadmap?
Monthly:   Which accepted risks or exceptions expired without review?
Quarterly: Which funded items changed outcomes, and what stops?
```

### STOP prompt

```
Trigger:      [what happened]
Domain gate:  [which gate failed]
Authority:    [who must decide]
Evidence:     [what is missing]
Options:      [continue / narrow / hold / stop]
Decision:     [recorded, dated, communicated]
```

---

## Glossary

| Term | Plain-language meaning |
|---|---|
| **Decision rights** | Who is allowed to make which decision, and with what limits |
| **Risk acceptance** | A recorded, owned decision to live with a residual risk |
| **Residual risk** | What remains after controls are applied |
| **Artefact** | A record produced by a domain: charter, register, brief, measurement pack |
| **ISMS** | Information security management system — a management structure for governing security |
| **Risk register** | The living list of risks, owners, treatments, and review dates |
| **Exception register** | Approved departures from policy, with owners and expiry dates |
| **Control owner** | The named role accountable for a control operating and producing evidence |
| **Escalation path** | The agreed route and contacts for a decision that cannot be made locally |
| **KRI** | Key risk indicator — a measure that signals whether exposure is changing |
| **Stop condition** | An agreed event that requires work to pause and authority to be reconfirmed |
| **Feedback loop** | The route by which incidents, metrics, and changes return to governance |
| **Roadmap** | A sequenced, funded set of changes with owners and review points |
| **Outcome measure** | Evidence that a change reduced risk, as opposed to counting activity |

---

## References and verification

- **ISO/IEC 27001** — the international standard for an information security
  management system. Verify the current edition and any amendments with ISO
  before citing a clause or date. ISO/IEC 27002 provides supporting control
  guidance; its current version also needs checking.
- **NIST Cybersecurity Framework (CSF)** — a widely used outcome-based
  framework. Verify the current release with NIST. Note carefully: a "Govern"
  function in a framework is a useful comparison, but it is **not** identical
  to the CCISO domain named Govern; do not treat the two as interchangeable.
- **COBIT** — ISACA's governance framework for enterprise IT. Verify the
  current release and supporting publications with ISACA; product names and
  editions change.
- **MITRE ATT&CK** — a public knowledge base of adversary behaviour used here
  only as a defensive reference for thinking about coverage. It is not a set of
  instructions, and its content is updated on a release cadence — check the
  current version and date.
- **NIST risk-management publications** (for example SP 800-30 and the Risk
  Management Framework) — useful background on risk assessment language;
  confirm current status and successors with NIST.
- **EC-Council official channels** — this site records CCISO v4 / AI-Enhanced
  branding as of 26 Nov 2026, following the site writing standard. Domain
  names, descriptions, eligibility, exam policy, pricing, and renewal rules
  change. Verify all of them at [eccouncil.org](https://www.eccouncil.org/),
  [cert.eccouncil.org](https://cert.eccouncil.org/), and the official
  certification page before making study or purchase decisions. This article
  deliberately states no domain weights, exam figures, prices, or CPD numbers.
- **Your own organisation's policies, legal obligations, and professional
  advisers** take precedence over any public framework or study article.

Nothing here is legal, regulatory, financial, or investment advice. Board,
risk, and finance examples are fictional and illustrative. Statistics published
by vendors are marketing claims with their own methodology, not guarantees.
For AI-specific governance questions, see [AI Governance: Reality Check](../career/ai-governance.md);
for study sequencing, see [A Practical Study Plan](../exam/study-plan.md).

## See also

- [What Is CCISO v4](what-is-cciso.md)
- [The CISO Role: From Technical to Executive](ciso-role.md)
- [CCISO Exam Format & Blueprint](../exam/exam-format.md)
- [A Practical Study Plan](../exam/study-plan.md)
- [Frameworks & Tools for the Executive](../exam/frameworks-tools.md)
- [Board Communication & Executive Presence](../career/board-communication.md)
- [Risk, Finance & Vendor Governance](../career/risk-finance.md)
- [AI Governance: Reality Check](../career/ai-governance.md)
- [CCISO vs CISSP & Other Leader Creds](cciso-vs-cissp.md)
