# AI Governance: Reality Check

> **Independent, unofficial study resource.** EC-Council, CCISO, CISSP, CISM,
> ISO, NIST and other credential or standards names belong to their owners.
> This site is not affiliated with or endorsed by EC-Council and contains no
> official courseware, exam dumps, or copyrighted material. EC-Council materials
> checked on **26 Nov 2026** use the label **CCISO v4 / AI-Enhanced**; this
> site's own brand is **CSIX CCISO v4**. Verify current program pages before
> study or purchase decisions. Vendor statistics and accuracy percentages are
> **marketing claims**, not guarantees. This is **defensive, governance and
> leadership education** — not legal, regulatory, financial, tax, or investment
> advice, and no offensive procedure.

## Learning objectives

After working through this article you should be able to:

1. Define an **AI system** for governance purposes and explain why ownership,
   not model architecture, is the starting point.
2. Build and classify an AI-system inventory, including unapproved "shadow AI",
   using an explicit impact tiering scheme.
3. Turn an AI risk scenario into a control, an evidence requirement, and a named
   owner in a risk register.
4. Explain what data lineage and retention mean for prompts, outputs, logs, and
   retrieval sources.
5. Distinguish a real oversight control from a rubber stamp, and define when an
   output should be escalated.
6. Adapt an existing incident-response playbook to AI-enabled systems.
7. Ask procurement questions that test vendor claims rather than repeat them.
8. Scan regulatory sources without making compliance claims you cannot support.

If you cannot do items 2, 3, and 5, you can discuss "AI ethics" abstractly but
you cannot yet govern a deployed system.

---

## Why this is governance, not an engineering course

An **AI system** is any product, feature, or workflow that uses a model —
statistical, generative, or rules-assisted — to produce an output a person or
another process acts on. A chatbot, resume-ranking service, fraud score,
forecast, and email summarizer all belong here: each can affect a decision,
handle data, and fail unexpectedly.

You need not train a model to govern one. Most CISO-level decisions concern
**who owns the output, what data entered, how errors are detected, and who can
stop it**. Engineers ask how it works; executives ask when its use is acceptable.

Three failure modes dominate:

- **Unowned** — a team adopts a tool, nobody is accountable for its outputs, and
  security discovers it during an unrelated review.
- **Unmeasured** — a vendor demo looked good, so nobody evaluates the tool on
  the organisation's own data or defines "good enough".
- **Unexplainable** — a decision affecting a person or a material transaction
  is made with no record of input, output, human override, or authorising rule.

The five CCISO domains are a useful container; this map makes no exam-blueprint
claim.

| Domain | AI-era question | Artifact a leader can show |
|---|---|---|
| **Govern** | Who is accountable for decisions? | Named owner, intake record, exception log |
| **Lead** | How do we hear about quiet tool adoption? | Reporting channel, escalation contacts, status line |
| **Operate** | How do we detect drift and bad outputs? | Monitoring thresholds, decision logs, playbook |
| **Secure** | What data, permissions, and abuse paths exist? | Data-flow record, access review, retention decision |
| **Strategize** | Which vendor claims and costs are real? | Evaluation results, contract terms, exit plan |

An ethical principle without an artifact is a poster; artifacts make it
auditable and improvable.

---

## Start with inventory: you cannot govern what you cannot name

The first control is a **register of AI systems** — less glamorous than a
policy, far more useful. Include in-house systems, vendor products, embedded
features, and **shadow AI** (tools adopted without approval). Shadow AI is
usually a deadline meeting a convenience, not malice. A "tell us so we can
help" route finds more systems than prohibition.

A minimal record holds: purpose; named owner and contact; vendor and model;
data inputs and sensitivity; outputs and recipients; integrations and
permissions; human review; reversibility; affected groups; tier; last review;
and links to evaluation and risk records.

Classify by consequence, not novelty:

