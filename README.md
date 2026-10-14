# AI Risk Register: VoiceAssist Voice Bot (Financial Services)

A risk register for an AI-powered voice bot, with each risk scored, assigned an owner, and mapped to the NIST AI 600-1 framework.

> Completed as part of a Coursera governance and compliance course. The company, system, and data are fictional.

## Problem
A fictional financial services firm plans to launch an AI voice bot that handles customer account questions and employee HR requests. It connects to the customer CRM system and to HR data. Before go-live, what could go wrong, and who should fix it?

## What I did
- Identified 7 risks across three categories: Data, Model, and Usage.
- Mapped each risk to a specific NIST AI 600-1 category, such as Confabulation, Information Security, and Data Privacy.
- Scored each risk with Likelihood × Impact (1 to 5 each), using the scoring rubric.
- Assigned each risk to the role that matches its category (for example, the ML Engineering Lead for model risks).
- Wrote a specific mitigation action for every risk, with the owner and a target date.
- Added a Data risk and a Model risk for the same bias problem, because the cause (training data) and the effect (model behavior) have different owners.

## Results

| Risk | NIST AI 600-1 category | Score | Level |
|---|---|---|---|
| RISK-002: Outdated loan interest rates in answers | Confabulation | 20 | Critical |
| RISK-004: GDPR and HIPAA obligations not yet covered | Data Privacy | 20 | Critical |
| RISK-001: Lower accuracy for rural and non-native English speakers | Harmful Bias and Homogenization | 16 | High |
| RISK-003: No protection against prompt injection | Information Security | 16 | High |
| RISK-006: No human escalation for high-stakes queries | Human-AI Configuration | 16 | High |
| RISK-007: Training data excludes rural and non-native speakers | Harmful Bias and Homogenization | 16 | High |
| RISK-005: Unreviewed encryption between voice bot and CRM | Data Privacy | 12 | High |

Critical risks (score 17 to 25) are escalated to the AI Governance Board.

## Key lessons
- A risk's category is where it shows up, not where it starts. Biased training data (Data) causes biased answers (Model), and each needs its own owner.
- Evidence should change the score. The outdated interest rates were seen in testing, so the likelihood is 5, not 4.
- A mitigation note is only useful if it says what will be done, by whom, and by when.

## What I would add next
- Track compliance risks in Microsoft Compliance Manager and model risks in the Azure Responsible AI Dashboard.
- From my SOC experience, add monitoring and alerting for prompt injection attempts, so misuse is detected quickly after launch.

## Files
- [AI_Risk_Register_VoiceAssist.pdf](AI_Risk_Register_VoiceAssist.pdf)
