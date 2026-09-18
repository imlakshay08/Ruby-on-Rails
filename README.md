# Ruby on Rails — Learning in Public

![progress](https://img.shields.io/badge/progress-0%25-lightgrey)
![status](https://img.shields.io/badge/status-active-brightgreen)
![last update](https://img.shields.io/badge/last%20update-2026--09--18-blue)

Public log of me working through —
Ruby fundamentals → Rails internals → SQL → testing → architecture →
infra → system design → AI-native engineering, run in parallel with a
career track. Everything here is real notes from real work, not a
polished highlight reel — including the stuff I got wrong.

> **How to use this template:** replace the checklist items below with
> your own roadmap, update the progress badge by hand (or wire up the
> GitHub Action in `.github/workflows/progress-badge.yml`, see bottom),
> and open one Issue per topic as you go — link it next to the checkbox.

---

## How this repo works

- **This README** — the index. One glance tells you where I am.
- **[Project board](../../projects)** — kanban view of every topic (Not Started / In Progress / Done).
- **[Issues](../../issues)** — one per topic. Notes, code snippets, what I got wrong, what an AI agent got wrong that I caught.
- **`logs/`** — short dated weekly entries. Raw material for future interview stories.
- **Linked repos** — real builds get their own repo with a proper README (problem → decisions → tradeoffs → outcome). Linked from the relevant phase below.

---

## Progress

| Phase | Status | Topics done |
|---|---|---|
| [0 · Ruby fundamentals](#phase-0--ruby-the-language) | 🟡 Not started | 0/15 |
| [1 · Rails internals & ActiveRecord](#phase-1--rails-internals--activerecord) | 🟡 Not started | 0/19 |
| [2 · SQL & databases](#phase-2--sql--databases) | 🟡 Not started | 0/19 |
| [3 · Testing](#phase-3--testing) | 🟡 Not started | 0/21 |
| [4 · Design & architecture](#phase-4--design--architecture) | 🟡 Not started | 0/18 |
| [5 · Infra & DevOps](#phase-5--infra--devops) | 🟡 Not started | 0/25 |
| [6 · System design & scale](#phase-6--system-design--scale) | 🟡 Not started | 0/20 |
| [7 · Modern Rails ecosystem](#phase-7--modern-rails-ecosystem) | 🟡 Not started | 0/15 |
| [8 · AI-native engineering](#phase-8--ai-native-engineering) | 🟡 Not started | 0/17 (ongoing, runs in parallel) |
| [9 · Platform breadth](#phase-9--platform-breadth) | 🟡 Not started | 0/28 |
| [10 · ML fundamentals, leadership & business](#phase-10--ml-fundamentals-leadership--business) | 🟡 Not started | 0/14 |
| [Career track](#career-track) | 🟡 Not started | ongoing, runs in parallel |

Legend: 🟡 Not started · 🔵 In progress · 🟢 Done

---

## Phase 0 · Ruby, the language

<!-- Issue: link here once opened, e.g. → #1 -->

- [ ] Object model — classes, modules, instances ` (#1)`
- [ ] Blocks, procs, lambdas
- [ ] Symbols vs strings
- [ ] Enumerable: map, select, reduce, each_with_object
- [ ] Mixins: include vs extend vs prepend
- [ ] method_missing / respond_to_missing?
- [ ] Error handling: rescue, raise, ensure, custom exceptions
- [ ] Frozen objects, immutability
- [ ] Singleton classes / eigenclass
- [ ] Garbage collection basics
- [ ] Memory & object allocation
- [ ] Fibers & concurrency basics
- [ ] Big-O and complexity analysis
- [ ] Core data structures (arrays, hashes, stacks, queues, trees, graphs)
- [ ] 30+ Exercism Ruby exercises

## Phase 1 · Rails internals & ActiveRecord

- [ ] Associations: all types, polymorphic, self-referential
- [ ] Query interface: where, joins, includes, preload, eager_load
- [ ] N+1 detection and fixes (Bullet)
- [ ] Scopes: named, default, chaining
- [ ] Callback lifecycle, ordering
- [ ] Validations: built-in and custom
- [ ] Transactions, save points
- [ ] Optimistic vs pessimistic locking
- [ ] STI — when to avoid it
- [ ] Counter caches, touch: true
- [ ] find_each vs each
- [ ] Arel
- [ ] Request lifecycle end to end
- [ ] Rack & middleware
- [ ] Routing: concerns, constraints, nesting
- [ ] Strong params, rescue_from
- [ ] Concerns — good and bad usage
- [ ] Engines
- [ ] Zeitwerk autoloading

## Phase 2 · SQL & databases

- [ ] SELECT/WHERE/ORDER BY/LIMIT without AR
- [ ] All JOIN types
- [ ] Aggregations: GROUP BY, HAVING
- [ ] Subqueries vs CTEs
- [ ] Window functions
- [ ] EXPLAIN / EXPLAIN ANALYZE
- [ ] Indexes: B-tree, composite, partial, expression
- [ ] Why the planner ignores an index
- [ ] ACID, isolation levels
- [ ] Deadlocks
- [ ] JSONB
- [ ] Array columns / hstore
- [ ] Full-text search (tsvector/tsquery)
- [ ] pg_stat_statements
- [ ] Connection pooling (PgBouncer)
- [ ] Normalization / intentional denormalization
- [ ] Soft deletes
- [ ] UUID vs integer PKs
- [ ] Zero-downtime migrations (strong_migrations)

## Phase 3 · Testing

- [ ] describe/context/it structure
- [ ] let, let!, subject
- [ ] before/after hooks
- [ ] Core matchers
- [ ] Shared examples/contexts
- [ ] Custom matchers
- [ ] Model specs
- [ ] Request specs
- [ ] Capybara integration tests
- [ ] Service object specs
- [ ] Job specs
- [ ] Mailer specs
- [ ] Doubles: instance_double, class_double
- [ ] allow/expect
- [ ] WebMock/VCR
- [ ] Recognizing over-mocking
- [ ] FactoryBot: create/build/build_stubbed, traits
- [ ] Red-green-refactor, practiced for real
- [ ] Outside-in TDD
- [ ] Test pyramid
- [ ] SimpleCov — reading it correctly

## Phase 4 · Design & architecture

- [ ] Service objects
- [ ] Form objects
- [ ] Query objects
- [ ] Decorators/presenters
- [ ] Policy objects
- [ ] Value objects
- [ ] Observer pattern
- [ ] Repository pattern
- [ ] SOLID with Rails examples
- [ ] Composition over inheritance
- [ ] Law of Demeter
- [ ] DRY vs WET judgment calls
- [ ] Refactoring: code smells, extract method/class
- [ ] Hexagonal/clean architecture in Rails
- [ ] DDD basics: entities, value objects, aggregates
- [ ] Event sourcing basics
- [ ] Multi-tenancy: row-based vs schema-based (apartment gem) vs separate databases
- [ ] Feature flags: Flipper or similar — shipping behind flags instead of long-lived branches

## Phase 5 · Infra & DevOps

- [ ] Linux permissions, processes, signals
- [ ] Networking basics (TCP/IP, DNS, HTTP/S)
- [ ] SSH keys & tunneling
- [ ] Bash scripting, cron
- [ ] Log management
- [ ] Containers vs VMs
- [ ] Production Dockerfile for Rails
- [ ] docker-compose for local dev
- [ ] Multi-stage builds
- [ ] Container registries
- [ ] GitHub Actions workflows
- [ ] Pipeline stages: lint → test → build → deploy
- [ ] Staging → production promotion
- [ ] Secrets management in CI
- [ ] Rails credentials: credentials.yml.enc, master.key, per-environment credentials
- [ ] EC2 basics
- [ ] S3 + Active Storage
- [ ] RDS
- [ ] IAM least-privilege
- [ ] Load balancers, SSL termination
- [ ] ElastiCache
- [ ] Puma config
- [ ] Nginx reverse proxy
- [ ] Let's Encrypt / TLS
- [ ] Error tracking, APM, structured logging

## Phase 6 · System design & scale

- [ ] Fragment/Russian-doll/low-level caching
- [ ] HTTP caching headers
- [ ] CDNs
- [ ] Sidekiq internals
- [ ] Memory profiling
- [ ] DB perf tuning, autovacuum
- [ ] Horizontal vs vertical scaling
- [ ] Read replicas
- [ ] Eventual consistency
- [ ] Message queues (Redis/Kafka concepts)
- [ ] REST API design, versioning, pagination
- [ ] ActionCable/WebSockets
- [ ] Rack::Attack rate limiting
- [ ] Idempotency
- [ ] Webhooks: designing outbound webhooks and verifying signatures on inbound ones
- [ ] OWASP Top 10 in Rails
- [ ] Mass assignment / strong params
- [ ] bcrypt / has_secure_password
- [ ] JWT / OAuth 2.0
- [ ] Brakeman

## Phase 7 · Modern Rails ecosystem

- [ ] Hotwire: Turbo Drive/Frames/Streams
- [ ] Stimulus
- [ ] ViewComponent
- [ ] Rails API mode
- [ ] Active Storage variants
- [ ] Action Mailbox
- [ ] Solid Queue / Solid Cache
- [ ] Kredis
- [ ] I18n: locale files, pluralization rules, translating a real view
- [ ] Pundit internals
- [ ] Devise internals
- [ ] Sidekiq retry/failure handling
- [ ] Pagy
- [ ] Searchkick + Elasticsearch
- [ ] RuboCop, custom cops

## Phase 8 · AI-native engineering
*(runs in parallel from week 1 — not a phase you "get to" later)*

- [ ] Using a coding agent well: scoping, context, reviewing diffs critically
- [ ] LLM API basics: streaming, system prompts, params
- [ ] Structured outputs
- [ ] Tool/function calling
- [ ] Embeddings & vector search
- [ ] RAG
- [ ] Building an evaluation set
- [ ] Latency/cost tradeoffs
- [ ] Prompt-injection defenses
- [ ] AI observability
- [ ] Agent architecture
- [ ] One real AI feature shipped end to end
- [ ] Daily agent use on real work
- [ ] Engineering journal: output → defect → lesson
- [ ] Alternative-implementation comparisons
- [ ] Periodic no-AI practice to keep fluency sharp

> **Ground rule for everything documented in this repo:** learn the
> concept myself first, attempt the problem myself, *then* use an agent
> for critique or implementation — and verify what it gives me with
> tests, source, benchmarks, or production evidence before it goes in
> a commit or a log entry.
>
> **Phases 9–10** widen the foundation from Phases 0–6 into platform
> breadth and the influence/ML/business judgment the staff-principal
> track expects. They land best once 0–6 are solid — sequence
> accordingly rather than skipping ahead.

## Phase 9 · Platform breadth
*Frontend, distributed systems, Kubernetes, polyglot, security, formal CS*

**Frontend depth**
- [ ] A real JS framework (React/Vue) beyond Hotwire/Stimulus
- [ ] Client-side state management fundamentals
- [ ] CSS fundamentals & a design system beyond utility classes
- [ ] Accessibility basics (semantic HTML, keyboard nav, ARIA)

**Distributed systems at real scale**
- [ ] CAP theorem in practice
- [ ] Sharding & partitioning strategies
- [ ] Multi-region architecture — replication lag, failover
- [ ] Service decomposition — when to actually split a monolith
- [ ] Consensus basics (Raft/Paxos) — enough to reason about it

**Kubernetes & orchestration**
- [ ] Pods, deployments, services
- [ ] ConfigMaps/Secrets, readiness/liveness probes
- [ ] Autoscaling (HPA), rolling deploys
- [ ] Run a Rails app on K8s end to end, once

**Polyglot breadth**
- [ ] One language outside Ruby to production-comfort level (Go/Python common picks)
- [ ] That language's concurrency model, compared honestly to Ruby's
- [ ] Reading a codebase in it without mentally translating back to Ruby

**Security engineering depth**
- [ ] Threat modeling a real system (not just running Brakeman)
- [ ] Auth deep dive: sessions vs tokens, refresh flows, SSO/SAML basics
- [ ] Secrets management/rotation at the infra level
- [ ] Compliance basics: what SOC2/GDPR require day to day
- [ ] Incident response — the first hour of a real breach

**Formal CS depth**
- [ ] Algorithms beyond interview-prep level
- [ ] OS scheduling & memory management, past "it just works"
- [ ] How a compiler/interpreter works, in broad strokes
- [ ] Networking beyond HTTP: TCP internals, LB algorithms

**Books & resources**
- *Kubernetes Up & Running* — Hightower, Burns, Beda
- *The Go Programming Language* — Donovan & Kernighan
- *The Web Application Hacker's Handbook*
- *Operating Systems: Three Easy Pieces* (free online)
- [react.dev/learn](https://react.dev/learn) · [Kubernetes tutorials](https://kubernetes.io/docs/tutorials/) · [A Tour of Go](https://go.dev/tour/) · [OWASP Top 10](https://owasp.org/www-project-top-ten/) · [System Design Primer](https://github.com/donnemartin/system-design-primer)

## Phase 10 · ML fundamentals, leadership & business
*From strong IC to someone trusted with more than code*

**ML/AI beyond API usage**
- [ ] Core ML concepts: supervised/unsupervised, overfitting, train/test splits
- [ ] How a transformer works, conceptually
- [ ] Fine-tuning vs prompting vs RAG — when each is right
- [ ] Train or fine-tune a small model yourself, once
- [ ] Where "AI application engineering" (Phase 8) stops and ML engineering starts

**Leadership & influence**
- [ ] Write an RFC that survives scrutiny from people who disagree
- [ ] Mentor — actually pair with and unblock someone less experienced
- [ ] Drive a cross-team decision without formal authority
- [ ] Give and receive critical code review well
- [ ] Run a postmortem that improves the system, not assigns blame

**Product & business judgment**
- [ ] Basic cost modeling for a feature or scaling decision
- [ ] Prioritization frameworks (RICE, cost of delay)
- [ ] Read a P&L / unit economics well enough to follow the "why"
- [ ] Translate engineering tradeoffs for non-engineers
- [ ] Know when "good enough" is the correct engineering answer

**Books & resources**
- *Hands-On Machine Learning* — Aurélien Géron
- *Designing Machine Learning Systems* — Chip Huyen
- *The Staff Engineer's Path* — Tanya Reilly
- *The Manager's Path* — Camille Fournier
- *Staff Engineer* — Will Larson
- [fast.ai](https://course.fast.ai) · [Hugging Face courses](https://huggingface.co/learn) · [StaffEng.com](https://staffeng.com) · [Reforge blog](https://www.reforge.com/blog)

## Career track
*(parallel, not sequential)*

- [ ] STAR stories from real projects
- [ ] Case study per shipped project
- [ ] Bullet + RuboCop + Brakeman on a real project, documented
- [ ] Dockerized project + CI pipeline, public
- [ ] One open-source contribution
- [ ] Git workflow as a skill: clean rebases, trunk-based dev, PRs that are easy to review
- [ ] Mock interviews
- [ ] Applying continuously as skills improve

---

## Logs

Weekly notes live in [`logs/`](logs/) — `YYYY-Www.md`, 3–5 bullets:
what I learned, what I built, one thing I caught an AI agent getting
wrong. Raw material for interview stories later.

## Real projects

| Project | What it is | Repo |
|---|---|---|
| _(add as you build)_ | | |

---

<details>
<summary>Optional: auto-updating progress badge</summary>

Drop this at `.github/workflows/progress-badge.yml` to recompute the
percentage of checked boxes in this README on every push and update
the badge automatically (uses `githubocto/flat-data`-style approach —
simplest version below just counts `- [x]` vs `- [ ]` and rewrites the
shields.io URL at the top of this file via a small script). Swap in
whatever badge tooling you prefer — this is a starting point, not a
requirement.

```yaml
name: progress-badge
on:
  push:
    paths: ["README.md"]
jobs:
  update-badge:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Compute and update progress
        run: |
          total=$(grep -o '\- \[.\]' README.md | wc -l)
          done=$(grep -o '\- \[x\]' README.md | wc -l)
          pct=$(( done * 100 / total ))
          sed -i "s/progress-[0-9]*%25-[a-z]*/progress-${pct}%25-brightgreen/" README.md
          git config user.name "progress-bot"
          git config user.email "actions@github.com"
          git add README.md
          git commit -m "chore: update progress badge to ${pct}%" || echo "no changes"
          git push
```

</details>
