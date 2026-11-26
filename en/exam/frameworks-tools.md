# Frameworks & Tools for the Executive

> **Independent, unofficial study resource.** EC-Council, CCISO, CISSP, CISM,
> ISO, NIST, COBIT, MITRE ATT&CK and other framework or credential names belong
> to their owners. This site is not affiliated with or endorsed by them and
> contains no official courseware, exam dumps, or copyrighted framework text.
> This is **governance and leadership education**, not legal, regulatory,
> financial, or investment advice. It explains how a leader chooses and uses
> structured references; it does not decide which law applies or which product
> to buy. Editions, certification rules, issuer policies, and vendor claims
> change — verify them with the official source before deciding.

## Learning objectives

After working through this article you should be able to:

1. Distinguish a **standard**, a **framework**, a **knowledge base**, an
   **architecture pattern**, and a **platform** by the decision each supports.
2. State, for ISO/IEC 27001, NIST CSF, COBIT, MITRE ATT&CK, Zero Trust, GRC
   platforms, and threat intelligence, the question each answers and the
   question it leaves unanswered.
3. Name at least one artefact and one honest metric associated with each tool.
4. Select a starting framework from a decision, an obligation, or a failure —
   not from a vendor demo or a wish to "do everything".
5. Recognise five common ways executives misuse frameworks and stop them early.
6. Build a framework-mapping worksheet and a metric catalogue a manager can
   challenge.
7. Explain why a framework output is evidence for a decision, not proof of
   safety.
8. Apply the selection logic to a startup, a regulated enterprise, and a merger
   integration.

If you can do items 2, 4, and 7, you are consuming frameworks as an executive
rather than collecting acronyms.

---

## Why a framework shelf, not a framework religion

A framework is a **structured way to ask questions and record answers**. It
makes gaps visible, gives teams a shared vocabulary, and turns "we feel secure"
into "here is what we can show". It becomes dangerous when it replaces
judgement: a filled template can look complete while the underlying decision
was never made.

| Failure | What it looks like | Executive fix |
|---|---|---|
| Framework collection | Three maturity models, no budget decision | Name the decision each framework serves |
| Certificate worship | "Certified, so the risk is gone" | Separate conformance from effectiveness |
| Tool-first buying | A GRC platform before control owners exist | Agree the taxonomy, then automate it |
| Metric theatre | A green dashboard with no definition | Publish formulas, sources, and review dates |
| Copy-cat targets | A peer's profile becomes your plan | Derive the target from your own risk appetite |

The leader asks: *What decision does this artefact improve, who owns it, and
what would change our mind?* A **standard** such as ISO/IEC 27001 states
auditable requirements. A **framework** such as NIST CSF offers outcomes and
profiles. A **knowledge base** such as MITRE ATT&CK describes behaviour without
setting priority. An **architecture pattern** such as Zero Trust changes access
decisions. A **GRC platform** stores evidence. **Threat intelligence** is an
outside-in input. Mixing these categories causes most framework disappointment.

---

## The purpose map: seven tools, seven questions

Read this as a menu, not a ranking. "Does not answer" is the most important
column: it marks where judgement takes over.

