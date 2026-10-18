# Statement of Interest

**Seungyoon Woo** · Seoul National University · October 2026

## The problem

I want to study how an AI system stays human-compatible after it ships. Deployed models keep changing: developers and users fine-tune them, agents write to their own memory, and one assistant can serve many people for months. Each update gives the system a chance to drift from what its principals want, yet most safety evaluations happen once, before release. From continual learning, I expect this drift: models forget what they learned earlier unless training protects it. I want to treat alignment the same way, as something a system has to retain while it keeps learning.

## Direction 1: Alignment that survives further training

My working hypothesis is that safety training suppresses unwanted behavior more than it removes it, so a few later updates can bring that behavior back. Emergent misalignment, fine-tuning attacks, and memory poisoning all fit this picture. At CHAI I would test the hypothesis directly and build training methods that remove the behavior, using continual learning tools such as distillation from the model's own earlier policy.

Two current projects are my starting point. One compares four training-time defenses against emergent misalignment at matched task performance across three open model families. The other keeps an aligned base model, a safety adapter, and a third-party task adapter separate, joined by learned per-layer gates. Beyond these, I want a formal account of what an update must preserve for a system to keep acting on its principals' preferences, and a training-time check that it did.

## Direction 2: Assistants that serve many people over time

Assistance games model an AI that learns a person's preferences while helping them. Deployed assistants differ in two ways: they serve many people, and they remember. [Multi-principal assistance games](https://arxiv.org/abs/2007.09540) (Fickinger et al., 2020) address the first. Memory adds the second, because every session changes what the agent believes about each person.

I want to study agents whose memory spans many users and sessions. Such an agent has to keep each person's preferences separate, update them when they change, and stop one user from corrupting what it does for another. I am building a three-level memory hierarchy for long-horizon stability in this setting. At CHAI I would connect it to the assistance-game view: when should the agent revise its belief about a person, and how far should it defer when its own memory might be wrong?

## Background and fit

My Ph.D. research at Seoul National University, advised by Prof. Gunhee Kim, is in continual learning. *COMET* (NeurIPS 2026) separates distillation, routing, and capacity control so a vision-language model learns new tasks without task labels and forgets less. *Meta-Continual Learning of Neural Fields* (ICLR 2025) combines a modular architecture with meta-learning to reduce forgetting and speed up convergence. Both rely on the tools I now bring to safety: modular separation, distillation, and careful measurement of what a model keeps.

CHAI lists lifelong learning, decision making over long time scales, and the structure of human preferences among its research areas. I want to join those threads at CHAI and build AI that keeps learning from the people it serves while it keeps acting on what they want.
