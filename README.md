# Research Portfolio

**Dr. Lebede Ngartera, Ph.D.**

Applied Mathematics | Probabilistic Machine Learning | Information Retrieval

ORCID: [0000-0003-0561-1305](https://orcid.org/0000-0003-0561-1305)

---

## Research Statement

My research addresses the fundamental challenge of uncertainty quantification in neural retrieval systems. Specifically, I develop Bayesian frameworks that provide calibrated confidence estimates for retrieval-augmented generation (RAG) architectures, enabling principled abstention under epistemic uncertainty. This work bridges probabilistic machine learning theory with practical information retrieval applications, contributing to more reliable AI systems in high-stakes domains.

---

## Selected Research Contributions

### Uncertainty-Aware Retrieval-Augmented Generation via Monte Carlo Dropout Ensembles

**Abstract**: We propose a Bayesian framework for quantifying predictive uncertainty in retrieval-augmented generation systems. By employing Monte Carlo Dropout at inference time, we obtain calibrated confidence intervals for retrieval relevance scores, enabling principled abstention when model uncertainty exceeds application-specific thresholds.

**Methodology**:
- Ensemble-based uncertainty decomposition (epistemic vs. aleatoric)
- Temperature-scaled calibration with Expected Calibration Error (ECE) optimization
- Threshold-based abstention mechanism grounded in decision theory

**Empirical Results**:

| Metric | Baseline (DPR) | Proposed Method | Relative Improvement |
|--------|----------------|-----------------|---------------------|
| P@3 | 0.412 | 0.497 | +20.6% |
| ECE | 0.156 | 0.114 | -26.8% (lower is better) |
| MRR@10 | 0.389 | 0.441 | +13.4% |

**Evaluation Protocol**: MS MARCO passage retrieval benchmark (Nguyen et al., 2016). 6,980 evaluation queries. Statistical significance verified via paired t-test (p < 0.01). Five-fold cross-validation with fixed random seeds.

**Status**: Preprint available. Under peer review.

**Code & Data**: [github.com/TeraSystemsAI/bayesian-rag-peer-review](https://github.com/TeraSystemsAI/bayesian-rag-peer-review)

---

## Methodological Rigor

### Reproducibility Statement

All experiments are fully reproducible. The repository includes:
- Complete source code under MIT license
- Configuration files with all hyperparameters
- Fixed random seeds (42, 123, 456, 789, 1011) for all stochastic components
- Hardware specifications (NVIDIA A100 40GB, CUDA 11.8)
- Evaluation scripts matching reported results within statistical variance

### Limitations and Scope

1. **Distributional Assumptions**: Monte Carlo Dropout provides an approximation to full Bayesian inference. In highly out-of-distribution scenarios, uncertainty estimates may be underestimated.

2. **Linguistic Scope**: Experiments conducted exclusively on English-language corpora. Cross-lingual generalization requires further investigation.

3. **Computational Overhead**: Ensemble methods introduce O(n) inference cost scaling, where n is ensemble size. Current implementation targets offline or batch processing; real-time deployment requires architectural optimization.

4. **Domain Transfer**: Calibration coefficients are dataset-specific. Application to new domains requires recalibration on held-out data.

---

## Research Agenda

### Current Investigations

1. **Calibrated Abstention in High-Stakes Domains**: Extending uncertainty-aware RAG to regulatory compliance (SR 11-7, EU AI Act) where false confidence carries material risk.

2. **Aleatoric-Epistemic Decomposition**: Disentangling irreducible data noise from reducible model uncertainty to inform targeted data collection strategies.

3. **Efficient Bayesian Approximations**: Investigating spectral-normalized neural networks and deterministic uncertainty quantification as computationally tractable alternatives to Monte Carlo methods.

### Open Research Questions

- How do calibration properties transfer across domain shifts in retrieval corpora?
- What theoretical guarantees can be established for abstention thresholds in RAG systems?
- Can uncertainty estimates improve active learning for retrieval model fine-tuning?

---

## Academic Background

| Degree | Field | Focus |
|--------|-------|-------|
| Ph.D. | Applied Mathematics | Probabilistic methods, statistical inference |

### Research Interests

- Probabilistic Machine Learning
- Bayesian Deep Learning
- Information Retrieval
- Uncertainty Quantification
- Natural Language Processing

---

## Technical Competencies

**Theoretical Foundations**: Bayesian inference, variational methods, information theory, statistical learning theory, calibration theory

**Methodologies**: Monte Carlo methods, ensemble learning, approximate Bayesian inference, conformal prediction

**Implementation**: PyTorch, Pyro (probabilistic programming), Hugging Face Transformers, pgvector, distributed training

---

## Scholarly Values

### Research Ethics

This research program adheres to principles of responsible AI development:

- **Transparency**: All methodological choices, hyperparameters, and negative results are documented.
- **Reproducibility**: Code, data, and evaluation protocols are publicly available.
- **Limitation Disclosure**: Known failure modes and scope boundaries are explicitly stated.
- **Dual-Use Awareness**: Uncertainty quantification methods are intended to improve AI reliability; misapplication to circumvent safety mechanisms is explicitly discouraged.

### Data Governance

- All experiments utilize publicly available benchmark datasets with documented provenance
- No personally identifiable information is collected, processed, or stored
- Synthetic data generation follows established privacy-preserving protocols

---

## Research Support

Funding enables continued investigation into Bayesian methods for reliable AI systems:

| Category | Purpose |
|----------|---------|
| Computational Resources | GPU cluster time for large-scale experiments |
| Benchmark Development | Curating domain-specific evaluation datasets |
| Open-Source Infrastructure | Maintaining reproducible codebases and documentation |

Institutional collaborations and research partnerships welcomed.

---

## Contact

| Channel | Address |
|---------|---------|
| Institutional | research@terasystems.ai |
| Direct | lebede@terasystems.ai |
| Professional Network | [LinkedIn](https://www.linkedin.com/in/lebede-ngartera-82429343) |
| Code Repository | [github.com/TeraSystemsAI](https://github.com/TeraSystemsAI) |
| Author Identifier | [ORCID 0000-0003-0561-1305](https://orcid.org/0000-0003-0561-1305) |

---

*Last updated: January 2026*

**Affiliation**: TeraSystemsAI | Independent Research
