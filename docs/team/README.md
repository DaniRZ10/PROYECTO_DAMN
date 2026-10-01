# Team

This folder contains the internal team agreements and governance framework for Proyecto DAMN.

## Contents

- [Contrato_Equipo_Proyecto_DAMN.pdf](Contrato_Equipo_Proyecto_DAMN.pdf): Signed team contract (in Spanish, version 1.0, dated 01/10/2026).

The signed PDF file is the binding version of the team contract. This README serves as an English summary of its provisions.

## Roles and Responsibilities

### Product Owner (Sergio Montes)
- Defines and prioritises the Product Backlog.
- Approves the project idea and scope.
- Validates each sprint increment at the Sprint Review.
- Resolves scope questions and decisions without team consensus.

### Scrum Master (Daniel Ríos Zea)
- Facilitates ceremonies.
- Keeps the board and backlog up to date.
- Removes blockers and escalates them to the PO.
- Main contact with the PO.
- Reviews and merges Pull Requests into `develop`.
- Administers the repository (permissions, branch protection, releases, CHANGELOG).
- Writes or supervises meeting minutes.
- Ensures the contract is followed.
- Contributes to development when sprint planning allows.

### Developers (Álvaro Morón López, Manuel Jesús Jiménez Romero, José Ramón Neira Vega)
- Estimate and commit to sprint tasks.
- Develop frontend, backend, database, external API integration, design/accessibility, and deployment tasks.
- Keep their tasks updated on the board.
- Work on feature branches and open PRs with a description and linked issue.
- Test their code before opening a PR.
- Document their work in English.
- Take part in reviews and retrospectives.
- Contribute to the business plan when assigned.

Technical areas are assigned at each Sprint Planning; every member works on frontend, backend, and documentation over the project.

## Ceremonies

| Ceremony | When | Output |
| --- | --- | --- |
| Sprint Planning | Start of sprint | Sprint goal and committed tasks |
| Daily | Every working day (asynchronous, WhatsApp) | Done / next / blockers |
| Sprint Review | End of sprint with the PO | Validated increment and feedback |
| Retrospective | After the Review (Sailboat format) | At least one improvement action |

## Kanban Board

- Columns: Backlog, To Do (sprint), In Progress, Review, Done.
- WIP limit: 2 tasks In Progress per person.
- Task structure: Every task has an issue and a single assignee.

## Communication

- Project-only WhatsApp group for daily coordination.
- GitHub (issues, board, PRs) as the single source of truth.
- Maximum response time: 24 hours on working days.
- Blockers reported immediately.
- Planned absences notified before Sprint Planning.

## Definition of Done

- Meets the issue's acceptance criteria.
- Tested with no known errors.
- PR approved and merged into `develop`.
- Related documentation updated.
- Task moved to Done.

## Decision-Making

- Consensus whenever possible.
- Otherwise the PO decides.

## Conflict Resolution

Escalation process:
1. Direct conversation.
2. Scrum Master mediation.
3. Discussion at the Retrospective or an extraordinary meeting.
4. Escalation to the PO.

Graduated consequences for non-compliance:
1. Private warning.
2. Discussion at the Retrospective with possible task reassignment and impact on peer evaluation.
3. Formal report to the PO.

## Data Protection

- Personal data shared within the team is used only for project coordination, in accordance with the GDPR (EU Regulation 2016/679) and the Spanish LOPDGDD (Organic Law 3/2018).
- Credentials are never shared outside the team or committed to the repository.
