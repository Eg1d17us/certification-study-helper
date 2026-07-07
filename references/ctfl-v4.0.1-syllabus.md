# ISTQB Certified Tester Foundation Level (CTFL) Syllabus v4.0.1

Source: ISTQB CTFL Syllabus v4.0.1 (errata release 2024-09-15, based on v4.0 general release 2023-04-21). Examinable content = chapters 1–6. Introduction and Appendices are not examinable. Highest cognitive level tested is K3.

Exam: 40 multiple-choice questions, 60 minutes, pass mark 26/40 (65%).

Minimum accredited training time: 1135 minutes across six chapters.

---

## Chapter 1 — Fundamentals of Testing (180 min)

**Keywords:** coverage, debugging, defect, error, failure, quality, quality assurance, root cause, test analysis, test basis, test case, test completion, test condition, test control, test data, test design, test execution, test implementation, test monitoring, test object, test objective, test planning, test procedure, test process, test result, testing, testware, traceability, validation, verification

**Learning Objectives:**
- FL-1.1.1 (K1) Identify typical test objectives
- FL-1.1.2 (K2) Differentiate testing from debugging
- FL-1.2.1 (K2) Exemplify why testing is necessary
- FL-1.2.2 (K1) Recall the relation between testing and quality assurance
- FL-1.2.3 (K2) Distinguish between root cause, error, defect, and failure
- FL-1.3.1 (K2) Explain the seven testing principles
- FL-1.4.1 (K2) Explain the different test activities and related tasks
- FL-1.4.2 (K2) Explain the impact of context on the test process
- FL-1.4.3 (K2) Differentiate the testware that supports the test activities
- FL-1.4.4 (K2) Explain the value of maintaining traceability
- FL-1.4.5 (K2) Compare the different roles in testing
- FL-1.5.1 (K2) Give examples of the generic skills required for testing
- FL-1.5.2 (K1) Recall the advantages of the whole team approach
- FL-1.5.3 (K2) Distinguish the benefits and drawbacks of independence of testing

### 1.1 What is Testing?
Software testing is a set of activities to discover defects and evaluate the quality of software work products (test objects). Testing is more than executing tests. It involves **verification** (checking the system meets specified requirements) and **validation** (checking it meets users'/stakeholders' needs in the operational environment). Testing may be **dynamic** (execution of software) or **static** (reviews and static analysis — no execution). Testing is largely an intellectual activity requiring analytical skills, critical thinking, and systems thinking.

**1.1.1 Test Objectives:** evaluating work products (requirements, user stories, designs, code); causing failures and finding defects; ensuring required coverage; reducing risk level of inadequate quality; verifying requirements fulfilled; verifying compliance (contractual, legal, regulatory); providing information for stakeholder decisions; building confidence in quality; validating the test object is complete and works as expected. Objectives vary by context.

**1.1.2 Testing and Debugging:** separate activities. Testing can trigger failures (dynamic) or find defects directly (static). Debugging (dynamic) = reproduction, diagnosis, fixing the defect. Confirmation testing checks the fix; regression testing checks nothing else broke. For static testing, debugging just removes the defect (no reproduction/diagnosis).

### 1.2 Why is Testing Necessary?
Testing is a form of quality control that helps achieve objectives within scope/time/quality/budget.

**1.2.1 Contributions to success:** cost-effective defect detection, direct quality evaluation supporting release decisions, indirect user representation.

