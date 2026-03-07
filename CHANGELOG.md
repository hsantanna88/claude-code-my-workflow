# Changelog

All notable changes to the Clo-Author are documented here.

---

## [2.0.3] — 2026-03-07

### Working Paper Format Rule

- **`working-paper-format.md`** — new always-on rule: enforces standard economics working paper format (12pt article, 1in margins, double-spaced body, single-spaced abstract, `titling` package for proper title/author font sizes, `\quad` author spacing, `booktabs` tables, `threeparttable` notes, `aer` bibliography style)
- Writer-critic deduction rubric included (e.g., -5 for wrong document class, -3 for `\textbf{}` on title, -5 for missing JEL codes)
- Ensures title page fits on one page: title + authors + abstract + JEL + keywords

---

## [2.0.2] — 2026-03-07

### Figures & Tables Rules

- **`figures.md`** — new always-on rule: no embedded ggplot titles, descriptive filenames, LaTeX `\caption{}` as authoritative title, serif fonts, publication-quality axis labels, show all years on x-axis (≤20 ticks)
- **`tables.md`** — new always-on rule: no embedded titles in generated `.tex` files, `threeparttable` + `booktabs`, notes in paper not R output
- These complement `content-standards.md` (path-scoped, comprehensive) with concise always-on reminders

---

## [2.0.1] — 2026-03-05

### Cross-Language Replication

- **`/analyze --dual r,python`** — run the same analysis in two languages in parallel, compare results within tolerance
- **`/review --replicate python`** — re-implement existing code in a different language, compare outputs
- Both use `domain-profile.md` Quality Tolerance Thresholds for pass/fail
- Coder agent updated with cross-language replication mode and common divergence sources
- Inspired by Scott Cunningham's approach to cross-language validation

---

## [2.0.0] — 2026-03-05

**The Great Restructure.** 16-agent worker-critic system, journal-calibrated referees, consolidated rules, 6-page guide with command reference dictionary.

### Architecture

- **16 specialized agents** in 7 worker-critic pairs + 2 blind referees + orchestrator + verifier
- **New agents:** data-engineer, coder-critic, writer-critic, strategist-critic, librarian-critic, explorer-critic, storyteller-critic, domain-referee, methods-referee
- **Retired agents:** Debugger, Proofreader, Econometrician, Editor, Surveyor, Discussant, Referee (replaced by specialized critic/referee counterparts)
- Worker-critic separation of powers: critics never edit files, creators never self-score

### Journal-Calibrated Peer Review

- `/review --peer JHR` makes referees emulate that journal's review culture
- 15 pre-populated journal profiles (Top-5 + top field + strong field)
- 3-tier fallback: pre-populated → unknown journal + domain profile → user-added custom
- Custom template at bottom of `journal-profiles.md` for adding your own journals

### Skills Consolidation

- **10 slash commands** (down from 20+), each with flags/modes instead of separate skills
- `/discover` replaces `/lit-review`, `/find-data`, `/research-ideation`, `/interview-me`
- `/review` replaces `/review-paper`, `/review-r`, `/econometrics-check`, `/proofread`, `/visual-audit`
- `/write` replaces `/draft-paper`, `/humanizer`
- `/talk` replaces `/create-talk`, `/compile-latex` (for talks)
- `/submit` replaces `/target-journal`, `/data-deposit`, `/audit-replication`, `/deploy`
- `/tools` replaces `/commit`, `/compile-latex`, `/validate-bib`, `/journal`, `/context-status`, `/learn`
- `/revise` replaces `/respond-to-referee`
- `/strategize` replaces `/identify`, `/pre-analysis-plan`
- `/analyze` replaces `/data-analysis`

### Rules Consolidation

- 18 single-topic rule files → 5 consolidated files:
  - `agents.md` — pairing, separation of powers, escalation
  - `workflow.md` — planning, orchestration, dependencies, standalone access
  - `quality.md` — scoring, thresholds, severity gradient
  - `logging.md` — sessions, reports, research journal
  - `content-standards.md` — writing, coding, formatting
- Old rule files archived to `.claude/rules/archive/`
- New: `journal-profiles.md` — 15 economics journal review profiles

### Guide Website

- **6 pages** (up from 3): Quick Start, User Guide, Agents, Architecture, Customization, Reference
- New **Command Reference** page: every command, flag, and subcommand in one scannable page
- New **Meet the Agents** page: all 16 agents with roles, what they create/check
- New **Customization Guide**: domain profile, journal profiles, rules, skills, agents, hooks
- Pipeline diagram with backward arrows (Peer Review → Discovery/Strategy/Execution)
- Cyberpunk neon theme throughout all Mermaid diagrams

### Other

- Pipeline diagram shows 3 feedback loops from Peer Review (missing lit, flawed ID, more checks)
- Archived old skills, agents, hooks, and rules (preserved in `archive/` directories)
- Updated README.md with 16-agent table and 10-command reference

---

## [1.0.1] — 2026-02-25–26

### Adversarial Architecture

- Worker-critic pairing: every creator has a paired reviewer
- Separation of powers: critics can't edit, creators can't self-score
- Three-strikes escalation protocol
- Dependency-driven orchestration (phases activate by dependency, not sequence)
- Cyberpunk neon theme for guide website
- 3-page Quarto website: Quick Start, User Guide, Architecture
- Reoriented from lecture production to applied econometrics research

---

## [1.0.0] — 2026-02-08–15

### Research Workflow

- Research skills: `/lit-review`, `/find-data`, `/identify`, `/draft-paper`, `/review-paper`
- Smart hooks: pre-compact context survival, post-session logging
- Skill creation template and two-tier memory system (MEMORY.md + personal)
- Meta-governance: dual nature of repo (working project + public template)
- Requirements specification phase with MUST/SHOULD/MAY framework
- Constitutional governance template

### Infrastructure

- Orchestrator/contractor protocol with dependency graph
- Plan-first workflow with context preservation
- Quality gates: 80 (commit), 90 (PR), 95 (submission)
- Figure and table generator rules (AER/QJE/Econometrica standards)
- Claude Pilot features integration

---

## [0.1.0] — 2026-02-06–07

### Initial Release

- Forked from [Pedro Sant'Anna's claude-code-my-workflow](https://github.com/pedrohcgs/claude-code-my-workflow)
- Plan-first workflow, context preservation, session logging
- Contractor/orchestrator protocol
- Hooks, MEMORY.md, responsive guide
- Parallel agents pattern, `/commit` skill
- Fork-first onboarding flow

---

[2.0.2]: https://github.com/hsantanna88/clo-author/compare/v2.0.1...v2.0.2
[2.0.1]: https://github.com/hsantanna88/clo-author/compare/v2.0.0...v2.0.1
[2.0.0]: https://github.com/hsantanna88/clo-author/compare/v1.0.1...v2.0.0
[1.0.1]: https://github.com/hsantanna88/clo-author/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/hsantanna88/clo-author/compare/v0.1.0...v1.0.0
[0.1.0]: https://github.com/hsantanna88/clo-author/commits/v0.1.0