| Tool | Primary question | Deliberately does not answer | Artefact | Metric showing real use |
|---|---|---|---|---|
| ISO/IEC 27001 (ISMS) | Do we govern information-security risk through a managed system with evidence and improvement? | That breach is impossible; which product to buy; every law in every jurisdiction | Scope, risk treatment plan, SoA, audit and review records | Ageing of corrective actions; share of material changes risk-reviewed before approval |
| NIST CSF 2.0 | Where are we, where do we want to be, and which gap do we fund first? | Certification; implementation steps; a universal maturity score | Current/target profiles, ranked gap register, crosswalk | Priority gaps with owner and dated action; profile review currency |
| COBIT | Are IT governance processes accountable, measurable, and aligned to stakeholder outcomes? | Which cipher to deploy; whether a detection works; legal compliance by itself | Decision-rights matrix, process owners, maturity baseline, improvement plan | Major IT decisions with business case and risk review; decision cycle time |
| MITRE ATT&CK | Which adversary behaviours matter to us, and where are our blind spots? | Likelihood for your company; attribution; a compliance verdict; a response script | Coverage matrix, telemetry gap register, defensive validation plan | Priority techniques with validated telemetry; gaps closed from the register |
| Zero Trust | How do we make access decisions explicit instead of granting implicit trust? | "Trust nothing"; one purchasable product; permission to drop other controls | Protect-surface inventory, policy model, exception register, roadmap | Critical access paths with documented policy; exceptions past expiry |
| GRC platform | Can authorised people see current controls, evidence, owners, and actions? | Whether controls work; what risk appetite should be; truth if data is stale | Control library, evidence register, issue tracker, audit trail | Evidence freshness; controls with owner and last-test date; evidence-pack cycle time |
| Threat intelligence | What is changing outside us that should change our priorities or briefings? | That we will be attacked; certain attribution; a decision without internal context | Requirements list, source/confidence register, decision brief | Briefs producing a named decision; time from warning to control change |

These tools **overlap deliberately**: ATT&CK can inform a CSF Detect outcome,
and ISO can supply evidence for a CSF profile. Write one crosswalk instead of
making teams translate repeatedly. None of the tools creates authority. An
unowned policy, profile, or dashboard is decoration.

---

## A selection diagram with real stops

This is a decision aid, not a project plan. The STOP branches are the point:
stopping before a purchase is cheaper than stopping after it.

```
              +--------------------------------+
              | A framework question appears   |
              +---------------+----------------+
                              v
              +--------------------------------+
              | Named decision owner?          |
              +---+--------------+-------------+
                  |NO            |YES
                  v              v
          [ STOP: assign    +---------------------------+
           owner first ]    | Scope and boundary        |
                            | written down?             |
                            +---+-----------+-----------+
                                |NO         |YES
                                v           v
                        [ STOP: define +---------------------------+
                         scope ]       | External obligation?      |
                                       +---+-----------+-----------+
                                           |YES        |NO
                                           v           v
                            +---------------------+  +------------------+
                            | Start with required |  | What is stuck?   |
                            | baseline; map to    |  +--+--+--+--+-----+
                            | ISMS / CSF later    |     |  |  |  |  |
                            +----------+----------+     |  |  |  |  |
                                       |                |  |  |  |  |
                                       v                v  v  v  v  v
                            +------------------+  Gov  Det  Acc  Evi  Ext
                            | LOOP: verify    |   |     |    |    |    |
                            | edition, signoff|  COBIT ATT& ZT   GRC  TI
                            +------------------+   |     |    |    |    |
                                                   +-----+----+----+----+
                                                             v
                            +-------------------------------------+
                            | One decision brief: question,       |
                            | artefact, owner, metric, review date|
                            +------------------+------------------+
                                               v
                            [ LOOP: review after next decision ]
```

"Buy a platform" is never a starting point. Choose a GRC system only after the
workflow is describable; choose an intelligence feed only after someone has
written an intelligence requirement.

---

## The seven tools, one at a time

### ISO/IEC 27001:2022 and the ISMS

**Answers.** An **ISMS** (Information Security Management System) sets scope,
assesses and treats risk, assigns responsibility, checks performance, and
improves. ISO/IEC 27001:2022 asks: *Do we run security as a governed management
system, not a pile of ad hoc controls?* ISO/IEC 27002:2022 gives implementation
guidance; do not treat it as a second certification requirement.

**Does not answer.** It does not prove a breach is impossible, settle every
legal duty, or select a product. Certification, where used, reports conformity
within a defined scope; it is not effectiveness or a transfer of liability.