| Tier | Example | Stakes | Minimum governance | Review |
|---|---|---|---|---|
| **T0 — Prohibited** | No lawful basis, or use the organisation rejects | Unacceptable by policy | Do not deploy; record the refusal | On challenge |
| **T1 — Low** | Internal drafting, meeting notes | Reversible, no external effect | Owner, acceptable-use note, basic logs | Annual |
| **T2 — Moderate** | Customer content assistance, internal analytics | Reversible with effort; commercial impact | Data flow, own-data evaluation, named reviewer, retention decision | Quarterly / on change |
| **T3 — High** | Hiring, credit, health, safety, access, rights | Hard to reverse; affected people may not know | Impact assessment, fairness and error analysis, meaningful review, contest path, executive sign-off | Pre-launch and continuous |

Tiering is a decision, not a vendor label. The same chatbot is T1 summarizing
public documentation and T3 advising on benefits eligibility. When unsure, tier
by the most sensitive conceivable output, then justify reductions with evidence.

### Intake flow with stop and escalate branches

This approval *process*, not a technical procedure, prevents an incomplete
request becoming a production system.

```
                    +--------------------------------+
                    |  Business request or idea      |
                    +---------------+----------------+
                                    v
                    +--------------------------------+
                    | 1. Named owner + stated purpose|
                    +-----+------------+-------------+
                          |NO           |YES
                          v             v
                    [ STOP:       +--------------------------------+
                     no owner,    | 2. Identify type + data inputs |
                     no intake ]  +-----+------------+------------+
                                        |UNKNOWN      |KNOWN
                                        v             v
                                  [ ESCALATE:   +--------------------------------+
                                    privacy /    | 3. Assign impact tier          |
                                    data review  +-----+------------+-----------+
                                    first ]            |NO          |YES
                                                       v            v
                                                 [ ESCALATE:  +--------------------------------+
                                                   assessor    | 4. Vendor terms + data use  |
                                                   sets tier   +-----+------------+-----------+
                                                                     |VAGUE       |CLEAR
                                                                     v            v
                                                               [ STOP:     +--------------------------------+
                                                                contract  | 5. Evaluation + human review  |
                                                                gap logged |    + rollback defined        |
                                                                           +-----+------------+-----------+
                                                                                |FAIL        |PASS
                                                                                v            v
                                                                          [ STOP:     [ APPROVE PILOT ]
                                                                           redesign ]
                                                                                             |
                                                                                             v
                                                                                 [ MONITOR -> REVIEW GATE ]
                                                                                   |DRIFT   |OK
                                                                                   v        v
                                                                            [ SUSPEND  [ CONTINUE /
                                                                             + ESCALATE  log decision ]
                                                                             + NOTIFY ]
```

A **STOP** means no deployment until the item is supplied. An **ESCALATE** means
the intake owner brings in a named function — privacy, legal, procurement, or
the risk committee. Both are recorded so the gap does not recur.

---

## Risk and impact assessment: from scenario to control

Likelihood × impact is a start, but AI risks hide behind a single number. Ask:

- **Who is affected?** Customer, employee, candidate, community, or us?
- **Reversible?** A wrong draft can be edited; a rejected application may cause
  harm before anyone notices.
- **Autonomy?** A recommendation a person may ignore differs from an automated
  action.
- **Blast radius?** One bad answer, one bad template, or thousands of decisions?
- **Will anyone know?** Silent failure lacks a feedback loop.

Map scenarios to controls **and to evidence that the control works**. A control
with no evidence is a belief.

