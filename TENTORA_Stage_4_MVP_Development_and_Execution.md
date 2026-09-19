# 🛠️ Stage 4: MVP Development & Execution – TENTORA

## Overview

TENTORA is an AI-powered, curated creative-solutions platform that helps project owners obtain creative work through two connected paths:

1. **Design Now:** Select a Ready Design, customize approved properties, preview the result, then save or export it.
2. **Work With a Creative:** Select services, discover visual taste, receive up to six recommendations, choose a creative or team, and manage the project through delivery.

The MVP is planned as a web application using **React, Flask, and PostgreSQL**.

> [!IMPORTANT]
> Stage 4 is an implementation and evidence plan. Planned features must not be reported as completed until they are implemented, tested, and supported by evidence.

---

## Technologies Used

| Area | Technology |
| :--- | :--- |
| **Backend** | Python and Flask REST API |
| **Frontend** | React, JavaScript, HTML5, and CSS3 |
| **Styling** | Tailwind CSS or the approved styling system |
| **Database** | PostgreSQL |
| **ORM & Migrations** | SQLAlchemy and migration tooling |
| **Authentication** | JWT-based progressive authentication |
| **API Documentation** | Swagger / OpenAPI |
| **File Storage** | Local storage during development, with an object-storage interface |
| **AI & Matching** | Controlled AI actions, weighted tags, cosine similarity, and rule-based ranking |
| **Version Control** | Git and GitHub |
| **Project Management** | GitHub Projects and GitHub Issues |
| **Database Inspection** | Postico or another PostgreSQL client |
| **Development Environment** | Visual Studio Code |

---

## MVP Development Objectives

The implementation stage aims to deliver and validate:

- Five visible and clickable sector entry points.
- Sector-specific services and curated creative examples.
- Clear access to Design Now and Work With a Creative.
- A complete **Restaurants & Cafés** functional pilot.
- A controlled Ready Design catalogue.
- Ready Design customization using approved properties.
- At least one validated preview and export flow.
- Limited AI-assisted discovery or customization.
- One or multiple service selections inside one project.
- One Main Taste Profile per project.
- Optional service-specific taste refinement.
- Curated Creative DNA.
- Explainable recommendations limited to six options.
- Creative profiles and portfolio exploration.
- Design-to-Creative handoff.
- A basic project workspace.
- Progressive authentication that preserves anonymous progress.

---

## Approved Sectors

The following sector names must remain consistent across the interface, database, routes, filters, test data, and documentation:

| # | Sector |
| :---: | :--- |
| 1 | **Restaurants & Cafés** |
| 2 | **Real Estate & Development** |
| 3 | **Events & Occasions** |
| 4 | **Exhibitions & Conferences** |
| 5 | **E-commerce** |

> [!NOTE]
> All five sectors will be visible and clickable. **Restaurants & Cafés** will be the first complete end-to-end functional pilot. The other sectors may initially use clearly labeled demo content.

---

## Approved MVP Journeys

### 🎨 Design Now

`Sector → Service → Ready Design → Customize → Preview → Save or Export`

Design Now begins with a structured Ready Design. It does not begin with blank-canvas AI generation and does not require the full Taste Discovery experience.

### ✨ Create with AI

`Describe Need → Interpret Request → Recommend Designs, Services, or Creatives`

The MVP focuses on prompt interpretation and retrieval of approved content rather than unrestricted design generation.

### 🤝 Work With a Creative

`Sector → Select Services → Taste Discovery → Main Taste Profile → Up to Six Recommendations → Selection → Workspace → Delivery`

### 🔄 Connected Handoff

`Saved Ready Design → Continue With a Creative → Transfer Design Context → Professional Development`

---

## Agile Methodology

The MVP will follow an Agile workflow organized into four proposed one-week sprints.

Each sprint includes:

1. Sprint planning.
2. Task assignment.
3. Development.
4. Continuous testing.
5. Pull Request review.
6. Sprint demonstration.
7. Sprint retrospective.
8. Evidence collection.

### Priority Method

| Priority | Meaning |
| :--- | :--- |
| **Must Have** | Required for the main MVP journey. |
| **Should Have** | Important but may be simplified if time is limited. |
| **Could Have** | Added only after Must Have requirements are stable. |
| **Won’t Have** | Explicitly excluded from Stage 4. |

---

## Team Roles & Responsibilities

