# AI Infrastructure Engineer — 52-Week Roadmap (v2)
**Piyush Kumar | Full-Stack AI Systems → Compute Infrastructure → AI Systems**

---

## North Star

Become the kind of engineer who can design, debug, benchmark, and improve the systems underneath frontier AI.

**Starting position:** TypeScript/JavaScript, Python, SQL, MongoDB, Redis, Node.js, Spring Boot, Kafka, Docker, CI/CD, AWS EC2, and LLM/AI tooling — with shipped deterministic AI workflows, DeepEval-based validation, Redis-backed LLM interfaces, Elasticsearch search, and production integrations. CSE degree, 9.68 CGPA.


## Standing Rules

| Rule | How you operate |
|---|---|
| Time | Target 12–16 focused hours/week alongside your job. Increase on lighter weeks; never compensate with burnout. |
| DSA | 4 sessions/week. Solve fewer problems, but record the pattern, proof/intuition, complexity, and alternative approaches. |
| Systems | 3–4 sessions/week. Learn from a primary source, then implement or reproduce something measurable. |
| Build | 4–6+ hours/week on the active project. Every phase ends with a production-style artifact. |
| Writing | One technical note per week, written as if teaching another engineer. |
| Measurement | Every project has benchmark targets, failure tests, observability, and a short design doc. |
| AI learning | Prefer internals over framework-collecting. Know why the abstraction works before adopting it. |
| Math thread *(new)* | Weeks 1–13 only, 2–3 hrs/week — see Phase 1 math table. Builds the foundation that Phase 3–4 ML content assumes. |
| Paper cadence *(new)* | From Week 27 onward, Core Study includes at least one primary paper, not just docs. |
| Career | From Month 4 onward, track target roles and map each requirement to a project or skill. Include behavioral/narrative prep alongside technical prep, not just in Week 52. |
| Buffer/flex *(new)* | A missed or compressed week is not a failure. The monthly-review weeks below are legitimate places to absorb slippage — shift the plan forward rather than cramming. Protect DSA + Build first if a week is tight; Writing can slip a few days. |

**Why-this-matters (applies to all 52 weeks):** every week connects back to the AI infrastructure stack — reliability, scale, scheduling, performance, data movement, or hardware utilization.

**Weekly operating checklist (applies to all 52 weeks):**
☐ 4 DSA sessions completed; pattern, complexity, and mistakes recorded.
☐ Study completed from a primary source; concept explained aloud.
☐ Code/lab committed to Git with tests and measurements.
☐ One technical note written; one learning added to your personal knowledge base.

**Review cadence:** Monthly review at the end of every 4-week block. **Phase Gate** at the end of Weeks 13, 26, 39, and 52 — do not advance because the calendar says so; package the artifact, benchmark it, test failure modes, write the architecture, and identify remaining gaps.

### Weekly cadence
| Day | Primary work | Typical output |
|---|---|---|
| Mon | DSA + systems reading (+ math thread, Weeks 1–13) | 2 DSA problems + notes |
| Tue | Core systems / implementation | Code or lab |
| Wed | DSA + project | 2 DSA problems + feature |
| Thu | AI systems / paper | Experiment notes |
| Fri | DSA + project | 1–2 DSA problems + feature |
| Sat | Deep work block | 3–4 hr build/benchmark session |
| Sun | Review / write / rest | 1 technical note + weekly scorecard |

### The five tracks
- **DSA + algorithms** — interview strength and algorithmic thinking.
- **Systems** — Linux, networking, storage, OS, concurrency, distributed systems.
- **AI systems** — ML fundamentals, transformers, serving, inference, evaluation, post-training.
- **Career/build** — portfolio, open source, technical writing, interview prep, role mapping.
- **Math for ML** *(new, Weeks 1–13 only)* — the linear algebra, probability, and optimization theory that Phase 3–4 assumes.

### The 12-month architecture
| Phase | Weeks | Theme | Flagship output |
|---|---|---|---|
| 01 | 1–13 | Software + Computer Systems | High-performance Python service |
| 02 | 14–26 | Distributed Systems + Cloud | Fault-tolerant distributed scheduler |
| 03 | 27–39 | ML Systems + Model Serving | Model serving + evaluation platform (incl. post-training) |
| 04 | 40–52 | GPU + AI Infrastructure | Mini AI inference platform |

---

## Phase 1 (Weeks 1–13): Software + Computer Systems

