# 5. Current Landscape and Baseline Analysis

This chapter presents the findings of the T4.2 stock-taking activity on **existing processes, technical implementations supporting online services, identity matching and identity management**. Its purpose is to establish the baseline against which the EUDIW-enabled use cases are designed: how things work today, what technology is already in place at each touchpoint, and where the gaps and pain points are. The chapter is the empirical ground of this deliverable: every design decision captured in the UC specifications (Chapter 4) and every risk flagged in Chapter 9 can be traced back to a finding recorded here.

### Purpose and role of the chapter

The chapter serves two purposes that complement each other.

The first purpose is to **justify the design choices** made in the UC specifications. By documenting what the current process looks like for each sector (travel, hospitality, student mobility), the chapter makes explicit the reasons why the EUDIW-enabled variant is being piloted. 

The second purpose is to provide the **"before" picture** against which the pilot results reported in D4.3 will later be evaluated. The stock-taking phase captures, in narrative form, the current processing times, the current manual steps, the current points of friction, and the current operational constraints. When D4.3 reports on the piloted implementations, it will refer back to this baseline to quantify the improvements (or the lack thereof) that the EUDIW-enabled variant delivers. For this reason, the findings are recorded with the necessary level of detail that will later support  comparison.

### Scope of the baseline

The baseline captured in this chapter covers three sectors, corresponding to the three WP4 scenarios:

* **Transport**, including air, rail, ferry, bus, and urban mobility. The baseline addresses how airlines, rail operators, ferry companies, bus operators, and transport authorities currently issue tickets, verify identity, and manage boarding.
* **Hospitality**, covering the booking-to-check-in chain. The baseline addresses how hotels take online bookings through online travel agencies (OTAs) or direct channels, how they perform identity verification at the front desk (typically through manual passport scanning), and how they report guest data to national police-registration systems where local law requires it.
* **Student mobility and access to campus services**, covering the issuance and acceptance of student credentials at European universities. The baseline addresses how universities currently issue and verify student cards, how ERASMUS students enrol at host institutions, how access-control systems work at campus entry points, and how student-fare discounts are granted by transport operators.

Within each sector, the analysis looks at the **existing digital infrastructure** (APIs, apps, identity systems, authentication mechanisms) that WP4 implementations will need to interoperate with, complement, or gradually replace. The chapter does not aim to describe every sector exhaustively; rather, it focuses on the touchpoints that the 11 WP4 use cases will actually address.

### How the chapter was produced

The content of this chapter is the consolidated output of contributions from all 11 UC leads, integrated by the WP4 coordinator (GRNET). Each UC lead, starting from its own sector and from the partner organisations it had engaged, contributed:

1. A description of the **current process** in its sector, based on first-hand operational knowledge of the credential issuers and relying parties involved in the use case (for example, airline operations teams for UC 1, hotel chains for UC 10, university student-services offices for UC 6).
2. A description of the **existing technical implementations** that support that process today: the identity systems (such as proprietary loyalty accounts, booking reference codes, university enrolment databases), the authentication mechanisms in place, the APIs exposed by the relying party to its own internal systems, and any third-party services (such as transliteration engines, watchlist checks) currently relied on.
3. A list of the **pain points** observed during the stock-taking interviews, ordered by the frequency with which they were reported across UC leads.

### Structure of the chapter

The chapter is organised into three sections, each addressing one of the three analytical dimensions defined in the T4.2 work plan.

* **Section 5.1 — Current Processes and Existing Implementations** describes how each of the three sectors currently handles the processes that WP4 aims to transform with the EUDIW. For each sector, the section presents the typical end-to-end flow from the user's perspective, the operational constraints that shape it, and the existing digital infrastructure that supports it. Particular attention is given to the interfaces that WP4 implementations will need to interoperate with (such as IATA NDC for airlines, OSDM for rail, national police-registration APIs for hotels, and institution-specific student-services systems for universities).
* **Section 5.2 — Identity Matching and Management** analyses how organisations in each sector currently match a person to their booking, ticket, or enrolment. It documents the current approaches (name-based matching against a passport or a national ID, booking reference codes, proprietary loyalty accounts, university enrolment databases) and their limitations (transliteration errors, name discrepancies across documents, the absence of an interoperable identity layer across providers or borders). The section then describes how the EUDIW technologies (cryptographic binding of the PID to the wallet, verifiable credentials, selective disclosure, trusted issuer lists) address these limitations by shifting the identity-matching problem from error-prone string comparison to cryptographic verification.
* **Section 5.3 — Current Constraints, Limitations and Pain Points** synthesises the pain points that emerge from Sections 5.1 and 5.2 into a consolidated view. It covers fragmented identity verification across touchpoints, the lack of credential portability between providers, the dependency on physical documents, long processing times at the point of service, inconsistent cross-border experiences, language barriers, and the limited accessibility support available today. The section also identifies the technical constraints (legacy systems, lack of standardised APIs, proprietary data formats) and the operational constraints (staff training requirements, regulatory inertia) that the pilot implementations will need to work within or around.