| Risk scenario | Early signal | Control | Evidence it works | Owner |
|---|---|---|---|---|
| Sensitive prompt data reused by vendor | Contract allows training; vague retention | Data-use clause, classification, redaction | Signed terms plus sampled prompt review | Procurement + data owner |
| Wrong output drives customer decision | Escalations rise on one topic | Scope limits, mandatory review, correction path | Logged overrides; lower error on held-out sample | Business owner |
| Bias in screening or scoring | Selection rates diverge across groups | Pre-launch fairness test, representative set, re-test | Metric definitions, results, remediation decisions | Risk committee |
| Cross-customer data exposure | Retrieval returns another tenant's content | Permission-aware retrieval, least privilege, segregation tests | Access reviews and isolation test results | Platform owner |
| Staff paste regulated data into unapproved tool | Unknown domains in usage data | Approved list, reporting route, DLP signals | Reports resolved; unapproved use declines | Security lead |
| Vendor change alters behaviour | Release notes; shifted outputs on fixed sample | Change-notice clause, regression sample, rollback | Version record and successful rollback test | System owner |
| Fluent answer treated as authoritative | Overrides rare despite known errors | Labels, source citation, quality review | Override logs show scrutiny | Product owner |
| Prompt logs become a breach | Personal data with no expiry | Minimisation, redaction, retention, restricted access | Retention job records and access reviews | Data owner |

Prioritisation is a business decision supported by evidence. A severe scenario
with a tested control may rank below a moderate one nobody watches. Record the
reasoning.

---

## Data lineage, retention, and the long tail of prompts

**Data provenance** means knowing where data came from and on what terms.
**Data lineage** means how it moved and changed to output. AI adds a dimension:
the prompt becomes new data, the output another, and both land in logs and
vendor systems the original owner never approved.

| Stage | Question | Record | Common gap |
|---|---|---|---|
| Source | Who collected it, why, with what limits? | Source register, licence or consent note | "It was in the shared drive" |
| Preparation | How was it cleaned, labelled, combined? | Transformation note, owner | Work done in a local file |
| Use | Training, fine-tuning, retrieval, or inference only? | Data-flow diagram, inventory entry | Training and retrieval conflated |
| Output | Can answers reproduce or expose another party's data? | Sample tests, access boundaries | No realistic cross-context test |
| Retention | How long do prompts, outputs, embeddings survive, and where? | Schedule, deletion evidence | Logs kept "for debugging" forever |
| Disposal | Can deletion requests reach all copies? | Deletion record, vendor confirmation | No map of downstream copies |

**Training** changes a model; **retrieval** looks up content at answer time;
**inference** runs the model on an input. A promise that "customer data is not
used to train the model" says nothing about storage, staff review, or a thirty-
day log. Ask each question separately.

Retention is a governance decision, not an engineering default. Keep enough to
reconstruct a contested decision and investigate an incident; keep no more.
Personal data in a prompt log deserves the same care as data in a database —
often more, because free text may contain more than intended. Privacy
obligations differ by country and sector; verify with qualified advisers.

---

## Bias and fairness: why one metric never settles it

**Bias** is systematic skew in outputs; **fairness** judges which differences
are acceptable in context. Competing metrics cannot all be satisfied at once.
A CISO need not resolve that conflict: make the choice explicit, test against
it, and expose limitations.

1. **Representative evaluation set.** Include the population, conditions, and
   edge cases the system will face. A convenient vendor sample is not
   independent evidence.
2. **Stated metric and trade-off.** Compare error or selection rates across
   groups and record what was accepted in exchange. Do not hide behind "the
   model is unbiased".
3. **Search for proxies.** Removing an obvious protected attribute may leave
   correlations through postcode, job history, or writing style. Absence of a
   field is not absence of bias.
4. **Monitor after launch.** Populations and rules change; one-time reviews
   decay. Schedule re-testing and define a threshold that suspends use.

"We removed the sensitive field" is a design fact, not a fairness result.
"Independent audit" is only as strong as its scope, date, sample, and match to
the deployed version. Fairness evidence is a snapshot with an expiry date.

---

## Transparency, explainability, and the record of a decision

**Transparency** asks whether people can know that AI is involved, what it does,
and what limits apply. **Explainability** asks whether a specific output can be
meaningfully accounted for. A system may be transparent in documentation and
still produce an output nobody can reconstruct.

Match explanation depth to stakes. A T1 drafting tool needs a label; a system
influencing employment, eligibility, or access needs a decision record:
material inputs, output, rule applied, reviewer, override, and contest route.
Keep that record in the business process, not only in vendor telemetry.

