# Proyecto DAMN

Integrative project (Proyecto Intermodular) for the 2nd year of the Vocational Higher Education Degree in Web Application Development (DAW) at ILERNA Sevilla, academic year 2026/2027. The project simulates a tech startup building a complete web product.

Status: Planning phase

## The Startup: Intramuros

> *Your AI, inside your walls.* (Intramuros is a working name.)

Intramuros sells computers that run AI models **on the customer's own premises**, so company data never leaves the office. It works like a PC component store: the customer picks a machine online according to what they need, we build it, and it arrives with open models installed and customised to their documents. Installation and maintenance services come on top.

**Target customers:** freelancers and SMEs (3–100 users) that need privacy but cannot hire AI engineers.

### Task 1: Initial sector exploration

| Deliverable | Link |
| --- | --- |
| Investor pitch, part 1 (in Spanish) | [Pitch: sector analysis](https://claude.ai/artifact/Eip6kYmGYdo8XjsGW3HgMj) |
| Full sector analysis | [docs/business/sector-analysis.md](docs/business/sector-analysis.md) |

Key findings:

- **Companies analysed:**
  - VORLUX AI, a startup.
  - AIHARD, a small integrator.
  - Coolmod, a medium retailer: 65 staff, €38–40 M.
  - PcComponentes, a large retailer: €825 M in 2025.
  - Dell Technologies, a multinational: $113 B in FY2026.
- **The gap:** retailers sell hardware with little service, and integrators are local or aimed at large companies. Nobody sells the complete solution online to SMEs in Spain.
- **Demand:** 21.1% of Spanish companies with 10+ employees used AI in Q1 2025 (INE). PcComponentes announced local AI systems for businesses in October 2026.
- **Business volume:** equipment ranges from about €550 (1–3 users) to €80,000+ (multi-GPU servers). Services add recurring revenue.

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
- One-week sprints with fixed team roles.
- Kanban task board hosted on GitHub Projects: [Project board](#).

## Planned Tech Stack

The tech stack is subject to confirmation during the planning phase:
- Frontend: React
- Backend: Laravel (REST API)
- Styling: Tailwind CSS
- Database: To be determined

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
  - `/docs/business`: Sector analysis and business documentation.
  - `/docs/team`: Team agreements and contract.

## Roadmap

The current roadmap for the planning phase includes:
1. Define product idea. *(Done: local AI hardware for businesses.)*
2. Define startup name and identity. *(In progress: "Intramuros" is a working name.)*
3. Define project scope and MVP.
4. Define software architecture.