**Artefacts.** ISMS scope; risk assessment and treatment plan; **Statement of
Applicability (SoA)** showing which controls are applied, excluded, and why;
policies; competence records; internal audit results; management-review minutes;
corrective actions.

**Metrics.** Ageing of overdue corrective actions; share of material changes
risk-reviewed before approval; recurrence of audit findings; management-review
actions with owner and due date. Counting published policies measures paperwork.

**Misuse.** Outsourcing the ISMS and treating the certificate as an achievement;
excluding an inconvenient unit from scope; ticking Annex A controls without a
risk link. Verify the current edition, national adoption, and certification
rules; the 2022 label is a check point, not permission to stop checking.

**Executive test.** Trace one recent risk decision from the register to the SoA
to the management-review minutes. If the trail breaks, the system is on paper
only.

### NIST Cybersecurity Framework 2.0

**Answers.** CSF 2.0 organises outcomes into Govern, Identify, Protect, Detect,
Respond, and Recover. Its power is the pair of **profiles**: a current view and
a target view. It asks: *Where are we, where are we going, and which gap do we
fund first?*

**Does not answer.** It is not certification, not an implementation manual, and
not a universal maturity score. It will not decide your risk appetite.

**Artefacts.** Evidence-annotated current profile; approved target profile;
ranked gap register with owners, dates, and dependencies; a note explaining how
the target reflects obligations and risk appetite; a crosswalk to other tools.

**Metrics.** Priority gaps with named owner and next action; reduction of those
gaps per quarter; critical services with documented recovery objectives; date of
last profile review versus agreed cadence. A radar diagram is a communication
aid, not a metric.

**Misuse.** Turning profiles into bonus scores; comparing dissimilar firms;
letting a consultant pick the target from a template; never re-baselining after
a merger or cloud migration. NIST CSF 2.0 was released in 2024 — verify current
publications and companions before quoting details.

**Executive test.** "Which single gap did we close last quarter, and what
changed in the risk register?" If nobody knows, the profile is a poster.

### COBIT

**Answers.** COBIT is enterprise IT governance. It asks: *Are the processes that
govern IT accountable, measurable, and aimed at stakeholder outcomes?* Where
CSF describes cybersecurity outcomes, COBIT asks who decides, who is
accountable, how performance is measured, and how value is realised.

**Does not answer.** It does not select technical controls, replace threat
intelligence, give legal opinions, or certify security.

**Artefacts.** Selected governance objectives; decision-rights/RACI matrix;
process ownership; control objectives; performance measures; maturity baseline
with a stated method; improvement plan tied to business goals.

**Metrics.** Major IT investments with business case and risk review; processes
with a named owner; decision cycle time above an approval threshold; benefit
realisation against the original case; movement against the documented
baseline. Maturity and effectiveness are related but not identical.

**Misuse.** Implementing every process at once; buying a tool before agreeing
decision rights; using a maturity level as a procurement score without reading
the assessment scope; reporting gains while decisions stay informal. COBIT 2019
is widely referenced — confirm the current edition from the publisher.

**Executive test.** Ask who may approve an IT policy exception. If the answer
depends on who is in the room, the central question is unanswered.

### MITRE ATT&CK

**Answers.** ATT&CK is a **knowledge base of adversary behaviour** organised by
tactics and techniques. Used defensively it asks: *Which behaviours matter to
us, and where are our visibility or control gaps?* It gives engineers,
responders, risk managers, and boards one language.

**Does not answer.** It does not estimate likelihood for your company, attribute
an incident alone, prescribe response, or certify compliance. "Covered" does
not mean "risk treated".

**Artefacts.** Scoped coverage matrix of techniques, data sources, and
controls; telemetry gap register; defensive validation plan; tabletop scenarios;
analyst learning material. Every mapping states the ATT&CK version used.

**Metrics.** Priority techniques with validated telemetry; gaps closed from the
register; detection performance by technique cluster; useful alerts carrying
enough context to guide a responder. "We cover 300 techniques" is a counting
exercise without scope and validation.