A generated after-the-fact explanation may be a plausible narrative rather than
the actual reason; fluency is not causation. A supplier **model card** is a
starting document, not proof of fitness for *your* use case.

Transparency also has an internal dimension: staff need to know when to distrust
the tool. Publish a short "do not rely on this without review" list and make
escalation easy. If people must guess whether review is required, the control
fails when needed.

---

## Human oversight that is actually a control

"Human in the loop" is a phrase, not a control. It becomes one only when:

- **Authority** — the reviewer can say no, without career cost.
- **Information** — the reviewer sees relevant sources, limits, and
  consequences.
- **Time** — there is enough attention to examine the output; a queue of two
  hundred click-throughs is a rubber stamp.

**Automation bias** — favouring an authoritative-looking suggestion — grows with
fluency and time pressure. Show uncertainty where available, require evidence for
high-stakes acceptance, sample reviews, and record overrides without treating
each as an error. A high override rate may mean a poor tool or engaged
reviewers; investigate.

Depth follows tier: T1 an acceptable-use rule; T2 a named reviewer; T3
documented review, a contest route, and a threshold that suspends automated
use. The human remains accountable; the tool absorbs no responsibility.

---

## Incident response for AI-enabled systems

Do not build a parallel "AI incident process". Extend the existing one. What
changes is the evidence and the remediation surface.

| Stage | AI-specific question | Typical extension |
|---|---|---|
| Detect | Bad output, data exposure, poisoned input, or vendor change? | Add quality and drift signals to monitoring |
| Triage | Which decisions used affected outputs, and who was affected? | Map output consumers and decision records |
| Contain | Can access be limited or the feature suspended? | Pre-agreed kill switch, rollback, retrieval scope limit |
| Investigate | Which prompts, sources, permissions, versions were involved? | Preserve logs and access records under custody rules |
| Recover | Are corrected decisions traced and communicated? | Decision recall, correction notices, re-evaluation sample |
| Notify | Which obligations apply, and who decides? | Legal/privacy assessment against verified rules |
| Learn | What control was missing, and what is the retest criterion? | Register update, intake change, vendor discussion |

Three traps recur: focusing on the model when the failure was a permission or
data flow; deleting logs needed for investigation; and announcing a cause before
evidence supports it. AI incidents involve chains of small design choices, so a
confident first statement is hard to walk back.

This is defensive operational education, with no instructions for manipulating
models, crafting adversarial inputs, or circumventing safeguards.

---

## Procurement questions: test the claim, do not repeat it

Supplier assurances are **marketing claims** until their scope, evidence, and
exclusions are examined. Ask before signature:

1. What does the advertised accuracy figure measure, on what data, baseline?
2. May we evaluate the tool on our own representative data under our terms?
3. Are prompts, outputs, or embeddings stored, staff-reviewed, or used for
   training or improvement? For how long, and in which regions?
4. How are tenant boundaries and permissions enforced during retrieval?
5. Will we be notified before a model or service version change reaches users?
6. Can we pin a version or roll back, and was the procedure tested?
7. Which subcontractors and model providers are in the chain, and where is data
   processed?
8. What incident-notification commitments exist, with what timeline and contact?
9. What audit claims are made, what is their scope, and when were they issued?
10. How are admin access, privileged functions, and logging handled?
11. What evaluation evidence exists for *our* use case, not a generic benchmark?
12. Which limitations and inappropriate uses does the vendor document?
13. How are corrections, complaints, and human review supported in the product?
14. What are data return, deletion, and exit-assistance terms?
15. What if the supplier is acquired, changes pricing materially, or retires the
    model?

Record answers as evidence. A claim that cannot be contracted should not underpin
a risk acceptance. Also consider **concentration risk**: several critical
workflows depending on one provider, region, or model create a shared failure
mode no certificate addresses.

---

## Regulatory scanning without legal claims

