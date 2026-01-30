
<!--
Sync Impact Report
Version change: template → 1.0.0
Modified principles: all template placeholders replaced
Added sections: Technology Stack & Constraints, Development Workflow
Removed sections: none
Templates requiring updates: plan-template.md (✅ aligned), spec-template.md (✅ aligned), tasks-template.md (✅ aligned)
Follow-up TODOs: TODO(RATIFICATION_DATE): Set original ratification date if known
-->

# RSSFeedReader Constitution

## Core Principles

### I. Security-First
All code MUST be designed and implemented to minimize security risks. Input validation, safe data handling, and secure defaults are required for all features. Dependencies MUST be kept up-to-date and reviewed for vulnerabilities.
Rationale: Protects user data and system integrity, especially as the app may handle external feeds and user input.

### II. Maintainability
Code MUST be clear, modular, and well-documented. Refactoring is encouraged. Features should be independently testable and changes must not introduce regressions.
Rationale: Ensures long-term sustainability and ease of future enhancements.

### III. Code Quality
All code MUST pass automated tests and code review before merging. Adhere to language and framework best practices (C#, .NET, Blazor). Use consistent formatting and naming conventions.
Rationale: High code quality reduces bugs and accelerates development.

### IV. Simplicity & MVP Discipline
Features MUST be implemented in the simplest way that delivers user value. MVP scope is strictly enforced: start with subscription management, then incrementally add feed fetching and display. Avoid premature optimization and unnecessary complexity.
Rationale: Enables rapid delivery and clear user value, supporting incremental improvement.

### V. Technology Alignment
All implementation MUST align with the chosen tech stack: ASP.NET Core Web API backend, Blazor WebAssembly frontend, C# language, and SQLite for persistence. Shared code and separation of concerns are required.
Rationale: Ensures compatibility, cross-platform support, and future scalability.

## Technology Stack & Constraints
The project uses ASP.NET Core Web API and Blazor WebAssembly for rapid, cross-platform development. MVP stores data in memory; future versions may use SQLite and EF Core. All code must be compatible with C# 8.0+, .NET 8.0+, and run on Windows, macOS, and Linux. No background polling in MVP; manual refresh only.

## Development Workflow
All features are developed incrementally, starting with MVP scope. Each feature must have independent user stories and acceptance tests. Code review and automated testing are mandatory before merging. Documentation must be updated with every change.

## Governance
This constitution supersedes all other practices. Amendments require documentation, approval, and a migration plan. All PRs and reviews must verify compliance with principles and sections above. Versioning follows semantic rules: MAJOR for principle/section changes, MINOR for additions, PATCH for clarifications. Compliance is reviewed quarterly.

**Version**: 1.0.0 | **Ratified**: TODO(RATIFICATION_DATE): Set original ratification date if known | **Last Amended**: 2026-01-30