**Misuse.** Matrix bingo; copying the entire enterprise list; treating a
technique match as attribution; chasing coverage while high-impact blind spots
stay open; publishing a version-free mapping. ATT&CK is regularly versioned;
record version and date, verified from MITRE's official site.

**Executive test.** "Which three behaviours worry us most, and what evidence
shows we would see them?" The answer is a short list, not the full matrix.

### Zero Trust

**Answers.** Zero Trust says access should not be granted merely because a user
or workload sits inside a trusted network. It asks: *How do we make access
decisions explicit, continuous, and proportionate to the resource?* NIST SP
800-207 is a useful public reference point.

**Does not answer.** It does not mean "trust nothing", remove all other
controls, or arrive as one product. It will not fix unowned identities or
unknown assets by itself.

**Artefacts.** A **protect surface** inventory of the data, assets, and services
actually needing protection; access-path and trust-boundary map; identity and
device posture requirements; policy decision points; exception register with
expiry dates; phased roadmap.

**Metrics.** Critical access paths with documented policy decisions; privileged
sessions using strong MFA where applicable; standing privileges converted to
just-in-time approvals; time to revoke access after a role change; exceptions
past expiry.

**Misuse.** Buying a label instead of changing decisions; rebranding a remote
gateway as a strategy; a big-bang rollout that breaks operations; declaring a
pilot "done". Verify current NIST guidance and treat vendor maturity claims as
marketing until tested against your architecture.

**Executive test.** For one recent access exception: who approved it, why, when
it expires, and who notices if it does not?

### GRC platforms

**Answers.** A **GRC** (Governance, Risk, and Compliance) platform records and
routes control, risk, policy, evidence, and audit work. It asks: *Can authorised
people see the current state of controls and their actions?* Its value is
coordination and traceability.

**Does not answer.** It cannot tell you whether a control works, choose risk
appetite, or repair stale data. Automating a bad taxonomy produces bad reports
faster.

**Artefacts.** Control library with unique identifiers; evidence register with
links and dates; policy attestations; issues and actions tracker; dashboards
with written definitions; change audit trail. Taxonomy matters more than the
interface.

**Metrics.** Evidence freshness; controls with owner and last-test date;
overdue action ageing; time to assemble an evidence pack; duplicate controls
consolidated; dashboard tiles with a definition. Measure your own cycle times;
vendor productivity claims are marketing.

**Misuse.** Buying before defining taxonomy; importing thousands of ownerless
controls; treating a green tile as effectiveness; automating escalation without
triage. Select the tool after the workflow fits on a whiteboard.

**Executive test.** Name one control, its owner, last result, and evidence
expiry. Four clicks and six-month-old data mean a filing cabinet.

### Threat intelligence as a decision input

**Answers.** Threat intelligence is external evidence about actors, tools, and
change, processed for an audience. An **intelligence requirement** is the
question asked before collection. Together they ask: *What is changing outside
us that should change our priorities, detections, or board briefing?*

**Does not answer.** It rarely predicts a date, guarantees attribution, or
chooses a control. A feed without a requirement is data, not intelligence.

**Artefacts.** Decision-owned requirements; source register with dates,
handling markings, and confidence labels; short decision brief; watchlist;
"so what?" decision log. STIX and TAXII are structure and transport
conventions, not a strategy.

**Metrics.** Brief items leading to a named decision; time from warning to
control change; requirements answered in the agreed window; false-positive rate
of operationalised indicators. Counting feeds consumed measures activity, not
value.

**Misuse.** Collecting feeds because a competitor does; unverified board claims;
indicator-as-strategy; attribution theatre; ignoring handling markings. Verify
sources, label confidence, and state limits in the same sentence as the claim.

**Executive test.** "Which decision changed because of last month's brief?"
None means the requirement needs rewriting.