A CISO can say "we are examining applicable rules" without becoming a lawyer —
if the process is disciplined. Keep a **source register**: source, version or
date, applicability questions, owner, last verified. Check the issuer, not a
summary blog; route interpretation to qualified counsel.

| Source | What it offers | What it does **not** do | Verify |
|---|---|---|---|
| NIST AI Risk Management Framework | Voluntary risk vocabulary and structure | Not a law or certification scheme | Current version and playbook |
| ISO/IEC 42001 | Management-system structure for AI governance | A certificate does not prove one system is safe | Edition and certificate scope |
| EU AI Act | Risk-based regulatory framework with phased duties | Not global; role and use case matter | Official texts and dates; legal advice |
| GDPR and national privacy laws | Rules for personal data in many AI uses | Do not answer every fairness question | Law in each relevant jurisdiction |
| Community LLM guidance, e.g. OWASP | Defensive terminology and risk categories | Not regulation; changes often | Current release; guidance only |

Name internal policy as authoritative and say what you are *not* asserting: no
blanket compliance claim, no statutory interpretation, no promise that a
framework covers every system. Regulatory scanning is a **repeatable habit of
verification**, not a one-time slide. Rules and versions move; last quarter's
sentence may be stale. This is education, not legal or regulatory advice.

---

## Three fictional case studies

These cases are invented and illustrative. They show decisions and artifacts,
not technical procedures.

### Case 1 — The HR screening tool

**Context.** A company pilots a vendor tool that ranks applicants for a
technical role. The deck cites high accuracy and calls the model "bias-free".
A recruiter "reviews" rankings but sees only a rank and a label. Applicant data
comes from several countries.

**Constraints.** Hiring is high-impact. HR wants the pilot before the next
cycle. Legal capacity is limited. The vendor cannot explain every ranking, and
its contract permits input use for service improvement.

**Decisions.** The CISO assigns **T3** and blocks production use pending an
impact assessment. The team requests anonymised historical data and defines
error-rate and selection-rate questions in advance. They ask for data-use
restrictions and change notice; the vendor declines the training restriction.
The review interface now shows source material, records reasons, and allows
escalation. A candidate contest route is drafted with HR and counsel. With those
gaps unresolved, the sponsor approves only a non-decisional pilot for recruiter
training — no applicant is rejected or advanced by the tool.

**Outcome.** The pilot yields evidence but no hiring decision; legal review
continues. The register holds an open item with an owner and date rather than a
"closed" label because a demo went well.

**What this teaches.** Vendor confidence is not evidence about your population.
Changing interface and decision authority mattered more than changing the model.
Tiering created the authority to say "not yet" without pretending to be an
ethics board.

### Case 2 — The customer chatbot with sensitive data

**Context.** A support organisation connects a chatbot to its knowledge base
and account system for billing questions. Agents notice answers quoting another
customer's details; transcripts contain full account identifiers.

**Constraints.** Customers already use the tool; switching it off may overwhelm
support. The vendor can change the service remotely. Transcripts are kept for a
year under "quality assurance".

**Decisions.** The commander treats this as a data-exposure incident first and
an AI-quality problem second. The integration is restricted via the pre-agreed
kill switch; retrieval is narrowed to published content. Transcripts and access
records are preserved under custody rules. The team identifies affected
conversations through decision records and sample queries, then asks privacy and
legal colleagues to assess notification duties using verified rules. Retention
is shortened to an investigation window. A permission-boundary test with a named
retest criterion precedes any account-connected feature. Manual support capacity
is restored and communicated.

**Outcome.** The tool returns in a restricted, non-account-connected mode. The
register records the exposure, control changes, and residual concern. A follow-
up asks why the design review never tested cross-customer retrieval.

**What this teaches.** The failure was a design and permission problem surfaced
through an AI interface. Extending the ordinary playbook was faster and more
defensible than inventing a new one. Limiting exposure came before polishing
answers.

### Case 3 — The board that wants "an AI policy"

