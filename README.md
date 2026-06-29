### Jonathan Gadea Harder

Software engineer — systems, ML infrastructure, and performance engineering.
Rust · Python · Go. Currently building training & inference infrastructure on Apple Silicon (MLX).

I care about code other engineers want to build on: small, tested, measured. The repos below
lead with numbers, not adjectives.

**Performance engineering**
- [par-vs-batch-bench](https://github.com/Jonathangadeaharder/par-vs-batch-bench) — LLM inference throughput / latency / memory study (MLX). On an 8B model, batching reaches **4.3× throughput at +8% memory**; process-parallelism only **1.34× at +300%** (weights replicated). Includes the methodology to make the numbers honest (per-shape warmup, forced eval, median repeats).
- [mlx-train-scaling](https://github.com/Jonathangadeaharder/mlx-train-scaling) — transformer training-loop scaling. Gradient accumulation grows the effective batch **4× at +2–7% memory** (vs ~linear for a real batch) — but only if gradients are realized each micro-step; the lazy-eval trap costs +43% peak otherwise.

**Systems & developer tooling** (Rust / Go)
- [structurelint](https://github.com/Jonathangadeaharder/structurelint) — architecture & dependency linting (Go).
- [pytest-linter](https://github.com/Jonathangadeaharder/pytest-linter) · [vitest-linter](https://github.com/Jonathangadeaharder/vitest-linter) · [cargo-test-lint](https://github.com/Jonathangadeaharder/cargo-test-lint) — static analysis for test quality across Python, JS, and Rust.
- [agentalign](https://github.com/Jonathangadeaharder/agentalign) — config-unification engine across AI coding tools (Rust).

**ML inference**
- [mlx-subtitler](https://github.com/Jonathangadeaharder/mlx-subtitler) — transcription, translation, and subtitle generation on Apple Silicon (MLX).

**Infrastructure**
- [runner-infra](https://github.com/Jonathangadeaharder/runner-infra) — self-hosted GitHub Actions runner fleet: launchd plists, bootstrap, health monitoring.