### How the tools fit together

ISO gives the **management system**; CSF the **current/target conversation**;
COBIT **decision rights**; ATT&CK an outside-in **behaviour language**; Zero
Trust an **access architecture**; GRC **evidence and actions**; threat
intelligence **external change signals**. Write one crosswalk, then use each
tool only for its best job. Everything else is duplication with extra meetings.

---

## Three fictional case studies

These organisations are invented. They contain no technical procedure — only
context, constraints, decisions, and lessons.

### Case 1 — Nine people and an investor questionnaire

**Context.** "Lumen Rail" is a nine-person startup with a cloud scheduling
product. A transport operator sends a 120-question security questionnaire with
a two-week deadline. There is no security team; the CTO owns everything.

**Constraints.** No certification budget, no GRC staff, and engineering is
committed to a product launch. The questionnaire mixes ISO-style, NIST-style,
and access-control evidence requests.

**Decisions.** The CTO writes a one-page CSF 2.0 current/target view solely to
order the answers, marking irrelevant outcomes "not yet in scope" with reasons.
She uses ISO/IEC 27001:2022 language for three artefacts the customer values: a
risk register, a SoA-style control rationale, and a management-review note. She
does **not** start certification. From a scoped ATT&CK view she selects three
credential-related behaviours and records available telemetry, not full
coverage. Zero Trust appears as two decisions — strong admin authentication and
removal of standing access — not a rebrand. Evidence lives in one indexed
folder; a GRC platform is deferred until there are more than a handful of
controls. Threat intelligence is one weekly line about changes to the identity
provider or hosting region.

**Artefacts.** One-page profile; risk register; control rationale; access-decision
log; evidence index; questionnaire answer log with open items.

**What this teaches.** A startup needs a decision, a boundary, and evidence that
survives the next customer question. Saying "not yet" to a framework is valid
when the reason is written down.

### Case 2 — A regulated enterprise with audit fatigue

**Context.** "Meridian Assure" is a 4,000-person insurer. It has a certified
ISMS for its claims platform, a SOC, a COBIT-based governance programme, and
two inherited GRC tools. The board receives four security reports each quarter
and has stopped reading them.

**Constraints.** Audits arrive on different calendars; legal applicability must
be confirmed jurisdiction by jurisdiction, not inferred from a framework. New
reporting must reduce workload. The board wants a line of sight from risk to
spend.

**Decisions.** The CISO keeps the ISMS as the control backbone but cuts the
board pack to four questions: what changed in risk, which controls failed, what
we funded, and what we ask the board to decide. The CSF profile structures that
pack; the ISMS supplies evidence. COBIT's decision-rights matrix settles who
approves a control exception — a dispute consuming two meetings a month. The
GRC tools are not merged immediately: first the team agrees one taxonomy and
one evidence definition, then duplicate reports are retired. ATT&CK is used by
the SOC for three behaviour clusters and detection gaps, not a giant coverage
score. Six intelligence feeds become two written requirements tied to actual
markets, with confidence labels.

**Artefacts.** Four-question board pack; approved target profile; decision-rights
matrix; consolidated taxonomy; evidence-freshness report; ATT&CK gap register;
requirements list.

**What this teaches.** The executive contribution is subtraction and wiring:
fewer reports, explicit decision rights, and one crosswalk. Maturity helps only
when it shortens the distance from risk to decision.

### Case 3 — Two companies, one integration window

**Context.** "Aster" and "Brightwell" merge. Both are mid-sized industrial
software firms with different customers, identity systems, and governance.
Integration leadership gives the CISO 90 days before shared services switch on.

**Constraints.** Customer contracts prevent early changes to security
commitments. A shared identity platform is proposed, but nobody can name the
owner of emergency access. An early "harmonisation" spreadsheet has 1,100 rows
and no decisions.

