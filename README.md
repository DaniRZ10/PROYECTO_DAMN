# Proyecto DAMN

Integrative project (Proyecto Intermodular) for the 2nd year of the Vocational Higher Education Degree in Web Application Development (DAW) at ILERNA Sevilla, academic year 2026/2027. The project simulates a tech startup building a complete web product.

Status: Planning phase (Sprint 2 of 3)

## The Startup: AIComp

> *La IA de tu empresa, montada a medida y sin salir de tu oficina.*

AIComp is a fictional startup that sells computers to run AI models **on the customer's own premises**, so company data never leaves the office. It works like an online PC component store: the customer chooses a machine by use case and sector, we build it, and it arrives with open models already installed and adapted to the customer's documents, plus installation, customisation and maintenance services. It serves companies of every size, with SMEs as the main focus.

What we build in this project is **the AIComp web platform**: the online store, a configurator by use case and a customer area.

### Deliverables

| Deliverable | Document (in Spanish) |
| --- | --- |
| Task 1 – Initial sector exploration (investor pitch, part 1) | [pitch.md](pitch.md) |
| Sprint 1 – Presentation (revised after the Sprint Review) | [docs/sprint-1/presentation.md](docs/sprint-1/presentation.md) |
| Sprint 1 – Detected need | [docs/sprint-1/01-need.md](docs/sprint-1/01-need.md) |
| Sprint 1 – Proposed solution | [docs/sprint-1/02-solution.md](docs/sprint-1/02-solution.md) |
| Sprint 1 – Innovative aspects | [docs/sprint-1/03-innovation.md](docs/sprint-1/03-innovation.md) |
| Sprint 1 – Feasibility | [docs/sprint-1/04-feasibility.md](docs/sprint-1/04-feasibility.md) |
| Sprint 1 – Sprint Review minutes | [docs/sprint-1/review-minutes.md](docs/sprint-1/review-minutes.md) |
| Sprint 2 – Presentation | [docs/sprint-2/presentation.md](docs/sprint-2/presentation.md) |
| Sprint 2 – Platform modules and integration | [docs/sprint-2/01-modules.md](docs/sprint-2/01-modules.md) |
| Sprint 2 – Human resources | [docs/sprint-2/02-human-resources.md](docs/sprint-2/02-human-resources.md) |
| Sprint 2 – Material resources | [docs/sprint-2/03-material-resources.md](docs/sprint-2/03-material-resources.md) |
| Sprint 2 – Budget | [docs/sprint-2/04-budget.md](docs/sprint-2/04-budget.md) |

## Team

| Name | Role |
| --- | --- |
| Sergio Montes | Product Owner (instructor) |
| Daniel Ríos Zea | Scrum Master |
| Álvaro Morón López | Developer |
| Manuel Jesús Jiménez Romero | Developer |
| José Ramón Neira Vega | Developer |

## Team Documentation

For team agreements, roles, ceremonies, and working rules, see the [Team README](docs/team/README.md).
The binding team contract is available directly at [Contrato_Equipo_Proyecto_DAMN.pdf](docs/team/Contrato_Equipo_Proyecto_DAMN.pdf) (in Spanish).

## Methodology

The project follows a hybrid Scrum and Kanban methodology:
- One-week sprints with fixed team roles, confirmed by the Product Owner.
- Kanban task board hosted on GitHub Projects: [AIComp – Board](https://github.com/users/DaniRZ10/projects/1). Columns: Backlog, To Do (sprint), In Progress, Blocked, Review, Done.
- Tasks are written as user stories, one issue per task with a single assignee.

## Tech Stack

Decided in Sprint 2 (see [material resources](docs/sprint-2/03-material-resources.md)):
- Frontend: React
- Backend: Laravel (REST API)
- Styling: Tailwind CSS
- Database: PostgreSQL on Supabase
- Frontend hosting: Cloudflare Pages
- API hosting: Laravel Cloud
- Local environment: XAMPP with `pdo_pgsql` and a local PostgreSQL

## Git Workflow

The project uses the Gitflow workflow model:
- Main branches: `main` and `develop`.
- Supporting branches: `feature/*`, `release/*`, `hotfix/*`.
- Direct commits to `main` or `develop` are strictly prohibited.
- All changes must be merged via Pull Requests.
- Commit messages must be written in English following the Conventional Commits specification.
- Every change is pre-reviewed by the Scrum Master as a diff before pushing, and only the Scrum Master approves and merges PRs. See [CONTRIBUTING.md](CONTRIBUTING.md) for the full flow.

## Planned Repository Structure

- `/frontend`: Web application user interface.
- `/backend`: REST API and business logic.
- `/docs`: Project documentation and team agreements.

## Roadmap

The current roadmap for the planning phase includes:
1. Define product idea. *(Done: local AI hardware for businesses, sold through a web platform.)*
2. Define startup name and identity. *(Done: AIComp.)*
3. Sprint 1 – Discovery and definition: need, proposed solution, innovation and feasibility. *(Done; revised after the Sprint Review on 3 November 2026.)*
4. Sprint 2 – Structure and planning: modules, human and material resources, and budget. *(Done; design postponed to Sprint 3 by the Product Owner.)*
5. Sprint 3 – Final iteration: design (diagrams, sketches, prototypes and wireframes), consolidated documentation, quality criteria and final pitch.