**Context.** A board asks for a one-page AI policy at the next meeting.
Directors want assurance the organisation is not "behind". There is no
inventory, yet three business units already use AI features.

**Constraints.** One page cannot express the range of uses. The board wants a
decision now. The CISO has no legal authority to declare compliance.

**Decisions.** The CISO offers two documents. The first is a short **policy
statement**: purpose, scope, prohibited uses, tier definitions, ownership,
escalation route. The second is an **evidence pack**: initial inventory, intake
flow, two impact assessments, and a risk register with open items and owners.
The presentation separates facts ("eleven systems found, four need
reassessment") from proposals ("T3 sign-off at committee"). The CISO declines
to claim compliance and asks the board to approve the *process* and a review
date, not a permanent verdict. A quarterly status line is proposed: systems,
assessments due, incidents, exceptions, decisions needed.

**Outcome.** Directors approve the process and request a six-month follow-up.
Two unowned systems gain owners within a fortnight. The policy stays one page;
the evidence grows.

**What this teaches.** A policy without evidence is theatre. Executives earn
trust by showing what they know, what they do not, and what will be measured
next — not by promising a document solved the problem.

---

## Practice by decision point

Answer aloud before opening each key.

**Q1.** A team says it "isn't really AI, it's just a smart filter" scoring
employee performance. Register it?
<details><summary>Key</summary>

Yes. Govern by what the system does and what decisions it influences, not the
label. A model-assisted output affecting evaluations belongs in the inventory.

</details>

**Q2.** An employee admits pasting customer records into a public assistant to
draft a reply. First two moves?
<details><summary>Key</summary>

Thank them and capture the facts (which data, which tool, when), then assess
whether an incident or disclosure obligation arises under verified rules. A
punishment-first culture drives shadow AI underground.

</details>

**Q3.** A vendor says its tool is "the same model everywhere". Why are two
departments' uses not equivalent?
<details><summary>Key</summary>

Risk depends on data, integration, authority, and affected people. The same
model is low tier for drafting and high tier for eligibility decisions. Tier the
use case.

</details>

**Q4.** A high-tier tool has no named owner and intake stalls. What now?
<details><summary>Key</summary>

STOP deployment. Escalate to the sponsor and require an accountable owner with
authority to accept residual risk. An unowned high-tier system is an exception
nobody can close.

</details>

**Q5.** The tool will be retired in six months. Does that remove the need for a
retention decision?
<details><summary>Key</summary>

No. Prompts, outputs, logs, and embeddings created now may outlive the tool.
Decide retention and deletion across vendor and local copies before launch, and
record who confirms deletion at exit.

</details>

**Q6.** A vendor promises "no customer data used for training". What next?
<details><summary>Key</summary>

Ask separately about storage, staff review, retention, regions, subcontractors,
and retrieval use, then put relevant promises in the contract. Training is only
one data path.

</details>

**Q7.** An evaluation reports improved fairness. What makes you trust it?
<details><summary>Key</summary>

Check the metric, sample, date, version, performer, and accepted trade-off.
Ask for re-testing on your cases. A number without scope is not evidence.

</details>

**Q8.** Reviewers approve 99% of recommendations in under two seconds. Is
oversight working?
<details><summary>Key</summary>

Almost certainly not. Check authority, information, and time; sample reviews
for scrutiny; show source material; investigate whether volume or interface
design made the gate a rubber stamp.

</details>

**Q9.** A fluent answer was wrong and a customer acted on it. What belongs in
the record?
<details><summary>Key</summary>

Affected decision and customer, input/output, version, source material, reviewer,
containment, corrections, and evidence for each claim. Separate observed fact
from early hypothesis.

</details>

**Q10.** During an AI incident someone proposes deleting all prompt logs to
"clean up". Respond.
<details><summary>Key</summary>

Pause deletion of relevant records. Preserve what investigation and custody
rules require, apply the approved retention decision, and document any later
disposal.

</details>

**Q11.** A supplier refuses to discuss model changes. Governance response?
<details><summary>Key</summary>

Record a residual risk; require change notice or version pinning if possible;
add regression tests on a fixed sample; escalate acceptance to an owner who can
decide whether to proceed.

</details>

**Q12.** A vendor cites an "independent AI audit". Three questions?
<details><summary>Key</summary>

Who performed it and with what independence? What was in scope, on what data and
version? When, and does the deployed configuration match? The label alone
proves little.

</details>

**Q13.** A director asks if the organisation is "compliant with the AI Act".
Defensible answer?
<details><summary>Key</summary>

State what was verified, by whom, and for which systems; note that applicability
depends on role, geography, and use case; say confirmation is sought. Do not
improvise a legal conclusion.

</details>

**Q14.** A framework uses a term your organisation defines differently. What do
you do?
<details><summary>Key</summary>

Check the current version and its definition, then map the terms explicitly in
the source register. Silently reusing a label with a different meaning makes
governance documents decorative.

</details>

**Q15.** The board wants a single "AI is safe" assurance. What do you offer?
<details><summary>Key</summary>

A bounded statement: scope, systems assessed, evidenced controls, open risks
and owners, next review date. Refuse an unbounded guarantee.

</details>

---

## Common mistakes worth memorising

- **Policy without inventory** — principles but not one named system.
- **Model-first thinking** — governing the algorithm while ignoring data,
  permissions, and the downstream decision.
- **Vendor-claim copy-paste** — repeating marketing percentages as your own test.
- **Rubber-stamp oversight** — calling a click-through a control.
- **Metric worship** — one fairness number as a moral verdict.
- **Infinite logs** — keeping every prompt forever and creating a second problem.
- **Parallel playbook** — an AI incident process omitting legal, privacy, and
  communications colleagues.
- **Frozen evidence** — a one-time assessment treated as valid after change.
- **Compliance theatre** — claiming a framework or regulation you have not
  scoped or verified.
- **No exit plan** — depending on a supplier with no data return or continuity.

---

## Reusable templates and checklists

Copy these into your notes; their value comes from honest completion.

### AI system intake template

```
System name:          [business name, not marketing name]
Purpose:              [decision or task supported]
Business owner:       [name, role, accountable for outcomes]
Technical contact:    [name / team]
Type:                 [built / bought / embedded feature / unknown]
Vendor + version:     [name, service or model identity, date observed]
Data inputs:          [categories + sensitivity + source]
Data outputs:         [recipients + decision driven]
Integrations:         [systems, permissions, retrieval boundaries]
Affected people:      [customers / staff / candidates / public]
Human review:         [none / advisory / mandatory before action]
Reversibility:        [reversible / costly / irreversible]
Tier:                 [T0 / T1 / T2 / T3] + rationale
Data-use terms:       [training / storage / retention / regions / processors]
Evaluation plan:      [sample, metric, threshold, owner, date]
Contest / correction: [route for affected people, where applicable]
Rollback / kill switch:[who suspends, how, last tested]
Open gaps:            [each gap has an owner and due date]
Decision:             [approve pilot / STOP / ESCALATE to ______]
Review date:          [date + trigger for earlier review]
```

### AI risk register

| ID | Scenario | Tier | Likelihood rationale | Impact rationale | Controls | Evidence | Residual risk | Treatment | Owner | Review |
|---|---|---|---|---|---|---|---|---|---|---|
| AI-01 | | | | | | | | mitigate / accept / avoid / transfer | | |
| AI-02 | | | | | | | | mitigate / accept / avoid / transfer | | |

Write likelihood and impact in words. An empty **Evidence** column means a
control is unverified. An accepted risk needs a named owner and date.

### Procurement question card

```
[ ] Accuracy metric + data + baseline understood?
[ ] Our own evaluation permitted under our terms?
[ ] Training / storage / review / retention / regions answered separately?
[ ] Tenant and permission boundaries documented?
[ ] Version changes notified; pinning or rollback possible?
[ ] Subcontractors and processing locations listed?
[ ] Incident notification timeline and contact agreed?
[ ] Audit claims scoped, dated, matched to deployed version?
[ ] Limitations and inappropriate uses documented?
[ ] Corrections, complaints, human review supported?
[ ] Data return, deletion, exit assistance in contract?
[ ] Concentration risk considered across the portfolio?
```

### Quarterly board status line

```
Systems: [n] | New: [n] | Assessments due: [n] | Incidents: [n]
Open T3 exceptions: [n] | Decisions needed: [one line]
```

---

## Glossary

| Term | Plain-language meaning |
|---|---|
| **AI system** | Product or workflow using a model to produce an output someone acts on |
| **Shadow AI** | A tool staff use without approval |
| **Impact tier** | Category based on how serious a wrong or harmful output could be |
| **Intake** | Structured first review of a proposed AI use |
| **Data provenance** | Where data came from and under what terms it may be used |
| **Data lineage** | How data moved and changed from source to output |
| **Inference** | Running a model on an input to produce an output |
| **Training** | Adjusting a model with data; different from retrieval or inference |
| **Retrieval** | Looking up content at answer time, usually from a knowledge source |
| **Prompt** | Input to a system, which may itself become stored data |
| **Automation bias** | Tendency to trust an authoritative-looking suggestion too much |
| **Human oversight** | Review with real authority, information, and time |
| **Contestability** | Route for an affected person to challenge or correct a decision |
| **Drift** | Change in behaviour or data making an old assessment unreliable |
| **Residual risk** | What remains after controls are applied |
| **Exit plan** | How the organisation continues if a supplier or tool goes away |

---

## References and verification

Verify versions, dates, and applicability with issuing bodies. This is a study
starting point, not a compliance determination.

- **EC-Council program information** — the **CCISO v4 / AI-Enhanced** label was
  seen in materials checked **26 Nov 2026**. Confirm brand, blueprint, and
  policies on [eccouncil.org](https://www.eccouncil.org/) and
  [cert.eccouncil.org](https://cert.eccouncil.org/).
- **NIST AI Risk Management Framework** — voluntary risk vocabulary and
  structure; check current version and companion materials.
- **ISO/IEC 42001** — AI management-system standard; check edition and exact
  certificate scope before relying on a claim.
- **EU AI Act and GDPR official texts** — applicability depends on jurisdiction,
  role, and use case; check official sources and dates, and obtain legal advice.
- **OWASP guidance for large language model applications** — community
  guidance for terminology and defensive design; check the current release.
- **MITRE ATLAS** — a knowledge base of adversary behaviour against AI systems,
  useful for defensive threat modelling, not a set of instructions.
- **Internal policies, risk appetite, contracts, and local rules** take
  precedence over public frameworks in internal decisions.
- **Companion CSIX notes (independent study sites):** [CSIX ISO 27001](https://siedysoes.github.io/csix-iso27001/),
  [CSIX COBIT](https://siedysoes.github.io/csix-cobit/),
  [CSIX ITIL](https://siedysoes.github.io/csix-itil/),
  [CSIX ECSA](https://siedysoes.github.io/csix-ecsa/),
  [CSIX CPENT AI](https://siedysoes.github.io/csix-cpent/). Replace `siedysoes`
  at deployment.

Vendor percentages, benchmarks, and survey statistics are **marketing claims**
unless independently reproduced under your conditions. This article is
educational: not legal, regulatory, financial, tax, or investment advice, and no
substitute for official course material or qualified professional judgement.

## See also

- [What Is CCISO v4](../fundamentals/what-is-cciso.md)
- [The Five Domains: Govern to Strategize](../fundamentals/five-domains.md)
- [Frameworks & Tools for the Executive](../exam/frameworks-tools.md)
- [Board Communication & Executive Presence](board-communication.md)
- [Risk, Finance & Vendor Governance](risk-finance.md)
- [Careers After CCISO](cciso-careers.md)
