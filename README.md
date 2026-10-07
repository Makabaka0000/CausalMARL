# CCRPO

**Causal Contribution and Responsibility-Guided Preventive Policy Optimization for Safe Multi-Agent Reinforcement Learning**

> Research preview. The manuscript has not yet been accepted for publication.

CCRPO is a safe multi-agent reinforcement learning framework for cooperative on-ramp merging in mixed traffic. It identifies inter-vehicle interactions, rewards behaviors that benefit the team, and uses causal responsibility to guide preventive safety corrections during policy updates.

## Key Contributions

- **Uncertainty-aware causal graph inference.** Infer latent environmental context from interaction histories and propagate posterior uncertainty to dynamic causal edge estimates.
- **Causal contribution and responsibility attribution.** Combine counterfactual behavioral influence with team utility to assess cooperative contributions, and use graph-conditioned diffusion and counterfactual tail risks to identify the sources of avoidable risk.
- **Responsibility-guided preventive optimization.** Preserve a reserved safety margin, impose agent-specific risk-reduction requirements, and verify candidate policies within a KL trust region before accepting updates.


## Selected Results

Results below are from the highway-env traffic-density experiments. Each setting uses three evaluation seeds with 100 test episodes per seed. Values report mean success and crash rates; higher success and lower crash rates are better.

| Traffic Density | Method | Success Rate (%) ↑ | Crash Rate (%) ↓ |
| --- | --- | ---: | ---: |
| Low | Safe-MAA2C | 83.33 | 2.33 |
| Low | **CCRPO** | **88.00** | **2.00** |
| Medium | Safe-MAA2C | 36.00 | 8.00 |
| Medium | **CCRPO** | **50.67** | **2.67** |
| High | Safe-MAA2C | 8.00 | 10.67 |
| High | **CCRPO** | **31.00** | **4.67** |

Under medium-density traffic, CCRPO improves success by **14.67 percentage points** and reduces crashes by **5.33 percentage points** compared with Safe-MAA2C.

Additional evaluations in CARLA and an NGSIM US-101 trajectory-driven merging environment support the framework's cooperative merging performance.
