<div align="center">

```
██╗   ██╗ █████╗ ███████╗██╗  ██╗    ██╗  ██╗ █████╗ ███████╗ █████╗ ██████╗ ███████╗
╚██╗ ██╔╝██╔══██╗██╔════╝██║  ██║    ██║ ██╔╝██╔══██╗██╔════╝██╔══██╗██╔══██╗██╔════╝
 ╚████╔╝ ███████║███████╗███████║    █████╔╝ ███████║███████╗███████║██████╔╝█████╗  
  ╚██╔╝  ██╔══██║╚════██║██╔══██║    ██╔═██╗ ██╔══██║╚════██║██╔══██║██╔══██╗██╔══╝  
   ██║   ██║  ██║███████║██║  ██║    ██║  ██╗██║  ██║███████║██║  ██║██║  ██║███████╗
   ╚═╝   ╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝    ╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝
```

### ML Engineer · GPU Systems · Agentic AI · Mumbai, India

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/yash-kasare-ai)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:yashnkasare16@gmail.com)
[![PyPI](https://img.shields.io/badge/PyPI-3775A9?style=flat-square&logo=pypi&logoColor=white)](https://pypi.org/project/docstream/)
![Profile Views](https://komarev.com/ghpvc/?username=YashKasare21&style=flat-square&color=6366f1)

</div>

---

## About

I build systems at the intersection of **GPU performance engineering** and **production LLM infrastructure** — from writing CUDA kernels in bare-metal C++ to shipping multi-agent pipelines that handle real workloads.

Currently a final-year B.E. student in AI & Data Science (CGPA 8.6/10) at VCET Mumbai, graduating 2026. Two internships in GenAI and DL. Open to **ML Engineering**, **GenAI Engineering**, and **MLOps** internship roles at AI-first companies.

```
What I care about:   Systems that are fast + correct + observable
What I avoid:        Toy demos and tutorial-rehash projects
Current obsession:   FlashAttention kernel optimization on T4/V100/A100
```

---

## Projects

### ⚡ FlashAttention CUDA Kernel
> *CUDA C++, WMMA Tensor Cores, Nsight Compute, PyTorch*

Custom FlashAttention forward pass from scratch — no cuDNN, no shortcuts.

- SRAM tiling + online softmax → memory complexity **O(N²) → O(N)**
- Eliminated 32-way shared memory bank conflicts via SMEM padding + `__ldg` cache loads
- WMMA fp16 Tensor Core ops → **2.42× speedup** validated on Tesla T4
- Full Nsight Compute profiling: compute SOL 8.5%, memory SOL 36% — memory-bound, improvements identified

[![Repo](https://img.shields.io/badge/View_Repo-181717?style=flat-square&logo=github)](https://github.com/YashKasare21/flashattention_cuda_kernel)

---

### 🤖 Auto-SWE-Agent
> *LangGraph, Claude API, LiteLLM, Docker Sandbox, ReAct Loop*

Autonomous software engineering agent that resolves real GitHub issues without human intervention.

- LangGraph ReAct loop + Claude API for planning and code generation
- Docker sandbox for safe bash execution and test isolation
- LiteLLM fallback chain: `Claude → Gemini 2.0 Flash → Groq Llama 3.3 70B` for resilience
- Eval harness benchmarks patches against unit-test assertions with autocorrection loops
- Validated on live DocStream Issue #13 (password-protected PDF bug)

[![Repo](https://img.shields.io/badge/View_Repo-181717?style=flat-square&logo=github)](https://github.com/YashKasare21/auto-swe-agent)

---

### 📄 DocStream
> *FastAPI, Next.js 14, PyMuPDF, Gemini 2.5 Flash, Groq, XeLaTeX, Docker, PyPI*

Open-source PDF ↔ LaTeX conversion engine. Published on PyPI. Running in production.

- 3-step pipeline: **PyMuPDF extraction → LLM skeleton fill → XeLaTeX compile** with automated figure insertion
- Multi-provider fallback chain: `Gemini 2.5 Flash → Groq Llama 3.3 → Kimi K2.5 (NVIDIA NIM) → Ollama`
- SSE streaming, plugin-style pipeline, Google OAuth, usage metering
- **99.9% uptime** across all providers via automatic failover

[![Repo](https://img.shields.io/badge/Monorepo-181717?style=flat-square&logo=github)](https://github.com/YashKasare21/docstream-new)
[![PyPI](https://img.shields.io/badge/PyPI_Package-3775A9?style=flat-square&logo=pypi&logoColor=white)](https://pypi.org/project/docstream/)

---

### 📈 AI Trading Bot
> *SAC, PPO, A2C, Stable-Baselines3, Optuna, LangChain, APScheduler, Telegram*

Personal NSE/Nifty50 EOD signal system with a hard viability gate before real capital.

- 80+ TA indicators + FFT + HMM + Gemini sentiment feeding a shared FeaturePipeline
- Ensemble RL inference: **A2C + PPO + RSI rule-based, 2-of-3 vote required**
- Walk-forward validation with expanding windows + Optuna hyperparameter tuning
- Paper trading requirement: 30 days, >52% win rate on HIGH confidence signals before live deployment

[![Repo](https://img.shields.io/badge/View_Repo-181717?style=flat-square&logo=github)](https://github.com/YashKasare21/trading_bot)

---

## Tech Stack

```python
stack = {
    "GPU / Systems":   ["CUDA C/C++", "WMMA Tensor Cores", "Nsight Compute", "SRAM Tiling"],
    "LLM / Agents":    ["LangGraph", "LangChain", "LlamaIndex", "Claude API", "LiteLLM", "RAG", "Ollama"],
    "ML / DL":         ["PyTorch", "HuggingFace Transformers", "Stable-Baselines3", "Optuna", "Scikit-learn"],
    "Backend":         ["FastAPI", "SQLAlchemy", "Docker", "GitHub Actions", "AWS Bedrock"],
    "Frontend":        ["Next.js 14", "React", "Vercel"],
    "Data":            ["PySpark", "FAISS", "ChromaDB", "MongoDB", "yfinance"],
}
```

---

## Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=YashKasare21&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=YashKasare21&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" />

</div>

---

## Experience

| Period | Role | Company | Key Work |
|--------|------|---------|----------|
| Jun–Aug 2025 | Data Science & DL Intern | Rogue Code | PyTorch/sklearn pipelines, Optuna tuning, CNN+Transformer training, +12% accuracy gain |
| Jun–Aug 2024 | GenAI Intern | VCET IIC | BERT+FAISS semantic search (2.7× recall), LangChain RAG pipeline, -40% hallucination rate |

---

## Education

**B.E. in Artificial Intelligence and Data Science** — VCET Mumbai · 2023–2026 · CGPA **8.6/10**

---

<div align="center">

*Open to ML Engineering / GenAI Engineering / MLOps internships at AI-first companies.*

**`yashnkasare16@gmail.com` · Mumbai, India**

</div>