| Team Member | Primary Role | Implementation Responsibilities |
| :--- | :--- | :--- |
| **Banan Aleid** | Database Lead & Project Manager | Database schema, migrations, data integrity, sprint planning, task coordination, documentation tracking, and delivery oversight. |
| **Khuloud Alqarni** | Backend Lead with Frontend & UI Support | Flask APIs, backend modules, integration, selected React components, and UI implementation after team restructuring. |
| **Layan Aldosari** | QA Engineer | Test planning, API testing, UI testing, defect tracking, regression testing, and evidence collection. |

### Shared or Unassigned Responsibilities

The following responsibilities must receive a named owner before their sprint begins:

- AI prompt interpretation.
- Taste Profile calculation.
- Creative DNA classification.
- Matching logic.
- Ready Design preparation.
- Creative-rights verification.
- Accessibility review.
- Deployment and environment configuration.

> One person may hold more than one responsibility, but every task must have a named owner and acceptance criteria.

---

# 🚀 Sprint Execution Plan

## Sprint 1: Platform Foundation & Sector Discovery

### Goal

Create the technical foundation and allow users to explore all five sectors, their services, and curated creative work.

### Backend & Database Tasks

- Initialize the Flask application using the modular structure defined in Stage 3.
- Configure PostgreSQL and database migrations.
- Create core user, sector, service, creative-profile, portfolio, and style-tag tables.
- Implement sector and service catalogue endpoints.
- Implement public creative-profile and portfolio endpoints.
- Seed the five approved sectors.
- Add the initial service taxonomy.
- Add anonymous-session support.

### Frontend Tasks

- Initialize the React application and route structure.
- Build the main landing-page entry.
- Build `SectorNavigation`.
- Build `SectorPage`.
- Build `ServiceFilters`.
- Build `ServiceGallery`.
- Build the initial public `CreativeProfile`.
- Add loading, empty, and error states.
- Create responsive desktop and mobile layouts.

### Content & Curation Tasks

- Define the controlled service taxonomy.
- Define the initial style-tag categories.
- Prepare approved or clearly labeled demo profiles.
- Prepare portfolio metadata.
- Confirm which content is licensed for public MVP use.

### QA Focus

- Five-sector visibility.
- Sector and service navigation.
- Correct service filtering.
- Public portfolio visibility.
- API response structures.
- Database relationships.
- Responsive layout.
- Basic accessibility.

### Sprint 1 Exit Criteria

- [ ] All five sectors are visible and clickable.
- [ ] Each sector displays its approved services.
- [ ] Curated work appears under the correct service.
- [ ] Public creative profiles load from the API.
- [ ] Anonymous browsing works without registration.
- [ ] Demo profiles and designs are clearly labeled.

---

## Sprint 2: Design Now Pilot

### Goal

Allow a user to select a Ready Design, modify approved properties, preview the result, and save or export it.

### Backend & Database Tasks

- Create Ready Design tables.
- Create Ready Design version and property tables.
- Create license and creator-rights tables.
- Create design-session and session-value tables.
- Create export and preview records.
- Implement Ready Design catalogue endpoints.
- Implement design-session creation and update endpoints.
- Validate all changes against the Ready Design schema.
- Implement the initial preview workflow.
- Implement the first approved export format.
- Implement one approved AI-assisted action or deterministic alternative.

### Frontend Tasks

- Build `ProductPathChoice`.
- Build `ReadyDesignGallery`.
- Build `ReadyDesignCard`.
- Build `DesignEditorShell`.
- Build schema-driven `PropertyControl`.
- Build `DesignCanvas`.
- Add preview, save, reset, and export actions.
- Display creator attribution.
- Display license and permitted-use information.
- Add progressive authentication when the user saves or exports.

### Ready Design Tasks

- Confirm the Restaurants & Cafés pilot service.
- Prepare the approved pilot design collection.
- Define editable and locked properties.
- Define AI permissions.
- Define supported export formats.
- Test realistic text lengths and uploaded images.
- Confirm attribution, ownership, and license information.

### QA Focus

- Only approved properties can be changed.
- Locked properties cannot be changed.
- Invalid values are rejected.
- Preview reflects stored values.
- Export produces the approved format.
- Creator attribution appears correctly.
- AI actions preserve design rules.
- Anonymous progress survives registration.

### Sprint 2 Exit Criteria

- [ ] At least one Ready Design works end to end.
- [ ] The pilot catalogue loads by sector and service.
- [ ] A user can customize approved properties.
- [ ] A valid preview can be generated.
- [ ] A user can save or export the result.
- [ ] Rights information is complete.
- [ ] Unsupported AI actions are blocked.

---

