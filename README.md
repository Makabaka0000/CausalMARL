# CCRPO

**Causal Contribution and Responsibility-Guided Preventive Policy Optimization for Safe Multi-Agent Reinforcement Learning**

> Research preview. The manuscript has not yet been accepted for publication.

CCRPO is a safe multi-agent reinforcement learning framework for cooperative on-ramp merging in mixed traffic. It identifies inter-vehicle interactions, rewards behaviors that benefit the team, and uses causal responsibility to guide preventive safety corrections during policy updates.

## Key Contributions

- **Uncertainty-aware causal graph inference.** Infer latent environmental context from interaction histories and propagate posterior uncertainty to dynamic causal edge estimates.
- **Causal contribution and responsibility attribution.** Combine counterfactual behavioral influence with team utility to assess cooperative contributions, and use graph-conditioned diffusion and counterfactual tail risks to identify the sources of avoidable risk.
- **Responsibility-guided preventive optimization.** Preserve a reserved safety margin, impose agent-specific risk-reduction requirements, and verify candidate policies within a KL trust region before accepting updates.
