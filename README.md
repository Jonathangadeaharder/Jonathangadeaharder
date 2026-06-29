### Jonathan Gadea Harder

Software engineer — ML training & inference infrastructure, performance engineering.
Rust · Python · Go. I build training/inference systems on Apple Silicon (MLX) and care about
code other engineers want to build on: small, tested, measured. The repos below lead with
numbers, not adjectives.

**Model training & fine-tuning**
- [eurobert-lemmatizer](https://github.com/Jonathangadeaharder/german-spanish-english-eurobert-lemmatizer) — per-language EuroBERT-210m UPOS/lemma taggers (DE/ES/EN/FR), LoRA fine-tune + edit-tree lemmatization, **exported to ONNX** to run in-browser via Transformers.js. Held-out: ES **96.7%** UPOS / 96.2% lemma, DE 94.4/91.8, EN 93.1/94.1.
- [subtitle-correction](https://github.com/Jonathangadeaharder/subtitle-correction) — LoRA fine-tune (Gemma-4-E4B, MLX) that corrects Whisper subtitles against a reference, driven by a **dynamic active-learning loop**: evaluate → target exact failures → regenerate data → retrain.
- [mlx-train-scaling](https://github.com/Jonathangadeaharder/mlx-train-scaling) — training-loop scaling study: gradient accumulation = 4× effective batch at +7% memory; **data-parallel gradient all-reduce** (MLX distributed), replica-drift verified.

**Performance engineering**
- [par-vs-batch-bench](https://github.com/Jonathangadeaharder/par-vs-batch-bench) — LLM inference throughput/latency/memory. On 8B: batching **4.3× throughput at +8% memory**; process-parallelism only 1.34× at +300% (weights replicated).

**ML systems**
- [semantic-clone-detection](https://github.com/Jonathangadeaharder/semantic-clone-detection) — Type-4 (semantic) code-clone detection: GraphCodeBERT embeddings + FAISS ANN + **ONNX INT8**, multi-language via tree-sitter.
- [mlx-subtitler](https://github.com/Jonathangadeaharder/mlx-subtitler) — transcription, translation, and subtitle generation on Apple Silicon (MLX).

**Developer tooling** (Rust / Go)
- [structurelint](https://github.com/Jonathangadeaharder/structurelint) — architecture & dependency linting (Go).
- [pytest-linter](https://github.com/Jonathangadeaharder/pytest-linter) · [vitest-linter](https://github.com/Jonathangadeaharder/vitest-linter) · [cargo-test-lint](https://github.com/Jonathangadeaharder/cargo-test-lint) — static analysis for test quality across Python, JS, and Rust.
- [agentalign](https://github.com/Jonathangadeaharder/agentalign) — config-unification engine across AI coding tools (Rust).

**Infrastructure**
- [runner-infra](https://github.com/Jonathangadeaharder/runner-infra) — self-hosted GitHub Actions runner fleet: launchd plists, bootstrap, health monitoring.
