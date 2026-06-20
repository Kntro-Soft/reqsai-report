# Changelog — Reqs-AI Report

All notable changes to this report are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and versioning follows [Semantic Versioning](https://semver.org/).

---

## [Unreleased]

### Added

- Section 7.1 (Software Configuration Management) covering development environment configuration, source code management (GitFlow and Conventional Commits), style guides (Angular/Service-as-a-Store and Spring Modulith conventions), and AWS deployment configuration with C4 Model diagram

### Changed

- Workspace `Organization`: `OrgStatus` now documents the `PENDING` state (the window between persisting the organization and finishing tenant-schema provisioning; the `TenantSchemaResolver` excludes it until it becomes `ACTIVE`)
- Workspace `GenerationSettings.meetingLanguage` retyped from `String` to the `LanguageCode` value object, now documented as part of the **Shared Kernel** (reused by the Discovery context's `DiscoverySession.language`)

**Authors:** Gutiérrez Soto, Jhosepmyr Orlando — Sulca Gonzales, Paul

---

## [2.2] - 2026-05-09

### Added

- GitHub Actions workflow to automatically generate a PDF from README.md on every merge to `main`, with the output available as a downloadable artifact in Actions (90-day retention)
- Local testing guide for GitHub Actions workflows using `act` (`ACT_LOCAL_TESTING.md`)
- `ReqsAI-Report.pdf` added to `.gitignore` to prevent accidental commits of generated files

**Author:** Gutiérrez Soto, Jhosepmyr Orlando

---

## [2.1] - 2026-05-09

### Changed

- TP1 feedback refinement: uniform expansion of all 5 Context Mapping patterns (ACL toward Jira, ACL toward LLM/STT, Customer/Supplier Discovery↔Workspace, Conformist Workspace↔Billing, OHS+PL Discovery↔Gateway) with detailed contracts, evolution scenarios, and explicit tradeoffs
- Rewrite of the Container Diagram with an explicit declaration of Modular Monolith vs. Microservices, Bounded Context → Maven Module mapping, and automated dependency rules using ArchUnit

**Author:** Gutiérrez Soto, Jhosepmyr Orlando

---

## [2.0] - 2026-04-26

### Added

- Software Architecture C4 diagrams: System Landscape, System Context, Container, and Deployment
- Final update of the Product Backlog in Jira
- Report conclusions section

**Authors:** Hernández Tuiro, Eric Ernesto — Gutiérrez Soto, Jhosepmyr Orlando

---

## [1.8] - 2026-04-26

### Added

- Analysis and findings from interviews for technical and functional roles
- Impact Mapping section
- Student Outcomes section

**Authors:** Varela Bustinza, Marcelo — Ramirez Mestanza, Salim — Sulca Gonzales, Paul

---

## [1.7] - 2026-04-26

### Added

- Complete Domain-Driven Design section: EventStorming, Context Discovery, Context Mapping, Bounded Context Canvases

**Author:** Hernández Tuiro, Eric Ernesto

---

## [1.6] - 2026-04-26

### Added

- User Personas (Empathy Mapping, User Journey, User Task Matrix)
- As-Is and To-Be scenario modeling

**Authors:** Sulca Gonzales, Paul — Gutiérrez Soto, Jhosepmyr Orlando

---

## [1.5] - 2026-04-25

### Changed

- Updated general project and report information

**Author:** Varela Bustinza, Marcelo Alessandro

---

## [1.4] - 2026-04-24

### Changed

- Drafted competitor strategies and tactics
- Updated the competitors section
- Technical iteration of user stories (INVEST criteria)

**Authors:** Varela Bustinza, Marcelo — Gutiérrez Soto, Jhosepmyr Orlando

---

## [1.3] - 2026-04-23

### Added

- Epics and User Stories in BDD format with acceptance criteria
- Prioritized Product Backlog
- Quality Attribute Scenarios

**Authors:** Gutiérrez Soto, Jhosepmyr Orlando — Hernández Tuiro, Eric Ernesto

---

## [1.2] - 2026-04-22

### Added

- Competitive analysis of competitors
- Preliminary design of interview questions
- Repository exclusions configuration (`.gitignore`)

**Authors:** Varela Bustinza, Marcelo — Ramirez Mestanza, Salim

---

## [1.1] - 2026-04-17

### Added

- Project background and problem statement
- Complete Lean UX process
- Target segments definition
- Team profiles (Team Profiles section)

**Author:** Hernández Tuiro, Eric Ernesto

---

## [1.0] - 2026-04-14

### Added

- Base report structure created
- Cover page with UPC and Kntro-Soft logos
- Initial description of the Kntro-Soft startup and Reqs-AI product

**Author:** Hernández Tuiro, Eric Ernesto
