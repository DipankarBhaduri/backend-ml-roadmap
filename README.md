**Window:** 240 days · 8 months · ~2 hours/day, 6 days/week (~480–500 focused hours)
**Positioning:** *Backend/Distributed Systems Engineer who specialises in production AI systems* — not "a GenAI developer who uses LangChain."

---

## Contents

**Part I — The plan**

- [0. Read this before Day 1](#0-read-this-before-day-1)
- [1. How to use this file](#1-how-to-use-this-file)
- [2. Daily structure](#2-daily-structure)
- [3. The 8-month arc](#3-the-8-month-arc)
- [4. Non-negotiable rules](#4-non-negotiable-rules)
- [Month 1 · Days 1–30](#month-1--days-130) — CS fundamentals, Python, Linux, Git
- [Month 2 · Days 31–60](#month-2--days-3160) — Networking, APIs, PostgreSQL, Redis
- [Month 3 · Days 61–90](#month-3--days-6190) — LLMs, embeddings, first RAG · **applications start Day 75**
- [Month 4 · Days 91–120](#month-4--days-91120) — Advanced RAG, Kafka, distributed systems
- [Month 5 · Days 121–150](#month-5--days-121150) — System design, Docker, AWS
- [Month 6 · Days 151–180](#month-6--days-151180) — Maths, ML, PyTorch
- [Month 7 · Days 181–210](#month-7--days-181210) — Transformers, fine-tuning, inference
- [Month 8 · Days 211–240](#month-8--days-211240) — Agents, MCP, security, capstone

**Part II — Projects**

- [Project 1 · Production Backend](#10-project-1--production-backend-service)
- [Project 2 · Enterprise RAG](#11-project-2--enterprise-rag-service)
- [Project 3 · Distributed AI Platform](#12-project-3--distributed-ai-document-platform)
- [Project 4 · Production AI Platform (capstone)](#13-project-4--production-ai-platform-capstone)

**Part III — Interview question bank**

- [Python internals](#141-python-and-language-internals) · [Databases](#142-databases-and-postgresql) · [Caching](#143-caching-and-redis) · [Kafka & reliability](#144-kafka-messaging-and-reliability) · [Distributed systems](#145-distributed-systems) · [System design](#146-system-design-the-method-plus-four-worked-skeletons) · [LLMs & RAG](#147-llms-rag-and-retrieval) · [Transformers & inference](#148-transformers-and-inference-the-50l-differentiators) · [Agents, MCP, security](#149-agents-mcp-and-ai-security) · [Behavioural](#1410-behavioural-prepare-six-stories-in-star-form)

**Part IV — Job search**

- [15. Timeline and cadence](#15-timeline-and-cadence)
- [16. Company tiers](#16-company-tiers)
- [17. Resume](#17-resume)
- [18. LinkedIn](#18-linkedin)
- [19. Outreach templates](#19-outreach-templates)
- [20. Interview process and negotiation](#20-interview-process-and-negotiation)
- [21. Final scorecard — Day 240](#21-final-scorecard--day-240)

---

## 0. Read this before Day 1

### The honest framing

₹50 LPA is a **target**, not a promise. In the Indian market, ₹50L+ AI compensation clusters in:

- Top-tier product companies and GCCs (Google, Microsoft, Databricks, Nvidia, Atlassian, Rubrik, Uber, Salesforce, Adobe, Wells Fargo AI, Goldman, JPMC AI/ML, Oracle OCI, Snowflake, Confluent…)
- Well-funded AI startups paying above-market for scarce skills (inference, agents, retrieval at scale)
- Specialist roles: inference optimisation, AI platform/infra, ML platform, distributed systems

Almost all of them assume **substantial prior engineering depth**, not just AI familiarity. What this plan does is remove the two things that actually block ₹40–50L offers:

1. **Depth gap** — most candidates can call an LLM API but cannot explain MVCC, KV cache, exactly-once semantics, or why their retrieval is bad.
2. **Evidence gap** — most candidates have 15 toy repos and zero production-shaped systems.

### What "success" looks like at Day 240

Even if you don't land ₹50L on Day 240, a realistic distribution of outcomes if you execute this properly:

| Outcome | Likelihood if executed well |
|---|---|
| Multiple ₹18–30L offers | High |
| At least one ₹30–45L offer | Moderate–high |
| ₹45–60L offer | Real but not guaranteed — depends on your current YOE, current CTC, interview luck, and market timing |

**Corollary:** do not reject a ₹25–35L offer because your target was ₹50L. A strong AI/backend role for 12–18 months is the cheapest path to the next jump. The single biggest determinant of your next offer is the *quality of the systems you touch*, not the number on your last payslip.

### Two hard rules

1. **You start applying on Day 75.** Not Day 240. Interviewing *is* a skill and it is trained separately from engineering. By the time you're ready for Tier A companies you should already have 30+ interviews behind you.
2. **DSA runs from Day 1 to Day 240.** Never "I'll do DSA at the end." That is the #1 reason strong engineers fail ₹50L loops.

---

## 1. How to use this file

- Each month has a **per-day table**: the day's topic, the concrete artefact you produce, the DSA target, and a **checkpoint question** you must be able to answer out loud without notes.
- The checkpoint question column is the whole point. If you can't answer it, the day is not done — even if you "read the material."
- Projects are not optional side-quests. They are the primary artefact. Sections 10–13 give full specs and repo layouts.
- Sunday (Day 7 of each week) is a **lighter consolidation day**: revise, redo failed DSA problems, write notes, push code. Do not add new topics.

### Notes discipline (non-negotiable)

Keep one repo: `engineering-notes/`. One markdown file per topic. Each file must contain:

```
# <Topic>
## What problem does this solve?
## Mental model / diagram
## How it actually works (mechanism, not vocabulary)
## Failure modes
## Interview answers (2–3 questions, written out)
## Code / command I ran
```

If a note has no "failure modes" section, you learned the vocabulary, not the topic. Interviewers at ₹50L probe failure modes almost exclusively.

---

## 2. Daily structure

**Months 1–2 (Days 1–60)** — building the base, no applications yet

| Block | Time | Content |
|---|---|---|
| A | 45 min | Core engineering topic (the day's row) |
| B | 45 min | DSA — 2 problems, one fresh, one revisit |
| C | 30 min | Project work / write the note |

**Months 3–8 (Days 61–240)** — applications live

| Block | Time | Content |
|---|---|---|
| A | 45 min | AI / engineering topic |
| B | 30 min | DSA — 1–2 problems |
| C | 30 min | Project work |
| D | 15 min | Applications, outreach, recruiter replies, mock scheduling |

### Weekly rhythm

| Day of week | Load |
|---|---|
| Mon–Fri | Full 2h |
| Sat | Full 2h + 1 extra hour on project if possible |
| Sun | 60–90 min consolidation only: revise notes, redo 3 failed DSA problems, push code, update tracker |

### Monthly rhythm

- **Every 4th Sunday:** 1 timed DSA mock (45 min, 2 problems) + 1 system design mock (45 min) — record yourself, watch it back once.
- **End of each month:** update resume, update LinkedIn, push all project code, write one public post (LinkedIn or blog) about something you built. 8 posts by Day 240 changes your inbound.

---

## 3. The 8-month arc

| Month | Days | Theme | Primary output |
|---|---|---|---|
| 1 | 1–30 | CS fundamentals, Python engineering, Linux, Git | Notes repo + FastAPI skeleton + 30 DSA |
| 2 | 31–60 | Networking, HTTP/API design, PostgreSQL, Redis | **Project 1: Production Backend** shipped |
| 3 | 61–90 | LLM fundamentals, APIs, embeddings, first RAG · **applications start Day 75** | **Project 2 v1: RAG service** |
| 4 | 91–120 | Advanced RAG, Kafka, reliability, distributed systems | **Project 3: Distributed AI platform** |
| 5 | 121–150 | System design, Docker, AWS | Everything deployed + 15 designs written |
| 6 | 151–180 | Maths, classical ML, ML engineering, PyTorch | ML fundamentals + serving demo |
| 7 | 181–210 | Transformers from scratch, fine-tuning, inference optimisation | Transformer implemented + LoRA run + inference benchmark |
| 8 | 211–240 | Agents, MCP, AI security, capstone platform, interview intensive | **Project 4: Production AI Platform** + offers in flight |

### Why this order

- **Backend before AI** because AI roles at ₹40L+ are backend roles with AI in them. The interview loop is: DSA → LLD → system design → AI depth → behavioural. Three of five rounds are pure engineering.
- **RAG before ML theory** because RAG is what gets you interviews *now*, and it is cheap to learn relative to its market value.
- **Transformers/inference in Month 7** because that's what separates ₹30L from ₹50L. "How do you cut p99 latency on a 70B model serving 2000 rps" is a ₹50L question. "What is RAG" is a ₹18L question.
- **Agents/MCP last** because the ecosystem churns fastest — learning it in Month 8 means your knowledge is current when you're in Tier A loops.

---

## 4. Non-negotiable rules

1. **Every topic produces a running artefact.** Code you ran, a command you executed, a diagram you drew. Reading is not studying.
2. **No tutorial completion as a goal.** The goal is being able to answer the checkpoint question and debug the thing when it breaks.
3. **Break things on purpose.** Kill a Kafka consumer mid-batch. Fill the disk. Drop the DB connection. Send a 10MB prompt. The stories you tell in interviews come from here.
4. **One repo per project, 4 repos total.** Not 15. Each with a real README, architecture diagram, and a 3-minute Loom demo.
5. **Write the interview answer as you learn.** Every note ends with 2–3 written-out interview answers. By Day 240 that file *is* your prep material.
6. **Ship > perfect.** A deployed ugly thing beats a beautiful local thing in every interview.
7. **Track everything.** DSA count, applications, interviews, rejections with reason. Section 15 has the schema.

### Failure modes to watch for

| Failure mode | Symptom | Fix |
|---|---|---|
| Tutorial hell | You've "learned" 8 topics, built 0 things | Force the deliverable column |
| DSA deferral | Month 5 and you're at 60 problems | Non-negotiable 30-min block; cut project time instead |
| Framework-only AI | You know LangChain, not retrieval | Build RAG once with zero frameworks, raw SQL + raw API calls |
| Application paralysis | Day 120, 4 applications sent | Weekly quota is a hard commitment, not a target |
| Breadth without depth | You can name 40 things, explain 3 | Checkpoint questions out loud, recorded |
| Notes as transcription | Notes are copied docs | Every note needs "failure modes" written by you |

---

# MONTH 1 · DAYS 1–30
## CS fundamentals → Python engineering → Linux → Git → first API

**Month goal:** you can reason about what the machine is actually doing, write Python like an engineer rather than a scripter, live in a terminal, and stand up an API.

**Month deliverables**

- `engineering-notes/` repo with ~25 topic notes
- 30 DSA problems solved (arrays → trees, easy-to-easy-medium)
- A working FastAPI service with tests, running in Docker locally
- Resume v0 and a cleaned GitHub profile

### Week 1 · Days 1–7 — How a computer actually executes your code

| Day | Topic (45 min) | Build / artefact (30 min) | DSA (45 min) | Must be able to answer |
|---|---|---|---|---|
| 1 | CPU, instruction cycle, fetch-decode-execute, clock speed vs IPC | Notes + `lscpu` output annotated | Big-O: derive complexity of 5 loops by hand | Why doesn't 2× clock speed give 2× program speed? |
| 2 | Cores, hyperthreading, registers, ALU, pipelining, branch prediction | Python script that runs the same work on 1 vs N cores, time it | Arrays: two-sum, max subarray (Kadane) | Why does a CPU-bound Python loop not get faster with threads? |
| 3 | RAM, memory hierarchy, latency numbers every engineer should know | Write out the latency table from memory; benchmark list vs dict lookup 1M times | Arrays: rotate array, move zeroes | Order these by latency: L1, RAM, SSD, network round-trip, disk seek |
| 4 | L1/L2/L3 cache, cache lines, spatial/temporal locality, false sharing | Benchmark row-major vs column-major 2D array traversal — measure the gap | Strings: reverse words, valid palindrome | Why is iterating a matrix row-wise faster than column-wise? |
| 5 | Processes, PCB, fork, address space isolation, zombie/orphan processes | `multiprocessing` demo; watch it in `htop`; find PIDs with `ps` | Hashing: contains duplicate, group anagrams | What exactly does the OS copy when you fork a process? |
| 6 | Threads, shared memory, race conditions, GIL, locks, deadlock basics | Write a counter race condition, prove it's wrong, fix with a Lock | Hashing: two-sum via hashmap, longest consecutive sequence | Give a concrete race condition and the minimum fix |
| 7 | **Consolidation** — context switching, cost of a switch, scheduler basics | Redraw the whole week as one diagram from memory | Redo the 3 hardest problems from the week | When is a thread cheaper than a process, and when is it not? |

### Week 2 · Days 8–14 — OS internals meets Python's execution model

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 8 | Virtual memory, MMU, page tables, TLB, why every process thinks it owns all memory | Read `/proc/<pid>/maps` for a Python process, annotate the segments | Two pointers: sorted two-sum, remove duplicates | Why can two processes both use address `0x400000` safely? |
| 9 | Pages, page faults (minor/major), swapping, thrashing, OOM killer | Trigger a page fault storm with a big array; watch with `vmstat 1` | Two pointers: 3-sum, container with most water | What is the difference between a minor and a major page fault, and which one hurts? |
| 10 | Stack vs heap, stack frames, recursion depth, memory layout of a process | Blow the Python recursion limit; measure stack vs heap allocation speed | Sliding window: max sum subarray size k, longest substring without repeats | Where do a Python list, its elements, and the variable name each live? |
| 11 | CPython execution model: bytecode, interpreter loop, `dis`, reference counting, GC | `dis.dis()` on 3 functions; explain the bytecode line by line | Sliding window: min window substring (attempt), longest repeating char replacement | What actually happens between `python x.py` and your first print? |
| 12 | Objects, references, identity vs equality, `is` vs `==`, small-int caching, interning | Draw memory diagrams for 5 assignment/aliasing snippets; verify with `id()` | Hashing: top-k frequent, subarray sum equals k | Why does `a = [1]; b = a; b.append(2)` change `a`? |
| 13 | Mutability, immutability, shallow vs deep copy, the mutable-default-argument trap | Reproduce the mutable default argument bug; fix it 2 ways | Stack: valid parentheses, min stack | Why is a list an unsafe default argument and a tuple safe? |
| 14 | **Consolidation** — functions as objects, scope, LEGB, closures, `nonlocal` | Write a closure-based counter and a decorator-free memoiser | Queue: implement queue with stacks; redo week's failures | What does a closure capture — the value or the variable? |

### Week 3 · Days 15–21 — Python as an engineering language

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 15 | OOP: classes, `__init__`, `self`, inheritance, MRO, composition over inheritance, dunder methods | Model a small domain (Document, Chunk, Embedding) with dataclasses + methods | Linked list: reverse, middle node | When would you choose composition over inheritance, with an example from your own code? |
| 16 | SOLID in Python, dependency injection, protocols/ABCs, why interfaces matter for testing | Refactor yesterday's classes so the embedding backend is swappable | Linked list: cycle detection (Floyd), merge two sorted | Show one class you wrote that violated SRP and the split you made |
| 17 | Iterators, iterables, generators, `yield`, lazy evaluation, generator pipelines, memory wins | Write a generator pipeline that streams a 1GB file with flat memory; prove it with `memory_profiler` | Binary search: classic, first/last occurrence | Why does a generator use constant memory over a 1GB file? |
| 18 | Decorators, `functools.wraps`, parameterised decorators, real uses: retry, timing, caching, auth | Write `@retry(times, backoff)` and `@timed` and use them for real | Binary search: search in rotated array, find peak | Write a retry decorator with exponential backoff from scratch |
| 19 | Context managers, `with`, `__enter__`/`__exit__`, `contextlib`, guaranteed cleanup, exception safety | Write a context manager for a DB transaction that rolls back on exception | Recursion: subsets, permutations | Why is `with` safer than try/finally that you wrote yourself? |
| 20 | `asyncio`: event loop, coroutines, `await`, `gather`, `TaskGroup`, when async wins | Fetch 50 URLs sequentially vs with `gather` — measure and explain the gap | Recursion: combination sum, generate parentheses | What is the event loop doing while you `await` a network call? |
| 21 | **Consolidation** — threads vs async vs processes: the decision table; GIL implications | Write the decision table yourself; benchmark all three on I/O work and CPU work | Redo week's failures; 1 timed 30-min problem | I/O-bound vs CPU-bound: which concurrency model and why? |

### Week 4 · Days 22–30 — Linux, Git, testing, first API

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 22 | Linux process management: `ps`, `top`/`htop`, signals, `kill -9` vs `-15`, `nohup`, exit codes | Start a long process, send SIGTERM, handle it gracefully in Python | Trees: inorder/preorder/postorder (recursive + iterative) | Difference between SIGTERM and SIGKILL, and why graceful shutdown matters in a container |
| 23 | Linux networking: `curl`, `dig`, `netstat`/`ss`, `lsof`, ports, `tcpdump` basics | Trace a request end-to-end: DNS → TCP → TLS → HTTP using CLI tools only | Trees: level-order BFS, max depth | A service returns "connection refused" — list your first 5 debugging commands |
| 24 | Text processing: `grep`, `sed`, `awk`, pipes, `find`, `xargs`, `jq` | Parse a 100k-line log file: top 10 error types, p95 latency, requests per minute — pipes only | BST: validate BST, search/insert | Extract p95 latency from a log file with one shell pipeline |
| 25 | Bash scripting: variables, conditionals, loops, functions, `set -euo pipefail`, exit codes, cron | Write a real script: back up a Postgres DB, log, rotate old backups, exit non-zero on failure | BST: lowest common ancestor, kth smallest | Why `set -euo pipefail` at the top of every script? |
| 26 | Git internals: objects, blobs/trees/commits, SHA, refs, HEAD, the index, what a commit really is | Use `git cat-file` to walk your own repo's object graph | Heap: kth largest, top-k frequent via heap | What are the four Git object types and how do they compose a commit? |
| 27 | Branching, merge vs rebase, cherry-pick, interactive rebase, reflog, resolving conflicts, PR hygiene | Deliberately create a conflict and resolve it; squash 5 commits into 1; recover a "lost" commit with reflog | Heap: merge k sorted lists, median from data stream | You committed a secret 3 commits ago. What do you do? |
| 28 | Testing: `pytest`, fixtures, parametrise, mocking, test pyramid, coverage, what not to test | 15 tests for your Week-3 code including one fixture and one mock | Mixed: 2 mediums, timed | What do you mock and what do you never mock? |
| 29 | FastAPI: routing, Pydantic models, validation, dependency injection, `/docs`, error handling, async endpoints | A 5-endpoint FastAPI service with Pydantic validation, DI, and tests | Mixed: 2 mediums, timed | How does FastAPI validate and where do you put business logic vs route logic? |
| 30 | **Month 1 review + Dockerise** | Dockerfile for the service; runs with one command; push to GitHub; resume v0; GitHub profile cleanup | **Mock test:** 2 problems, 45 min, no hints | Explain your Month-1 service architecture in 90 seconds |

### Month 1 checkpoint — you must be able to do all of these

- [ ] Explain what happens from `python app.py` to a response leaving the process
- [ ] Explain why threads don't speed up CPU-bound Python and what does
- [ ] Write a decorator, a context manager, and a generator pipeline from a blank file
- [ ] Debug a hung process with only Linux CLI tools
- [ ] Explain a Git commit in terms of objects
- [ ] Stand up a validated, tested, Dockerised FastAPI service in under an hour
- [ ] 30 DSA problems logged, with your own notes on each pattern

---

# MONTH 2 · DAYS 31–60
## Networking → API design → PostgreSQL → Redis → **Project 1 shipped**

**Month goal:** become the person who can build and defend a production backend. This is the month that makes the AI months credible. Skip it and you become "an AI person who can't build services" — which caps you around ₹20L.

**Month deliverables**

- **Project 1: Production AI Backend** — deployed, tested, documented
- 60 cumulative DSA problems
- 40+ meaningful SQL queries written
- Notes on transactions, isolation, indexing, caching with failure modes

### Week 5 · Days 31–37 — Networking

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 31 | TCP/IP model, layers, encapsulation, MTU, ports, sockets; TCP vs UDP | Draw a packet's journey with headers at each layer; raw socket client in Python | Binary search on answer: min capacity to ship packages | When would you choose UDP over TCP in a real system? |
| 32 | DNS: recursive resolution, records (A/AAAA/CNAME/MX/TXT), TTL, caching layers, DNS-based failover | `dig +trace` a domain; explain every hop; check TTLs | Trees: diameter, path sum | Why does a DNS change take time to propagate, and what controls that? |
| 33 | TCP three-way handshake, sequence numbers, ACKs, retransmission, flow control, congestion control, TIME_WAIT | Capture a handshake with `tcpdump`; identify SYN/SYN-ACK/ACK; explain TIME_WAIT flooding | Trees: serialize/deserialize, right side view | Why does a connection cost latency before any data moves, and how does keep-alive fix it? |
| 34 | TLS: symmetric vs asymmetric, handshake, certificates, chain of trust, SNI, mTLS, TLS 1.3 improvements | Inspect a cert with `openssl s_client`; explain the chain; generate a self-signed cert | Heap: task scheduler, reorganize string | Walk through a TLS handshake and say where the asymmetric crypto stops being used |
| 35 | HTTP/1.1: request/response anatomy, persistent connections, head-of-line blocking, pipelining failure | `curl -v` a real API; annotate every header; measure connection reuse | Heap: k closest points, sliding window max | What is HTTP head-of-line blocking and why did pipelining not solve it? |
| 36 | HTTP/2: binary framing, multiplexing, HPACK, server push, why it still suffers TCP-level HOL | Compare HTTP/1.1 vs HTTP/2 load times for 50 small assets | Graphs: representations, adjacency list/matrix, build a graph | How does HTTP/2 fix application-layer HOL but not transport-layer HOL? |
| 37 | **Consolidation** — HTTP/3 + QUIC, UDP-based transport, 0-RTT, connection migration | One-page diagram: HTTP/1.1 vs 2 vs 3, with the specific problem each solved | Graphs: number of islands, clone graph | Why did HTTP/3 abandon TCP? |

### Week 6 · Days 38–44 — HTTP semantics and API design

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 38 | Methods, safety, idempotency, PUT vs PATCH vs POST, why idempotency matters for retries | Add an idempotency-key header to a POST endpoint and make retries safe | BFS: shortest path in grid, rotting oranges | Is POST ever idempotent? How do you make it so? |
| 39 | Status codes with intent: 4xx vs 5xx, 409, 422, 429, 503 + Retry-After; what a client should do with each | A status-code decision table for your API; implement 409 and 429 properly | DFS: path exists, course schedule (cycle detection) | When 400 vs 422 vs 409, and why does the distinction matter to a client? |
| 40 | Headers, cookies, `Cache-Control`, ETags, conditional requests, CORS, content negotiation, compression | Add ETag + `If-None-Match` to a GET endpoint; prove the 304 | BFS: word ladder, 01-matrix | How does an ETag save bandwidth and how do you generate one? |
| 41 | REST resource modelling, nested resources, naming, HATEOAS reality check, when REST is wrong (gRPC/GraphQL) | Redesign your API's resource model; write the OpenAPI spec first | DFS: number of provinces, surrounded regions | Design the REST API for a document ingestion + query service |
| 42 | Pagination: offset vs cursor/keyset, sorting, filtering, why offset pagination dies at scale | Implement cursor pagination over a 100k-row table; compare query plans to offset | Intervals: merge intervals, insert interval | Why is `OFFSET 100000 LIMIT 20` slow, and what replaces it? |
| 43 | API versioning: URL vs header vs media type, deprecation policy, backward-compatible change rules | Version your API; document what counts as a breaking change | Intervals: non-overlapping intervals, meeting rooms II | Which schema changes are backward compatible and which break clients? |
| 44 | **Consolidation** — error contracts (RFC 7807), correlation IDs, structured logging, rate-limit headers | Uniform error envelope + request-ID middleware across all endpoints | Greedy: jump game, gas station | Design an error response a client can act on programmatically |

### Week 7 · Days 45–52 — PostgreSQL, properly

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 45 | SQL foundations: SELECT/WHERE/GROUP BY/HAVING, aggregates, NULL semantics, CTEs, window functions | Load a 1M-row dataset; write 15 queries including 3 window functions | Greedy: partition labels, candy | Why doesn't `WHERE col = NULL` work? |
| 46 | Joins: inner/left/right/full/cross/self, join algorithms (nested loop, hash, merge), when each is chosen | 10 join queries; `EXPLAIN` each and identify the join algorithm | Backtracking: N-queens, word search | When does Postgres choose a hash join over a nested loop? |
| 47 | Indexes: B-tree, composite index column order, covering indexes, partial indexes, GIN/GiST, index bloat | Add indexes to slow queries; measure before/after with `EXPLAIN ANALYZE`; find one index Postgres refuses to use | Backtracking: combination sum II, palindrome partitioning | Why did Postgres ignore your index? Give three reasons |
| 48 | B-tree/B+tree mechanics: node structure, fanout, height, why disk-oriented, page size, selectivity, cardinality | Draw a B+tree insert/split by hand; compute height for 100M rows | Graphs: topological sort (Kahn + DFS) | Why B+tree and not a hash index or a binary tree for a database? |
| 49 | Transactions, BEGIN/COMMIT/ROLLBACK, savepoints, MVCC, tuple visibility, VACUUM, transaction ID wraparound | Two psql sessions: demonstrate MVCC visibility; watch a dead tuple; run VACUUM | Graphs: Dijkstra | Explain MVCC and why it means readers don't block writers |
| 50 | ACID in practice: what Postgres actually guarantees, WAL, fsync, durability vs performance, crash recovery | Read the WAL config; explain `synchronous_commit` tradeoff; simulate crash recovery | Graphs: Bellman-Ford / cheapest flights k stops | What does the D in ACID cost you, and what knob trades it for speed? |
| 51 | Isolation levels: read committed, repeatable read, serializable; dirty/non-repeatable/phantom reads; write skew | Reproduce each anomaly in two psql sessions — actually reproduce them, don't read about them | DP intro: climbing stairs, house robber | Reproduce write skew and name the isolation level that prevents it |
| 52 | Locks: row/table locks, `FOR UPDATE`, `SKIP LOCKED`, advisory locks, deadlock detection, lock ordering | Cause a deadlock on purpose; read the Postgres log; fix it by lock ordering; build a job queue with `SKIP LOCKED` | DP: coin change, longest increasing subsequence | Build a safe job queue in Postgres with no double-processing |

### Week 8 · Days 53–60 — Redis, production concerns, Project 1 ships

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 53 | Redis: single-threaded event loop, data types (string/hash/list/set/zset/stream), TTL, persistence (RDB/AOF), eviction policies | Use all 6 data types for a real purpose; configure `maxmemory-policy`; measure ops/sec | DP: house robber II, decode ways | Why is single-threaded Redis fast, and when does that become the bottleneck? |
| 54 | Caching patterns: cache-aside, read-through, write-through, write-behind; cache hit ratio; what to cache | Add cache-aside to your hottest endpoint; measure p50/p99 before and after; log hit ratio | DP: unique paths, min path sum | Which pattern for a read-heavy endpoint with occasional writes, and why? |
| 55 | Invalidation: TTL vs explicit, stampede/thundering herd, mutex/single-flight, stale-while-revalidate, negative caching | Trigger a cache stampede with concurrent requests; fix it with a lock or single-flight | DP: word break, LCS | Your cache expires and 5000 requests hit the DB at once. Fix it three ways |
| 56 | Connection pooling: why connections are expensive in Postgres, pool sizing, pgBouncer, pool exhaustion symptoms | Set pool size to 2 under load, observe queueing and timeouts; tune it; document the formula you used | Union-Find: implement with union by rank + path compression | Why does Postgres suffer more from too many connections than MySQL, and what's the fix? |
| 57 | Rate limiting: fixed window, sliding window log, sliding window counter, token bucket, leaky bucket; distributed limiting in Redis | Implement token bucket in Redis with Lua for atomicity; return 429 + `Retry-After` | Union-Find: number of connected components, accounts merge | Implement a distributed rate limiter and explain the race condition Lua prevents |
| 58 | Authentication: sessions vs JWT, JWT structure/signing/expiry, refresh tokens, OAuth2 flows, token revocation problem, password hashing (bcrypt/argon2) | Full auth: register, login, JWT access + refresh, rotation, revocation list in Redis | Mixed: 2 mediums timed | How do you revoke a stateless JWT, and what does that cost you? |
| 59 | Authorization: RBAC vs ABAC, roles/permissions modelling, multi-tenancy isolation, row-level security, the IDOR bug class | RBAC with 3 roles + tenant isolation; write a test that proves tenant A can't read tenant B | Mixed: 2 mediums timed | How do you guarantee tenant isolation, and how do you test it? |
| 60 | **Project 1 productionisation + month review** | Structured logging, health/readiness endpoints, graceful shutdown, Dockerfile, docker-compose, GitHub Actions CI, README + architecture diagram, load test with `locust`/`k6` | **Mock:** 45-min timed, 2 problems + 20-min system design | Walk through Project 1 architecture and defend every technology choice |

### Month 2 checkpoint

- [ ] Project 1 running, tested, containerised, CI green, load-tested, documented
- [ ] You reproduced (not read about) all four isolation anomalies
- [ ] You caused and fixed: a deadlock, a cache stampede, a pool exhaustion
- [ ] You can defend Postgres vs MongoDB, Redis vs in-process cache, JWT vs sessions
- [ ] 60 DSA problems; graphs and DP started
- [ ] Resume v1 written around Project 1

---

# MONTH 3 · DAYS 61–90
## LLMs → LLM APIs in production → embeddings → first RAG · 🚨 **applications start Day 75**

**Month goal:** you can build a retrieval-augmented system that a company would actually deploy, and you understand the cost/latency/quality triangle. Simultaneously, your job search machine goes live.

**Month deliverables**

- **Project 2 v1: RAG service** with citations, streaming, and an eval set
- 90 cumulative DSA problems
- LinkedIn + GitHub + resume v1 shipped by Day 61; first applications out by Day 75
- Target-company spreadsheet with 60+ rows

### Week 9 · Days 61–67 — LLM fundamentals (behaviour, not internals yet)

> Internals come in Month 7. This week is about being able to *use and reason about* a model correctly.

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 61 | LLM landscape and mental model: next-token prediction, pretraining vs instruction tuning vs RLHF, what a model can and cannot know, hallucination as a property not a bug. **+ profile day:** LinkedIn headline/about, GitHub README, resume v1 | Notes + all three profiles updated and public | Trees: BST iterator, count good nodes | Why does a model hallucinate confidently, and what class of fix actually helps? |
| 62 | Tokenisation: BPE, subwords, why token ≠ word, non-English token inflation, token costs, counting tokens | Tokenise the same paragraph in 3 tokenisers; compare counts; compute cost per 1M requests | Graphs: Dijkstra revisit, network delay time | Why does the same sentence cost more in Hindi than English? |
| 63 | Context window: what it is, why it's finite, attention cost growth, lost-in-the-middle, context vs retrieval tradeoff | Test recall of a fact placed at start/middle/end of a long context — chart the result | Graphs: min spanning tree (Kruskal/Prim) | Long context vs RAG — when do you pick which? Give the cost argument |
| 64 | Sampling: greedy, temperature, top-k, top-p, repetition penalty, seeds, determinism limits, structured-task settings | Same prompt at temp 0/0.3/0.7/1.2 × 5 runs; document variance; pick defaults per task type | Graphs: bipartite check, alien dictionary | What temperature for extraction vs brainstorming, and why is temp 0 still not deterministic? |
| 65 | Prompt engineering that survives production: role/instruction/context/format separation, few-shot, CoT, delimiters, negative instructions, prompt versioning | Build a prompt template module with versioning; A/B two versions on 20 inputs | DP: edit distance | Show two prompt versions and the measured difference — not your opinion |
| 66 | Structured output: JSON mode, function/tool schemas, constrained decoding, Pydantic validation loops, repair strategies | Extract structured records from 30 messy documents; measure schema-valid rate; add a repair retry | DP: longest palindromic substring | Your model returns invalid JSON 4% of the time. Three fixes, ranked |
| 67 | Streaming: SSE vs WebSocket, token streaming, TTFT vs total latency, backpressure, cancellation, partial-failure UX | Stream tokens over SSE through FastAPI; support client cancellation mid-stream | DP: partition equal subset sum | Why does streaming improve perceived latency without improving throughput? |

### Week 10 · Days 68–74 — LLM APIs as production dependencies

> This week is where "AI engineer" starts meaning "engineer." Treat the LLM as a flaky, expensive, rate-limited third-party dependency — because that's exactly what it is.

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 68 | LLM API integration: client abstraction, timeouts, connection reuse, async concurrency, semaphores, provider differences | Provider-agnostic LLM client interface with 2 implementations behind one protocol | Medium arrays: product except self, subarray sum divisible by k | Why abstract the provider, and what leaks through the abstraction anyway? |
| 69 | Function calling: schema design, argument validation, multi-call, parallel calls, error feedback to the model | 4 tools the model can call; validate args; feed errors back for self-correction | Medium strings: longest substring k distinct, string compression | How do you stop a model calling a tool with hallucinated arguments? |
| 70 | Tool execution layer: dispatch, sandboxing, timeouts per tool, idempotency, side-effect safety, result truncation | Tool registry with per-tool timeout, retry policy, and output size cap | Medium hashing: LRU cache implementation | A tool takes 90s and the model waits. What does your architecture do? |
| 71 | Enforced structured output at scale: schema evolution, optional fields, enums, nested objects, validation telemetry | Log schema-failure rate as a metric; alert threshold; dashboard it | Medium trees: construct from traversals, LCA | How do you monitor output quality in production without human review of everything? |
| 72 | Reliability: retries with jitter, exponential backoff, circuit breakers, provider fallback, timeout budgets, graceful degradation | Kill the provider (bad API key) mid-load-test; system degrades instead of dying | Medium graphs: pacific-atlantic water flow | Provider returns 429 for 10 minutes. Exactly what does your service do? |
| 73 | Model routing: cheap-model-first, escalation on low confidence, task-based routing, semantic caching, quality/cost tradeoff | Router: small model default, escalate on validation failure; measure cost saved and quality delta | Medium graphs: word ladder II / course schedule II | How would you cut LLM spend 60% without users noticing? |
| 74 | Cost + latency observability: tokens per request, cost per request/tenant, TTFT, p50/p95/p99, tracing spans, log redaction | OpenTelemetry-style spans + cost per request per tenant + a real dashboard | Medium DP: max product subarray, jump game II | What are your p99 and cost per query, and which component owns each? |

### Week 11 · Days 75–81 — Embeddings and vector search · 🚨 **applications go live**

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 75 | **🚨 JOB SEARCH DAY 1** + embeddings: what a vector represents, dimensions, model choice, normalisation, domain mismatch, embedding drift | Embed 1000 docs; visualise clusters with UMAP/t-SNE; **send first 5 applications** | Trees/graphs mixed: 2 problems | What does the distance between two embeddings actually mean? |
| 76 | Similarity: cosine vs dot vs Euclidean, normalisation, why cosine dominates text, thresholds, calibration | Brute-force similarity search over 10k vectors in NumPy; measure latency; find the threshold where precision collapses | Arrays medium: 2 problems | Cosine vs dot product — when are they identical and when not? |
| 77 | Vector databases: ANN algorithms (HNSW, IVF, PQ), recall vs latency tradeoff, index build cost, filtering strategies, managed vs embedded options | Same 10k vectors in an ANN index; plot recall vs latency vs `ef_search` | Graph medium: 2 problems | Explain HNSW in three sentences and what you sacrifice for speed |
| 78 | pgvector: extension setup, vector column, HNSW/IVFFlat in Postgres, hybrid filtering with SQL, when one database beats two | Migrate your vectors into Postgres + pgvector; filter by metadata *and* similarity in one query | DP medium: 2 problems | Argue for pgvector over a dedicated vector DB, then argue against it |
| 79 | Chunking: fixed vs recursive vs semantic vs structural, overlap, chunk size vs retrieval quality, tables/code/lists, parent-document retrieval | Three chunking strategies on the same corpus; measure retrieval quality difference on a 30-question eval set | Backtracking: 2 problems | Your retrieval is bad. Why is chunking usually the first suspect? |
| 80 | Metadata + filtering: schema design, pre- vs post-filtering, permissions in retrieval, tenant scoping, freshness/recency boosting | Metadata schema + permission-aware retrieval; test that a user can't retrieve a doc they can't read | Intervals/greedy: 2 problems | How do you enforce document-level ACLs inside vector search? |
| 81 | Retrieval pipeline assembly: query → embed → search → filter → assemble context; top-k selection, dedup, token budgeting, truncation strategy | End-to-end mini-RAG working, unframeworked — raw SQL + raw API calls | Mixed: 2 problems | Your context budget is 8k tokens and retrieval returns 40 chunks. What's your algorithm? |

### Week 12 · Days 82–90 — Project 2: RAG service you'd actually deploy

**Architecture**

```
Documents (pdf/docx/html/md)
    ↓ Parser + layout extraction
    ↓ Chunker (recursive + structural)
    ↓ Embedding pipeline (batched, retried, resumable)
    ↓ PostgreSQL + pgvector  (chunks, embeddings, metadata, ACLs)
    ↓ Retriever (vector + metadata filter + dedup + budget)
    ↓ Prompt assembly (with citation markers)
    ↓ LLM (streamed)
    ↓ Answer + inline citations + confidence + cost/latency trace
```

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 82 | Document ingestion: PDF/DOCX/HTML parsing, layout loss, tables, OCR fallback, encoding hell, idempotent ingestion, dedup by content hash | Ingestion endpoint handling 4 formats; re-ingest is a no-op; 20 real messy documents loaded | Mixed medium: 2 | A 300-page scanned PDF arrives. Walk me through your pipeline |
| 83 | Chunking implementation: structure-aware splitting, heading context injection, overlap tuning, chunk metadata | Configurable chunker; store chunk lineage (doc → section → chunk) | Mixed medium: 2 | How do you keep a chunk from losing the meaning its heading gave it? |
| 84 | Embedding pipeline: batching, rate limits, retries, partial failure recovery, checkpointing, backfill, re-embedding on model change | Resumable batch embedder — kill it halfway, restart, no duplicates, no gaps | Mixed medium: 2 | Your embedding model gets deprecated. What is your migration plan? |
| 85 | Retrieval implementation + tuning: top-k, thresholds, MMR/diversity, metadata boosts, latency budget | Retriever with tunable params exposed as config; latency measured at each stage | Mixed medium: 2 | Where do the milliseconds go in a RAG query? Give the breakdown |
| 86 | Prompt assembly: context ordering, citation markers, instruction to abstain, token budget enforcement, prompt injection from documents | Assembler that enforces budget, orders context deliberately, and instructs abstention | Mixed medium: 2 | A retrieved document says "ignore previous instructions." What happens? |
| 87 | Citations + groundedness: span-level attribution, citation verification, "I don't know" behaviour, faithfulness checks | Every answer sentence maps to a chunk ID; unsupported claims flagged | Mixed medium: 2 | How do you prove an answer came from the source and not the model's memory? |
| 88 | Streaming + UX: SSE from retrieval through generation, progressive citations, cancellation, timeout handling, partial answers | Streamed answers with citations arriving progressively; cancellable | Mixed medium: 2 | What do you stream first and why does ordering matter to the user? |
| 89 | Evaluation: golden set construction, retrieval metrics (recall@k, MRR, nDCG), answer metrics (faithfulness, relevance), LLM-as-judge and its biases, regression gating in CI | 50-question golden set + automated eval run + CI gate that fails on regression | Mixed medium: 2 | How do you know your RAG got better and not just different? |
| 90 | **Deploy + demo + month review** | Deployed publicly, README with architecture diagram, 3-min Loom demo, eval numbers in the README, resume updated with measured results | **Mock:** 2 problems timed + RAG system design out loud | Present Project 2 in 3 minutes with numbers, not adjectives |

### Month 3 checkpoint

- [ ] RAG service deployed with citations, streaming, evals, and an eval-gated CI
- [ ] Built retrieval once with **no framework** — you can explain every line
- [ ] Cost per query and p95 latency known and documented
- [ ] Applications live: 5–10/week since Day 75, tracker maintained
- [ ] 90 DSA problems; graphs and DP no longer scary
- [ ] One public post written about something you built

### 🚨 Job search activation (Days 61–90)

**Day 61 — profile day (do it all in one sitting)**

- LinkedIn headline: `AI / Backend Engineer · LLM · RAG · Distributed Systems · Python · Postgres · Kafka · AWS`
- LinkedIn About: 4 short paragraphs — what you build, the stack, two projects with numbers, what you're looking for
- GitHub profile README linking your 2 (eventually 4) flagship repos
- Resume v1: one page, projects above education, numbers in every bullet
- Target-company spreadsheet: 60+ rows across four tiers (Section 15)
- 20 recruiters + 20 engineers identified for outreach

**Day 75 onward — 5–10 applications/week**

Roles to search (Priority 1): AI Engineer · GenAI Engineer · Applied AI Engineer · AI Backend Engineer · LLM Engineer · AI Platform Engineer · AI Infrastructure Engineer

Roles to search (Priority 2): Backend Engineer (AI) · Platform Engineer · Distributed Systems Engineer · ML Platform Engineer · Software Engineer (GenAI)

**Target band for Days 75–90: ₹15–30L.** Yes, below your goal. These are for interview reps and calibration data. Take the interviews, learn the loop, then aim higher with real experience.

---

# MONTH 4 · DAYS 91–120
## Advanced retrieval → Kafka → reliability → distributed systems

**Month goal:** move from "builds AI features" to "designs AI systems." This month is what makes ₹35L+ conversations possible.

**Month deliverables**

- **Project 3: Distributed AI Document Platform** (Kafka, workers, DLQ, idempotency, observability)
- 120 cumulative DSA problems
- 8+ system designs written up
- Applications at 10–15/week

### Week 13 · Days 91–97 — Advanced RAG

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 91 | Query understanding + rewriting: intent classification, decontextualisation of follow-ups, HyDE, multi-query generation, cost of extra LLM hops | Rewrite layer; measure recall improvement on your golden set and the added latency | 2 mediums | When is a query rewrite worth an extra 400ms? |
| 92 | Query expansion + decomposition: synonyms, acronym handling, sub-question decomposition, routing to different indexes | Decompose multi-hop questions into sub-queries; aggregate the answers | 2 mediums | "Compare our 2023 and 2024 refund policies" — how does retrieval handle this? |
| 93 | Hybrid search: dense vs sparse failure modes, exact-match and rare-token problems, when keyword beats vectors | Find 10 queries where vector search fails and keyword wins; document the pattern | 2 mediums | Give a query where embeddings fail badly and explain why |
| 94 | BM25 and lexical scoring: TF-IDF, term saturation, length normalisation, Postgres full-text search / `tsvector` | BM25 or Postgres FTS running alongside your vector index | 2 mediums | How does BM25 differ from TF-IDF and why does saturation matter? |
| 95 | Fusion: reciprocal rank fusion, weighted score fusion, score normalisation across incomparable scales, tuning weights | RRF over both retrievers; measure the lift on your golden set | 2 mediums | Why can't you just average a cosine score and a BM25 score? |
| 96 | Reranking: cross-encoder vs bi-encoder, latency cost, top-k → top-n funnel, when reranking beats better chunking, ColBERT/late interaction | Cross-encoder reranker on top-50 → top-8; measure precision gain vs latency cost | 2 mediums | Why is a cross-encoder more accurate and unusable at scale as a first-stage retriever? |
| 97 | RAG evaluation at depth: component-wise eval, retrieval vs generation attribution, failure taxonomy, human review sampling, online metrics | Failure taxonomy over 30 real failures, each attributed to a stage | 2 mediums | Answer is wrong. How do you determine whether retrieval or generation failed? |

### Week 14 · Days 98–104 — Kafka

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 98 | Kafka architecture: brokers, log-structured storage, append-only segments, ZooKeeper vs KRaft, retention, compaction, why it's fast | Local Kafka running; inspect log segments on disk | 2 mediums | Why is Kafka fast when it writes everything to disk? |
| 99 | Topics, partitions, replication factor, leader/follower, ISR, partition keys and skew | Multi-partition topic; produce keyed messages; observe distribution and one hot partition | 2 mediums | How do you choose the number of partitions, and what breaks if you're wrong? |
| 100 | Producers: acks 0/1/all, batching, `linger.ms`, compression, `max.in.flight` vs ordering, idempotent producer, delivery guarantees | Benchmark throughput vs durability across `acks` settings; chart it | 2 mediums | `acks=all` vs `acks=1` — what exactly do you lose, and how much throughput do you gain? |
| 101 | Consumers: poll loop, `max.poll.records`, `max.poll.interval.ms`, auto vs manual commit, rebalance triggers, session timeouts | Consumer with manual commit; trigger a rebalance mid-processing and observe duplicates | 2 mediums | Your consumer takes 5 minutes per message. What breaks and how do you fix it? |
| 102 | Consumer groups: group coordination, partition assignment strategies, scaling limits, static membership, cooperative rebalancing | Scale consumers 1 → 3 → 5 on a 3-partition topic; document what happens at 5 | 2 mediums | Why does adding a 4th consumer to a 3-partition topic do nothing? |
| 103 | Offsets: `__consumer_offsets`, commit semantics, replay, seeking, lag monitoring, offset reset policies | Replay from an earlier offset; build a lag dashboard | 2 mediums | How do you reprocess yesterday's messages without reprocessing today's? |
| 104 | Ordering: per-partition guarantees, global ordering cost, causal ordering, keying for order, out-of-order handling downstream | Prove ordering holds per key and breaks across partitions | 2 mediums | You need strict ordering per user. How do you partition, and what does it cost? |

### Week 15 · Days 105–111 — Reliability engineering

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 105 | At-least-once delivery: the default, when duplicates appear, why "just don't duplicate" is impossible | Force duplicates by killing a consumer before commit; count them | 2 mediums | Prove that at-least-once delivery must produce duplicates sometimes |
| 106 | At-most-once: commit-before-process, when data loss is acceptable, metrics/telemetry as legitimate use cases | Implement it; force a loss; measure the loss rate | 2 mediums | Name a real feature where losing a message is the correct tradeoff |
| 107 | Exactly-once semantics: transactions, `read_committed`, transactional outbox, why EOS is really effectively-once, cross-system limits | Kafka transactional producer + consumer; explain where the guarantee ends | 2 mediums | Why can't you have exactly-once between Kafka and a third-party HTTP API? |
| 108 | Retry strategy: transient vs permanent errors, exponential backoff with jitter, retry budgets, retry storms, retry topics with delays | Retry classifier + backoff + a bounded retry budget | 2 mediums | Retrying made the outage worse. Explain the mechanism |
| 109 | Dead-letter queues: when to DLQ, DLQ schema (payload + error + attempts + trace), replay tooling, DLQ monitoring and alerting | DLQ + a replay CLI that reprocesses selectively | 2 mediums | What goes in a DLQ record so a human can actually act on it 3 days later? |
| 110 | Idempotency: idempotency keys, dedup stores with TTL, natural vs synthetic keys, idempotent writes vs idempotent effects, upserts | Make every consumer idempotent; prove it by replaying the whole topic and diffing DB state | 2 mediums | Make "send an email" idempotent. Be specific |
| 111 | Backpressure + flow control: queue depth as a signal, bounded queues, load shedding, rate limiting upstream, autoscaling on lag, the bufferbloat trap | Load-test until lag grows; implement shedding; document the breaking point | 2 mediums | Producers outpace consumers 3:1. Rank your options |

### Week 16 · Days 112–120 — Distributed systems theory that gets asked

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 112 | CAP theorem precisely: what P really means, why CA is not a choice in practice, common misuses of CAP | Classify 8 systems you know (Postgres, Kafka, Redis, DynamoDB, Cassandra, S3, etcd, Zookeeper) | 2 mediums | Why is "we chose CA" almost always wrong? |
| 113 | PACELC: latency vs consistency in the non-partitioned case, why it explains real database choices better than CAP | Re-classify the same 8 systems under PACELC | 2 mediums | Two systems are both AP. PACELC distinguishes them how? |
| 114 | Replication: leader-follower, multi-leader, leaderless, sync vs async, replication lag, read-your-writes, failover and split-brain | Set up Postgres streaming replication; measure lag; read stale data on purpose | 2 mediums | User updates their profile and doesn't see the change. Diagnose and fix |
| 115 | Consistency models: linearizability, sequential, causal, eventual, monotonic reads, session guarantees, cost of each | Map each model to a feature where it's the right choice | 2 mediums | Where would eventual consistency be unacceptable in a payments product? |
| 116 | Quorums: R + W > N, sloppy quorums, hinted handoff, read repair, anti-entropy, tunable consistency | Compute quorum configurations for N=3 and N=5 across failure scenarios | 2 mediums | N=5, W=3, R=2 — what does that guarantee and what does it not? |
| 117 | Distributed locks: why they're dangerous, leases, fencing tokens, Redlock and its critique, when to use etcd/ZooKeeper instead | Implement a Redis lease lock with a fencing token; then break it with a GC pause | 2 mediums | Why is a Redis lock with a TTL not sufficient for correctness? |
| 118 | Transactional outbox + CDC: the dual-write problem, outbox pattern, Debezium/CDC, ordering guarantees, at-least-once downstream | Outbox table + relay publishing to Kafka; kill it mid-flight and prove no loss | 2 mediums | Why can't you write to your DB and publish to Kafka in one transaction? |
| 119 | Sagas + long-running workflows: choreography vs orchestration, compensating actions, semantic rollback, timeouts, workflow engines | Design a 4-step saga with compensations for your ingestion pipeline | 2 mediums | Step 3 of 4 fails after side effects. What happens? |
| 120 | **Month review + system design mock** | Project 3 walkthrough written up; architecture diagram; failure-mode document | **Mock:** 45-min system design (distributed job processing system) + 2 DSA | Design a distributed document processing pipeline handling 1M docs/day |

### Month 4 checkpoint

- [ ] Project 3 deployed: Kafka, workers, retries, DLQ, idempotency, observability
- [ ] You killed consumers mid-processing and can describe exactly what happened
- [ ] You can whiteboard the outbox pattern and explain why it exists
- [ ] Hybrid search + reranking measurably improved your golden-set numbers
- [ ] 120 DSA problems; 8 system designs written
- [ ] Applications at 10–15/week; first-round interviews happening

---

# MONTH 5 · DAYS 121–150
## System design → Docker → AWS

**Month goal:** stop being a person who builds services and become a person who designs systems and runs them in the cloud. System design is the round that most often decides between ₹25L and ₹45L.

**Month deliverables**

- 20+ written system designs (one page each, with capacity numbers)
- All three projects containerised and deployed on AWS
- Terraform or at minimum reproducible infra scripts
- 150 cumulative DSA problems

### Week 17 · Days 121–127 — System design method

> Do not memorise designs. Learn the *method*, then apply it 20 times. Every design gets a one-pager in `system-design-notes/`: requirements → estimates → API → data model → architecture → bottlenecks → failure modes → tradeoffs.

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 121 | Requirements gathering: functional vs non-functional, clarifying questions, scoping down, identifying the actual hard part, SLOs | Write the question checklist you'll use in every interview; apply it to "design a URL shortener" | 2 mediums | What are the first 6 questions you ask before designing anything? |
| 122 | Capacity estimation: DAU → QPS, read/write ratio, peak multiplier, storage per record, bandwidth, cost per month, back-of-envelope discipline | Estimate for 3 systems; sanity-check against real published numbers | 2 mediums | 10M DAU, 5 reads/user/day, 2KB per read — QPS at peak and monthly egress? |
| 123 | API + interface design in interviews: contract first, sync vs async, idempotency, pagination, versioning, gRPC vs REST tradeoffs | API contracts for 3 designs | 2 mediums | Which operations in your design must be async, and why? |
| 124 | Data store selection: RDBMS vs document vs KV vs wide-column vs search vs vector vs object store vs time-series; access-pattern-driven choice | Decision matrix mapping access patterns → store; justify pgvector vs Pinecone vs OpenSearch | 2 mediums | Justify Postgres over Cassandra for one system and the reverse for another |
| 125 | Caching architecture: client/CDN/edge/app/DB layers, cache key design, TTL strategy, invalidation at scale, hot key mitigation, negative caching | Add a caching layer to 3 designs; identify the hot-key risk in each | 2 mediums | One celebrity user's data is 40% of your traffic. Fix it |
| 126 | Async processing: queues vs streams vs schedulers, fan-out patterns, priority queues, scheduled/delayed jobs, exactly-once effects, worker autoscaling | Design a job system with priorities, delays, retries, and DLQ | 2 mediums | When a queue and when a stream? Give the deciding factor |
| 127 | Load balancing: L4 vs L7, algorithms, health checks, sticky sessions, service discovery, connection draining, cross-AZ balancing | Design the LB layer with health checks and draining for one project | 2 mediums | How does a load balancer avoid sending traffic to a dying instance? |

### Week 18 · Days 128–134 — Scale and resilience patterns

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 128 | Sharding: key selection, range vs hash vs directory, hot shards, resharding pain, cross-shard queries and joins, distributed transactions avoidance | Shard plan for a 10TB table including the resharding procedure | 2 mediums | Your shard key turned out to be wrong in production. What now? |
| 129 | Replication in design: read replicas, replica lag handling, write amplification, geo-replication, active-active conflicts, CRDTs at a high level | Add replicas to 2 designs and specify which reads may be stale | 2 mediums | Which reads in your design tolerate 500ms of staleness, and which don't? |
| 130 | Consistent hashing: the rebalancing problem, hash ring, virtual nodes, bounded loads, where it's actually used | Implement consistent hashing with virtual nodes; measure key movement on node add/remove | 2 mediums | Add a node to a 10-node ring — what fraction of keys move, with and without vnodes? |
| 131 | Rate limiting + quotas at system level: per-user/tenant/API-key, distributed counters, burst allowance, tiered plans, LLM token quotas | Design multi-tenant quota system with token-based LLM budgets | 2 mediums | Design fair-share rate limiting for an LLM API with 5000 tenants |
| 132 | Circuit breakers, bulkheads, timeouts, retry budgets, graceful degradation, feature flags, fallback hierarchies | Add a circuit breaker to your LLM client; define the degraded experience explicitly | 2 mediums | Your embedding provider is down. What does your product still do? |
| 133 | Failure handling + blast radius: cascading failures, thundering herds, retry amplification, cell-based architecture, chaos testing, graceful restart | Write a failure-mode analysis table for Project 3: 10 failures × detection × mitigation × blast radius | 2 mediums | Walk me through a cascading failure and where you'd cut it |
| 134 | Observability: logs vs metrics vs traces, RED/USE/golden signals, cardinality cost, distributed tracing, SLI/SLO/error budgets, alert design and alert fatigue | Dashboard with the four golden signals + 3 alerts that would actually page someone | 2 mediums | You get paged at 3am. What are the first three things you look at? |

### Week 19 · Days 135–141 — Docker and containers

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 135 | Container fundamentals: namespaces, cgroups, union filesystems, images vs containers, why containers ≠ VMs, OCI | Explain what `docker run` does in kernel terms; inspect namespaces of a running container | 2 mediums | How is a container isolated if it shares the host kernel? |
| 136 | Dockerfile craft: layers, cache invalidation, `COPY` ordering, `.dockerignore`, base image choice, non-root user, `ENTRYPOINT` vs `CMD`, signal handling and PID 1 | Rewrite your Dockerfile: build time and image size both cut significantly; document before/after | 2 mediums | Your image is 1.8GB and rebuilds take 6 minutes. Fix both |
| 137 | Multi-stage builds, distroless/slim images, dependency caching, reproducible builds, vulnerability scanning, image tagging strategy | Multi-stage build under 200MB; `trivy` scan clean of criticals | 2 mediums | Why does the build stage need a compiler and the runtime stage must not have one? |
| 138 | Container networking: bridge/host/none, port publishing, DNS between containers, `localhost` inside containers, egress | Debug a real container-to-container connection failure | 2 mediums | Your app can't reach Postgres in another container. First 4 checks |
| 139 | Volumes and state: bind mounts vs named volumes, data persistence, permissions/UID mismatches, secrets *not* in images, config via env | Postgres with a persistent volume that survives container recreation; secrets injected, not baked | 2 mediums | Why is a secret in an image layer still a secret leak after you delete it? |
| 140 | Docker Compose: multi-service local stack, `depends_on` vs actual readiness, healthchecks, profiles, resource limits, dev/prod parity | One `docker compose up` brings up API + Postgres + pgvector + Redis + Kafka + worker, with healthchecks | 2 mediums | `depends_on` says the DB started but your app crashes. Why? |
| 141 | Production containers: resource requests/limits, OOMKilled, liveness vs readiness vs startup probes, graceful shutdown, log/stdout discipline, 12-factor | Add health endpoints, `SIGTERM` handling, and resource limits to all services; force an OOMKill and read the exit code | 2 mediums | Difference between liveness and readiness, and what happens if you swap them? |

### Week 20 · Days 142–150 — AWS

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 142 | IAM: users vs roles, policies, trust relationships, assume-role, instance profiles, least privilege, IRSA concept, access key hygiene | Roles for your app with least-privilege policies; zero long-lived keys in the app | 2 mediums | Why is an IAM role better than an access key on an EC2 instance? |
| 143 | VPC: subnets public/private, route tables, IGW vs NAT, security groups vs NACLs, VPC endpoints, AZs | Draw and then build a 2-AZ VPC: public ALB subnets, private app + DB subnets | 2 mediums | Your private instance can't reach the internet. What's missing? |
| 144 | Compute: EC2 instance families, EBS vs instance store, user data, ASGs, spot vs on-demand vs reserved; ECS/Fargate vs EKS vs Lambda tradeoffs | Deploy the API on ECS Fargate (or EC2 + ASG); document why you chose it | 2 mediums | ECS vs EKS vs Lambda for an LLM gateway — argue the choice |
| 145 | S3: buckets, keys, storage classes, lifecycle policies, versioning, presigned URLs, consistency model, encryption, event notifications | Documents stored in S3 with presigned upload; S3 event triggers ingestion | 2 mediums | How do you let a browser upload a 500MB file without proxying it through your API? |
| 146 | RDS: managed Postgres, parameter groups, multi-AZ vs read replicas, backups/PITR, failover behaviour, connection limits, pgvector on RDS | Migrate to RDS with multi-AZ; trigger a failover and time the recovery | 2 mediums | What actually happens to in-flight connections during a multi-AZ failover? |
| 147 | ALB/NLB: listeners, target groups, health checks, TLS termination, ACM certificates, sticky sessions, WAF basics, Route 53 | HTTPS with a real domain, ACM cert, health-checked target group | 2 mediums | Where do you terminate TLS and what are the tradeoffs? |
| 148 | CloudWatch + observability on AWS: log groups, metric filters, custom metrics, alarms, dashboards, X-Ray tracing, cost of logs | Alarms on error rate, p99 latency, and Kafka consumer lag | 2 mediums | How would you alert on p99 latency without alerting on every blip? |
| 149 | Secrets + config: Secrets Manager vs Parameter Store, rotation, KMS envelope encryption, encryption at rest and in transit, cost management and tagging | All secrets externalised; a cost dashboard tagged per project | 2 mediums | How do you rotate a database password with zero downtime? |
| 150 | **Deploy everything + month review** | All three projects deployed on AWS behind HTTPS, monitored, with a documented teardown/spin-up; infra as code if possible; architecture diagrams updated | **Mock:** 45-min system design + 45-min DSA | Give a 5-minute tour of your production infrastructure and its costs |

### Month 5 checkpoint

- [ ] 20 system designs written, each with capacity numbers and failure modes
- [ ] All projects on AWS, HTTPS, monitored, alarmed, cost-tracked
- [ ] You can Dockerfile from scratch and explain every line
- [ ] You survived a deliberate RDS failover and know the recovery time
- [ ] 150 DSA problems
- [ ] Interviews: at least 5 first rounds done; feedback logged

---

# MONTH 6 · DAYS 151–180
## Maths → classical ML → ML engineering → PyTorch

**Month goal:** stop being an "LLM API user" and become someone who understands what the model is doing. You will not become a research scientist in 30 days; you will become an engineer who can hold a technical conversation about models without bluffing.

**Month deliverables**

- Maths notes with worked examples by hand
- 5 classical ML models trained and evaluated properly
- A neural network trained from scratch in PyTorch, no high-level trainer
- A model served behind an API with batching
- 180 cumulative DSA problems

### Week 21 · Days 151–157 — The maths you actually need

> Goal: intuition and mechanics, not proofs. Every day: do it by hand once, then in NumPy.

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 151 | Vectors: representation, norms (L1/L2), unit vectors, vector spaces, high-dimensional intuition, curse of dimensionality | Compute norms by hand then NumPy; demonstrate that random high-dim vectors are near-orthogonal | 2 mediums | Why do distances become less meaningful in 1000 dimensions? |
| 152 | Matrices: multiplication as transformation, shapes, transpose, inverse, rank, broadcasting rules, why shape errors happen | Multiply matrices by hand; implement matmul in pure Python; compare to NumPy timing | 2 mediums | What does multiplying by a matrix do geometrically? |
| 153 | Dot product, projection, cosine similarity derivation, orthogonality, matrix-vector products in a neural layer | Derive cosine from the dot product yourself; connect it back to your embedding retrieval code | 2 mediums | Derive cosine similarity from the dot product and explain the normalisation |
| 154 | Probability: joint/marginal/conditional, Bayes' theorem, independence, expectation, variance, log-probabilities and why we use them | Solve 5 Bayes problems by hand; compute log-prob of a token sequence | 2 mediums | Why do models work in log space instead of probability space? |
| 155 | Distributions: Bernoulli, binomial, normal, softmax as a distribution, entropy, cross-entropy, KL divergence, perplexity | Implement softmax and cross-entropy in NumPy; compute perplexity of a toy sequence | 2 mediums | What is cross-entropy loss actually measuring? |
| 156 | Calculus: derivatives, partial derivatives, chain rule, gradients, Jacobians conceptually, why differentiability matters | Differentiate a 2-layer network by hand; verify numerically | 2 mediums | Apply the chain rule through a 2-layer network on paper |
| 157 | Gradient descent: loss surfaces, learning rate, batch vs mini-batch vs SGD, momentum, local minima vs saddle points, convergence failure | Implement gradient descent from scratch on linear regression; plot loss for 4 learning rates | 2 mediums | Your loss is oscillating and then explodes. Diagnose it |

### Week 22 · Days 158–164 — Classical ML

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 158 | Linear regression: hypothesis, MSE, closed form vs gradient descent, assumptions, multicollinearity, residual analysis | Implement from scratch, then with scikit-learn; compare and explain any difference | 2 mediums | When does linear regression fail even with lots of data? |
| 159 | Logistic regression: sigmoid, log loss, decision boundary, odds/log-odds, interpretability, class imbalance handling | Train on a real imbalanced dataset; tune the threshold deliberately, not by default | 2 mediums | Why not MSE for classification? |
| 160 | Decision trees: splitting criteria (gini/entropy), information gain, depth and overfitting, pruning, feature importance, categorical handling | Train and visualise a tree; show overfitting by increasing depth; plot train vs val | 2 mediums | Why does an unpruned decision tree memorise the training set? |
| 161 | Random forests: bagging, bootstrap sampling, feature subsampling, variance reduction, OOB error, why they're strong baselines | Compare a single tree vs a forest; explain the variance reduction with numbers | 2 mediums | Why does averaging many overfit trees generalise well? |
| 162 | Boosting: AdaBoost intuition, gradient boosting, XGBoost/LightGBM, learning rate vs n_estimators, why boosting still beats deep learning on tabular data | Train a gradient boosting model; tune 3 hyperparameters; beat your forest | 2 mediums | Bagging vs boosting — which reduces bias, which reduces variance? |
| 163 | Clustering: k-means (and its assumptions), choosing k, elbow/silhouette, DBSCAN, hierarchical clustering, clustering embeddings | Cluster your document embeddings; label the clusters; use it for retrieval routing | 2 mediums | Why does k-means fail on non-spherical clusters? |
| 164 | Dimensionality reduction: PCA (variance maximisation, eigenvectors intuitively), explained variance, t-SNE/UMAP for visualisation only | PCA your embeddings to 64 dims; measure retrieval quality loss and latency gain | 2 mediums | Can you compress 1536-dim embeddings to 256 and keep retrieval quality? Show data |

### Week 23 · Days 165–171 — ML engineering discipline

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 165 | Data splitting: train/val/test, stratification, k-fold CV, temporal splits, leakage sources, duplicate leakage, group splits | Build a leakage bug on purpose, detect it, then fix the split | 2 mediums | Give three ways data leakage sneaks into a pipeline |
| 166 | Overfitting/underfitting: bias-variance, learning curves, capacity, when more data helps and when it doesn't | Plot learning curves for 3 model capacities; diagnose each | 2 mediums | Train acc 0.99, val acc 0.71 — your next three actions |
| 167 | Regularisation: L1 vs L2, dropout, early stopping, data augmentation, weight decay, label smoothing | Apply L1 and L2; show the sparsity difference in the coefficients | 2 mediums | Why does L1 produce sparse weights and L2 doesn't? |
| 168 | Classification metrics: confusion matrix, precision, recall, F1, macro vs micro, when accuracy lies, threshold selection by business cost | Compute all metrics by hand on a confusion matrix; pick a threshold from a stated cost model | 2 mediums | 99% accuracy on fraud detection — why might that be worthless? |
| 169 | ROC/AUC vs precision-recall curves, calibration, Brier score, why calibrated probabilities matter downstream | Plot both curves for an imbalanced dataset; explain why PR is more informative here | 2 mediums | When is PR-AUC the right metric over ROC-AUC? |
| 170 | Feature engineering: scaling, encoding (one-hot/target/embedding), missing values, outliers, leakage in feature construction, feature stores conceptually | Build a feature pipeline as a scikit-learn `Pipeline` so preprocessing can't leak | 2 mediums | Why must scaling be fit on train only? |
| 171 | Model serving: pickling risks, model registry, versioning, input validation, batch vs real-time, drift monitoring, shadow deployment, rollback | Serve your best model behind FastAPI with input validation and version in the response | 2 mediums | How do you roll back a model, and how do you know you need to? |

### Week 24 · Days 172–180 — PyTorch

| Day | Topic | Build / artefact | DSA | Must be able to answer |
|---|---|---|---|---|
| 172 | Tensors: creation, dtypes, shapes, views vs copies, broadcasting, device movement, contiguity, memory layout | 20 tensor manipulation exercises without looking anything up | 2 mediums | Difference between `view` and `reshape`, and when the first one fails |
| 173 | Autograd: computational graph, `requires_grad`, `backward()`, `grad_fn`, `no_grad`, gradient accumulation, detaching | Compute gradients by hand for a small expression; verify with autograd | 2 mediums | What does `loss.backward()` actually build and traverse? |
| 174 | `nn.Module`: layers, parameters, `forward`, initialisation, `train()` vs `eval()` mode, parameter counting | An MLP from scratch as `nn.Module`; count parameters manually and verify | 2 mediums | Why does forgetting `model.eval()` change your outputs? |
| 175 | Loss functions: MSE, cross-entropy (and why it takes logits), BCE, ignore_index, class weights, numerical stability, `logsumexp` | Implement cross-entropy yourself; match PyTorch's output to 6 decimals | 2 mediums | Why does PyTorch's CrossEntropyLoss want logits, not softmax outputs? |
| 176 | Optimisers: SGD, momentum, Adam/AdamW, learning-rate schedules, warmup, gradient clipping, `zero_grad()` | Train the same model with 4 optimisers; plot convergence | 2 mediums | Why AdamW instead of Adam for transformers? |
| 177 | The training loop: batching, DataLoader, epochs, validation loop, checkpointing, reproducibility/seeding, mixed precision, common bugs | A complete, correct training loop written from a blank file, no template | 2 mediums | Write a training loop from memory and name the four most common bugs in it |
| 178 | CNNs (for architectural literacy): convolution, kernels, stride, padding, pooling, receptive field, why weight sharing works | Train a small CNN on MNIST/CIFAR to a reasonable accuracy | 2 mediums | Why does a CNN need far fewer parameters than an MLP for images? |
| 179 | Model serving with PyTorch: `torch.save`/`load`, `state_dict`, eval mode, TorchScript/ONNX, dynamic batching, GPU vs CPU inference cost | Serve the CNN behind FastAPI with request batching; measure throughput gain from batching | 2 mediums | How much throughput does batching buy you, and what does it cost in latency? |
| 180 | **Month review + ML project** | One end-to-end ML project: data → features → training → eval → served API → README with metrics | **Mock:** 2 DSA + ML fundamentals grilling | Explain overfitting, regularisation, and your metric choice using your own project's numbers |

### Month 6 checkpoint

- [ ] You did the maths by hand at least once per topic, not just in NumPy
- [ ] 5+ models trained with honest evaluation and no leakage
- [ ] A training loop written from scratch, from memory
- [ ] A served model with batching and measured throughput
- [ ] 180 DSA problems
- [ ] Interviews: you're passing first rounds; system design rounds are the current bottleneck (that's normal — Month 5 helps, Month 7 finishes it)

---

# MONTH 7 · DAYS 181–210
## Transformers from scratch → fine-tuning → inference optimisation

**Month goal:** this is the month that separates ₹30L from ₹50L. Almost nobody applying for AI roles can explain KV cache, continuous batching, or why their p99 is bad. If you can, you stop competing with the crowd.

**Month deliverables**

- A working transformer implemented from scratch (attention → full block → tiny LM that generates text)
- One real LoRA/QLoRA fine-tune with before/after evaluation
- An inference benchmark report: latency vs throughput vs batch size vs quantisation, with charts
- 210 cumulative DSA problems (timed medium sets from here)

### Week 25 · Days 181–187 — Attention, built up piece by piece

| Day | Topic | Build / artefact | DSA (timed) | Must be able to answer |
|---|---|---|---|---|
| 181 | Tokenisation internals: BPE training, merges, vocabulary size tradeoffs, special tokens, byte fallback, why vocab size affects both quality and speed | Train a small BPE tokeniser on your own corpus; inspect the merge list | 2 timed mediums | Why does a larger vocabulary shorten sequences but enlarge the output layer? |
| 182 | Token embeddings: embedding matrix as a lookup, dimensionality, weight tying with the output head, parameter cost | Compute the embedding parameter count for vocab 50k × d 4096; implement the lookup | 2 timed mediums | How many parameters does the embedding layer of a 7B model consume? |
| 183 | Positional information: why attention is permutation-invariant, sinusoidal encoding, learned positions, RoPE, ALiBi, context extension | Implement sinusoidal encoding and RoPE; visualise both | 2 timed mediums | Why can RoPE extrapolate to longer contexts better than learned embeddings? |
| 184 | Attention intuition: the retrieval analogy, why we need it over RNNs, soft alignment, what attention weights do and don't tell you | Implement single-head attention in NumPy on a toy sequence; inspect the weight matrix | 2 timed mediums | Explain attention to a backend engineer in 60 seconds without maths |
| 185 | Q, K, V: the three projections, what each represents, learned parameters, why three and not one, self vs cross attention | Implement the Q/K/V projections; verify shapes at every step | 2 timed mediums | What would break if Q and K were the same matrix? |
| 186 | Scaled dot-product attention: the formula, why divide by √d_k, softmax saturation, causal masking, padding masks, attention as O(n²) | Implement scaled dot-product attention with a causal mask from scratch | 2 timed mediums | Why the √d_k scaling, and what happens numerically without it? |
| 187 | Multi-head attention: splitting into heads, per-head subspaces, concatenation and output projection, head count vs head dim, MQA and GQA | Implement multi-head attention; verify output equals the single-head case when heads=1 | 2 timed mediums | Why multiple heads instead of one big head? And what do MQA/GQA save? |

### Week 26 · Days 188–194 — The full transformer

| Day | Topic | Build / artefact | DSA (timed) | Must be able to answer |
|---|---|---|---|---|
| 188 | Feed-forward network: position-wise MLP, expansion ratio (~4×), activations (ReLU/GELU/SwiGLU), where most parameters actually live | Implement the FFN; compute what fraction of total parameters it holds | 2 timed mediums | Which holds more parameters — attention or FFN? By roughly how much? |
| 189 | Residual connections: vanishing gradients, identity path, gradient flow, pre-norm vs post-norm, depth stability | Train a deep net with and without residuals; plot the gradient norms | 2 timed mediums | Why can't you train a 40-layer network without residual connections? |
| 190 | Normalisation: LayerNorm vs BatchNorm vs RMSNorm, why BatchNorm fails for sequences, pre-norm's stability advantage, learnable scale/shift | Implement LayerNorm and RMSNorm; match PyTorch numerically | 2 timed mediums | Why LayerNorm and not BatchNorm in transformers? |
| 191 | Encoder stack: bidirectional attention, BERT-style objectives (MLM), use cases (classification, embedding, reranking) | Use an encoder model as a reranker; connect it to your Month-4 reranking work | 2 timed mediums | Why is an encoder better for reranking and useless for generation? |
| 192 | Decoder stack: causal masking, autoregressive objective, GPT-style, why decoder-only won, teacher forcing during training | Implement a decoder block; verify the causal mask prevents future leakage | 2 timed mediums | Prove your causal mask works — how do you test it? |
| 193 | Autoregressive generation: prefill vs decode, sampling loop, EOS handling, stop sequences, beam search vs sampling, speculative decoding intuition | Implement a generation loop from scratch, including stop conditions | 2 timed mediums | Why is generating 1000 tokens ~1000× more sequential work than reading 1000? |
| 194 | **Assemble the whole thing** — full transformer LM: embeddings + positions + N blocks + norm + LM head; train on a small corpus until it produces plausible text | Working tiny LM in one file, trained, generating text. **This goes on your resume and in your GitHub.** | 2 timed mediums | Walk through your implementation from token IDs to sampled next token |

### Week 27 · Days 195–201 — Training and fine-tuning

| Day | Topic | Build / artefact | DSA (timed) | Must be able to answer |
|---|---|---|---|---|
| 195 | Pretraining: objectives, data scale and curation, compute cost, scaling laws (Chinchilla), tokens-per-parameter, emergent behaviour claims | Compute the rough FLOPs and dollar cost to pretrain a 7B model; write the number down | 2 timed mediums | Why doesn't your company pretrain its own model? Give the numbers |
| 196 | Instruction tuning + alignment: SFT, preference data, RLHF, DPO at a high level, reward models, why instruction-tuned ≠ more knowledgeable | Compare a base model and its instruct variant on 10 identical prompts; document the difference | 2 timed mediums | Does instruction tuning add knowledge? What does it actually change? |
| 197 | Full fine-tuning: when it's justified, dataset size requirements, catastrophic forgetting, memory requirements (params + grads + optimiser states + activations) | Compute the GPU memory for full fine-tuning a 7B model in fp16 with Adam; show the arithmetic | 2 timed mediums | Why does full fine-tuning a 7B model need far more than 14GB? |
| 198 | LoRA: low-rank decomposition, rank and alpha, which modules to target, parameter savings, adapter merging, serving many adapters | LoRA fine-tune a small model on a real task; report the trainable parameter percentage | 2 timed mediums | Explain LoRA's maths and why it works despite the rank constraint |
| 199 | QLoRA: 4-bit NF4 quantisation, double quantisation, paged optimisers, quality tradeoff, consumer-GPU/Colab feasibility | QLoRA the same task; compare quality, memory, and time against LoRA | 2 timed mediums | How does QLoRA fit a 7B fine-tune in under 16GB? |
| 200 | PEFT landscape: prefix tuning, prompt tuning, IA³, adapter composition, when to fine-tune vs RAG vs prompt engineering (the decision tree) | Write the decision tree: prompting → RAG → fine-tuning, with cost and latency per branch | 2 timed mediums | Client wants the model to "know our data." Prompting, RAG, or fine-tuning? Defend it |
| 201 | Dataset construction: instruction format, quality over quantity, deduplication, contamination, synthetic data generation, train/eval separation, human review | Build a 500-example instruction dataset with a documented quality process | 2 timed mediums | 500 great examples or 50,000 noisy ones? Justify with what you observed |

### Week 28 · Days 202–210 — Inference: where the ₹50L questions live

| Day | Topic | Build / artefact | DSA (timed) | Must be able to answer |
|---|---|---|---|---|
| 202 | Quantisation: fp32/fp16/bf16/int8/int4, PTQ vs QAT, GPTQ/AWQ/GGUF, per-channel vs per-tensor, quality degradation measurement | Run the same model at 3 precisions; measure latency, memory, and quality on your eval set; chart it | 2 timed mediums | What do you actually lose going from fp16 to int4, and how do you measure it? |
| 203 | GPU memory model: weights + KV cache + activations + fragmentation, VRAM budgeting, how many concurrent requests fit, OOM causes | Compute max concurrent requests for a 7B model on a 24GB GPU at 4k context — show the arithmetic | 2 timed mediums | You have an A10G 24GB. How many concurrent 4k-context requests fit? |
| 204 | KV cache: what it caches and why, size formula (2 × layers × heads × head_dim × seq_len × batch × bytes), memory growth with context, MQA/GQA savings, paged attention | Compute KV cache size for your target config; explain the paged-attention improvement | 2 timed mediums | Derive the KV cache size formula and explain why long context is expensive |
| 205 | Prefill: compute-bound, parallel across the prompt, TTFT drivers, chunked prefill, prompt caching, why long prompts hurt TTFT | Measure TTFT for prompts of 100 / 1k / 8k tokens; plot the curve | 2 timed mediums | Why is prefill compute-bound and decode memory-bandwidth-bound? |
| 206 | Decode: sequential, memory-bandwidth-bound, tokens/sec ceiling, arithmetic intensity, why batching helps decode enormously | Measure tokens/sec at batch 1 / 4 / 16 / 64; plot throughput and per-request latency together | 2 timed mediums | Why does batch size 32 barely slow down each individual request during decode? |
| 207 | Static batching: batch formation, padding waste, tail latency from the slowest sequence, timeout-based batching, batch size vs latency SLA | Implement static batching with a max wait window; measure the padding waste | 2 timed mediums | What's wrong with static batching when sequence lengths vary 10×? |
| 208 | Continuous batching: iteration-level scheduling, admitting new requests mid-generation, evicting finished ones, vLLM/TGI approach, throughput gains | Benchmark a continuous-batching server vs your naive server; report the multiple | 2 timed mediums | Explain continuous batching and quantify what it buys you |
| 209 | Latency vs throughput: the fundamental tradeoff, SLA-driven capacity planning, p50 vs p99, queueing theory intuition, autoscaling on queue depth, speculative decoding | Capacity plan: "p95 TTFT under 800ms at 500 rps" — how many GPUs, what config, what cost | 2 timed mediums | Design serving for p95 TTFT < 800ms at 500 rps. Show the arithmetic |
| 210 | **Cost optimisation + month review** | Full inference report: cost per 1M tokens across self-hosted vs API, break-even analysis, quantisation quality/cost curve, batching gains. **Publish this — it's a portfolio piece.** | **Mock:** 2 timed DSA + LLM inference grilling | When is self-hosting cheaper than an API? Give the break-even volume |

### Month 7 checkpoint

- [ ] Transformer implemented from scratch and it generates text
- [ ] One LoRA and one QLoRA fine-tune with measured before/after
- [ ] Inference benchmark report published with charts
- [ ] You can derive KV cache size and explain prefill vs decode on a whiteboard
- [ ] 210 DSA problems, timed
- [ ] Applications: 15–20/week, targeting ₹30–50L

---

# MONTH 8 · DAYS 211–240
## Agents → MCP → AI security → capstone platform → interview intensive

**Month goal:** finish the capstone, and convert. From here, interviewing is half the job.

**Month deliverables**

- **Project 4: Production AI Platform** — the capstone
- 240 cumulative DSA problems; 20–30 mock interviews total
- Offers in flight

### Week 29 · Days 211–217 — Agents

| Day | Topic | Build / artefact | DSA (timed) | Must be able to answer |
|---|---|---|---|---|
| 211 | Tool calling as the agent primitive: schemas, dispatch, result formatting, error feedback loops, tool selection failure modes, tool count limits | Agent with 6 tools; log tool-selection accuracy over 50 tasks | 2 timed mediums | Your agent picks the wrong tool 20% of the time. Five fixes, ranked by cost |
| 212 | Agent architectures: ReAct, plan-and-execute, reflection, router/supervisor, multi-agent vs single-agent, when an agent is overkill | Implement ReAct and plan-execute for the same task; compare cost, latency, and success rate | 2 timed mediums | When is a deterministic pipeline strictly better than an agent? |
| 213 | Agent state: conversation state vs task state, checkpointing, resumability after crash, state store design, concurrent agent runs | Durable agent state in Postgres; kill the process mid-run and resume it | 2 timed mediums | Your agent dies on step 7 of 12. What happens when the user retries? |
| 214 | Memory: short-term (context) vs long-term (retrieval), summarisation/compaction strategies, entity memory, what to forget, memory poisoning | Memory layer with summarisation triggered by token budget; measure quality retention | 2 timed mediums | A conversation exceeds the context window. What exactly do you drop? |
| 215 | Agent loops + control: max iterations, cost ceilings, loop detection, progress checks, timeouts, cancellation, budget per run | Hard limits: max steps, max cost, max wall-clock — enforced and observable | 2 timed mediums | How do you stop an agent burning ₹4000 on an infinite loop? |
| 216 | Planning + decomposition: task decomposition, DAG execution, parallel tool calls, dependency handling, replanning on failure, verification steps | Plan-execute agent with parallel independent steps and a replan-on-failure path | 2 timed mediums | Which steps can run in parallel, and how does the agent know? |
| 217 | Human-in-the-loop: approval gates, risk-tiered actions, dry runs and diffs, audit trails, undo paths, confidence-based escalation | Approval gate on destructive tools with a diff preview and an audit log | 2 timed mediums | Which agent actions require human approval, and how do you decide the tier? |

### Week 30 · Days 218–224 — MCP (Model Context Protocol)

| Day | Topic | Build / artefact | DSA (timed) | Must be able to answer |
|---|---|---|---|---|
| 218 | MCP architecture: the problem it solves (N×M integrations), hosts/clients/servers, JSON-RPC transport, stdio vs HTTP, capability negotiation, lifecycle | Architecture note comparing MCP against bespoke tool integrations | 2 timed mediums | What problem does MCP solve that a plain function-calling API does not? |
| 219 | MCP tools: definitions, input schemas, annotations (read-only/destructive), error handling, tool discovery, versioning | An MCP server exposing 3 tools with proper schemas and annotations | 2 timed mediums | How does a client know a tool is destructive before calling it? |
| 220 | MCP resources: URIs, resource listing and reading, subscriptions, templates, resources vs tools (the distinction that matters) | Expose your document corpus as MCP resources | 2 timed mediums | When do you model something as a resource and not a tool? |
| 221 | MCP prompts + sampling: reusable prompt templates, arguments, server-initiated sampling, elicitation, roots | Prompt templates exposed over MCP with arguments | 2 timed mediums | Why would a server ask the client to run a completion? |
| 222 | MCP security: authorisation, OAuth for remote servers, token handling, confused-deputy risk, tool poisoning, sandboxing, least privilege per tool | Auth on your MCP server + a per-tool permission model | 2 timed mediums | An MCP server tool description contains injected instructions. What defends you? |
| 223 | MCP clients: connecting to servers, tool aggregation, name collisions, latency budgets, failure isolation across servers | A client that aggregates 2 MCP servers with namespacing and per-server timeouts | 2 timed mediums | One MCP server hangs. What happens to the other tools? |
| 224 | **MCP integration in your platform** | Your platform exposes RAG search + document tools over MCP, and consumes at least one external MCP server | 2 timed mediums | Demo your MCP integration end to end |

### Week 31 · Days 225–231 — AI security

| Day | Topic | Build / artefact | DSA (timed) | Must be able to answer |
|---|---|---|---|---|
| 225 | Prompt injection: direct vs indirect, why it's unsolved, instruction/data separation, spotlighting, dual-LLM patterns, output constraints, defence in depth | Red-team your own RAG with 20 injection payloads; log the success rate; then mitigate and re-measure | 2 timed mediums | Why can't a system prompt saying "ignore injected instructions" work? |
| 226 | RAG poisoning + data-layer attacks: malicious documents, retrieval manipulation, embedding attacks, ingestion trust boundaries, provenance | Add ingestion trust tiers + provenance metadata; downweight untrusted sources in ranking | 2 timed mediums | An attacker uploads a document designed to hijack answers. Where do you stop it? |
| 227 | Tool + action security: least privilege per tool, parameter validation, allow-lists, SSRF via tools, command injection, filesystem/network scoping, blast radius | Threat model your tool layer; implement allow-lists and parameter validation | 2 timed mediums | Your agent has a `fetch_url` tool. List the attacks and your controls |
| 228 | Sandboxing + isolation: containers/gVisor/microVMs, network egress control, resource limits, timeouts, ephemeral execution, tenant isolation | Sandboxed code-execution tool: no network, capped CPU/memory, hard timeout | 2 timed mediums | How do you run model-generated code without risking your infrastructure? |
| 229 | Authentication for AI systems: API keys vs OAuth, service identity, key rotation, per-tenant credentials, credential passthrough risks, secret leakage into prompts/logs | Prompt/log redaction + per-tenant credential isolation; test that secrets never hit logs | 2 timed mediums | A user's API key ends up in a prompt. What prevents it reaching your logs? |
| 230 | Authorisation in AI systems: permission-aware retrieval, ACL enforcement at query time, tool permissions per role, delegated authority, the "AI as a confused deputy" problem | Prove permission-aware retrieval with a test suite; role-gated tools | 2 timed mediums | How do you guarantee an LLM never surfaces a document the user can't read? |
| 231 | Audit + compliance: what to log, PII handling, retention, prompt/response storage decisions, reproducibility of an answer, incident response for AI systems | Audit log capturing prompt version, retrieved chunk IDs, model version, tool calls, cost, user — enough to reproduce any answer | 2 timed mediums | A customer says your AI leaked data. How do you investigate? |

### Week 32 · Days 232–240 — Capstone + conversion

**Architecture (Project 4)**

```
                        CLIENT (web / API / MCP client)
                                    ↓
                            API GATEWAY (ALB + WAF)
                                    ↓
                     AUTH / RBAC / TENANT ISOLATION / QUOTAS
                                    ↓
                            AI ORCHESTRATOR
                    ┌───────────────┼───────────────┐
                    ↓               ↓               ↓
                  RAG            AGENTS           TOOLS
              (hybrid +        (plan-execute,   (MCP server
               rerank)          memory, HITL)    + client)
                    ↓               ↓               ↓
        PostgreSQL + pgvector   Redis (state,   MCP registry
        (docs, chunks, ACLs,     cache, locks,   + permissions
         audit, outbox)          rate limits)
                    └───────────────┼───────────────┘
                                    ↓
                    KAFKA (ingestion, async jobs, events)
                                    ↓
                    LLM ROUTER (cost/quality/latency policy)
                        ┌───────────┴───────────┐
                        ↓                       ↓
                   Model A (small)         Model B (large)
                        └───────────┬───────────┘
                                    ↓
                     EVALUATION (online + offline, CI-gated)
                                    ↓
                OBSERVABILITY (traces, cost/tenant, quality metrics)
                                    ↓
                    Docker · ECS/EKS · Terraform · AWS
```

| Day | Focus | Build / artefact | DSA (timed) | Must be able to answer |
|---|---|---|---|---|
| 232 | Architecture + ADRs: component boundaries, data model, sync/async split, written architecture decision records | Architecture doc + diagram + 6 ADRs each with rejected alternatives | 2 timed mediums | Why this architecture? What did you reject and why? |
| 233 | Multi-tenancy: shared-schema vs schema-per-tenant vs DB-per-tenant, tenant context propagation, noisy-neighbour control, per-tenant quotas and cost attribution | Tenant isolation implemented + a test that proves cross-tenant reads fail | 2 timed mediums | How do you stop one tenant degrading everyone else? |
| 234 | Auth/RBAC/quotas: OAuth or JWT, roles, permission-aware retrieval, token budgets per tenant, 429 semantics, usage metering | Full auth + RBAC + per-tenant token budgets with metering | 2 timed mediums | A tenant hits their monthly token budget mid-conversation. What happens? |
| 235 | RAG integration: hybrid retrieval + reranking + citations + abstention + eval gate, all inside the platform | Production RAG path wired in, eval-gated in CI | 2 timed mediums | Show your retrieval metrics and where the remaining failures come from |
| 236 | Agents + tools: orchestrator, plan-execute, memory, HITL gates, cost ceilings, tracing per step | Agent path with limits, approvals, and full step-level tracing | 2 timed mediums | Trace one agent run end to end and account for every rupee |
| 237 | MCP: server exposing platform capabilities + client consuming external servers, with permissions and namespacing | MCP in and out, secured | 2 timed mediums | Why expose your platform over MCP at all? |
| 238 | LLM router + resilience: policy-based routing, fallback chain, circuit breakers, semantic cache, degraded modes, cost/quality dashboard | Router with fallback; kill the primary provider under load and stay up | 2 timed mediums | Your primary provider is down for 20 minutes. Narrate the user experience |
| 239 | Evaluation + observability: offline golden sets, online quality signals, CI gates, traces, cost per tenant, quality dashboards, alerting | Dashboards + CI eval gate + 5 real alerts | 2 timed mediums | How do you detect a quality regression before customers do? |
| 240 | **Final: demo, docs, portfolio** | Load test the platform and record the numbers · 5-min recorded demo · architecture document · README with metrics · resume final · LinkedIn post · portfolio page linking all 4 projects | **Mock:** full loop simulation — DSA + LLD + system design + AI depth | Present the entire platform in 5 minutes to a staff engineer |

### Month 8 checkpoint

- [ ] Capstone deployed, load-tested, documented, demoed on video
- [ ] 240 DSA problems; 20–30 mocks done
- [ ] You red-teamed your own system and fixed what you found
- [ ] Portfolio page with 4 projects, each with numbers
- [ ] Interviews in progress at Tier A and Tier B; offers in flight

---

# PART II · PROJECTS

Four repositories. Not fifteen. Depth is the signal; quantity is noise.

## General rules for all four

**Every repo must contain**

```
README.md              # see template below — this is what recruiters read
docs/
  architecture.md      # diagram + component responsibilities
  decisions/           # ADR-001.md, ADR-002.md … one per real decision
  failure-modes.md     # what breaks, how you detect it, what you do
  runbook.md           # how to deploy, how to debug, how to roll back
src/
tests/                 # unit + integration; at least one that proves isolation
Dockerfile
docker-compose.yml
Makefile               # make up / make test / make load-test / make deploy
.github/workflows/ci.yml
```

**Every repo README must have, in this order**

1. One-sentence description of what it does and for whom
2. Architecture diagram (Mermaid or a committed PNG)
3. **Numbers** — p50/p95 latency, throughput, cost per operation, eval scores
4. Tech stack with a one-line justification each
5. What's interesting about it engineering-wise (the 3 hardest problems and your solutions)
6. Failure modes handled
7. How to run it locally (must actually work from a clean clone)
8. Link to a live demo and to a 3-minute Loom

### README template

````markdown
# <Project Name>
<One sentence: what it does, for whom, and the hard part.>

**Live:** <url> · **Demo (3 min):** <loom> · **Architecture:** [docs/architecture.md](docs/architecture.md)

## Numbers
| Metric | Value | How measured |
|---|---|---|
| p50 / p95 latency | 180ms / 640ms | k6, 200 rps, 10 min |
| Throughput | 340 rps sustained | 2× t3.medium, 1 worker each |
| Cost per 1k queries | ₹— | measured, not estimated |
| Retrieval recall@5 | 0.87 | 50-question golden set |
| Answer faithfulness | 0.91 | LLM-judge + 20 human-checked |

## Architecture
<diagram>

## Why these choices
- **Postgres + pgvector over a dedicated vector DB** — <reason, with the tradeoff you accepted>
- **Kafka over Celery/SQS** — <reason>
- …

## The three hardest problems
1. **<Problem>** — <what broke, how you diagnosed it, what you changed, the measured result>
2. …
3. …

## Failure modes handled
| Failure | Detection | Behaviour |
|---|---|---|
| Embedding provider 429s | error-rate alarm | backoff + queue, ingestion delayed not lost |
| … | | |

## Run locally
```bash
make up && make test
```
````

> The "three hardest problems" section is what interviewers actually read. Write it as debugging stories with measurements — not as feature lists.

---

## 10. Project 1 · Production Backend Service
**Months 1–2 · Days 29–60**

### What it is

A multi-tenant document management API — the boring, correct backend that Project 2 will later put AI on top of. The point of this project is **not novelty**. It is to prove you can build something that survives contact with production.

### Scope

- Users, organisations (tenants), documents, folders, sharing
- Full auth: register, login, JWT access + refresh with rotation, revocation
- RBAC: owner / editor / viewer, enforced at the query layer
- Document upload with metadata, versioning, soft delete
- Search (Postgres full-text at this stage — vectors come in Project 2)
- Background jobs: thumbnail/text extraction via a worker
- Rate limiting per tenant and per API key
- Audit log of every mutation

### Must include (the checklist that makes it "production")

| Area | Requirement |
|---|---|
| API | REST with OpenAPI, cursor pagination, RFC-7807 errors, versioned routes, idempotency keys on POST |
| Auth | JWT access + refresh, rotation, Redis revocation list, argon2 password hashing |
| Authz | RBAC + tenant isolation with a test proving cross-tenant reads fail |
| Data | Postgres with migrations (Alembic), proper indexes justified by `EXPLAIN`, constraints and FKs, no ORM N+1s |
| Cache | Redis cache-aside on hot reads + stampede protection |
| Async | Worker process, retry with backoff, DLQ table |
| Reliability | Timeouts everywhere, connection pooling tuned, graceful shutdown on SIGTERM |
| Observability | Structured JSON logs with request IDs, `/health` + `/ready`, Prometheus-style metrics |
| Testing | Unit + integration, ≥70% coverage on business logic, one load test |
| Ops | Dockerfile (multi-stage, non-root), docker-compose, GitHub Actions CI, deployed on AWS |

### Repo structure

```
prod-backend/
├── src/app/
│   ├── main.py                 # app factory, middleware, lifespan
│   ├── config.py               # pydantic-settings, env-driven
│   ├── api/v1/
│   │   ├── routes/             # auth.py, documents.py, orgs.py, search.py
│   │   ├── deps.py             # DI: db session, current_user, tenant context
│   │   └── errors.py           # RFC 7807 handlers
│   ├── domain/                 # entities + business rules, NO framework imports
│   │   ├── models.py
│   │   ├── services.py
│   │   └── policies.py         # RBAC decisions live here, testable in isolation
│   ├── infra/
│   │   ├── db/                 # engine, session, repositories, migrations/
│   │   ├── cache/              # redis client, cache-aside helpers, locks
│   │   ├── storage/            # S3 / local adapter behind one protocol
│   │   └── queue/              # producer + worker
│   ├── middleware/             # request_id, rate_limit, logging, timing
│   └── observability/          # logging config, metrics, tracing
├── tests/
│   ├── unit/                   # policies, services — fast, no I/O
│   ├── integration/            # real Postgres + Redis via testcontainers
│   └── load/                   # k6 or locust scripts
├── docs/                       # architecture, ADRs, failure-modes, runbook
├── Dockerfile · docker-compose.yml · Makefile · .github/workflows/ci.yml
```

### Deliberate breakage exercises (do these — the stories are the point)

1. Set the DB pool to 2 and load test → observe queueing → tune → document the formula
2. Cause a deadlock with two concurrent updates in opposite order → fix by lock ordering
3. Expire a hot cache key under load → observe the stampede → fix with single-flight
4. `kill -9` the worker mid-job → prove the job is retried, not lost
5. Send 10k requests from one tenant → prove other tenants are unaffected

### Resume bullets this project earns you

- Built a multi-tenant document API (FastAPI/Postgres/Redis) sustaining **X rps at p95 Y ms**, with per-tenant rate limiting and RBAC enforced at the query layer
- Cut p95 latency **Z%** by adding cache-aside with single-flight stampede protection after load-testing revealed a thundering-herd failure
- Designed retry + DLQ semantics for a background worker; verified no job loss under forced process kills

---

## 11. Project 2 · Enterprise RAG Service
**Months 3–4 · Days 82–97**

### What it is

A document Q&A service with citations, built to survive real corpora — messy PDFs, tables, scanned pages, permissions, and 200-page documents. Built **without a framework first**, so you can explain every line.

### Scope

- Ingestion: PDF, DOCX, HTML, Markdown, plus OCR fallback for scans
- Structure-aware chunking with heading context and lineage
- Resumable, batched embedding pipeline
- Hybrid retrieval: pgvector dense + Postgres FTS/BM25 sparse, fused with RRF
- Cross-encoder reranking (top-50 → top-8)
- Permission-aware retrieval (ACLs enforced inside the query)
- Prompt assembly with token budgeting, deliberate ordering, abstention instruction
- Streamed answers with sentence-level citations
- Offline eval: 50-question golden set, recall@k, MRR, faithfulness, CI gate

### Must include

| Area | Requirement |
|---|---|
| Ingestion | Idempotent (content-hash dedup), 4+ formats, OCR fallback, per-doc failure isolation |
| Chunking | Configurable strategy, lineage stored, overlap tuned with measured evidence |
| Embedding | Batched, rate-limit-aware, checkpointed/resumable, re-embed migration path |
| Retrieval | Hybrid + RRF + rerank + MMR dedup + metadata filters + ACL filters |
| Generation | Token budget enforcement, citation markers, abstention when unsupported |
| Eval | Golden set in the repo, automated run, CI fails on regression |
| Security | Injection tests from retrieved content; provenance/trust tiers |
| Observability | Per-stage latency breakdown, cost per query, retrieval hit/miss logging |

### Repo structure

```
enterprise-rag/
├── src/rag/
│   ├── ingestion/
│   │   ├── parsers/            # pdf.py, docx.py, html.py, ocr.py
│   │   ├── pipeline.py         # orchestration, idempotency, dedup
│   │   └── trust.py            # source trust tiers, provenance
│   ├── chunking/
│   │   ├── strategies.py       # fixed, recursive, structural, semantic
│   │   └── lineage.py
│   ├── embedding/
│   │   ├── client.py           # provider-agnostic
│   │   ├── batcher.py          # batching + rate limits + retries
│   │   └── checkpoint.py       # resumability
│   ├── retrieval/
│   │   ├── dense.py            # pgvector
│   │   ├── sparse.py           # tsvector / BM25
│   │   ├── fusion.py           # RRF, weighted fusion
│   │   ├── rerank.py           # cross-encoder
│   │   └── acl.py              # permission-aware filtering
│   ├── generation/
│   │   ├── assembler.py        # context ordering + token budget
│   │   ├── citations.py        # span attribution + verification
│   │   └── stream.py           # SSE
│   ├── eval/
│   │   ├── golden_set.jsonl    # 50 questions, committed
│   │   ├── retrieval_metrics.py
│   │   ├── answer_metrics.py
│   │   └── run.py              # invoked by CI
│   └── api/                    # FastAPI routes
├── notebooks/                  # chunking + retrieval experiments (keep them, they're evidence)
├── docs/ · tests/ · Dockerfile · docker-compose.yml · Makefile
```

### Experiments to run and publish in the README

| Experiment | What you report |
|---|---|
| 3 chunking strategies × same golden set | recall@5 table + which failed and why |
| Dense only vs sparse only vs hybrid+RRF | metric lift + 10 queries where each wins |
| With vs without reranking | precision gain vs added latency (ms) |
| Embedding dim 1536 vs PCA-256 | quality loss vs latency and storage gain |
| Context ordering: relevant-first vs last | measured accuracy difference |

### Resume bullets

- Built a hybrid-retrieval RAG service (pgvector + BM25 + RRF + cross-encoder reranking) improving recall@5 from **0.62 → 0.87** on a 50-question golden set
- Implemented permission-aware retrieval enforcing document ACLs inside the vector query; verified with an isolation test suite
- Added CI-gated retrieval evaluation, catching **N** quality regressions before deploy
- Cut cost per query **X%** via context budgeting and small-model routing with escalation on validation failure

---

## 12. Project 3 · Distributed AI Document Platform
**Months 4–5 · Days 98–120**

### What it is

Project 2's ingestion pipeline, rebuilt as a distributed event-driven system that can process 1M documents/day and survive failures. This is the project that gets you distributed-systems interviews.

### Architecture

```
   Upload API ──▶ S3 ──▶ Kafka: documents.uploaded
                                    │
        ┌───────────────────────────┼───────────────────────────┐
        ▼                           ▼                           ▼
   parser-worker              ocr-worker                metadata-worker
        │                           │                           │
        └────────▶ Kafka: documents.parsed ◀────────────────────┘
                            │
                   chunker-worker ──▶ Kafka: chunks.created
                            │
                   embedder-worker (batched) ──▶ Postgres + pgvector
                            │
                   Kafka: documents.indexed ──▶ notification-worker
                            │
   All workers ──▶ retry topics (delayed) ──▶ DLQ topic ──▶ replay CLI
```

### Must include

| Area | Requirement |
|---|---|
| Kafka | Multiple topics, deliberate partition-key choice, consumer groups, manual commits |
| Idempotency | Every consumer idempotent; full-topic replay produces identical DB state (prove with a diff) |
| Retries | Classified transient vs permanent, exponential backoff + jitter, retry topics with delays, bounded budget |
| DLQ | Rich records (payload, error, attempt count, trace ID, timestamp) + a selective replay CLI |
| Outbox | Transactional outbox for DB→Kafka publishing; no dual-write bug |
| Backpressure | Lag-based autoscaling or shedding; documented breaking point |
| Observability | Consumer lag dashboard, per-stage throughput, end-to-end document latency histogram, DLQ alerting |
| Chaos | Documented results of killing each worker mid-processing |

### Repo structure

```
distributed-ai-platform/
├── services/
│   ├── upload-api/
│   ├── parser-worker/
│   ├── ocr-worker/
│   ├── chunker-worker/
│   ├── embedder-worker/
│   └── notification-worker/
├── libs/common/
│   ├── kafka/          # producer, consumer base class, serialization, headers
│   ├── idempotency/    # dedup store with TTL
│   ├── retry/          # classifier, backoff, retry-topic router
│   ├── dlq/            # writer + replay CLI
│   ├── outbox/         # table + relay
│   └── observability/  # tracing across topic hops (correlation IDs in headers)
├── infra/
│   ├── terraform/
│   └── k8s/ or ecs/
├── load/               # 100k-document generator
├── chaos/              # scripts: kill-consumer.sh, partition-broker.sh, fill-disk.sh
├── docs/               # architecture, ADRs, failure-modes (the centrepiece), runbook
```

### Chaos experiments (each one is an interview story)

| Experiment | What you must be able to state |
|---|---|
| Kill a consumer mid-batch before commit | exact number of duplicates, and why idempotency absorbed them |
| Scale consumers beyond partition count | what the extra consumers did (nothing) and why |
| Make the embedding provider return 429 for 5 min | lag growth curve, recovery time, zero loss |
| Poison message (malformed PDF) | attempts before DLQ, DLQ record contents, replay result |
| Kill the outbox relay mid-publish | proof of no loss and no duplicate-visible-effect |
| Push 100k docs at once | throughput ceiling, which stage saturated first, and what you'd scale |

### Resume bullets

- Built an event-driven document pipeline (Kafka + Python workers + Postgres/pgvector) processing **N docs/hour** with idempotent consumers, delayed retry topics, and DLQ replay tooling
- Achieved zero data loss under forced consumer kills and a 5-minute provider outage; verified by full-topic replay producing byte-identical database state
- Implemented the transactional outbox pattern to eliminate a dual-write inconsistency between Postgres and Kafka
- Reduced end-to-end p95 ingestion latency **X%** by identifying the embedding stage as the bottleneck and adding adaptive batching

---

## 13. Project 4 · Production AI Platform (capstone)
**Months 7–8 · Days 232–240 (design from Day 211)**

### What it is

The one you lead with. A multi-tenant AI platform: RAG + agents + MCP + model routing + evaluation + security + observability, deployed on AWS. It absorbs Projects 1–3 as components rather than replacing them.

### Scope by subsystem

| Subsystem | Requirements |
|---|---|
| Gateway | ALB + WAF, TLS, request IDs, per-tenant rate limits, quota enforcement with 429 + Retry-After |
| Identity | OAuth2/JWT, service accounts, API keys with scopes, key rotation |
| Tenancy | Shared schema + tenant column + enforced query-layer isolation; per-tenant cost attribution and token budgets |
| Orchestrator | Route a request to RAG path, agent path, or direct completion by policy |
| RAG | Everything from Project 2, plus permission-aware retrieval and abstention |
| Agents | Plan-execute + ReAct, durable state, memory with compaction, HITL approval gates, step/cost/time ceilings |
| Tools + MCP | MCP server exposing platform capabilities; MCP client consuming external servers; per-tool permissions, namespacing, timeouts |
| LLM router | Policy-based (cost/quality/latency), fallback chain, circuit breakers, semantic cache, degraded mode |
| Async | Kafka for ingestion and long jobs (from Project 3) |
| Evaluation | Offline golden sets per capability, CI gate, online signals (abstention rate, citation coverage, thumbs, retry rate) |
| Security | Injection defences, ingestion trust tiers, sandboxed execution, prompt/log redaction, audit trail sufficient to reproduce any answer |
| Observability | Distributed traces across LLM/tool/retrieval spans, cost per tenant per feature, quality dashboards, 5+ real alerts |
| Infra | Docker, ECS/EKS, Terraform, multi-AZ, secrets in Secrets Manager, CI/CD |

### Repo structure

```
ai-platform/
├── services/
│   ├── gateway/
│   ├── orchestrator/           # the interesting service
│   │   ├── router/             # policy engine: which model, which path
│   │   ├── rag/                # imports the rag lib
│   │   ├── agents/             # planner, executor, memory, hitl
│   │   ├── tools/              # registry, sandbox, permissions
│   │   └── mcp/                # server + client
│   ├── ingestion/              # from Project 3
│   └── eval-runner/
├── libs/
│   ├── llm/                    # provider abstraction, retries, circuit breaker, cost accounting
│   ├── rag/                    # from Project 2
│   ├── tenancy/                # context propagation, quotas, metering
│   ├── security/               # redaction, injection filters, trust tiers
│   └── observability/
├── evals/
│   ├── rag/ · agents/ · safety/     # golden sets + judges
│   └── ci_gate.py
├── infra/terraform/
├── docs/
│   ├── architecture.md
│   ├── decisions/              # 8–12 ADRs
│   ├── threat-model.md
│   ├── failure-modes.md
│   ├── slos.md                 # SLIs, SLOs, error budgets
│   └── runbook.md
└── load/ · chaos/
```

### The numbers to publish

| Metric | Target to measure and report |
|---|---|
| p50 / p95 / p99 end-to-end latency | per path (RAG vs agent) |
| TTFT | streaming, per path |
| Sustained throughput | rps at which p95 breaches SLO |
| Cost per query | per path, per tenant tier |
| Cost saved by routing + semantic cache | % vs always-large-model |
| Retrieval recall@5 / MRR | on the golden set |
| Faithfulness / abstention rate | offline + online |
| Injection attack success rate | before vs after mitigations |
| Recovery time | on primary provider failure |

### The 5-minute demo script (rehearse this until it's boring)

1. **0:00–0:30** — the problem and who it's for
2. **0:30–1:15** — architecture diagram, three sentences per layer
3. **1:15–2:15** — live: ask a question, show streamed answer with citations, show the trace with cost and latency per span
4. **2:15–3:00** — live: an agent task with a human approval gate and a step-level trace
5. **3:00–3:45** — break it: kill the primary LLM provider, show the fallback and the degraded mode
6. **3:45–4:30** — attack it: a prompt-injected document, show the defence and the audit record
7. **4:30–5:00** — the numbers table, and the one thing you'd do next with more time

### Resume bullets

- Designed and shipped a multi-tenant AI platform (RAG + agents + MCP + model routing) on AWS serving **N rps** at p95 **X ms**, with per-tenant token budgets and cost attribution
- Reduced LLM cost **X%** via policy-based model routing, semantic caching, and context budgeting, with CI-gated evals ensuring no quality regression
- Built agent execution with durable state, cost/step ceilings, and human-in-the-loop approval gates for destructive tools
- Reduced prompt-injection success rate from **X% → Y%** through instruction/data separation, ingestion trust tiers, and output constraints, measured with a 20-payload red-team suite
- Implemented an audit trail capturing prompt version, retrieved chunk IDs, model version, and tool calls — sufficient to reproduce any historical answer

---

## Project timing summary

| Project | Design | Build | Ship | Keep improving until |
|---|---|---|---|---|
| 1 · Production Backend | Day 29 | Days 30–59 | Day 60 | Day 150 (AWS deploy) |
| 2 · Enterprise RAG | Day 81 | Days 82–96 | Day 90 | Day 235 (folded into capstone) |
| 3 · Distributed Platform | Day 104 | Days 105–119 | Day 120 | Day 150 (AWS + IaC) |
| 4 · AI Platform (capstone) | Day 211 | Days 232–239 | Day 240 | — |

**Rule:** never have more than one project in "build" state at a time. Finished and deployed beats two half-built.

---

# PART III · INTERVIEW QUESTION BANK

Model answers are **compressed** — the shape of a good answer, not a script. In a real interview, expand each into 60–90 seconds and anchor it to something you actually built. The strongest pattern is: *direct answer → mechanism → tradeoff → "in my project I hit this when…"*.

Use this as a self-quiz. Cover the answer column, say it out loud, then compare.

---

## 14.1 Python and language internals

| Question | Model answer |
|---|---|
| Why don't threads speed up CPU-bound Python? | The GIL allows only one thread to execute bytecode at a time. Threads still help I/O-bound work because the GIL is released during blocking I/O. For CPU-bound work you need `multiprocessing`, a C extension that releases the GIL (NumPy), or a different runtime. |
| `is` vs `==`? | `is` compares identity (same object in memory), `==` compares value via `__eq__`. Small ints and short strings are cached/interned, so `is` sometimes appears to work on values — which is exactly why you must not rely on it. |
| Why is a mutable default argument dangerous? | Defaults are evaluated once at function definition, so the same list object is shared across every call and accumulates state. Use `None` as the default and create the list inside the body. |
| What does a closure capture? | The variable, not the value — it holds a reference to the enclosing scope's cell. This is why closures in a loop all see the loop variable's final value unless you bind it with a default argument. |
| Generators vs lists — why care? | A generator yields lazily and holds one item at a time, so memory stays flat regardless of input size, and you can start consuming before production finishes. A list materialises everything. For a 1GB file, one is O(1) memory and one is O(n). |
| Threads vs async vs processes? | Async: many concurrent I/O waits, single thread, no GIL contention, but any blocking call stalls the whole loop. Threads: I/O concurrency with blocking libraries, preemptive, needs locks. Processes: CPU parallelism, separate memory, expensive IPC. Choose by whether you're waiting or computing. |
| What does `async def` actually give you? | A coroutine object. Nothing runs until it's awaited or scheduled on an event loop. `await` yields control back to the loop, which runs other ready tasks until your I/O completes. |
| Shallow vs deep copy? | Shallow copies the container and shares the references inside; deep recursively copies everything. Shallow is usually what you want and usually the source of the bug when it isn't. |
| Why `functools.wraps` in a decorator? | Without it the wrapper replaces the wrapped function's `__name__`, `__doc__`, and signature metadata, which breaks introspection, docs, and some frameworks' dependency resolution. |
| How does CPython manage memory? | Reference counting for immediate reclamation, plus a generational cycle collector for reference cycles. Freed memory goes back to CPython's allocator pools, not necessarily to the OS — which is why RSS often doesn't drop. |

---

## 14.2 Databases and PostgreSQL

| Question | Model answer |
|---|---|
| Why Postgres over MongoDB? | My access patterns were relational with multi-entity invariants, so I wanted foreign keys, joins, and real transactions with checked constraints. Postgres also gave me JSONB when I needed schema flexibility, plus full-text search and pgvector — one operational system instead of three. I'd pick MongoDB for genuinely document-shaped, schema-volatile data with no cross-document consistency needs. |
| Explain MVCC. | Each row version carries the transaction IDs that created and deleted it. A transaction sees only versions visible to its snapshot, so readers never block writers and writers never block readers. The cost is dead tuples, which VACUUM must reclaim, and transaction-ID wraparound to manage. |
| Isolation levels and their anomalies? | Read Committed: no dirty reads, but non-repeatable reads and phantoms are possible. Repeatable Read (snapshot isolation in Postgres): no non-repeatable reads or phantoms, but write skew is possible. Serializable: prevents write skew too, via predicate-conflict detection, at the cost of serialization failures you must retry. |
| What is write skew? | Two transactions each read a set, each decides its write is safe, and both commit — jointly violating an invariant neither broke alone. Classic case: two on-call doctors, each checks "at least one other is on duty," both go off duty. Snapshot isolation permits it; Serializable does not. |
| Why B+tree for database indexes? | High fanout means very shallow trees, so a lookup is a handful of page reads. Nodes match disk/page size. Leaves are linked, making range scans and ordered traversal efficient — which hash indexes can't do and binary trees do far too deep. |
| Why did Postgres ignore my index? | Low selectivity (a sequential scan is cheaper than many random reads), a function or implicit cast on the indexed column, wrong leading column in a composite index, stale statistics, a data-type mismatch, or the query needs columns not covered so the heap fetches dominate. `EXPLAIN ANALYZE` and `ANALYZE` are the first two moves. |
| Composite index column order? | Equality predicates first, then range, then sort columns. The index can only be used left-to-right, so `(a, b)` serves `WHERE a=…` and `WHERE a=… AND b=…` but not `WHERE b=…` alone. |
| Why is `OFFSET 100000 LIMIT 20` slow? | The database must produce and discard 100,000 rows before returning 20 — cost grows with the offset. Keyset pagination (`WHERE (sort_key, id) < (:last_key, :last_id) ORDER BY … LIMIT 20`) is O(log n) via the index and also stable under concurrent inserts. |
| How do you build a job queue in Postgres? | `SELECT … FOR UPDATE SKIP LOCKED LIMIT n` inside a transaction to claim jobs without blocking other workers, a status column with a visible-after timestamp for delays, an attempt counter, and an index on `(status, run_after)`. It's correct and simple up to moderate throughput; beyond that use a real broker. |
| What does connection pooling solve in Postgres? | Postgres forks a process per connection, so each connection costs memory and scheduler pressure — thousands of connections degrade the server even when idle. A pool keeps a small set of warm connections and multiplexes application concurrency onto them; pgBouncer adds transaction-level pooling for very high client counts. |
| Sizing a connection pool? | Start from the database's capacity, not the app's optimism: roughly `cores × 2 + effective_spindles` as a ceiling for the whole system, divided across app instances. Too large just moves the queue from your app into the database, where it's worse. |
| What causes a deadlock and how do you fix it? | Two transactions acquire the same locks in opposite order. Postgres detects the cycle and kills one. Fix by imposing a global lock ordering (e.g. always update rows in ascending primary-key order), shortening transactions, and retrying on deadlock. |

---

## 14.3 Caching and Redis

| Question | Model answer |
|---|---|
| Why is single-threaded Redis fast? | Everything is in memory, the command execution is O(1)–O(log n) for most operations, and single-threaded execution means no locks and no context switching, with an efficient event loop for I/O. The limit is that one slow command (a big `KEYS` or a large `ZRANGE`) blocks everything, and one core caps throughput. |
| Cache-aside vs write-through? | Cache-aside: app reads cache, misses go to DB and populate the cache. Simple, resilient to cache loss, but the first read after a write is stale or a miss. Write-through: writes go through the cache to the DB, keeping them consistent at the cost of write latency and caching data nobody reads. Cache-aside is the default for read-heavy workloads. |
| Cache stampede — what and how do you fix it? | A hot key expires and every concurrent request misses simultaneously, all hitting the database at once. Fixes: single-flight/mutex so one request recomputes while others wait or serve stale; probabilistic early expiry to desynchronise TTLs; stale-while-revalidate; and pre-warming known-hot keys. |
| How would you build a distributed rate limiter? | Token bucket in Redis with a Lua script so the read-decide-write is atomic. Key per tenant, fields for tokens and last-refill; the script refills based on elapsed time and decrements if allowed. Return 429 with `Retry-After`. Sliding-window counters are a cheaper approximation; a sorted-set log is exact but memory-heavy. |
| What eviction policy and why? | For a cache, `allkeys-lru` (or `allkeys-lfu` if access is skewed and long-tailed) so Redis stays within `maxmemory`. `noeviction` is correct only when Redis holds data you cannot lose — and then it's a database, and you need persistence and replication to match. |
| Redis persistence options? | RDB: periodic point-in-time snapshots — compact, fast restart, but loses writes since the last snapshot. AOF: appends every write, more durable, replayed on restart, larger and slower. Many setups run both. Neither makes Redis a system of record on its own. |

---

## 14.4 Kafka, messaging, and reliability

| Question | Model answer |
|---|---|
| Why is Kafka fast despite writing to disk? | Append-only sequential writes (sequential disk I/O is orders of magnitude faster than random), the OS page cache serving reads, zero-copy transfer to sockets, and batching plus compression amortising per-message overhead. |
| How do you choose partition count? | It's your unit of parallelism: you can't have more useful consumers than partitions. Estimate target throughput divided by per-consumer throughput, add headroom, and consider key cardinality to avoid skew. Too many partitions costs metadata, open file handles, and rebalance time; increasing later is easy, decreasing is not, and adding partitions rehashes key→partition mapping, breaking ordering assumptions. |
| `acks=all` vs `acks=1`? | `acks=1` returns when the leader has written — you lose messages if the leader fails before replication. `acks=all` waits for all in-sync replicas, so you survive leader loss but pay latency. With `min.insync.replicas=2` and `acks=all` plus an idempotent producer you get strong durability; that's the correct default for anything you can't afford to lose. |
| Why does adding a 4th consumer to a 3-partition topic do nothing? | A partition is assigned to at most one consumer within a group, so the 4th sits idle as a hot standby. To scale further you must add partitions — or restructure so processing fans out downstream. |
| Consumer takes 5 minutes per message — what breaks? | It exceeds `max.poll.interval.ms`, the coordinator considers the consumer dead, the group rebalances, and the work gets reprocessed — potentially forever. Fixes: lower `max.poll.records`, raise the interval, or better, hand long work to a separate worker pool and keep the poll loop fast. |
| Can you get exactly-once? | Within Kafka, yes — idempotent producer plus transactions plus `read_committed` gives exactly-once from topic to topic. Across an external system it's effectively-once: you achieve at-least-once delivery plus idempotent processing keyed on a deterministic ID. There is no exactly-once against a third-party HTTP API that may have applied your call before the timeout. |
| How do you make "send an email" idempotent? | Derive a deterministic idempotency key (message ID + recipient + template version), check-and-insert into a dedup store atomically before sending, and use the provider's own idempotency key if offered. You still can't guarantee exactly-one-email if the provider accepted the request and the response was lost — so record intent before sending and reconcile after. |
| What goes in a DLQ record? | Original payload and headers, source topic/partition/offset, error type and message, stack trace, attempt count, first- and last-failure timestamps, correlation/trace ID, and consumer version. Enough that someone three days later can diagnose without the original context, plus a replay tool that can select a subset. |
| Retries made the outage worse — why? | Retry amplification: each failing request became N requests, multiplying load on an already-degraded dependency and preventing recovery. Fixes: exponential backoff with jitter, a retry budget capping the fraction of traffic that is retries, circuit breakers to stop trying, and load shedding at the edge. |
| Why can't you write to Postgres and publish to Kafka atomically? | They're separate systems with no shared transaction, so a crash between the two leaves them inconsistent — the dual-write problem. The outbox pattern fixes it: write the event to an outbox table in the same DB transaction, then a relay (or CDC) reads the table and publishes, at-least-once, with consumer idempotency absorbing duplicates. |
| Producers outpace consumers 3:1 — options? | Scale consumers (up to partition count), then add partitions; make processing cheaper or batch it; shed or sample low-value messages; apply backpressure upstream via rate limiting; tier the work so critical messages get priority. Kafka's retention buys you time — but only until retention expires, so lag alerting matters. |

---

## 14.5 Distributed systems

| Question | Model answer |
|---|---|
| CAP theorem, precisely? | When a network partition occurs, you must choose between consistency and availability. P is not optional — networks partition. So the real question is what the system does *during* a partition: refuse writes (CP) or accept possibly-divergent writes (AP). "We chose CA" usually means "we haven't thought about partitions." |
| Why is PACELC more useful? | CAP only describes partition behaviour, which is rare. PACELC adds: else (E), when running normally, you trade latency (L) against consistency (C). That's the choice you make every day — and it's what actually distinguishes, say, DynamoDB's tunable reads from Cassandra's, or a synchronous replica from an asynchronous one. |
| Linearizability vs eventual consistency? | Linearizable: every operation appears to take effect atomically at a single point in time, and all clients see one consistent order — expensive, requires coordination. Eventual: replicas converge if writes stop, with no ordering guarantee in the meantime — cheap and available. Most systems need linearizability for a few operations (balances, uniqueness) and eventual for most. |
| User updates their profile and doesn't see the change — diagnose. | Read-after-write against an asynchronous replica with lag. Fixes: route the user's reads to the primary for a short window after their write, use sticky sessions per user, track a write timestamp/LSN and require replicas to have caught up, or read your own writes from a cache populated at write time. |
| N=5, W=3, R=2 — what do you get? | W + R = 5 = N, which is not > N, so quorum overlap isn't guaranteed and reads may miss the latest write. For strong reads you need W + R > N, e.g. W=3, R=3. W=3 tolerates 2 node failures for writes; R=2 gives fast reads at the cost of possible staleness. |
| Why is a Redis lock with a TTL not enough for correctness? | Between acquiring the lock and doing the work, your process can pause (GC, VM freeze, network partition) past the TTL, so the lock expires and another holder starts — now two processes both believe they hold it. You need fencing: a monotonically increasing token issued with the lock and validated by the resource, which rejects writes from stale holders. Without a fencing-aware resource, locks give you efficiency, not correctness. |
| Explain consistent hashing. | Map nodes and keys onto a hash ring; a key belongs to the next node clockwise. Adding or removing a node moves only the keys in its arc — roughly 1/N — instead of rehashing everything. Virtual nodes (many ring positions per physical node) smooth the load imbalance and make removals spread across all remaining nodes. |
| Sharding key turned out wrong — now what? | You can't fix it in place cheaply. The playbook: add a routing/directory layer if you don't have one, dual-write to the new sharding scheme, backfill historical data, verify with shadow reads comparing old and new, cut reads over gradually, then decommission. The lesson to state: choose a key with high cardinality and even access, and build the directory indirection early so re-sharding is possible at all. |
| Saga — step 3 of 4 fails after side effects? | Run compensating actions for the completed steps in reverse order — semantic undo, not rollback, since the side effects are already visible. Compensations must be idempotent and retryable, and some are irreversible (an email sent), which is why irreversible steps go last. Orchestration (a coordinator) is easier to debug than choreography (events); the state must be durable so recovery can resume. |
| How do you cut a cascading failure? | Timeouts everywhere (no unbounded waits), circuit breakers to stop calling a failing dependency, bulkheads so one dependency's thread pool can't starve others, load shedding at the edge based on queue depth, retry budgets, and graceful degradation with a defined reduced experience. Then verify with load and chaos tests, not hope. |

---

## 14.6 System design (the method plus four worked skeletons)

**The method — apply it every time, in this order**

1. **Clarify** (2–3 min): who uses it, what scale, read/write ratio, latency requirement, consistency requirement, what's explicitly out of scope
2. **Estimate** (2 min): DAU → QPS → peak QPS, storage/day, bandwidth, and — for AI systems — tokens/day and cost/month
3. **API** (2 min): the 4–6 endpoints or events that matter, sync vs async
4. **Data model** (3 min): entities, access patterns, then store choice justified by those patterns
5. **High-level architecture** (8 min): draw it, name each component's responsibility
6. **Deep dive** (10 min): let the interviewer pick, or go to the actual hard part yourself
7. **Bottlenecks and failure modes** (5 min): what saturates first, what breaks, what you'd monitor
8. **Tradeoffs** (2 min): what you chose against, and what you'd change at 10× scale

### Skeleton 1 · Enterprise AI assistant for 10M users

- **Clarify:** internal docs or public? per-user permissions? conversational or one-shot? acceptable p95? compliance/residency?
- **Estimate:** 10M DAU × 3 queries = 30M queries/day ≈ 350 qps average, ~1200 qps peak. At ~4k input + 500 output tokens: ~135B tokens/day. That number is the design driver — it immediately tells you routing, caching, and self-hosting are not optional.
- **Architecture:** gateway (auth, rate limit, quota) → orchestrator → semantic cache → retrieval (hybrid, ACL-filtered, reranked) → prompt assembly → LLM router (small model default, escalate) → streamed response; async ingestion via Kafka; per-tenant metering.
- **Hard parts to volunteer:** permission-aware retrieval at this scale; semantic cache hit rate versus staleness; multi-tenant fairness so one tenant can't consume the fleet; cost per query as a first-class SLO; eval to detect quality regressions when you change any of the above.
- **Bottleneck:** GPU/token capacity, not CPU. Capacity plan in GPUs, and derive concurrency from KV-cache memory per request.

### Skeleton 2 · Distributed document processing, 1M docs/day

- **Estimate:** ~12 docs/sec average, ~40/sec peak; 1M × 2MB = 2TB/day raw into object storage; ~30 chunks/doc = 30M embeddings/day.
- **Architecture:** presigned S3 upload → S3 event → Kafka → parse/OCR/chunk/embed worker stages, each its own consumer group → Postgres+pgvector → index-complete event. Retry topics with delays, DLQ, transactional outbox, idempotency keyed on content hash.
- **Hard parts:** embedding provider rate limits (adaptive batching + backpressure), OCR being 50× slower than parsing (separate pool and topic so it can't starve the fast path), poison documents, re-embedding when the model changes (versioned embedding columns and a backfill path).
- **Bottleneck:** embedding throughput. State it, then design around it.

### Skeleton 3 · Multi-tenant LLM gateway

- **Estimate:** per-tenant qps, token budgets, cost ceilings; the metering write rate is its own design problem.
- **Architecture:** API key auth with scopes → per-tenant token-bucket rate limit in Redis → quota check against budget → semantic cache → router (model choice by policy) → provider clients with circuit breakers and fallback → streaming response → async metering pipeline (Kafka → aggregation → billing).
- **Hard parts:** fair-share scheduling across tenants; accurate cost attribution when a request fans out to several models; a semantic cache that respects tenant boundaries; streaming plus metering (you only know the token count at the end); graceful behaviour when a tenant hits their budget mid-stream.

### Skeleton 4 · Real-time agent execution platform

- **Architecture:** request → planner → durable state store (Postgres) → step executor with a tool registry → sandboxed execution → HITL approval queue → event stream for progress → resumable on crash.
- **Hard parts:** durability and resumability (a step's side effects may have happened before the crash — so record intent, make steps idempotent); cost and step ceilings; loop detection; concurrency between steps with dependencies; approval gates without blocking the whole system; observability per step.

---

## 14.7 LLMs, RAG, and retrieval

| Question | Model answer |
|---|---|
| How does RAG work, in one minute? | Index: documents are parsed, chunked, embedded, and stored with metadata. Query: the question is embedded, similar chunks are retrieved (often dense + sparse, fused and reranked), filtered by permissions, assembled into a prompt within a token budget, and the model answers with citations. The model supplies fluency and reasoning; retrieval supplies facts and freshness. |
| My RAG answers are bad. Where do you look? | Attribute the failure to a stage before changing anything. Was the right chunk retrieved at all? If not, it's chunking, embedding, or query formulation. If it was retrieved but ranked low, it's ranking or fusion. If it was in context and the answer still ignored it, it's prompt assembly, ordering, or context length. Measure per-stage with a golden set; most teams tune the prompt when the problem is chunking. |
| Long context vs RAG? | Long context is simpler and better for holistic reasoning over one document, but cost and latency grow with tokens, attention degrades in the middle, and you re-pay for the same tokens every request. RAG is cheaper per query, scales to corpora that will never fit, gives citations and access control, but adds retrieval failure modes. In practice: RAG to select, long context to reason over what was selected. |
| Why hybrid search? | Embeddings capture semantics but are weak on exact tokens — product SKUs, error codes, names, negation, rare jargon. BM25 nails exact matches but misses paraphrase. Fusing them (RRF, which needs no score normalisation) recovers both classes of query. I found ~15% of my golden set was only answerable by lexical match. |
| Why can't you just average cosine and BM25 scores? | They're on incomparable, unbounded, query-dependent scales. Reciprocal rank fusion uses only rank positions, which sidesteps normalisation entirely and is robust in practice. If you want weighted score fusion you must normalise per query (e.g. min-max over the result set) and tune the weight on a golden set. |
| Bi-encoder vs cross-encoder? | A bi-encoder embeds query and document independently, so document vectors are precomputed and search is an ANN lookup — fast, scalable, less accurate. A cross-encoder reads query and document together, producing much better relevance, but must run per candidate pair at query time, so it can't be a first-stage retriever. Standard pattern: bi-encoder retrieves top-50, cross-encoder reranks to top-8. |
| Explain HNSW. | A multi-layer proximity graph. Upper layers are sparse long-range links for coarse navigation; lower layers are dense local links for refinement. Search greedily descends from an entry point, so you find approximate nearest neighbours in roughly logarithmic hops. You trade recall for latency via `ef_search`, and pay in memory and build time. |
| Why is chunking usually the first suspect? | Because a chunk is the unit of retrieval: if the answer spans two chunks, or a chunk lost the heading that gave it meaning, or a table was split mid-row, then no ranking improvement can recover it. Retrieval can only rank what chunking created. |
| How do you evaluate RAG? | Separately per stage. Retrieval: recall@k, MRR, nDCG against a golden set with labelled relevant chunks. Generation: faithfulness/groundedness (is every claim supported by retrieved context), answer relevance, and abstention correctness. Gate CI on a golden set so regressions fail the build. LLM-as-judge is useful but biased toward verbosity and its own outputs — calibrate it against human labels on a sample. |
| How do you guarantee an LLM never surfaces a document the user can't read? | Enforce it at retrieval, not generation. Filter by ACL inside the vector query (metadata predicate in the same SQL/ANN query), never post-filter after assembling context, and never rely on prompt instructions. Then test it: a suite where user A queries content only B can read and must get nothing. Prompt-level authorisation is not authorisation. |
| Prompting vs RAG vs fine-tuning? | Prompting: the behaviour you want is already in the model, you just need to elicit it — cheapest, fastest to iterate. RAG: the model lacks *knowledge*, especially changing or private knowledge, and you need citations and access control. Fine-tuning: the model lacks a *behaviour, format, or style*, or you need to cut prompt length and latency at high volume. "The model should know our data" is almost always RAG, not fine-tuning. |

---

## 14.8 Transformers and inference (the ₹50L differentiators)

| Question | Model answer |
|---|---|
| Explain attention without maths. | For each token, the model asks "which other tokens should I look at to represent this one?" It computes a relevance score against every other token, turns those into weights, and builds a weighted blend of their information. That's the mechanism that lets "it" find its referent 40 words earlier. |
| What are Q, K, V? | Three learned linear projections of the same input. Query is what a token is looking for, Key is what each token offers as an index, Value is the content it contributes. Score = Q·K (how well the offer matches the request), softmax to weights, then a weighted sum of V. Separating them lets "what I'm looking for" differ from "what I contain." |
| Why divide by √d_k? | Dot products of two d-dimensional vectors grow in variance with d. Without scaling, large logits push softmax into saturation, gradients vanish, and training destabilises. Dividing by √d_k keeps logit variance roughly constant across dimensions. |
| Why multiple heads? | One attention distribution must pick a single mixture. Multiple heads let the model attend to several relationships at once — syntactic dependency in one head, coreference in another — in lower-dimensional subspaces, then concatenate and project. Total compute is comparable because head dimension shrinks as head count grows. |
| Why LayerNorm and not BatchNorm? | BatchNorm normalises across the batch per feature, which requires batch statistics — unreliable with variable-length sequences, broken at batch size 1, and awkward at inference. LayerNorm normalises across features within a single token, so it's independent of batch and sequence length. RMSNorm drops the mean-centring and is cheaper with equivalent quality in practice. |
| Why residual connections? | They give gradients an identity path back through the network, so depth doesn't multiply small Jacobians into vanishing gradients. Each block then learns a *residual* correction to its input rather than a full transformation, which is an easier optimisation problem. Pre-norm placement makes very deep stacks trainable without warmup tricks. |
| What is the KV cache and why does it exist? | During autoregressive decoding, each new token attends to all previous tokens' keys and values. Those don't change, so recomputing them every step would make generation quadratic. Caching them makes each decode step attend against stored K/V, so generation is linear in sequence length — at the cost of memory that grows with context and batch. |
| Derive the KV cache size. | `2 (K and V) × layers × kv_heads × head_dim × seq_len × batch × bytes_per_element`. For a 7B-class model with 32 layers, 32 heads × 128 head_dim, fp16, 4k context, batch 1: 2 × 32 × 4096 × 4096 × 2 ≈ 2.1GB. Multiply by batch size — which is exactly why concurrency is capped by memory, not compute. GQA/MQA shrink `kv_heads` and cut this several-fold. |
| Prefill vs decode? | Prefill processes the whole prompt in parallel — a big matrix multiply, compute-bound, saturates the GPU's FLOPs, and dominates time-to-first-token. Decode generates one token at a time, so each step is a small matmul that must stream all model weights from HBM — memory-bandwidth-bound, low arithmetic intensity, and the reason tokens/sec plateaus regardless of GPU FLOPs. |
| Why does batching help decode so much? | Because decode is bandwidth-bound: you pay to read the weights once per step regardless of how many sequences you're advancing. Batching amortises that read across many sequences, so throughput scales nearly linearly while per-request latency barely moves — until KV-cache memory or compute becomes the new limit. |
| Static vs continuous batching? | Static batching forms a batch, runs it to completion, and every sequence waits for the longest one, wasting compute on padding and inflating tail latency. Continuous batching schedules at the iteration level: finished sequences leave the batch immediately and new requests join mid-flight. On mixed-length traffic this typically multiplies throughput several-fold at the same latency. |
| What does int4 quantisation cost you? | Weight precision, which shows up as small quality degradation — usually modest on general tasks and larger on reasoning, long-context, and rare-token tasks. It buys ~4× weight memory reduction and better bandwidth utilisation, hence higher throughput. The engineering point is that you must *measure* it on your own eval set, not trust a benchmark, and remember quantising weights doesn't shrink the KV cache unless you quantise that too. |
| Design serving for p95 TTFT < 800ms at 500 rps. | TTFT is prefill-dominated, so budget: queueing + prefill + first token. Measure single-request prefill time at your prompt length, compute how many prefill token-batches a GPU does per second, and derive GPUs needed with headroom for the 95th percentile — then constrain concurrency by KV-cache memory per request. Use continuous batching with chunked prefill so long prompts don't block short ones, cap max input length, prompt-cache shared prefixes, route short requests to a small model, and autoscale on queue depth rather than CPU. State the arithmetic out loud; that's what's being tested. |
| When is self-hosting cheaper than an API? | Compute your fully-loaded hourly GPU cost, divide by achieved tokens/sec at your target latency to get cost per million tokens, and compare with API list price. Self-hosting wins above a volume threshold and when utilisation is high and steady; APIs win for spiky, low-volume, or high-variance traffic because you don't pay for idle GPUs. Also price in engineering time, on-call, and the cost of falling behind on model quality. |

---

## 14.9 Agents, MCP, and AI security

| Question | Model answer |
|---|---|
| When is an agent the wrong choice? | When the task's steps are known in advance. A deterministic pipeline is cheaper, faster, testable, and debuggable. Agents earn their cost only when the sequence genuinely depends on intermediate results. Most "agent" products would be better as a workflow with one or two LLM steps. |
| How do you stop an agent looping forever or burning money? | Hard ceilings enforced outside the model: max steps, max wall-clock, max cumulative token cost per run. Plus loop detection on repeated (tool, arguments) pairs, a progress check that requires state to change every N steps, and per-tenant budgets so a runaway run can't consume the fleet. Ceilings must be enforced by the orchestrator, never by prompt instruction. |
| Your agent dies mid-run. What happens? | State must be durable per step, not in memory: the plan, each step's status, its output, and whether side effects were applied. On restart the executor resumes at the first incomplete step. Steps must be idempotent, because a step may have completed its side effect before the crash but not recorded it — so record intent before acting and reconcile on resume. |
| How do you handle memory when the conversation exceeds context? | Keep the system prompt and the most recent turns verbatim, compact older turns into a running summary, and move durable facts into structured memory (entities, decisions, preferences) retrieved on demand. Log what was dropped. The failure mode to guard against is summarisation quietly losing the constraint the user stated at the start. |
| Which agent actions need human approval? | Tier tools by reversibility and blast radius. Read-only: auto. Reversible writes with an undo path: auto with an audit record. Irreversible or externally visible (sending mail, moving money, deleting data, deploying): explicit approval with a diff or dry-run preview. The tier belongs in the tool's declared metadata, enforced by the executor. |
| What problem does MCP solve? | The N×M integration problem: every AI application otherwise writes bespoke connectors for every data source and tool. MCP standardises the protocol — capability discovery, tool invocation, resources, prompts — so a server written once works with any compliant client. It's a plumbing standard, not a capability; it doesn't make the model better at choosing tools. |
| Resources vs tools in MCP? | Resources are addressable, readable context — data the client can fetch and put in front of the model (files, records, documents), typically read-only and enumerable. Tools are actions with side effects and arguments. If the model needs to *know* something, it's a resource; if it needs to *do* something, it's a tool. |
| Why is prompt injection unsolved? | Because the model sees instructions and data in the same channel, and there is no cryptographic or architectural separation between "what the developer asked" and "what arrived in a retrieved document." Any content that reaches the context can attempt to steer behaviour. You mitigate rather than solve: separate and label untrusted content, spotlight/delimit it, constrain output format, apply least privilege to tools, require approval for consequential actions, and treat model output as untrusted input to the next system. |
| An attacker uploads a poisoned document. Where do you stop it? | Defence in depth. Ingestion: trust tiers by source, scanning, provenance metadata, and downweighting untrusted content in ranking. Retrieval: never let untrusted content outrank authoritative sources for policy-type questions. Assembly: label untrusted spans explicitly and instruct the model that content in that block is data, never instruction. Execution: least-privilege tools plus approval gates, so a successful injection still can't do damage. Detection: red-team suite in CI plus audit logs so you can find what an attack touched. |
| How do you run model-generated code safely? | In a disposable sandbox with no network egress by default, a read-only filesystem apart from a scratch directory, CPU/memory/process limits, a hard wall-clock timeout, no credentials mounted, and container or microVM isolation. Return only stdout/stderr with a size cap, and log everything executed. Never run it in the application process. |
| A customer says your AI leaked data. How do you investigate? | From the audit trail: reconstruct the exact request — user, tenant, timestamp, prompt version, retrieved chunk IDs with their ACLs, model and version, tool calls with arguments, and the response. Then check whether the retrieved chunks were actually authorised for that user, whether ACLs changed after indexing, and whether the content came from retrieval or from model memorisation. That's exactly why the audit record must be sufficient to reproduce an answer. |

---

## 14.10 Behavioural (prepare six stories in STAR form)

Have these written and rehearsed. Each should be 90 seconds with one number in it.

| Prompt | The story to have ready |
|---|---|
| Hardest technical problem you've solved | A debugging story with a measurement: symptom → hypotheses → how you narrowed it → root cause → fix → verified result |
| A time you were wrong | A design or technology choice you reversed, what evidence changed your mind, what it cost |
| A production incident | Detection, immediate mitigation, root cause, permanent fix, and the process change afterwards |
| Disagreement with a colleague/manager | How you separated the technical question from the interpersonal one, and how it resolved |
| Something you shipped under time pressure | What you deliberately cut, why that was the right cut, and what you paid later |
| Why are you leaving / why this role | Forward-looking and specific to their systems — never a complaint about the current employer |

### Questions to ask them (asking well is a signal)

- What does the AI/ML stack actually look like in production today, and what's the biggest gap?
- How do you evaluate model quality before shipping a change? Is it gated in CI?
- What's your cost per query, and who owns that number?
- Who is on call for the AI systems, and what pages most often?
- What's the split between building new capability and maintaining what exists?
- What would you want me to have accomplished by the end of my first six months?

---

# PART IV · JOB SEARCH

The engineering half of this plan makes you employable. This half is what converts it into an offer. Most people execute the first half and neglect this one, then conclude the market is bad.

---

## 15. Timeline and cadence

| Phase | Days | Applications/week | Target band | Purpose |
|---|---|---|---|---|
| Build | 1–60 | 0 | — | Don't burn your first impressions with a weak profile |
| Activate | 61–74 | 0 (profile + list + outreach only) | — | Profiles live, target list built, warm contacts opened |
| Calibrate | 75–90 | 5–10 | ₹15–30L | Interview reps. Learn the loop. Collect rejection reasons |
| Scale | 91–120 | 10–15 | ₹20–40L, selectively ₹40L+ | Real pipeline. Convert to onsites |
| Serious | 121–180 | 15–20 | ₹30–50L | Tier B and Tier A. This is the main phase |
| Convert | 181–240 | 10–15 (higher quality, more referrals) | ₹40–60L | Fewer, better, mostly referred. Negotiate |

**Why apply during the calibrate phase at a band below your target:** you will fail interviews for reasons that have nothing to do with knowledge — pacing, thinking out loud, clarifying questions, whiteboard structure, negotiating. Those failures are cheap at ₹20L and expensive at ₹50L. Take the reps early.

**Rejections are data.** Log the reason for every one. If three companies say "system design was shallow," that's not bad luck, that's Month 5 needing more work.

### Weekly job-search block (15 min/day = ~1.75 h/week)

| Day | Activity |
|---|---|
| Mon | Source 15 new roles into the tracker |
| Tue | Send applications (batch them; tailor the top line only) |
| Wed | 5 outreach messages (engineers, not recruiters) |
| Thu | Follow up on anything 7+ days silent |
| Fri | Reply to recruiters, schedule interviews |
| Sat | Post or comment publicly; update a project README |
| Sun | Update tracker, review the week's rejection reasons, adjust |

---

## 16. Company tiers

Build the spreadsheet on Day 61 with **60+ rows**. Categories, not specific guarantees — verify current comp bands yourself on Levels.fyi, AmbitionBox, and Glassdoor, since these move.

| Tier | Typical band | Who | How you get in | Your target count |
|---|---|---|---|---|
| **A** | ₹40–70L+ | Global product companies and their India GCCs; top-tier infra/data/AI companies; well-funded AI-native startups paying for scarce skills | Referral or a very strong profile; 4–6 round loops with real DSA + system design + AI depth | 15 companies |
| **B** | ₹25–45L | Strong Indian and global SaaS, fintech, developer-tools, enterprise-AI companies; mid-size GCCs | Applications work here; referrals help a lot | 25 companies |
| **C** | ₹15–30L | AI startups (seed to Series B), good product companies, digital-native businesses | Direct applications, founder outreach, AngelList/Wellfound-style channels | 20 companies |
| **D** | ₹10–20L | Anywhere you can get an interview quickly — services companies with AI teams, early startups | Apply freely; these are for practice | 10 companies |

**The ladder is deliberate:** Tier D gives interview reps → Tier C gives you an offer in hand and real experience → Tier B is the realistic ₹30–45L landing zone → Tier A is the stretch. An offer in hand from Tier C changes your negotiating posture in Tier B and A completely.

### Tracker schema

| Column | Notes |
|---|---|
| Company | |
| Tier | A/B/C/D |
| Role title | Exact posting title |
| Band (est.) | Your estimate + source |
| Source | Job board / referral / outreach / recruiter inbound |
| Applied date | |
| Referral | Name, or blank |
| Status | Sourced → Applied → Screen → Tech1 → Tech2 → Design → Onsite → Offer → Rejected → Ghosted |
| Last touch | Date of your last action |
| Next action | The single next thing *you* must do |
| Rounds notes | Questions asked, what went badly |
| **Rejection reason** | The most valuable column in the sheet |
| Comp discussed | Base / variable / equity / expectation stated |

**Rule:** every row must have a "next action" or be closed. A tracker with 80 rows and no next actions is a diary, not a pipeline.

### Where to source roles

- LinkedIn Jobs with saved searches for each Priority-1 and Priority-2 title, set to daily alerts
- Company career pages directly (higher signal than aggregators; recruiters see these first)
- Wellfound/AngelList for AI startups
- Hiring-focused communities and newsletters in the Indian AI/backend space
- GitHub: find companies whose engineers are active in the tools you use, then find their careers page
- Recruiter inbound — which grows once your LinkedIn headline and posts are working

### Search terms to save

**Priority 1:** AI Engineer · GenAI Engineer · Generative AI Engineer · Applied AI Engineer · LLM Engineer · AI Backend Engineer · AI Platform Engineer · AI Infrastructure Engineer · ML Platform Engineer

**Priority 2:** Backend Engineer AI · Software Engineer GenAI · Software Engineer AI Platform · Distributed Systems Engineer · Platform Engineer · Senior Backend Engineer Python · Inference Engineer · MLOps Engineer

**Also worth watching:** Forward Deployed Engineer · Solutions Engineer AI · AI Systems Engineer · Staff Engineer AI (stretch, but read the JDs — they tell you exactly what to learn)

---

## 17. Resume

### Structure (one page, always)

```
NAME · dipankar@… · +91… · linkedin.com/in/… · github.com/… · portfolio-url

SUMMARY  (2 lines, rewritten per tier)
Backend/AI engineer building production LLM systems — RAG, agents, and
distributed pipelines on Python, Postgres/pgvector, Kafka, and AWS.

SKILLS  (grouped, no proficiency bars, no "familiar with")
Languages: Python, SQL, Bash
AI/ML: LLM APIs, RAG (hybrid retrieval, reranking, evals), agents, MCP,
       LoRA/QLoRA, PyTorch, transformers, inference optimisation
Backend: FastAPI, PostgreSQL, pgvector, Redis, Kafka, REST, async Python
Infra: Docker, AWS (ECS, RDS, S3, ALB, IAM, CloudWatch), Terraform, CI/CD
Practices: system design, observability, load testing, evaluation pipelines

PROJECTS   ← above experience, since projects are your strongest evidence
<Project 4 — capstone, 4 bullets>
<Project 3 — distributed, 3 bullets>
<Project 2 — RAG, 3 bullets>
<Project 1 — backend, 2 bullets>

EXPERIENCE
<current/past roles — reframed toward systems and scale, not tasks>

EDUCATION  (2 lines, at the bottom)
```

### Bullet formula

`<Verb> <what you built> <with what constraint/scale> — <measured result>`

| Weak | Strong |
|---|---|
| "Worked on a RAG chatbot using LangChain" | "Built a hybrid-retrieval RAG service (pgvector + BM25 + RRF + cross-encoder reranking), improving recall@5 from 0.62 → 0.87 on a 50-question golden set" |
| "Used Kafka for message processing" | "Designed idempotent Kafka consumers with delayed retry topics and DLQ replay tooling; verified zero data loss under forced consumer kills and a 5-minute provider outage" |
| "Optimised API performance" | "Cut p95 latency 68% (1.9s → 610ms) by adding cache-aside with single-flight protection after load testing revealed a thundering-herd failure at 200 rps" |
| "Familiar with LLM inference" | "Benchmarked inference across fp16/int8/int4 and batch sizes 1–64; continuous batching raised throughput 4.1× at equal p95, cutting cost per million tokens 61%" |

**Rules**

- Every bullet has a number. If you don't have one, measure it — that's why the projects specify metrics.
- No adjectives. "Robust," "scalable," "cutting-edge" are noise. The number is the claim.
- Name the failure you fixed, not just the feature you added. Engineers read that as competence.
- One page until you have 8+ years. Two pages says you can't prioritise.
- Tailor only the summary line and the top project's framing per application. Full rewrites per company are not worth the time.
- Plain single-column layout, no graphics — ATS parsers mangle columns and icons.

### Three versions to maintain

| Version | Emphasis | Use for |
|---|---|---|
| AI-forward | RAG, agents, MCP, evals, inference | AI Engineer / GenAI / LLM Engineer roles |
| Platform-forward | Kafka, distributed systems, AWS, reliability, observability | AI Platform / Infra / Distributed Systems roles |
| Backend-forward | Postgres, API design, scale, correctness | Senior Backend Engineer roles |

---

## 18. LinkedIn

**Headline** (this is what recruiters search)

```
AI / Backend Engineer · LLM · RAG · Agents · Distributed Systems ·
Python · PostgreSQL · Kafka · AWS
```

**About** (4 short paragraphs, first two lines matter most since the rest is collapsed)

```
I build production AI systems — the retrieval, orchestration, and
infrastructure that sit between an LLM and a real user.

Currently: <Project 4 in one line, with a number>. Recently:
<Project 2 or 3 in one line, with a number>.

Stack: Python, FastAPI, PostgreSQL + pgvector, Redis, Kafka, Docker, AWS.
On the AI side: hybrid retrieval, reranking, evaluation pipelines, agent
orchestration, MCP, LoRA/QLoRA, and inference optimisation (KV cache,
quantisation, continuous batching).

Open to AI Engineer / AI Platform / Backend roles where the hard part is
the system, not the prompt. <city / remote preference>
```

**Featured section:** capstone repo, RAG repo, inference benchmark writeup, portfolio page.

**Posting cadence: one post per month (8 total).** Not thought-leadership — engineering writeups. These are what make recruiters come to you.

| Month | Post |
|---|---|
| 2 | "What load testing taught me about connection pools" — with the graph |
| 3 | "Building RAG without a framework: what each layer actually does" |
| 4 | "I killed my Kafka consumers on purpose. Here's what broke." |
| 5 | "Six failure modes I designed for, and the two that still scare me" |
| 6 | "Implementing cross-entropy from scratch to finally understand it" |
| 7 | "KV cache, prefill vs decode, and why your p99 is bad" — your best post |
| 8 | "I built a multi-tenant AI platform in 8 months. Architecture and numbers." |

Rules: lead with the number or the surprise, keep it under 250 words, always include the repo link, never use engagement bait.

---

## 19. Outreach templates

Referrals convert at a dramatically higher rate than cold applications. Budget 5 outreach messages a week from Day 61.

### Engineer at a target company (best ROI — send this one most)

> Hi <Name> — I'm a backend engineer working on production LLM systems (RAG, agents, distributed ingestion pipelines). I saw <Company> is hiring for <Role> and the <specific thing: their inference work / their retrieval scale / a talk or blog post they published> is close to what I've been building.
>
> I recently built <one project, one number — e.g. "an event-driven document pipeline doing 40k docs/hour with idempotent Kafka consumers and DLQ replay">: <repo link>.
>
> Would you be open to a 15-minute call about what the team's actually working on? And if it seems like a fit, whether a referral would make sense.

### Recruiter (inbound or cold)

> Hi <Name> — thanks for reaching out / I saw you're hiring for <Role>.
>
> Quick context: I build production AI systems — RAG with hybrid retrieval and eval pipelines, agent orchestration, and distributed ingestion on Kafka/Postgres/AWS. Most recent: <project + number>. Portfolio: <link>.
>
> My expectation is ₹<X>L total comp. If that's in range for this role, happy to talk this week — <two time windows>.

*State the number early with recruiters. It saves both of you three rounds of discovery.*

### Founder / hiring manager at a startup

> Hi <Name> — I've been following <Company> since <specific thing>. I build the infrastructure layer under LLM products: retrieval that survives real corpora, agents with cost ceilings and durable state, and the eval pipelines that stop quality regressions shipping.
>
> Two things I built that are close to your problem: <project 1 + number>, <project 2 + number>.
>
> If you're hiring for anything on the AI platform side, I'd love 20 minutes. If not, I'd still be interested in how you're handling <a specific technical problem their product implies>.

### Following up (once, after 7 days; twice maximum)

> Hi <Name> — following up on my note about <Role>. Adding one thing since it's relevant to <their problem>: <one new artefact — a benchmark, a writeup, a repo>. Happy to be told it's not a fit; just didn't want it lost in the inbox.

### After an interview (same day, always)

> Hi <Name> — thanks for the conversation today. The question about <specific thing> stuck with me; <one sentence of additional thinking, or a correction if you got something wrong>. I'm genuinely interested in <specific thing about the team's work>. Happy to do a follow-up exercise if that's useful.

*Correcting something you got wrong in the interview, unprompted, is one of the highest-signal moves available to you.*

---

## 20. Interview process and negotiation

### The typical ₹40L+ loop

| Round | What's tested | Your preparation |
|---|---|---|
| Recruiter screen | Comp expectation, notice period, basic fit | Know your number; have a 60-second pitch |
| Online assessment / DSA screen | 1–2 mediums in 60–90 min | Timed practice from Month 5 onward |
| Technical 1 | DSA + language depth | 240 problems + Section 14.1 |
| Technical 2 | LLD / code design / debugging | Section 14.1–14.3 + your project code |
| System design | The method, tradeoffs, scale | Section 14.6, 20+ written designs |
| AI depth | RAG, inference, agents — increasingly this is its own round | Sections 14.7–14.9 |
| Hiring manager / behavioural | Ownership, incidents, collaboration | Six STAR stories from Section 14.10 |
| Bar raiser (some companies) | Depth on anything, judgment | Be honest about limits; show how you learn |

### Interview-day rules

- **Clarify before designing.** Silence for 30 seconds while you write down constraints reads as senior, not slow.
- **Think out loud, but structured.** "Three options: A, B, C. A's problem is X. I'd take B because Y." Not stream-of-consciousness.
- **Say "I don't know" and then reason.** "I haven't used that. From first principles I'd expect… — is that close?" This scores far better than bluffing, and bluffing on inference internals is instantly detectable.
- **Anchor everything to what you built.** "I hit this exact problem in my ingestion pipeline" is worth more than any textbook answer.
- **Always give the tradeoff.** An answer with no tradeoff sounds memorised. Every real choice cost you something — name it.
- **Numbers over adjectives.** Every time.

### Negotiation

1. **Never state a number first if you can avoid it.** "I'd like to understand the role's band — what's budgeted for this level?"
2. **When you must, anchor on total comp, above target, with a justification:** "Based on the scope and my work on AI platform and inference, I'm targeting ₹<target + 20%> total."
3. **Never share your current CTC as a limit.** If pressed: "I'd rather anchor on the market rate for this scope — my current comp reflects a role with a much narrower remit."
4. **Get competing offers deliberately.** Cluster your Tier A and Tier B onsites into the same 3-week window in Months 7–8. One offer in hand is worth more than any argument you can make.
5. **Negotiate the whole package:** base, variable/bonus %, equity (ask about strike price, vesting, refreshers, and the last valuation), joining bonus, notice-period buyout, remote/hybrid terms, and level. **Level is the highest-leverage item** — it sets your ceiling for the next three years, and one level is often worth more than any base bump you can win.
6. **Always ask once, politely, after the offer:** "I'm excited about this. Is there flexibility on <one specific item>?" Most companies have 10–15% of headroom and expect the question.
7. **Get it in writing before resigning.** Always.

### Reading a comp number in India

- **Fixed vs total:** ₹50L "CTC" often includes a 15–20% variable, joining bonus amortised, and RSUs at a stale valuation. Ask for the fixed number and the vesting schedule separately.
- **RSUs at a public company** are close to cash on vest (subject to price risk). **Startup equity** is a lottery ticket — value it near zero unless you understand the preference stack and the last round's terms.
- **Retention/joining bonuses** are one-time. Don't let them inflate the number you compare year two against.

---

## 21. Final scorecard — Day 240

| Area | Target | Evidence it's real |
|---|---|---|
| DSA problems | 220–250 quality problems | Log with pattern notes; 240 is the plan's cumulative number |
| SQL | 75+ meaningful queries, incl. window functions and `EXPLAIN` analysis | Query notebook in the notes repo |
| System designs | 30+ written | `system-design-notes/`, each with capacity numbers and failure modes |
| LLD / code design | 15+ | Refactorings and class designs in the notes repo |
| Backend project | 1, deep, deployed | Project 1 with load-test numbers |
| RAG projects | 1 deep + capstone integration | Project 2 with golden-set metrics |
| Distributed project | 1, with chaos results | Project 3 with the failure-modes document |
| AI platform | 1 capstone | Project 4 deployed, demoed, documented |
| AWS | Production deployment with IaC | Terraform in the repo; live URLs |
| Docker | Strong | Multi-stage, non-root, <200MB images, healthchecks |
| Kubernetes | Working knowledge | Manifests for at least one service; can explain probes and resource limits |
| Kafka | Production-style project | Project 3 + chaos experiment results |
| PostgreSQL | Strong | Reproduced isolation anomalies; index tuning with `EXPLAIN` evidence |
| Redis | Strong | Caching, rate limiting with Lua, locks with fencing awareness |
| Python | Strong | Async, generators, decorators, context managers used deliberately in real code |
| ML fundamentals | Solid | 5 models trained honestly; metrics chosen for a stated cost model |
| PyTorch | Working knowledge | Training loop written from scratch; model served with batching |
| Transformers | Strong conceptual + implemented | Your from-scratch transformer that generates text |
| Inference | **Differentiator** | Published benchmark: quantisation × batching × latency/throughput/cost |
| RAG | Very strong | Hybrid + rerank + evals + CI gate, with measured lift |
| Agents | Strong | Durable state, ceilings, HITL, tracing |
| MCP | Working + project | Server and client, secured |
| AI evaluation | Strong | Golden sets, CI gate, failure taxonomy |
| AI security | Strong | Red-team suite with before/after numbers |
| Observability | Working | Traces, cost per tenant, golden signals, real alerts |
| Mock interviews | 20–30 | Recorded; feedback logged |
| Public writing | 8 posts | One per month |
| Applications | 400+ over Days 75–240 | Tracker |
| Interviews | 30+ | Tracker, with rejection reasons |

### If you're behind on Day 120 (you probably will be — this is normal)

Cut in this order, and never the other way round:

1. **Cut breadth, keep depth.** Skip CNNs (Day 178), skip encoder deep-dives, skip PACELC nuance. Never skip DSA or the projects.
2. **Cut a project's scope, never a project.** Project 3 with 3 workers instead of 6 still teaches Kafka and idempotency. Zero distributed projects teaches nothing.
3. **Cut Month 6 depth before Month 7 depth.** Classical ML is nice-to-have; inference optimisation is your differentiator.
4. **Never cut:** DSA cadence, the application cadence, and the four projects existing at all.

### The single highest-leverage thing in this document

Everything on Day 240 traces back to two habits:

1. **You produced an artefact every single day.** 240 artefacts is a portfolio; 240 days of reading is a feeling.
2. **You started applying on Day 75.** Interviewing is a separate skill from engineering, trained separately, and 165 days of reps is what makes the last 30 days convert.

Everything else in these 21 sections is detail.