| Wk | Theme | DSA | Core Study | Hands-On Lab | Definition of Done | Checkpoint |
|---|---|---|---|---|---|---|
| 1 | Baseline + Python systems mindset | Arrays/strings, 5–6 problems | Python data model docs; CPython overview | Mono-repo, benchmark harness, pytest, ruff/mypy, Docker | Baseline report + benchmark harness + 1-page career gap matrix | Explain the Python object model and Big-O without notes |
| 2 | Python under the hood | Hashing, maps/sets | Iterator protocol, decorators, context managers | Streaming pipeline via generators | Streaming parser + memory benchmark | Measure list vs. generator memory difference |
| 3 | Concurrency foundations | Stacks/queues, monotonic stack | asyncio docs; GIL concept | Async task runner, bounded concurrency | Throughput vs. concurrency benchmark | Explain when async helps and when it doesn't |
| 4 | Linux fundamentals | Linked lists, two pointers | *The Linux Programming Interface* chapters | Inspect processes/fds/memory in a container | Linux troubleshooting playbook | Find and explain a leaked file descriptor |
| **— Monthly review —** |
| 5 | Networking I | Binary search | Networking/HTTP docs | TCP client/server + HTTP benchmarker | Latency/throughput: reuse vs. new connections | Trace a request from DNS to response |
| 6 | Networking II | Trees intro, DFS/BFS | *High Performance Browser Networking* | Reverse proxy + TLS + health checks | Service diagram + failure scenarios | Explain timeout placement across a request path |
| 7 | Databases I | BSTs + traversals | PostgreSQL / database internals | Profile queries; add/remove indexes | Before/after query plan report | Predict when an index hurts |
| 8 | Databases II | Heaps + priority queues | MVCC/isolation docs | Simulate concurrent updates; inspect locks | Concurrency anomaly lab report | Explain lost update, dirty read, phantom read |
| **— Monthly review —** |
| 9 | Caching + memory | Hashmaps, LRU design | Redis docs, caching patterns | Layered cache; measure hit/miss | Cache strategy decision record | Design an anti-stampede strategy |
| 10 | Observability + profiling | Graphs BFS/DFS | OpenTelemetry; Brendan Gregg profiling material | Instrument + profile CPU/memory | Flame-graph-backed optimization PR | Prove one optimization with data |
| 11 | Systems design I | Shortest path, topo sort | *Designing Data-Intensive Applications* (selected) | Design your service for 10x load, on paper | 2-page architecture doc with numbers | Defend three trade-offs orally |
| 12 | Production hardening | DP fundamentals, 5 patterns | Google SRE workbook | Resilience layer + failure injection | Chaos/failure test report | Show system recovery under injected failures |
| **— Monthly review —** |
| 13 | **Phase 1 capstone** | Mixed timed, 10–12 problems | Review own notes | Finish high-performance Python service | GitHub release + arch doc + benchmarks + demo | **Phase gate:** explain every subsystem and benchmark |

### Math for ML thread (Weeks 1–13, ~2–3 hrs/week, runs alongside the table above)
| Wk | Topic |
|---|---|
| 1 | Vectors, matrices, matrix multiplication — build the intuition |
| 2 | Eigenvalues/eigenvectors, SVD intuition (why it matters for embeddings/PCA) |
| 3 | Probability basics — distributions, expectation, variance |
| 4 | Bayes' theorem, conditional probability |
| 5 | Derivatives, chain rule — why backpropagation works |
| 6 | Convexity, local vs. global minima, loss-landscape intuition |
| 7 | Gradient descent math — step size, convergence intuition |
| 8 | Statistics — sampling, confidence intervals, light hypothesis testing |
| 9 | Information theory — entropy, cross-entropy, KL divergence (loss functions) |
| 10 | Numerical stability — floating point, over/underflow, why fp16 causes issues |
| 11 | Linear algebra review + problem set |
| 12 | Optimization review — SGD variants, momentum, Adam intuition |
| 13 | **Math capstone** — mixed problem set without notes; connect each concept to a specific ML mechanism |

---

## Phase 2 (Weeks 14–26): Distributed Systems + Cloud

