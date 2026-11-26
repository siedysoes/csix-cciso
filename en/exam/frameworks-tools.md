# Frameworks & Tools for the Executive

A CISO does not need to memorise every framework sentence. They need to know **which tool answers which business question**, and what that tool cannot do. This unofficial guide maps common frameworks and tools to executive decisions. Verify current versions and official guidance from each standard body and from [eccouncil.org](https://www.eccouncil.org/train-certify/certified-chief-information-security-officer-cciso/), [cert.eccouncil.org](https://cert.eccouncil.org/), and [ciso.eccouncil.org/cciso-certification](https://ciso.eccouncil.org/cciso-certification/). EC-Council states that policies may change without notice; framework names and trademarks belong to their respective owners.

## Frameworks: what each one is for

| Framework | Executive question it helps answer |
|---|---|
| ISO/IEC 27001 | Do we have a managed information security management system? |
| ISO 27005 | How do we structure information risk assessment and treatment? |
| NIST CSF | Where are we on Core functions, and what is our target profile? |
| NIST RMF | How do we categorise, authorise, and monitor a system's risk? |
| COBIT | Are our enterprise IT governance processes accountable and measurable? |
| MITRE ATT&CK | Which adversary behaviours should our detections and tests cover? |
| Zero Trust | Why should no user or workload be trusted by default? |
| TOGAF / Zachman / SABSA | How does security fit into enterprise architecture and strategy? |

None of these replaces judgment. A framework is a structured way to ask questions, not a certificate of safety.

## Tools and practices you should recognise

- **GRC platforms** track controls, evidence, policies, and audits — useful for visibility, but only as good as the data entered.
- **SIEM and SOAR** collect and correlate signals and can automate response steps; they need tuning and human oversight.
- **DevSecOps tooling** includes SAST, DAST, and IAST for finding software issues earlier in the lifecycle.
- **Cryptography and PKI** support confidentiality, integrity, identity, and signing; key management matters as much as algorithms.
- **Privacy impact assessments** help identify and document privacy risks in a new project or data use.

## Law and regulation: examples only

GDPR, HIPAA, SOX, PCI DSS, and the EU AI Act are examples of regulatory or contractual areas a leader may encounter. Applicability depends on country, sector, data, and organisation size. **Verify applicability with official sources and qualified professionals.** Nothing here is legal, financial, tax, or regulatory advice.

## Study it the executive way

For each framework, write one page with four lines: **purpose**, **main concepts**, **one artifact it produces**, and **one limitation**. Example: NIST CSF can help set a target profile, but it does not by itself implement controls. Then connect the framework to the five domains — Govern (COBIT, ISO 27001), Operate (SIEM/SOAR), Secure (Zero Trust, DevSecOps), Strategize (architecture, risk appetite). See [A Practical Study Plan](study-plan.md) for a writing routine.

## Go deeper in the CSIX companion sites

- [CSIX ISO 27001:2022](https://siedysoes.github.io/csix-iso27001/) — ISMS requirements and Annex A controls
- [CSIX ISO 27001 Assessor](https://siedysoes.github.io/csix-iso27001-assessor/) — auditing and certification
- [CSIX COBIT 7](https://siedysoes.github.io/csix-cobit/) — IT governance
- [CSIX ITIL 5](https://siedysoes.github.io/csix-itil/) — service management
- [CSIX CPENT AI](https://siedysoes.github.io/csix-cpent/) — offensive-security context

Vendor surveys and product claims are marketing, not guarantees that a tool or framework will deliver a specific outcome.

## See also
- [The Five Domains: Govern to Strategize](../fundamentals/five-domains.md)
- [A Practical Study Plan](study-plan.md)
- [Risk, Finance & Vendor Governance](../career/risk-finance.md)
- [AI Governance: Reality Check](../career/ai-governance.md)
- [CCISO vs CISSP & Other Leader Creds](../fundamentals/cciso-vs-cissp.md)