**Decisions.** The CISO creates a temporary integration governance board with
one named owner per company and a written escalation path. The first STOP
branch is identity ownership: federation pauses until an authorised approver is
named. A common CSF current profile is built from both companies' ISMS control
sets; certificates are kept until a scope decision is made. COBIT's matrix
settles integration approval rights. The 1,100-row sheet is reduced to a taxonomy
before any GRC migration. ATT&CK compares what each SOC can observe, not which
team is superior. Intelligence gets one requirement: phishing and
supplier-impersonation changes aimed at manufacturing customers during the
window.

**Artefacts.** Integration decision-rights matrix; two-source current profile;
provisional ISMS crosswalk; taxonomy and duplicate list; telemetry comparison;
integration brief with named recipients.

**What this teaches.** The risk is often governance ambiguity, not a missing
control. Stop when ownership is unclear; map before merging; keep customer
commitments stable until someone with authority changes them.

---

## Practice by decision

Answer aloud before opening the key. These rehearse judgement, not vocabulary.

**Q1.** A board member says, "We should adopt Zero Trust this year." What is
your first question, not your first purchase?

<details>
<summary>Key</summary>
Ask which decision or risk should change — admin access, third-party access, or
lateral movement — and who owns it. Zero Trust is an approach to access
decisions, not a product or a whole programme. Without a protect surface and an
owner, "adopt Zero Trust" cannot be measured.
</details>

**Q2.** A customer requires evidence of an ISMS. Must you immediately pursue
certification?

<details>
<summary>Key</summary>
No. Confirm the written requirement and your scope. They may accept a mapped
control rationale, a management system in progress, or a contractual
commitment. Certification is one possible response with its own scope and cost,
not an automatic first step.
</details>

**Q3.** Your team has three maturity assessments and no control owner. Which
tool do you reach for first?

<details>
<summary>Key</summary>
Neither COBIT nor a GRC platform yet. Name the decision and accountable owner,
then define scope and taxonomy. COBIT can clarify decision rights; a GRC system
can store results; neither fixes an unowned process.
</details>

**Q4.** A peer publishes an impressive CSF target profile. Should you copy it?

<details>
<summary>Key</summary>
No. Treat it as a reading example. Derive your target from your own risk
appetite, obligations, services, and dependencies. A copied target either
overfunds irrelevant gaps or omits the ones that matter.
</details>

**Q5.** An auditor says an Annex A control is excluded as "not applicable". What
do you ask?

<details>
<summary>Key</summary>
Ask for the risk-based justification, who approved it, and whether the context
still holds. "Not applicable" without reasoning is a hidden decision. The SoA
is valuable because it forces a written rationale.
</details>

**Q6.** A dashboard shows every control green. What three things do you check
before briefing the board?

<details>
<summary>Key</summary>
Check the definition behind green, the date and source of the evidence, and
whether effectiveness was tested rather than implementation merely reported.
Green without fresh evidence and a written threshold is metric theatre.
</details>

**Q7.** Your ATT&CK matrix reports 80% coverage. Why might that mislead?

<details>
<summary>Key</summary>
Coverage may be counted rather than validated, scoped to the wrong techniques,
or mapped to a stale version. Ask which behaviours matter to your sector, which
have validated telemetry, and which gaps remain open.
</details>

**Q8.** A GRC migration is proposed before the taxonomy is agreed. What is the
likely outcome?

<details>
<summary>Key</summary>
Duplicate controls, inconsistent names, and untrusted reports. Agree taxonomy,
ownership, and evidence definitions first; automate the agreed workflow second.
Tool-first migrations magnify existing confusion.
</details>

**Q9.** Which is the better executive metric: "1,200 policies published" or
"92% of corrective actions closed on time, oldest 12 listed by owner"? Why?

<details>
<summary>Key</summary>
The second. It measures behaviour and exposes exceptions with owners. The first
counts output and can rise while risk stays untreated. Good metrics tell you
where to intervene.
</details>