## Sprint 3: Project Needs, Taste & Matching

### Goal

Allow a client to select one or multiple services, complete Taste Discovery, and receive no more than six relevant recommendations.

### Backend & Database Tasks

- Create project and project-service tables.
- Create Taste Test and Taste Session tables.
- Create Taste Profile and weighted-tag tables.
- Create Creative DNA tables.
- Create recommendation-run and recommendation-option tables.
- Implement My Project Needs endpoints.
- Implement Taste Discovery endpoints.
- Store selected, rejected, and skipped images.
- Generate one Main Taste Profile.
- Implement optional service-specific direction.
- Aggregate approved portfolio tags into Creative DNA.
- Implement candidate filtering.
- Implement the initial matching score.
- Generate concise recommendation explanations.
- Support limited team recommendations when necessary.

### Frontend Tasks

- Build `ProjectNeedsTray`.
- Build multi-service selection.
- Build `TasteDiscovery`.
- Build `TasteProfileSummary`.
- Build optional `ServiceDirectionEditor`.
- Build `CreativeMatches`.
- Build `RecommendationCard`.
- Build `RecommendationReason`.
- Add save, reject, compare, and select actions.

### Data & Curation Tasks

- Prepare Taste Discovery images.
- Assign reviewed style tags.
- Review portfolio attributes.
- Confirm services covered by each creative.
- Prepare a controlled matching-evaluation dataset.
- Clearly label fictional or demo profiles.

### QA Focus

- One Main Taste Profile is created per project.
- The Taste Profile is reused across selected services.
- Service refinement does not repeat the full test.
- Unapproved creatives are excluded.
- Recommendations never exceed six options.
- Recommendation reasons match stored data.
- Team options contain only necessary members.

### Sprint 3 Exit Criteria

- [ ] A client can select multiple services.
- [ ] Taste Discovery creates one stored profile.
- [ ] Optional service refinement is stored separately.
- [ ] Matching returns a ranked result.
- [ ] Results contain no more than six options.
- [ ] Every recommendation includes understandable reasons.
- [ ] Matching evaluation results or corrective actions are documented.

---

## Sprint 4: Handoff, Workspace & System Hardening

### Goal

Connect the product paths, support professional execution, and stabilize the complete MVP demonstration.

### Backend & Database Tasks

- Implement progressive registration.
- Transfer anonymous-session ownership after authentication.
- Implement creative selection.
- Implement Design-to-Creative handoff snapshots.
- Create workspace-membership tables.
- Create messages, files, milestones, feedback, and deliverable tables.
- Implement protected workspace endpoints.
- Add authorization and ownership checks.
- Add audit events for handoff, rights, AI, exports, and approvals.
- Resolve critical integration and data-integrity issues.

### Frontend Tasks

- Add **Continue With a Creative** to saved designs.
- Preserve design version, content, values, assets, and preview references.
- Build the basic `ProjectWorkspace`.
- Build message and file views.
- Build milestone tracking.
- Build feedback and deliverable views.
- Complete authentication-conversion flows.
- Refine loading, empty, success, and error states.
- Complete responsive and accessibility reviews.

### QA Focus

- Complete Design Now journey.
- Complete Work With a Creative journey.
- Design-to-Creative handoff integrity.
- Anonymous-to-authenticated ownership transfer.
- Workspace access control.
- File and asset privacy.
- Deliverable version history.
- Regression testing.

### Sprint 4 Exit Criteria

- [ ] Both primary product paths can be demonstrated.
- [ ] Handoff preserves the required design context.
- [ ] Anonymous work transfers without loss.
- [ ] Unauthorized users cannot access private projects.
- [ ] Critical defects are closed or formally documented.
- [ ] Final test evidence is attached.
- [ ] Demonstration steps are documented.

---

## Sprint Planning

Before each sprint, the team must:

- Confirm the sprint goal.
- Review previous sprint dependencies.
- Create GitHub Issues.
- Assign task owners.
- Add priorities and acceptance criteria.
- Identify QA tasks before development begins.
- Confirm the sprint demonstration.
- Confirm the evidence required for completion.

---

## Sprint Reviews

At the end of each sprint, record:

- Completed features.
- Partially completed features.
- Deferred features.
- Pull Requests merged.
- Test results.
- Screenshots or recordings.
- Important feedback.
- Scope or architecture decisions.
- Remaining defects.

> Board status alone is not sufficient evidence of implementation.

---

## Retrospectives

After each sprint, the team should document:

- What worked well.
- What caused delays.
- Which defects required rework.
- Which communication problems occurred.
- What should change during the next sprint.
- Whether the remaining scope is achievable.

---

## Source Control Strategy

### Branching Strategy

- **`main`** — stable and reviewed code.
- **`develop`** — integration branch.
- **`feature/*`** — feature development.
- **`fix/*`** — defect correction.
- **`docs/*`** — documentation changes.

### Git Workflow

Before starting a task:

```bash
git pull origin develop
git checkout -b feature/short-name
```

After completing and testing the task:

```bash
git add <specific-files>
git commit -m "Add concise feature description"
git push origin feature/short-name
```

A Pull Request is then created from the feature branch into `develop`.

### Example Branches

```text
feature/sector-navigation
feature/ready-design-editor
feature/taste-discovery
feature/creative-matching
feature/project-workspace
fix/anonymous-session-transfer
docs/api-documentation
```

---

## Pull Request Requirements

Each Pull Request should include:

- Problem being solved.
- Implemented solution.
- Related GitHub Issue.
- Acceptance criteria addressed.
- Files and modules changed.
- Screenshots for visual changes.
- API examples for endpoint changes.
- Database migration notes.
- Tests executed.
- Test results.
- Known limitations.
- Security implications.
- Creator-rights implications.

### Pull Request Checklist

- [ ] Issue and acceptance criteria linked.
- [ ] Branch contains only relevant changes.
- [ ] Code formatting passes.
- [ ] Linting passes.
- [ ] Tests pass or limitations are documented.
- [ ] Database migrations are included.
- [ ] API documentation is updated.
- [ ] UI screenshots are attached.
- [ ] Security and authorization are reviewed.
- [ ] Creative-rights effects are reviewed.
- [ ] At least one peer review is complete.
- [ ] QA verification is complete.

---

## Quality Assurance Strategy

| Test Type | Scope |
| :--- | :--- |
| **Unit Testing** | Validation, Taste Profile calculations, matching scores, permissions, and state transitions. |
| **API Testing** | HTTP methods, schemas, status codes, authorization, validation, and persistence. |
| **Database Testing** | Relationships, constraints, migrations, rollback, and data integrity. |
| **Frontend Testing** | User interaction, forms, editor controls, loading, empty, success, and error states. |
| **Integration Testing** | Frontend-to-API, API-to-database, renderer, storage, and AI flows. |
| **End-to-End Testing** | Design Now, Work With a Creative, handoff, authentication, and workspace. |
| **Security Testing** | Ownership, roles, token handling, uploads, rights enforcement, and data isolation. |
| **Accessibility Testing** | Keyboard navigation, labels, focus, contrast, image alternatives, and editor controls. |
| **Usability Testing** | Path clarity, editor ease, Taste Discovery time, matching relevance, and handoff comprehension. |

---

## Defect Severity

| Severity | Definition | Release Rule |
| :--- | :--- | :--- |
| **Critical** | Data loss, unauthorized access, rights violation, unusable export, or broken core journey. | Must be fixed before acceptance. |
| **High** | Major feature failure without a reliable workaround. | Fix before the final demonstration unless formally accepted. |
| **Medium** | Partial failure with an available workaround. | Fix if capacity allows or document clearly. |
| **Low** | Cosmetic or minor usability issue. | May be deferred with an issue reference. |

### Bug Workflow

`New → Triaged → Assigned → In Progress → Ready for QA → Verified → Closed`

If the defect is not resolved or cannot be reproduced, it returns to the responsible developer with QA evidence.

---

## MVP Test Plan

> [!WARNING]
> Test status must remain **Not Run** until the scenario is actually executed.

