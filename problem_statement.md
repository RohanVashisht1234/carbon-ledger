# Software Engineering & Project Management

## Case Study no. 38

### CarbonLedger - Emissions Accounting for a Multi-Plant Manufacturer

#### Problem Statement:
A manufacturer with nine plants must report emissions across three scopes to a customer who has made it a supply contract condition. Data comes from electricity bills, fuel purchase records, logistics invoices and supplier declarations of varying reliability. The calculation is not difficult; the auditability is. A reported figure must be reproducible two years later from the same inputs with the same emission factors, and emission factors are revised annually by the publishing authority, which means the system must apply the factor that was valid at the time, not the current one. (With Proper Justification)

#### Given Project Data (use these figures - do not invent your own):
- **Reproducibility:** design the versioning of emission factors so a 2024 report recomputes identically in 2026. Specify the requirement and the test that proves it.
- **Data quality tiers:** metered (±2%), invoiced (±8%), estimated (±25%). Specify how uncertainty propagates to the reported total and how it is disclosed.
- **Decision table inputs:** data source (metered / invoiced / estimated / missing), scope (1 / 2 / 3), supplier declaration present (Y/N), period closed (Y/N). Build the table and derive the test set.

#### Objectives
- **Requirements Engineering:** Specify calculation, factor versioning, uncertainty disclosure and period-close rules; define precisely what happens to a late invoice after period close.
- **Testing & Quality Assurance:** Build the decision table above and derive tests; design the reproducibility regression test that recomputes a historical report.
- **Software Design & UML:** Design temporal reference data; draw the class diagram for activity data, emission factor and report, and an activity diagram for a reporting cycle.
- **Configuration Management:** Version reference data and calculation logic together so a report is reproducible as a pair, not just as code.
- **Metrics & Quality Assurance:** Define data quality metrics per plant and a target for shifting estimated data to metered over three reporting cycles.
- **Project Management:** Produce a WBS, a Gantt aligned to the customer's contractual reporting date, and a risk register including supplier non-response.

---

## Software Engineering & Project Management

#### Outcomes
- A temporal reference data design that makes historical reproduction possible by construction.
- A decision table covering the awkward combinations, especially missing data after period close.
- An uncertainty disclosure method that is honest rather than falsely precise.
- A regression test that recomputes an old report and compares it byte for byte.
- A data quality improvement target with a measurable trajectory.

#### Deliverables
- **SRS** - Calculation, factor versioning, uncertainty, period close and late-data rules.
- **Decision Table & Test Set** - Complete table, derived tests, reproducibility regression test.
- **Design Pack** - Temporal data model, class diagram, reporting cycle activity diagram.
- **Configuration Management Plan** - Joint versioning of code and reference data.
- **Data Quality Plan** - Per-plant metrics and a three-cycle improvement target.
- **Project Plan** - WBS, Gantt to contractual date, risk register.

*B.Tech CSE 2024-28 Software Engineering & Project Management Semester V*