**1.2.2 Testing and QA:** Testing is a **product-oriented, corrective** approach — a major form of quality control. QA is a **process-oriented, preventive** approach focused on improving processes (everyone's responsibility). Test results feed both: testing uses them to fix defects; QA uses them for process feedback.

**1.2.3 Errors, Defects, Failures, Root Causes:** A human **error** (mistake) produces a **defect** (fault, bug), which may cause a **failure**. Not all defects cause failures; failures can also come from environmental conditions (e.g., radiation). A **root cause** is the fundamental reason for a problem, found via root cause analysis.

### 1.3 Testing Principles (seven)
1. **Testing shows the presence, not the absence of defects.**
2. **Exhaustive testing is impossible** (except trivial cases) — use techniques, prioritization, risk-based testing.
3. **Early testing saves time and money** (shift left).
4. **Defects cluster together** (Pareto principle).
5. **Tests wear out** — repeating the same tests loses effectiveness.
6. **Testing is context dependent.**
7. **Absence-of-defects fallacy** — verification alone doesn't guarantee success; validation is also needed.

### 1.4 Test Activities, Testware and Test Roles
**1.4.1 Activities (a test process):** Test planning; test monitoring and test control; test analysis ("what to test?"); test design ("how to test?"); test implementation (create testware); test execution (run tests, compare/log results, analyze anomalies); test completion (archive testware, lessons learned, completion report). Often iterative/parallel.

**1.4.2 Test Process in Context** — factors: stakeholders, team members, business domain, technical factors, project constraints, organizational factors, SDLC, tools.

**1.4.3 Testware** — outputs per activity: planning (test plan, schedule, risk register, entry/exit criteria); monitoring/control (progress reports, control directives); analysis (test conditions, defect reports on test basis); design (test cases, charters, coverage items, test data/environment requirements); implementation (test procedures, scripts, suites, test data, execution schedule, environment items e.g. stubs/drivers/simulators/service virtualizations); execution (test logs, defect reports); completion (completion report, action items, lessons learned, change requests).

**1.4.4 Traceability** (test basis ↔ testware ↔ results ↔ defects): supports coverage evaluation, impact analysis, audits, IT governance, clearer reports.

**1.4.5 Roles:** **Test management role** (planning, monitoring, control, completion) and **testing role** (analysis, design, implementation, execution). One person can hold both.

### 1.5 Essential Skills and Good Practices
**1.5.1 Generic skills:** testing knowledge; thoroughness/curiosity/attention to detail; communication & teamwork; analytical/critical thinking/creativity; technical knowledge; domain knowledge. Testers are "bearers of bad news" — communicate defects constructively.

**1.5.2 Whole team approach** (from Extreme Programming): any member with skills can do any task; everyone owns quality; co-location aids collaboration. Not always appropriate (e.g., safety-critical may need independence).

**1.5.3 Independence of testing:** levels — author (none), author's peers (some), testers outside team but in org (high), outside org (very high). Benefit: independent testers find different defects, challenge assumptions. Drawbacks: isolation, communication problems, developers losing quality ownership, bottleneck perception.

---

## Chapter 2 — Testing Throughout the SDLC (130 min)

**Keywords:** acceptance testing, black-box testing, component integration testing, component testing, confirmation testing, functional testing, integration testing, maintenance testing, non-functional testing, regression testing, shift left, system integration testing, system testing, test level, test object, test type, white-box testing

**Learning Objectives:**
- FL-2.1.1 (K2) Explain the impact of the chosen SDLC on testing
- FL-2.1.2 (K1) Recall good testing practices that apply to all SDLCs
- FL-2.1.3 (K1) Recall the examples of test-first approaches to development
- FL-2.1.4 (K2) Summarize how DevOps might impact testing
- FL-2.1.5 (K2) Explain shift left
- FL-2.1.6 (K2) Explain how retrospectives can be used for process improvement
- FL-2.2.1 (K2) Distinguish the different test levels
- FL-2.2.2 (K2) Distinguish the different test types
- FL-2.2.3 (K2) Distinguish confirmation testing from regression testing
- FL-2.3.1 (K2) Summarize maintenance testing and its triggers

### 2.1 Testing in the Context of an SDLC
SDLC models: sequential (waterfall, V-model), iterative (spiral, prototyping), incremental (Unified Process). Methods/practices: ATDD, BDD, DDD, XP, FDD, Kanban, Lean IT, Scrum, TDD.

**2.1.1 Impact:** SDLC affects scope/timing of test activities, documentation detail, techniques/approach, automation extent, tester's role. Sequential: early reviews/analysis, dynamic testing later. Iterative/incremental: static+dynamic at all levels each iteration, needs regression. Agile: lightweight docs, extensive automation, experience-based techniques.

**2.1.2 Good practices (all SDLCs):** every dev activity has a corresponding test activity; test levels have distinct objectives; test analysis/design begins in the corresponding dev phase (early testing); testers review drafts early (shift left).

**2.1.3 Testing as a driver (test-first):**
- **TDD** — directs coding through test cases; tests first, then code, then refactor.
- **ATDD** — tests derived from acceptance criteria during design; written before development.
- **BDD** — desired behavior in natural language (Given/When/Then), translated to executable tests.

**2.1.4 DevOps and Testing:** dev+ops synergy; CI/CD, automation, fast feedback. Benefits: fast feedback, CI promotes shift left, stable environments, non-functional visibility, less repetitive manual testing, reduced regression risk. Risks: pipeline setup, tool maintenance, automation resources. Manual testing still needed.

**2.1.5 Shift Left:** testing earlier (= early testing principle). Practices: review specs, write tests before code, use CI/CD, static analysis before dynamic, early non-functional testing. Extra early effort saves later. Needs stakeholder buy-in.

**2.1.6 Retrospectives:** held at end of project/iteration/milestone. Discuss what worked, what to improve, how to apply. Benefits: test effectiveness/efficiency, testware quality, team bonding/learning, better test basis, dev-test cooperation.

### 2.2 Test Levels and Test Types
**Test levels** (instances of the test process at a development phase); **test types** (grouped by quality characteristic, apply at any level).

**2.2.1 Five test levels:**
- **Component (unit) testing** — components in isolation; by developers.
- **Component integration testing** — interfaces between components; strategy: bottom-up/top-down/big-bang.
- **System testing** — overall behavior of whole system; functional + non-functional.
- **System integration testing** — interfaces with other systems/external services.
- **Acceptance testing** — validation, readiness for deployment; forms: UAT, operational, contractual, regulatory, alpha, beta.

Levels distinguished by: test object, objectives, test basis, defects/failures, approach & responsibilities.

**2.2.2 Four test types:**
- **Functional** ("what" it does): completeness, correctness, appropriateness.
- **Non-functional** ("how well"): ISO/IEC 25010 characteristics — performance efficiency, compatibility, usability (interaction capability), reliability, security, maintainability, portability (flexibility), safety.
- **Black-box** (specification-based): behavior vs specifications.
- **White-box** (structure-based): cover internal structure.

**2.2.3 Confirmation vs Regression:**
- **Confirmation testing** — confirms an original defect is fixed (rerun failed tests / add new).
- **Regression testing** — confirms no adverse consequences from a change. Uses impact analysis; strong candidate for automation.

### 2.3 Maintenance Testing
Categories: corrective, adaptive, perfective (performance/maintainability). Scope depends on: risk of change, size of existing system, size of change. Triggers: **modifications** (enhancements, corrective changes, hot fixes); **upgrades/migrations** of environment; **retirement** (data archiving, restore/retrieval).

---

## Chapter 3 — Static Testing (80 min)

**Keywords:** anomaly, dynamic testing, formal review, informal review, inspection, review, static analysis, static testing, technical review, walkthrough

**Learning Objectives:**
- FL-3.1.1 (K1) Recognize types of work products examinable by static testing
- FL-3.1.2 (K2) Explain the value of static testing
- FL-3.1.3 (K2) Compare and contrast static and dynamic testing
- FL-3.2.1 (K1) Identify the benefits of early and frequent stakeholder feedback
- FL-3.2.2 (K2) Summarize the activities of the review process
- FL-3.2.3 (K1) Recall responsibilities of the principal roles in reviews
- FL-3.2.4 (K2) Compare and contrast the different review types
- FL-3.2.5 (K1) Recall the factors that contribute to a successful review

### 3.1 Static Testing Basics
No execution. Manual examination (reviews) or tool-assisted (static analysis). Assesses readability, completeness, correctness, testability, consistency. Supports verification and validation.

**3.1.1 Examinable work products:** almost any readable work product (requirements, code, test plans/cases, backlog items, charters, contracts, models). Static analysis needs a formal structure. Not appropriate: hard-to-interpret items, 3rd-party executables (legal).

**3.1.2 Value:** detects defects earliest (early testing); finds defects dynamic testing can't (unreachable code, non-executable products); builds shared understanding; lower overall cost.

**3.1.3 Static vs Dynamic:** both detect defects but some types only via one. Static finds defects directly; dynamic causes failures analyzed later. Static reaches rarely-executed paths, non-executable products, non-code-dependent characteristics (maintainability). Typical static-found defects: requirement defects, design defects, coding defects, standards deviations, interface spec errors, security vulnerabilities, test basis coverage gaps.

### 3.2 Feedback and Review Process
**3.2.1 Early/frequent stakeholder feedback** prevents misunderstandings, aligns product with vision, focuses on value/risk.

**3.2.2 Review process activities** (ISO/IEC 20246): planning; review initiation; individual review (log anomalies/recommendations/questions); communication and analysis (decide status/ownership/actions); fixing and reporting.

**3.2.3 Roles & responsibilities:** manager (decides what, provides resources); author (creates/fixes); moderator/facilitator (runs meetings); scribe/recorder (records); reviewer (reviews); review leader (overall responsibility).

**3.2.4 Review types (informal → formal):**
- **Informal review** — no defined process, no formal output; goal: detect anomalies.
- **Walkthrough** — led by author; many objectives; individual review optional.
- **Technical review** — qualified reviewers, led by moderator; consensus/decisions on technical problems.
- **Inspection** — most formal, full process; goal: max anomalies; metrics collected; author can't be leader/scribe.

**3.2.5 Success factors:** clear objectives & measurable exit criteria (never evaluate participants); appropriate review type; small chunks; feedback to authors; adequate prep time; management support; part of culture; adequate training; facilitated meetings.

---

## Chapter 4 — Test Analysis and Design (390 min)

**Keywords:** acceptance criteria, acceptance test-driven development, black-box test technique, boundary value analysis, branch coverage, checklist-based testing, collaboration-based test approach, coverage, coverage item, decision table testing, equivalence partitioning, error guessing, experience-based test technique, exploratory testing, state transition testing, statement coverage, test technique, white-box test technique

**Learning Objectives:**
- FL-4.1.1 (K2) Distinguish black-box, white-box and experience-based test techniques
- FL-4.2.1 (K3) Use equivalence partitioning to derive test cases
- FL-4.2.2 (K3) Use boundary value analysis to derive test cases
- FL-4.2.3 (K3) Use decision table testing to derive test cases
- FL-4.2.4 (K3) Use state transition testing to derive test cases
- FL-4.3.1 (K2) Explain statement testing
- FL-4.3.2 (K2) Explain branch testing
- FL-4.3.3 (K2) Explain the value of white-box testing
- FL-4.4.1 (K2) Explain error guessing
- FL-4.4.2 (K2) Explain exploratory testing
- FL-4.4.3 (K2) Explain checklist-based testing
- FL-4.5.1 (K2) Explain how to write user stories in collaboration with developers/business
- FL-4.5.2 (K2) Classify the different options for writing acceptance criteria
- FL-4.5.3 (K3) Use ATDD to derive test cases

### 4.1 Test Techniques Overview
- **Black-box (specification-based):** from specified behavior, independent of implementation.
- **White-box (structure-based):** from internal structure; created after design/implementation.
- **Experience-based:** use tester knowledge/experience; complementary.

### 4.2 Black-Box Test Techniques
**4.2.1 Equivalence Partitioning (EP):** divide data into partitions processed the same way; one test per partition suffices. Partitions must not overlap, non-empty. Valid vs invalid partitions. Coverage items = partitions; 100% = every partition covered ≥ once. Each Choice coverage for multiple parameter sets.

**4.2.2 Boundary Value Analysis (BVA):** exercise boundaries of ordered partitions (developers err at boundaries). **2-value BVA**: boundary + closest neighbor in adjacent partition. **3-value BVA**: boundary + both neighbors (more rigorous — e.g., detects `if(x=10)` vs `if(x≤10)` with x=9). Coverage measured over boundary values (and neighbors for 3-value).

**4.2.3 Decision Table Testing:** conditions + actions in rows; each column = a decision rule (combination). Limited-entry (T/F) or extended-entry (values). Notation: T, F, – (irrelevant), N/A (infeasible); X (action occurs), blank (not). Coverage items = feasible columns; 100% = exercise all feasible columns. Finds gaps/contradictions in requirements.

**4.2.4 State Transition Testing:** state diagram (states + valid transitions; transition = "event [guard] / action"); state table (rows=states, cols=events; empty cells = invalid transitions). Coverage criteria: **all states coverage** (weakest); **valid transitions coverage** (0-switch — most widely used); **all transitions coverage** (valid + attempt invalid; avoids defect masking — minimum for mission/safety-critical). Full valid-transitions ⇒ full all-states. Full all-transitions ⇒ both.

### 4.3 White-Box Test Techniques
**4.3.1 Statement testing / coverage:** coverage items = executable statements. 100% = all executable statements exercised. Doesn't guarantee all decision logic / branches tested; may miss data-dependent defects.

**4.3.2 Branch testing / coverage:** a branch = transfer of control between two nodes (unconditional or conditional). 100% = all branches exercised. **Branch coverage subsumes statement coverage** (100% branch ⇒ 100% statement, not vice versa).

**4.3.3 Value of white-box testing:** whole implementation considered (finds defects even with vague spec); weakness — misses defects of omission (unimplemented requirements). Usable in static testing (dry runs). Provides objective coverage measurement.

### 4.4 Experience-Based Test Techniques
**4.4.1 Error Guessing:** anticipate errors/defects/failures from experience (past behavior, common developer mistakes, similar apps). **Fault attacks** = structured lists of possible errors. Related to input, output, logic, computation, interfaces, data.

**4.4.2 Exploratory Testing:** simultaneous design/execution/evaluation while learning the test object. Often **session-based** (time box, test charter, debriefing, session sheets). Useful with poor specs / time pressure; complements formal techniques; more effective with experienced testers.

**4.4.3 Checklist-Based Testing:** design/execute tests covering checklist conditions (built from experience, user importance, failure knowledge). Items often as questions. Update regularly via defect analysis; avoid too-long or too-general checklists. Provides guidance without detailed test cases; high-level = more coverage but less repeatability.

### 4.5 Collaboration-Based Test Approaches
Focus on **defect avoidance** via collaboration/communication.

**4.5.1 Collaborative User Story Writing:** "3 C's" — Card, Conversation, Confirmation (acceptance criteria). Format: "As a [role], I want [goal], so that [value]". Combine business/development/testing perspectives. Good stories = **INVEST** (Independent, Negotiable, Valuable, Estimable, Small, Testable).

**4.5.2 Acceptance Criteria:** conditions an implementation must meet; viewed as test conditions. Used to define scope, reach consensus, describe positive/negative scenarios, base acceptance testing, allow planning/estimation. Formats: **scenario-oriented** (Given/When/Then, BDD) or **rule-oriented** (bullet list / input-output table).

**4.5.3 ATDD:** test-first; test cases created before implementing the user story, by multiple perspectives. Steps: specification workshop → create test cases (from acceptance criteria). Positive first, then negative, then non-functional. Test cases understandable to stakeholders (natural language: preconditions, inputs, postconditions). Cover all story characteristics, don't go beyond; no duplicate test cases. Can become executable requirements when automated.

---

## Chapter 5 — Managing the Test Activities (335 min)

**Keywords:** defect management, defect report, entry criteria, exit criteria, product risk, project risk, risk, risk analysis, risk assessment, risk control, risk identification, risk level, risk management, risk mitigation, risk monitoring, risk-based testing, test approach, test completion report, test control, test monitoring, test plan, test planning, test progress report, test pyramid, test strategy, testing quadrants

**Learning Objectives:**
- FL-5.1.1 (K2) Exemplify the purpose and content of a test plan
- FL-5.1.2 (K1) Recognize how a tester adds value to iteration and release planning
- FL-5.1.3 (K2) Compare and contrast entry criteria and exit criteria
- FL-5.1.4 (K3) Use estimation techniques to calculate the required test effort
- FL-5.1.5 (K3) Apply test case prioritization
- FL-5.1.6 (K1) Recall the concepts of the test pyramid
- FL-5.1.7 (K2) Summarize the testing quadrants and their relationships with test levels/types
- FL-5.2.1 (K1) Identify risk level by using risk likelihood and risk impact
- FL-5.2.2 (K2) Distinguish between project risks and product risks
- FL-5.2.3 (K2) Explain how product risk analysis may influence thoroughness and test scope
- FL-5.2.4 (K2) Explain measures in response to analyzed product risks
- FL-5.3.1 (K1) Recall metrics used for testing
- FL-5.3.2 (K2) Summarize purposes, content, and audiences for test reports
- FL-5.3.3 (K2) Exemplify how to communicate the status of testing
- FL-5.4.1 (K2) Summarize how configuration management supports testing
- FL-5.5.1 (K3) Prepare a defect report

### 5.1 Test Planning
**5.1.1 Purpose & content:** documents means/schedule, ensures criteria met, communicates, aligns with policy/strategy. Content: context, assumptions/constraints, stakeholders, communication, risk register, test approach, budget & schedule.

**5.1.2 Tester's contribution:** **release planning** (product backlog, test approach across iterations); **iteration planning** (detailed risk analysis, testability, tasks, effort). Testers write testable stories/criteria, do risk analysis, estimate effort.

**5.1.3 Entry vs Exit criteria:** entry = preconditions to start (resources, testware, initial quality); exit = what declares an activity done (thoroughness measures, binary yes/no). Running out of time/budget can be valid exit criteria (with accepted risk). Agile: exit = **Definition of Done**, entry = **Definition of Ready**.

**5.1.4 Estimation techniques:**
- **Ratios** (metrics-based) — historical dev:test ratios (e.g., 3:2 → 600 dev-days ⇒ 400 test-days).
- **Extrapolation** (metrics-based) — extend early measurements (good for iterative).
- **Wideband Delphi** (expert-based, iterative consensus; **Planning Poker** variant).
- **Three-point estimation:** E = (a + 4m + b)/6; SD = (b − a)/6. Example a=6,m=9,b=18 → E=10, SD=2 → 10±2.

**5.1.5 Test Case Prioritization:** **risk-based**, **coverage-based** (incl. additional coverage), **requirements-based**. Dependencies may override priority; resource availability matters.

**5.1.6 Test Pyramid:** layers of tests by granularity. Higher layer = lower granularity, lower isolation, higher execution time, fewer tests. Bottom = small/fast/isolated (many). Top = complex end-to-end (few). Original (Cohn): unit / service / UI. Another: unit / integration / end-to-end.

**5.1.7 Testing Quadrants** (Marick): business-facing vs technology-facing × support the team vs critique the product.
- **Q1** (tech-facing, support team): component & component integration tests; automated, in CI.
- **Q2** (business-facing, support team): functional/user story tests, examples, prototypes, API, simulations; manual or automated.
- **Q3** (business-facing, critique product): exploratory, usability, UAT; user-oriented, often manual.
- **Q4** (tech-facing, critique product): smoke & non-functional tests (except usability); often automated.

### 5.2 Risk Management
Activities: **risk analysis** (identification + assessment) and **risk control** (mitigation + monitoring). **Risk-based testing** = activities selected/prioritized/managed by risk.

**5.2.1 Risk & attributes:** risk = potential event with adverse effect. **Risk likelihood** (probability, 0–1) × **risk impact** (harm) = **risk level**.

**5.2.2 Project vs Product risks:** **Project risks** (management/control): organizational, people, technical, supplier issues → affect schedule/budget/scope. **Product risks** (quality characteristics): missing/wrong functionality, wrong calculations, poor performance, security vulns → user dissatisfaction, revenue/reputation loss, damage, costs, penalties, injury/death.

**5.2.3 Product Risk Analysis:** risk identification (brainstorming, workshops, interviews, cause-effect diagrams) + assessment (categorize, likelihood/impact/level, prioritize). Quantitative (likelihood × impact) or qualitative (risk matrix). Influences scope, levels/types, techniques/coverage, effort, prioritization, additional activities.

**5.2.4 Product Risk Control:** mitigation (implement actions) + monitoring (check effectiveness, find emerging risks). Response options: mitigation by testing, acceptance, transfer, contingency plan. Mitigate by testing: right testers, appropriate independence, reviews/static analysis, appropriate techniques/coverage/types, dynamic + regression testing.

### 5.3 Test Monitoring, Control and Completion
**Test monitoring** gathers info to assess progress/exit criteria. **Test control** issues corrective directives (reprioritize, re-evaluate criteria, adjust schedule, add resources). **Test completion** consolidates experience/testware at milestones.

**5.3.1 Metrics:** project progress; test progress; product quality; defect; risk; coverage; cost metrics.

**5.3.2 Test reports:** **test progress reports** (ongoing control; period, progress, impediments, metrics, risks, next period). **Test completion reports** (summary, quality evaluation vs plan, deviations, impediments, metrics, unmitigated risks/unfixed defects, lessons learned). Audience affects formality/frequency (ISO/IEC/IEEE 29119-3 templates).

**5.3.3 Communicating status:** verbal; dashboards (CI/CD, task boards, burn-down charts); electronic channels; online docs; formal reports. Tailor to stakeholder; more formal for distributed teams.

### 5.4 Configuration Management
Identifies/controls/tracks work products as **configuration items**. Approved item = **baseline**, changed only via formal change control; possible to revert to reproduce results. Ensures unique identification, version control, traceability, unambiguous references. Often automated in DevOps pipeline.

### 5.5 Defect Management
Established process essential. Anomalies may be real defects, false positives, or change requests. Workflow: log → analyze/classify → decide response → close. Handle static-testing defects similarly.

**Defect report objectives:** enough info to resolve; track work-product quality; ideas for process improvement.

**Defect report content (dynamic testing):** unique identifier; title/summary; date, org, author + role; test object & environment; context (test case, activity, SDLC phase, technique/checklist/data); description enabling reproduction (steps, logs, dumps, screenshots); expected vs actual results; severity; priority; status (open, deferred, duplicate, waiting, awaiting confirmation, re-opened, closed, rejected); references. Some fields auto-filled by tools. (ISO/IEC/IEEE 29119-3 = "incident reports".)

---

## Chapter 6 — Test Tools (20 min)

**Keyword:** test automation

**Learning Objectives:**
- FL-6.1.1 (K2) Explain how different types of test tools support testing
- FL-6.2.1 (K1) Recall the benefits and risks of test automation

### 6.1 Tool Support for Testing
Types: test management tools; static testing tools; test design & implementation tools; test execution & coverage tools; non-functional testing tools; DevOps tools; collaboration tools; scalability/deployment tools (VMs, containers); any tool assisting testing (e.g., a spreadsheet).

### 6.2 Benefits and Risks of Test Automation
Acquiring a tool doesn't guarantee success (needs introduction/maintenance/training effort).

**Benefits:** time saved on repetitive work; fewer human errors (consistency/repeatability); more objective assessment; easier access to test info; reduced execution time (faster feedback); more time for testers to design deeper tests.

**Risks:** unrealistic expectations; inaccurate estimates; using automation when manual is better; over-reliance (ignoring critical thinking); vendor dependency; abandoned open-source; incompatibility with platform; unsuitable tool (regulatory/safety non-compliance).

---

## K-Level quick reference (CTFL tests K1–K3 only)
- **K1 Remember** — identify, recall, remember, recognize.
- **K2 Understand** — classify, compare, contrast, differentiate, distinguish, exemplify, explain, give examples, interpret, summarize.
- **K3 Apply** — apply, implement, prepare, use.