| ID | Feature | Test Scenario | Expected Result | Status |
| :--- | :--- | :--- | :--- | :--- |
| **T-01** | Sector Discovery | Open the sector catalogue. | Five approved sectors are displayed. | Not Run |
| **T-02** | Service Filtering | Select a sector. | Only relevant services and work appear. | Not Run |
| **T-03** | Path Choice | Open a service. | Design Now and Work With a Creative are distinguishable. | Not Run |
| **T-04** | Ready Design | Open a published design. | The correct version and controls load. | Not Run |
| **T-05** | Property Validation | Submit an invalid property value. | API rejects it without corrupting the session. | Not Run |
| **T-06** | Preview | Change properties and request a preview. | Preview reflects the stored values. | Not Run |
| **T-07** | Export | Request an approved format. | Export completes and an authorized download is available. | Not Run |
| **T-08** | AI Permission | Request a disallowed AI action. | The action is blocked safely. | Not Run |
| **T-09** | Creator Rights | Publish a design with missing rights fields. | Publication is blocked. | Not Run |
| **T-10** | Multi-Service Needs | Add multiple services. | All services remain in one project. | Not Run |
| **T-11** | Taste Discovery | Complete the visual selections. | One Main Taste Profile is created. | Not Run |
| **T-12** | Taste Reuse | Continue through selected services. | The complete test is not repeated. | Not Run |
| **T-13** | Service Direction | Refine one service. | The change is stored separately. | Not Run |
| **T-14** | Creative Filtering | Run matching with unapproved profiles. | Unapproved profiles are excluded. | Not Run |
| **T-15** | Recommendation Limit | Generate recommendations. | No more than six options appear. | Not Run |
| **T-16** | Recommendation Reason | View an option. | Taste, service, and sector reasons appear. | Not Run |
| **T-17** | Anonymous Conversion | Register after temporary activity. | Ownership transfers without losing progress. | Not Run |
| **T-18** | Handoff | Continue from a design to a creative. | Design data, content, and assets are preserved. | Not Run |
| **T-19** | Workspace Access | Open another client’s project. | Access is denied. | Not Run |
| **T-20** | Deliverable Version | Submit a revised deliverable. | The previous version remains in history. | Not Run |

---

## API Testing Checklist

- [ ] Correct HTTP status code returned.
- [ ] Correct JSON response structure returned.
- [ ] Required fields are validated.
- [ ] Domain rules are enforced.
- [ ] Authentication is enforced where required.
- [ ] Authorization and ownership are enforced.
- [ ] Database persistence is verified.
- [ ] Errors do not expose internal information.
- [ ] Repeated requests do not create unintended duplicate data.
- [ ] API documentation matches implementation.

---

## Usability Test Tasks

Representative users should be asked to:

1. Identify the difference between Design Now and Work With a Creative.
2. Select the Restaurants & Cafés sector.
3. Find and customize a Ready Design.
4. Preview or export the design.
5. Select multiple creative services.
6. Complete Taste Discovery.
7. Explain why a recommended creative appears relevant.
8. Transfer a saved design to a creative.

Record:

- Completion status.
- Time required.
- Errors.
- Confusing areas.
- User comments.
- Assistance required.

---

## Definition of Done

A task is complete only when:

- [ ] Acceptance criteria are satisfied.
- [ ] Code builds and runs without relevant errors.
- [ ] Required tests pass.
- [ ] API documentation is updated.
- [ ] Database migrations are included and verified.
- [ ] Authentication and authorization effects are tested.
- [ ] Creative-rights effects are reviewed.
- [ ] Loading, empty, success, and error states are implemented.
- [ ] Responsive behavior is checked.
- [ ] Accessibility checks are completed.
- [ ] Pull Request is reviewed and approved.
- [ ] QA evidence is attached.
- [ ] Known limitations are documented.

---

## Local Development Environment

### Backend

The Flask API runs locally during development.

```text
http://localhost:5000
```

### Frontend

The React development server runs locally.

```text
http://localhost:5173
```

### Database

The project uses local PostgreSQL or an approved development container.

Postico or another PostgreSQL client may be used to inspect the database.

> Database structure must be changed through migrations, not manual edits.

### Storage

Local development storage may be used during early implementation, but the application should use a storage interface that can later connect to private object storage.

---

## Environment Variables & Secrets

Real secret values must never be committed to GitHub.

An `.env.example` file may include safe placeholder values:

```env
FLASK_ENV=development
DATABASE_URL=postgresql://user:password@localhost:5432/tentora
JWT_SECRET_KEY=replace-me
FRONTEND_ORIGIN=http://localhost:5173
STORAGE_BACKEND=local
STORAGE_PATH=./storage
AI_PROVIDER=disabled
AI_API_KEY=replace-me
```

The real `.env` file must be excluded using `.gitignore`.

---

## MVP Demonstration Plan

### Demo 1 — Design Now

1. Select **Restaurants & Cafés**.
2. Select a pilot service such as Menu Design.
3. Open a Ready Design.
4. Change approved content and properties.
5. Run one approved AI-assisted action, if implemented.
6. Preview the result.
7. Save or export the design.

### Demo 2 — Work With a Creative

1. Select one or multiple services.
2. Complete Taste Discovery.
3. View the Main Taste Profile.
4. Optionally refine one service direction.
5. View no more than six recommendations.
6. Review recommendation reasons.
7. Select a creative or team.
8. Open the project workspace.