**Q10.** An intelligence brief lists fifteen dramatic incidents. What do you
change?

<details>
<summary>Key</summary>
Rewrite the requirement. Ask which external changes would alter decisions here,
then limit the brief to those items with confidence labels and a "so what?"
line. Drama is not relevance.
</details>

**Q11.** Your CSF gap register has forty items and no sequencing. What do you
add?

<details>
<summary>Key</summary>
Add decision criteria: business impact, dependencies, owner, target date, and an
explicit "why now" for the first items. A gap list becomes a plan only when it
is sequenced against risk appetite and capacity.
</details>

**Q12.** During the merger, nobody will accept accountability for emergency
access to the shared identity platform. What do you do?

<details>
<summary>Key</summary>
STOP the federation step and escalate to the integration governance board.
Record the blocked decision and the risk of proceeding. Do not solve an
ownership vacuum with a technical workaround.
</details>

---

## Common mistakes worth memorising

- **Acronym collecting.** Knowing a framework's name is not using it.
- **Certificate as shield.** Conformance and effectiveness are different claims.
- **Tool before taxonomy.** Automation amplifies the mess you already have.
- **Copy-cat targets.** Another firm's profile is not your risk appetite.
- **Counting coverage.** Techniques, policies, and tiles are not outcomes.
- **Version-free mappings.** A mapping without version and date decays silently.
- **Ownerless artefacts.** No owner means a document, not a decision.
- **Threat theatre.** Drama without a requirement or a "so what?".
- **Framework shopping after failure.** Avoiding the one hard decision in front
  of you by adopting a new framework.

---

## Reusable templates

Copy these into your notes. They are structures, not completed work.

### Framework selection canvas

```
Decision to support:   [one sentence, with the person who decides]
Why now:               [risk change / obligation / failure / opportunity]
Scope and boundary:    [in scope, explicitly out of scope]
Current artefact:      [what exists today, with date]
Starting framework:    [one primary, with version/edition]
Secondary input:       [one, and the question it answers]
Explicitly deferred:   [framework + reason + review trigger]
Owner and approver:    [names or roles]
Metric and review:     [measure, baseline, next review date]
Stop condition:        [what makes us pause and escalate]
```

### Framework-mapping worksheet

| Framework / input | Decision served | Version / date | Scope boundary | Artefact + owner | Evidence source | Metric | Misuse guard | Review |
|---|---|---|---|---|---|---|---|---|
| ISO/IEC 27001:2022 | Controls for claims platform | 2022 edition; verify | Claims only | SoA; risk lead | Risk register, audit file | Overdue actions | No silent scope growth | Quarterly |
| ATT&CK | Detection priorities this quarter | Record version | Identity/endpoint | Coverage matrix; SOC lead | Telemetry records | Validated share | No bingo counting | Monthly |
|  |  |  |  |  |  |  |  |  |

### Metric catalogue template

| ID | Decision | Definition | Source / formula | Cadence + owner | Baseline / threshold | Trigger action | Gaming risk | Review |
|---|---|---|---|---|---|---|---|---|
| M-01 | Which failures need board attention | Corrective actions past due date, by age | Issue log; due date < today | Monthly; risk lead | Set first run; >60 days | Escalate to risk committee | Closing without evidence | Quarterly |
| M-02 | Whether intelligence changed anything | Brief items with a named decision | Brief log; decision items / total | Monthly; intel lead | Set first run; agreed minimum | Rewrite requirements | Inventing trivial decisions | Quarterly |
|  |  |  |  |  |  |  |  |  |

### One-line decision brief

```
Decision:      [what we are asking for]
Frameworks:    [primary + secondary, with version]
What changed:  [risk or evidence, one sentence]
Evidence:      [artefact name and date]
Ask:           [approve / decline / defer, with owner and date]
```

If this cannot fit on one page, the decision is not ready.

---

## Glossary

