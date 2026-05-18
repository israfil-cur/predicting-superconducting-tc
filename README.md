Predicting Superconducting Critical Temperature with Machine Learning
Motivation
In 2024, severe flooding hit Dagestan, Russia. Local officials attributed part of the infrastructure damage to degraded electrical wiring — cables that wear out, overheat, and fail under stress.
That event made me ask a question: what if electrical grids didn't lose energy at all?
Superconductors — materials that conduct electricity with zero resistance — could be the answer. They don't overheat, they don't degrade the same way, and they could make power infrastructure dramatically more reliable. The problem is that most superconductors only work at extremely low temperatures, making them impractical for real-world use.
Finding materials with a high critical temperature (Tc) — the temperature below which superconductivity kicks in — is one of the most important open problems in modern physics and materials science. This project uses machine learning to predict Tc from material descriptors, as a first step toward building a screening pipeline for promising superconducting candidates.

Dataset
The project uses a real-world superconductivity dataset containing engineered numerical descriptors (atomic mass, electron affinity, valence, etc.) and the target variable critical_temp (in Kelvin).

21,263 samples
81 engineered features
Source: UCI Machine Learning Repository — Superconductivity Data


Models Tested
ModelNotesLinear RegressionBaselineRidge RegressionRegularized linear modelDecision Tree RegressorNonlinear, interpretableRandom Forest RegressorBest overall performanceGradient Boosting RegressorStrong ensemble methodXGBoost RegressorOptimized boosting

Results
Random Forest achieved the best performance:
MetricValueR² (test set)~0.92RMSE~9.5 K
The results confirm that the relationship between material descriptors and critical temperature is strongly nonlinear — tree-based ensemble methods significantly outperform linear models.

Additional Analysis

Feature importance — identified which material descriptors drive Tc predictions most
Correlation analysis — explored relationships between features and target
Target distribution visualization — most superconductors cluster at low Tc, with a long tail
PCA-based feature-space visualization — reduced dimensionality to visualize material clustering


Key Takeaway
ML can meaningfully predict superconducting critical temperature from material descriptors. This kind of model could serve as an early-stage screening tool — quickly filtering thousands of candidate materials before expensive laboratory synthesis. Combined with future quantum simulation methods, this approach may accelerate the discovery of room-temperature superconductors.

What I Learned

Ensemble methods handle nonlinear physical relationships much better than linear models
Feature engineering matters enormously — raw composition alone is not enough
Real scientific datasets are messy and require careful preprocessing
Framing a physical problem as an ML task requires understanding both domains


Future Work

Add deep learning models (MLP, Graph Neural Networks for molecular structure)
Explore quantum ML approaches for feature encoding
Incorporate crystal structure data for richer representations
Compare against recent LLM-based materials science models


File

predicting_critical_temperature_ml.ipynb — main project notebook


Built by a 10th-grade student from Dagestan, Russia, interested in the intersection of quantum physics and machine learning