### Demo 3 — Connected Handoff

1. Open a saved Design Now session.
2. Select **Continue With a Creative**.
3. Confirm that design context transfers.
4. Open the resulting professional project.

> If any feature is simulated, it must be labeled as a **Prototype**, **Mock**, or **Demo**, not as a completed backend feature.

---

## Implementation Risks

| Risk | Effect | Response |
| :--- | :--- | :--- |
| **Four sprints are insufficient** | Core journeys remain incomplete. | Prioritize one complete vertical slice for each path. |
| **Ready Design editor becomes too broad** | Sprint 2 is delayed. | Use one renderer and controlled two-dimensional properties. |
| **No dedicated AI/ML engineer** | Taste or matching lacks ownership. | Assign a named owner and use transparent rule-based methods. |
| **Insufficient Ready Designs** | Editor demonstration becomes weak. | Approve designs, rights, schema, and assets before development. |
| **Incomplete portfolio data** | Matching quality becomes unreliable. | Prioritize accurate tags over catalogue size. |
| **Team matching is too complex** | Results become unstable. | Use small teams only when service coverage requires them. |
| **Rights data is incomplete** | Designs cannot be published safely. | Block publication until all required rights fields are complete. |
| **Old project code is reused unchanged** | Interior-design provider concepts remain. | Map every reused component and table to the TENTORA model. |
| **Test evidence is collected late** | Final report cannot prove implementation. | Attach evidence during every sprint. |
| **Secrets appear in Git history** | Security and submission risk. | Use `.env`, `.gitignore`, secret scanning, and immediate key rotation. |

---

## Evidence Register

Replace `TBD` only with real evidence.

| Evidence | Reference | Status |
| :--- | :--- | :--- |
| **TENTORA GitHub Repository** | TBD | Pending |
| **GitHub Project Board** | TBD | Pending |
| **Sprint 1 Review** | TBD | Pending |
| **Sprint 2 Review** | TBD | Pending |
| **Sprint 3 Review** | TBD | Pending |
| **Sprint 4 Review** | TBD | Pending |
| **API Documentation** | TBD | Pending |
| **Database Diagram & Migrations** | TBD | Pending |
| **Design Now Demonstration** | TBD | Pending |
| **Taste & Matching Demonstration** | TBD | Pending |
| **Connected Handoff Demonstration** | TBD | Pending |
| **Final QA Report** | TBD | Pending |

> Do not reuse evidence links from the previous Interior Design Platform unless the repository has officially become the TENTORA repository and the source code has been replaced with the TENTORA implementation.

---

## Completion Summary Template

Complete this section only at the end of Stage 4.

| Area | Planned | Implemented | Verified | Evidence |
| :--- | :---: | :---: | :---: | :--- |
| **Sector & Service Discovery** | Yes | Pending | Pending | TBD |
| **Design Now Catalogue** | Yes | Pending | Pending | TBD |
| **Interactive Editor** | Yes | Pending | Pending | TBD |
| **AI-Assisted Discovery** | Yes, Limited | Pending | Pending | TBD |
| **Multi-Service Project Needs** | Yes | Pending | Pending | TBD |
| **Main Taste Profile** | Yes | Pending | Pending | TBD |
| **Service-Specific Direction** | Yes | Pending | Pending | TBD |
| **Creative DNA** | Yes | Pending | Pending | TBD |
| **Up-to-Six Recommendations** | Yes | Pending | Pending | TBD |
| **Creative Profiles** | Yes | Pending | Pending | TBD |
| **Design-to-Creative Handoff** | Yes | Pending | Pending | TBD |
| **Basic Workspace** | Yes | Pending | Pending | TBD |
| **Progressive Authentication** | Yes | Pending | Pending | TBD |

### Final Summary

At the end of Stage 4, replace this paragraph with a factual summary of:

- What was implemented.
- What was tested and verified.
- What was deferred.
- Known limitations.
- Links to supporting evidence.

---

## Stage 4 Conclusion

Stage 4 implements the technical architecture defined during Stage 3.

The planned four-sprint sequence is:

1. Platform foundation and five-sector discovery.
2. Restaurants & Cafés Ready Design pilot.
3. Taste Discovery and creative matching.
4. Connected handoff, workspace, integration, and system hardening.

The stage is not complete until the implementation is supported by Pull Requests, tests, screenshots, demonstrations, and QA evidence.

> **Next Step:** After implementation and verification, proceed to Stage 5 — Project Closure.