| Term | Plain-language meaning |
|---|---|
| **ISMS** | Information Security Management System: how a company sets scope, treats risk, checks results, and improves |
| **Standard** | Published requirements or guidance from a recognised body; ISO/IEC 27001 is a requirements standard |
| **Framework** | Structured outcomes or practices for organising a conversation, such as NIST CSF |
| **Knowledge base** | A catalogue of observed behaviour, such as MITRE ATT&CK; it does not set priority |
| **SoA** | Statement of Applicability: which controls you apply, exclude, and why |
| **Current / target profile** | What you do now and what you intend to do, used to rank gaps |
| **Decision rights** | Who may approve, who is consulted, and who is accountable |
| **Protect surface** | Specific data, systems, and services needing protection — narrower than "the whole network" |
| **GRC** | Governance, Risk, and Compliance: processes and often software for tracking controls, evidence, and actions |
| **Intelligence requirement** | The question a decision-maker asks before intelligence is collected |
| **Confidence label** | A plain statement of how much trust to place in an intelligence item |
| **Evidence freshness** | How recent and still-valid the proof behind a control claim is |

---

## References and verification

All references are starting points for checking, not permission to stop
checking. Editions, dates, and policies can change; record what you actually
used.

- **ISO/IEC 27001:2022** and **ISO/IEC 27002:2022** — verify current edition,
  national adoptions, and certification rules with ISO and your accredited body.
  These edition labels reflect commonly referenced versions as of 26 Nov 2026;
  confirm before use.
- **NIST CSF 2.0** — released in 2024 and includes the Govern function. Verify
  current publications and companions on NIST's site; do not assume a later
  update exists or does not exist without checking.
- **COBIT** — COBIT 2019 is widely referenced. Confirm the current edition and
  official material from ISACA before quoting process names or maturity details.
- **MITRE ATT&CK** — a versioned, regularly updated knowledge base. State the
  version and date in every mapping; verify from MITRE's official site.
- **NIST SP 800-207**, *Zero Trust Architecture* (2020), and **NIST SP 800-150**,
  *Guide to Cyber Threat Information Sharing* — public reference points; check
  current revisions or successors. Public CISA guidance is similarly useful and
  similarly time-sensitive.
- **EC-Council CCISO pages** — verify the current CCISO v4 programme, blueprint,
  and policies with the issuer. This article states no exam weights, prices,
  retake rules, or CPD figures as fact; check the official source for all such
  details.
- **Your organisation's policies, contracts, and qualified advisers** take
  precedence over public frameworks in real decisions. Applicability of laws
  depends on jurisdiction, sector, data, and circumstances. This article is not
  legal or regulatory advice.

Vendor surveys and product claims are marketing, not evidence that a tool will
produce an outcome. All organisations in the cases are fictional and illustrate
governance judgement only.

## See also

- [What Is CCISO v4](../fundamentals/what-is-cciso.md)
- [The Five Domains: Govern to Strategize](../fundamentals/five-domains.md)
- [The CISO Role: From Technical to Executive](../fundamentals/ciso-role.md)
- [CCISO Exam Format & Blueprint](exam-format.md)
- [A Practical Study Plan](study-plan.md)
- [Risk, Finance & Vendor Governance](../career/risk-finance.md)
- [Board Communication & Executive Presence](../career/board-communication.md)
- [AI Governance: Reality Check](../career/ai-governance.md)

Companion CSIX sites — placeholder owner, replace with your deployment owner:

- [CSIX ISO 27001:2022](https://siedysoes.github.io/csix-iso27001/)
- [CSIX ISO 27001 Assessor](https://siedysoes.github.io/csix-iso27001-assessor/)
- [CSIX COBIT](https://siedysoes.github.io/csix-cobit/)
- [CSIX ITIL](https://siedysoes.github.io/csix-itil/)
- [CSIX CPENT AI](https://siedysoes.github.io/csix-cpent/)
