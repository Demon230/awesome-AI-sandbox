# Awesome AI Sandboxing

> A curated list of projects, tools, and references for running AI agents inside safer execution environments, with a focus on open-source solutions.

AI coding agents are useful precisely because they can read files, run commands, install packages, open network connections, and modify code. That also makes them risky. This list focuses on projects that reduce that risk with OS sandboxes, separate user accounts, virtual machines, containers, policy engines, and related guardrails.

## Contents

- [macOS-native sandboxes](#macos-native-sandboxes)
- [Virtual machines and disposable environments](#virtual-machines-and-disposable-environments)
- [Container and runtime sandboxes](#container-and-runtime-sandboxes)
- [Foundational sandbox tools](#foundational-sandbox-tools)
- [Permission and policy guardrails](#permission-and-policy-guardrails)
- [Deprecated and archived projects](#deprecated-and-archived-projects)
- [References](#references)

## macOS-native sandboxes

- [Agent Safehouse](https://github.com/eugene1g/agent-safehouse) - Deny-first macOS sandboxing for coding agents using composable `sandbox-exec` profiles, policy builder tooling, and audited profile fragments.
- [ClodPod](https://github.com/webcoyote/clodpod) - Runs AI agents inside a macOS VM while mapping one or more host project directories into the guest for isolated development.
- [SandVault](https://github.com/webcoyote/sandvault) - Runs Claude Code, OpenAI Codex, Gemini, and shell commands in a sandboxed macOS user account with a shared workspace and optional `sandbox-exec` hardening.
- [yoloAI](https://github.com/kstenerud/yoloai) - Sandboxed runner for AI coding agents that can use `sandbox-exec` on macOS, Tart on Apple Silicon, or Docker, with a review-and-apply workflow based on diffs and commits.
- [agent-sandbox.nix](https://github.com/archie-judd/agent-sandbox.nix) - Nix-based wrappers for sandboxing AI CLI tools with explicit package, state, and optional domain-level network allowances.
- [nixcage](https://github.com/hamidr/nixcage) - Sandboxed Nix environments with direnv auto-activation. Cross-platform: bwrap on Linux, sandbox-exec on macOS.
- [sandbox-shell](https://github.com/agentic-dev3o/sandbox-shell) - macOS Seatbelt sandbox CLI with deny-by-default filesystem isolation for developer and agent workflows.
- [agentbox](https://github.com/gbrindisi/agentbox) - Agent Safehouse – macOS-native sandboxing for local agents
- [agentfs](https://github.com/tursodatabase/agentfs) - macOS's Little-Known Command-Line Sandboxing Tool (2025)
- [ansible](https://github.com/debops-contrib/ansible-firejail) - Agent Safehouse – macOS-native sandboxing for local agents
- [bvisor](https://github.com/butter-dot-dev/bvisor) - macOS's Little-Known Command-Line Sandboxing Tool (2025)
- [claude](https://github.com/trailofbits/claude-code-devcontainer) - Agent Safehouse – macOS-native sandboxing for local agents
- [clawvisor](https://github.com/clawvisor/clawvisor) - Agent Safehouse – macOS-native sandboxing for local agents
- [deepclause](https://github.com/deepclause/deepclause-sdk) - Agent Safehouse – macOS-native sandboxing for local agents
- [firejail](https://github.com/chiraag-nataraj/firejail-profiles) - Agent Safehouse – macOS-native sandboxing for local agents
- [firetools](https://github.com/netblue30/firetools) - Agent Safehouse – macOS-native sandboxing for local agents
- [firewarden](https://github.com/pigmonkey/firewarden) - Agent Safehouse – macOS-native sandboxing for local agents
- [sacre_bleu](https://github.com/hsaliak/sacre_bleu) - Agent Safehouse – macOS-native sandboxing for local agents
- [sandbox](https://github.com/carderne/sandbox-runtime) - Agent Safehouse – macOS-native sandboxing for local agents
- [sandnix](https://github.com/srid/sandnix) - Agent Safehouse – macOS-native sandboxing for local agents
- [shai](https://github.com/colony-2/shai) - macOS's Little-Known Command-Line Sandboxing Tool (2025)
- [yolobox](https://github.com/finbarr/yolobox) - macOS's Little-Known Command-Line Sandboxing Tool (2025)
- [treebeard](https://github.com/divmain/treebeard) - Agent Safehouse – macOS-native sandboxing for local agents
- [vibebox](https://github.com/robcholz/vibebox) - Show HN: VibeBox – an ultrafast macOS sandbox for AI agents
## Virtual machines and disposable environments

- [Chamber](https://github.com/cirruslabs/chamber) - Runs Claude or Codex inside ephemeral Tart macOS VMs with the current directory mounted, aimed at safer YOLO-mode agent execution.
- [Cleanroom](https://github.com/buildkite/cleanroom) - Self-hosted microVM sandbox for untrusted code with deny-by-default egress policy, repository-scoped allowlists, and host-side credential proxying.
- [ClodPod](https://github.com/webcoyote/clodpod) - macOS VM workflow for local Apple-platform development with Xcode and multiple mapped projects.
- [smolVM](https://github.com/smol-machines/smolvm) - Runs local microVMs for sandboxed workloads, with both ephemeral sandbox mode and persistent Linux VMs for isolated agent execution.
- [Sculptor](https://github.com/imbue-ai/sculptor) - Desktop app for running parallel Claude agents in isolated containers and pairing with their environments to test and merge changes.
- [yoloAI](https://github.com/kstenerud/yoloai) - Supports disposable Tart-backed sandboxes on macOS alongside other backends.
- [zapcode](https://github.com/TheUncharted/zapcode) - TypeScript interpreter for AI agents. Written in Rust. 2µs cold start. Sandboxed. Alternative to MCP tool calling.
- [BoxLite](https://github.com/boxlite-ai/boxlite) - Embeddable agent sandboxing with persistent state, snapshots, and hardware isolation.
- [K7](https://github.com/Katakate/k7) - Self-hosted infrastructure for lightweight VM sandboxes with CLI, API, and Python SDK support.
- [firecracker](https://github.com/avkcode/firecracker-sandbox) - Sandboxing Like a Pro in the Age of GasTown
- [firecracker](https://github.com/firecracker-microvm/firecracker-go-sdk) - Sandbox: Run untrusted AI code safely, fast
- [firecracker](https://github.com/hhtpcd/firecracker-sandbox) - Sandbox: Run untrusted AI code safely, fast
- [lima](https://github.com/recodelabs/lima-devbox) - Show HN: Lima-devbox – Claude skill for creating a VM dev sandbox on your Mac
- [nervos](https://github.com/ashishgituser/nervos) - Show HN: NervOS – Sandbox for AI Agents Using Firecracker MicroVMs
- [python](https://github.com/okeso/python-firecracker) - Cloudflare Sandbox SDK
- [zapcode](https://github.com/theuncharted/zapcode) - Zapcode: A TypeScript interpreter in Rust for AI agents (2µs start, sandbox)
## Container and runtime sandboxes

- [AIO Sandbox](https://github.com/agent-infra/sandbox) - All-in-one sandbox environment that combines browser, shell, file APIs, VS Code server, Jupyter, and MCP services in a single Docker container.
- [ClaudeBox](https://github.com/RchGrav/claudebox) - Docker-based Claude Code environment with per-project isolation, development profiles, persistent state, and firewall allowlists.
- [Kilntainers](https://github.com/Kiln-AI/Kilntainers) - MCP server that gives each agent an isolated ephemeral Linux sandbox backed by Docker, Podman, cloud microVMs, or WebAssembly.
- [sandbox-run](https://codeberg.org/Grauwolf/sandbox-run) - Lightweight `bubblewrap` wrapper for sandboxing development tools with per-project isolation for writes, temporary files, and session history.
- [sandclaude](https://github.com/binwiederhier/sandclaude) - Opinionated Docker wrapper for running Claude Code without restrictions inside a sandboxed container with mounted workspace and host-matched user IDs.
- [vibebin](https://github.com/jgbrwn/vibebin) - Incus/LXC-based platform for self-hosting persistent AI coding agent sandboxes on a Linux server with HTTPS routing, SSH access, and per-container tooling.
- [cco](https://github.com/nikvdp/cco) - Thin wrapper that launches Claude Code or Codex inside native OS sandboxes when available, with Docker as a stronger fallback barrier.
- [bunkervm](https://github.com/ashishgituser/bunkervm) - BunkerVM is a tiny operating system that boots in 2 seconds and gives AI agents a safe, isolated Linux machine to work in. Install it with one command. No Docker. No cloud. No config files.
- [Amazing Sandbox](https://github.com/ashishb/amazing-sandbox) - Runs third-party tools and AI agents securely on your machine.
- [EdgeBox](https://github.com/BIGPPWONG/EdgeBox) - Local GUI-powered sandbox for LLM agents with MCP support and a full desktop environment.
- [Fence](https://github.com/Use-Tusk/fence) - Container-free command sandbox with network and filesystem restrictions.
- [Greywall](https://github.com/GreyhavenHQ/greywall) - Local agent sandbox with live network controls and visibility via GreyProxy.
- [Matchlock](https://github.com/jingkaihe/matchlock) - Linux-based sandbox for securing AI agent workloads.
- [Microbox](https://github.com/HQarroum/microbox) - Lightweight ephemeral sandboxes for Linux workloads.
- [Nono](https://github.com/always-further/nono) - Kernel-enforced sandbox CLI and SDKs for AI agents with capability-based isolation and auditability.
- [Pent](https://github.com/valentinradu/Pent) - Runs untrusted processes with filesystem and network restrictions using native OS primitives.
- [Sandbox Runtime](https://github.com/anthropic-experimental/sandbox-runtime) - Lightweight OS-level sandboxing for filesystem and network restrictions without containers.
- [SkillSandbox](https://github.com/theMachineClay/skillsandbox) - Capability-based sandbox runtime for AI agent skills.
- [agentbox](https://github.com/rcarmo/agentbox) - Notes for January 19-25 (My Coding Agent Sandboxing Setup)
- [agentsafe](https://github.com/sarthak30/agentsafe) - Show HN: AgentSafe – per-task micro-VM sandbox for AI agents (Go)
- [ash](https://github.com/ash-ai-org/ash-ai) - Building secure, scalable agent sandbox infrastructure
- [bouvet](https://github.com/vrn21/bouvet) - Built a Sandbox for Agents in Rust
- [boxed](https://github.com/akshayaggarwal99/boxed) - Show HN: Boxed – Sovereign exec engine for AI agents (Vercel Sandbox inspired)
- [boxlite](https://github.com/boxlite-labs/boxlite) - BoxLite Love AI agent – SQLite for VMs: embeddable AI agent sandboxing
- [cagent](https://github.com/noperator/cagent) - Let's discuss sandbox isolation
- [claude](https://github.com/tech-and-ai/claude-rule-enforcer) - Claude Code escapes its own denylist and sandbox
- [co](https://github.com/paulkinlan/co-do) - The Browser Is the Sandbox
- [coderunner](https://github.com/instavm/coderunner) - Sandbox: Run untrusted AI code safely, fast
- [codex](https://github.com/paulux84/codex-lockbox) - Run Codex CLI in a firewalled Docker sandbox
- [conch](https://github.com/sd2k/conch) - Show HN: Amla Sandbox – WASM bash shell sandbox for AI agents
- [construct](https://github.com/estebanforge/construct-cli) - Observed Agent Sandbox Bypasses
- [edgebox](https://github.com/bigppwong/edgebox) - Show HN: EdgeBox – A local sandbox that gives your LLM agent a full GUI desktop
- [fence](https://github.com/use-tusk/fence) - Show HN: Fence – Sandbox CLI commands with network/filesystem restrictions
- [forgemax](https://github.com/postrv/forgemax) - Code Mode inspired local sandboxed MCP Gateway
- [greywall](https://github.com/greyhavenhq/greywall) - Show HN: Userland local agent sandbox with real-time network control dashboard
- [gvisor](https://github.com/google/gvisor) - Sandboxing AI agents at the kernel level
- [k7](https://github.com/katakate/k7) - Cloudflare Sandbox SDK
- [libkrun](https://github.com/containers/libkrun) - Show HN: Era – Open-source local sandbox for AI agents
- [litterbox](https://github.com/gerharddc/litterbox) - A deep dive on agent sandboxes
- [microbox](https://github.com/hqarroum/microbox) - Show HN: Lightweight, Ephemeral, Sandboxes for Linux
- [microsandbox](https://github.com/zerocore-ai/microsandbox) - The Sandbox Explosion
- [omniglass](https://github.com/goshtasb/omniglass) - Show HN: OmniGlass – An open-source, sandboxed Visual Action Engine
- [packnplay](https://github.com/obra/packnplay) - Matchlock – Secures AI agent workloads with a Linux-based sandbox
- [pent](https://github.com/valentinradu/pent) - Show HN: Pent – A sandbox for AI agents
- [qonqrete](https://github.com/illdynamics/qonqrete) - Show HN: QonQrete – Local-first multi-agent system for sandboxed code generation
- [runbox](https://github.com/sahilb315/runbox) - Show HN: Minimal container-like sandbox built from scratch in C
- [sbox](https://github.com/cvpaul/sbox) - Show HN: Sbox – zero intelligence, pure isolation sandbox
- [selenai](https://github.com/almclean/selenai) - Show HN: SelenAI – Terminal AI pair-programmer with sandboxed Lua tools
- [shannot](https://github.com/corv89/shannot) - Observed Agent Sandbox Bypasses
- [skillsandbox](https://github.com/themachineclay/skillsandbox) - Show HN: SkillSandbox – Capability-based sandbox for AI agent skills (Rust)
- [smith](https://github.com/sibyllinesoft/smith-core) - Run NanoClaw in Docker Sandboxes
- [tsk](https://github.com/dtormoen/tsk) - Show HN: TSK – agent sandbox, delegation, and parallelization tool
- [voratiq](https://github.com/voratiq/voratiq) - YOLO in the Sandbox
- [vtcode](https://github.com/vinhnx/vtcode) - Show HN: VT Code – LLM-agnostic coding agent with MCP/ACP and sandboxed tools
- [yourownpersonaljean](https://github.com/waynecider/yourownpersonaljean-luc) - Show HN: YOPJ – Local AI coding agent with 8-layer security sandbox (no cloud)
- [workmux](https://github.com/raine/workmux) - Sandboxed Git worktrees for AI coding agents
## Foundational sandbox tools

- [bubblewrap](https://github.com/containers/bubblewrap) - Low-level Linux sandbox builder that creates restricted environments via namespaces and filesystem layout controls; used by higher-level tools to define their own security model.
- [Firejail](https://github.com/netblue30/firejail) - Lightweight Linux sandbox program using namespaces, seccomp-bpf, capabilities, and bundled profiles to restrict untrusted applications.
- [Minijail](https://github.com/google/minijail) - Sandboxing and containment tool used in ChromeOS and Android, providing both a launcher for sandboxed processes and a library for self-sandboxing.
- [syd](https://git.sr.ht/~alip/syd) - Linux application sandboxing tool that intercepts system calls in userspace and combines mechanisms like Landlock, namespaces, ptrace, and seccomp into a secure-by-default containment model.

- [bubblewrap](https://github.com/reubenfirmin/bubblewrap-tui) - Bui – TUI for painless Bubblewrap sandboxing
- [island](https://github.com/landlock-lsm/island) - Island: Linux sandboxing tool powered by Landlock
## Permission and policy guardrails

- [Agent Safehouse](https://github.com/eugene1g/agent-safehouse) - Includes reusable least-privilege policy composition for running agents with fewer blanket permissions.
- [Cupcake](https://github.com/eqtylab/cupcake) - Policy enforcement layer for coding agents that evaluates hook events against OPA/Rego rules and can allow, modify, block, warn, or require review.
- [cco](https://github.com/nikvdp/cco) - Useful when the goal is to keep an agent in fast autonomous mode while interposing a sandbox boundary.
- [nah](https://github.com/manuelschipper/nah) - Context-aware Claude Code permission guard that classifies tool calls by action type and applies deterministic allow, ask, or block policies.
- [predicate-secure](https://github.com/PredicateSystems/predicate-secure) - Policy-based authorization wrapper for AI agents that adds pre-action guardrails, post-execution verification, and auditability across frameworks like Playwright, LangChain, and PydanticAI.
- [punkgo-jack](https://github.com/PunkGo/punkgo-jack) - Hook adapter for Claude Code and custom agents that records actions in an append-only Merkle log with cryptographic receipts and offline-verifiable session proofs.

- [sucoder](https://github.com/ligon/sucoder) - Sucoder: Sandbox for coding agents based on Unix filesystem permissions
## Deprecated and archived projects

- [Claude Code Sandbox](https://github.com/textcortex/claude-code-sandbox) - Archived Docker-based proof of concept for running Claude Code autonomously in isolated containers with a web UI and Git workflow integration.

## References

- [Awesome Sandbox](https://github.com/restyler/awesome-sandbox) - Survey of sandboxing technologies and platforms, including AI-oriented runtimes.
- [Awesome Agent Sandboxes](https://github.com/arjan/awesome-agent-sandboxes) - A curated list of code-execution sandboxing solutions for AI/LLM agents.
- [Hacker News discussion: Agent Safehouse](https://news.ycombinator.com/item?id=47301085) - Discussion that surfaced several current approaches to local agent isolation, including SandVault and yoloAI.
- [Hacker News discussion: Let's discuss sandbox isolation](https://news.ycombinator.com/item?id=47184049) - Practitioner discussion comparing user-account isolation, VMs, `bubblewrap`, and other models.
- [Hacker News thread 47343927](https://news.ycombinator.com/item?id=47343927) - Additional recent context on permission systems and the limits of coarse allow-or-deny prompts.

## Contributing

Suggestions and pull requests are welcome. Favor projects that are specifically about isolating, constraining, or safely operating AI agents, especially tools with a clear security model and practical documentation.