| Wk | Theme | DSA | Core Study | Hands-On Lab | Definition of Done | Checkpoint |
|---|---|---|---|---|---|---|
| 14 | Distributed systems mental model | Union-find, graph connectivity | DDIA distributed systems chapter | 3-node toy key/value service | Failure matrix | Explain why distributed bugs are different |
| 15 | Replication | Intervals + greedy | Dynamo paper (summary) | Primary/replica simulation | Read/write semantics doc | Design a consistency trade-off |
| 16 | Consensus | Backtracking | Raft paper | Simplified Raft simulator (not production) | State-machine diagrams | Explain split-brain prevention |
| **— Monthly review —** |
| 17 | Distributed logs + Kafka | Trie/string patterns | Kafka design docs | Run Kafka locally; worker consumers | Throughput/rebalance benchmark | Explain at-least-once + idempotency |
| 18 | Queues + backpressure | Heap/priority queue review | Queueing/backpressure articles | Rate-limited scheduler queue | Overload behavior benchmark | Show graceful degradation |
| 19 | Storage systems | Binary search variations | LevelDB/RocksDB material | Tiny log-structured KV store | Compaction benchmark | Explain write amplification |
| 20 | Sharding | Advanced graphs | DDIA partitioning chapter | Shard a task/state store | Rebalancing design | Explain hotspot mitigation |
| **— Monthly review —** |
| 21 | Kubernetes I | DP review | Kubernetes docs | Deploy scheduler skeleton to local K8s | Manifest repo + rollout demo | Explain control-plane basics |
| 22 | Kubernetes II | Mixed medium | K8s scheduler docs | Worker labels + scheduling policy | Scheduling policy demo | Explain bin-packing trade-offs |
| 23 | Cloud infrastructure | Graphs, timed | AWS architecture docs | Deploy w/ private/public boundaries | Cloud architecture diagram | Threat-model the deployment |
| 24 | SLOs + reliability | Greedy/intervals mixed | Google SRE workbook | Define SLOs + alerts; load-test | Reliability scorecard | Explain one SLO trade-off |
| **— Monthly review —** |
| 25 | Scheduler engineering | System-design coding | Cluster scheduling papers | Scheduler core w/ worker leases | Scheduling benchmark + fairness test | Prove fairness with a test |
| 26 | **Phase 2 capstone** | 12–15 mixed, timed | Review | Finish fault-tolerant scheduler | GitHub release + arch + incident report | **Phase gate:** kill nodes and recover correctly |

---

## Phase 3 (Weeks 27–39): ML Systems + Model Serving

| Wk | Theme | DSA | Core Study | Hands-On Lab | Definition of Done | Checkpoint |
|---|---|---|---|---|---|---|
| 27 | ML foundations | Graphs + DP mixed | *Dive Into Deep Learning* (selected) | Tiny linear/logistic regression from scratch | Notebook + intuition notes | Explain gradient descent geometrically |
| 28 | PyTorch fundamentals | Heaps/graphs | PyTorch docs | Train small model; profile data vs. compute | Training profile | Find one data bottleneck |
| **— Monthly review —** |
| 29 | Transformers I | Tree/graph mixed | *Attention Is All You Need* | Implement miniature self-attention | Attention visualization/benchmark | Derive attention dimensions |
| 30 | Transformers II | Strings + DP | Transformer papers + model docs | Toy autoregressive generation | KV cache memory estimate | Why KV cache changes latency/memory |
| 31 | Inference basics | Binary search/heap mixed | vLLM docs/papers | Benchmark an open model locally | Throughput vs. batch-size chart | Identify a serving bottleneck |
| 32 | Serving architecture | Scheduling problems | Serving systems articles + *Orca* paper *(added)* | Async inference gateway | P50/P95/P99 load test | Explain queue buildup |
| **— Monthly review —** |
| 33 | Quantization + memory | Mixed, timed | Quantization papers — GPTQ / LLM.int8 *(added)* | Experiment with a quantized model | Quality vs. latency vs. memory report | Choose precision for a stated constraint |
| 34 | RAG as a systems problem | Graph shortest paths | RAG survey / retrieval docs | Retrieval pipeline with cache | Recall/latency evaluation | Know where retrieval latency comes from |
| 35 | Evaluation infrastructure | DP + hashing | Your DeepEval experience, reframed as infra + *HELM* paper *(added)* | Eval runner + CI gate | Eval dashboard/report | Explain why eval is a deployment dependency |
| 36 | Observability for AI | System-design coding | OpenTelemetry + serving metrics docs | Instrument serving stack end-to-end | AI serving observability dashboard | Trace a request end-to-end |
| **— Monthly review —** |
| 37 | Distributed inference | Graphs, advanced | Megatron-LM concepts / distributed PyTorch | Simulate sharding across workers | Communication-cost model | Explain when each parallelism scheme fits |
| 38 | **[NEW] RLHF & post-training** | Mixed, timed | InstructGPT paper + DPO paper *(added)* | Implement a toy DPO loss on a small preference dataset, or trace an open RLHF implementation (e.g. `trl`) end-to-end | Post-training experiment report: base vs. preference-tuned toy outputs | Explain the difference between SFT, RLHF, and DPO |
| 39 | **Phase 3 capstone** | 12–15 mixed | Review | Finish serving + evaluation platform | Release + benchmarks + architecture + SLOs | **Phase gate:** defend architecture and benchmark results |

---

## Phase 4 (Weeks 40–52): GPU + AI Infrastructure

| Wk | Theme | DSA | Core Study | Hands-On Lab | Definition of Done | Checkpoint |
|---|---|---|---|---|---|---|
| 40 | GPU architecture | Mixed, 3 hard problems | CUDA programming guide intro | GPU profiling tools on a simple workload | GPU glossary + bottleneck notes | Compute-bound vs. memory-bound |
| **— Monthly review —** |
| 41 | CUDA mental model | Graphs + DP, hard | CUDA docs | First CUDA kernels (or simulator/Colab) | Kernel timing report | Explain coalesced memory access |
| 42 | GPU profiling | System-design coding | NVIDIA profiling materials | Profile matrix/vector ops; optimize one | Before/after profile | Optimization backed by measurement |
| 43 | Inference engines | Scheduling + heap | vLLM paper/docs | Trace vLLM architecture; build a mini scheduler | Scheduler design note | Explain paged KV cache |
| 44 | **[MERGED] High-performance communication & AI cluster networking** | Graph, hard set | NCCL docs + NVIDIA networking/HPC materials (merged from old Wk 44+45) | Model all-reduce cost across topologies, including RDMA/InfiniBand vs. standard networking | Combined latency/topology trade-off model | Explain why both topology and network path matter |
| **— Monthly review —** |
| 45 | **[NEW] Distributed training internals** | Mixed, hard | FSDP/ZeRO papers, DeepSpeed docs | Implement or simulate a sharded training loop; measure memory savings from gradient checkpointing + mixed precision | Memory/throughput comparison: data-parallel vs. sharded | Explain optimizer state sharding and when to use gradient checkpointing |
| 46 | Cluster scheduling | Scheduling + graph | Cluster scheduling research | Add a GPU resource model to the scheduler | GPU placement simulator | Demonstrate fragmentation |
| 47 | System software | DSA weak areas | Linux kernel/Ubuntu packaging docs | Reproducible machine-image/bootstrap workflow | Rebuild/recover a node in automation | Explain the host boot/provisioning path |
| 48 | **[MERGED] Deployment lifecycle & reliability at fleet scale** | Hard, mixed | MLOps deployment patterns + SRE/infra incident writeups (merged from old Wk 38+48) | Model registry + rollout controller, plus node health/quarantine/recovery | Canary/rollback demo + failure-injection matrix | Recover from a bad model deployment *and* from correlated failures |
| **— Monthly review —** |
| 49 | Performance engineering | Mock interview DSA **+ 1 behavioral/narrative mock** *(added)* | Google Benchmark / benchmarking guides | Benchmark suite for the inference platform | Performance regression CI | Trust your benchmark |
| 50 | Capstone integration | Mock interview: 45-min coding | Review all prior material | Integrate mini AI inference platform | Architecture review v1 | Identify the top 3 remaining bottlenecks |
| 51 | Open-source + public proof | Mock onsite: 2 problems + explanation | Project docs/source code | One real OSS contribution related to infra/ML systems | Merged PR, or documented attempt + follow-up issue | Can a stranger understand your work quickly? |
| 52 | **Final review + hiring package** | Full mock: coding + systems design **+ behavioral/narrative mock** *(added)* | Current target-company roles | Finish capstone, README, demo, benchmarks, design doc | Portfolio package + interview gap list + 90-day next plan | **Phase gate:** greenlight to apply, or a precise gap list |

---

## End-state capability matrix

| Capability | By Week 52 you should be able to... |
|---|---|
| Software engineering | Write production-quality Python and one systems language; profile, test, debug under load |
| Algorithms | Solve common DSA patterns fluently; communicate trade-offs under interview pressure |
| Math foundations *(new)* | Explain the linear algebra, probability, and optimization behind core ML mechanisms without notes |
| OS + Linux | Reason about processes, memory, filesystems, networking, provisioning, and system failures |
| Distributed systems | Design for partition, replication, consistency, retries, ordering, backpressure, and failure |
| Cloud + Kubernetes | Deploy, schedule, observe, and secure distributed workloads |
| ML systems | Explain training/inference differences, transformers, KV cache, batching, and serving |
| Post-training / alignment *(new)* | Explain RLHF, DPO, and reward modeling, and their systems implications |
| GPU systems | Understand GPU architecture, memory, kernels, profiling, and communication basics |
| AI infrastructure | Design an inference/compute platform around scheduling, reliability, performance, observability |
| Research collaboration | Read papers, inspect real code, turn ambiguous requirements into measurable systems |
| Career proof | Public artifacts, benchmarks, technical writing, and at least one meaningful OSS contribution |

