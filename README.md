<<<<<<< HEAD
# Kinetic — Incentive Design Under Adversarial Conditions

A prototype demonstrating a contribution-gated information sharing system for 1,800 competing physiotherapy clinics.

## How to Run

Open `index.html` in any browser. No installation required. 'clinic-view.html' shows the clickable prototype.

---

## The Problem

Patients increasingly see multiple physiotherapists. Each clinic, however, treats them as a brand new patient. Intake forms are completed from the ground-up and prior injuries may be unmentioned or misremembered. Relevant treatment history is invisible. Clinics have asked for shared patient history, but their incentives are misaligned.

1,800 clinics where asked about sharing patient history:

- **71%** wanted to receive patient history from other clinics
- **19%** were willing to share their own
- **Primary fear:** *"I don't want to help patients switch to competitors."*
- **Secondary fear:** *"What if another physio judges my treatment?"*

Clinics want the benefit of a shared network without bearing any of the cost. The design task is to produce a system in which sharing becomes the selfish, rational choice, satisfying the clinic desire to have shared patient history.

---

## Game Theory Analysis of Patient Record Sharing

### 1 — The equilibrium is fixed at 19%

Each clinic makes two independent decisions: share (S) or not share (NS). Currently, this structure creates a classic dominant strategy problem that is collectively sub-optimal, even though it is individually rational. Regardless of what a competitor does, competitive actors prefer to withhold records. This avoids the cost of sharing while still being able to receive records.

> **Interactive payoff matrix with deviation arrows is in `index.html`.**

In the payoff matrix above, both clinics have an incentive to move toward "not sharing" (NS), if the competitor's position is fixed. Therefore, the system's stable resting point is NSNS.

If we take the survey data as intrinsic preference values:

- α = 0.19 (propensity to share) and,
- γ = 0.71 (propensity to receive) 

the stationary distribution in the ungated system is:

| State | Meaning | Probability |
|-------|---------|-------------|
| SR | Shares and receives | α × γ = **13.5%** |
| SNR | Shares, does not receive | α × (1−γ) = **5.5%** |
| NSR | Receives without sharing | (1−α) × γ = **57.5%** |
| NSNR | Neither | (1−α) × (1−γ) = **23.5%** |

> For a given clinic, the most likely position is NSR (57.5%), not sharing but still receiving patient records. It is the rational outcome in a competitive system. 

### 2 — Contribution-gating makes data-sharing the selfish option

The solution presented here is contribution-gated access: a clinic can only receive patient history if it shares its own.

> Sharing is becomes the selfish act, it is necessary to access a valuable resource. The question each clinic faces is no longer "should I help competitors?" but "how do I access data that makes me competitive?"

Once NSR is inaccessible, any clinic that wants to receive (71%) now has to share to get it:

| State | Meaning | Probability |
|-------|---------|-------------|
| SR | Shares and receives | γ = **71.0%** |
| SNR | Shares, does not receive | α × (1−γ) = **5.5%** |
| NSR | Eliminated by gating | **0%** |
| NSNR | Rational non-participants | (1−α) × (1−γ) = **23.5%** |

Assuming that sharing and receiving are independent motivators, this produces a total sharing of **76.5%**. In practice, however, a well-designed system would:

- **A:** Increase incentive to share and receive
- **B:** Make sharing more attractive when more data is available
- **C:** Factor in competition between clinics

### 3 — Accounting for competitive friction and achieving 80% opt-in

> With gating in place, 76.5% of clinics are expected to share. This is a plateau reached by modelling the clinics as competitive actors. Achieving >80% opt-in requires incentivisation by the competitive advantage of the new program. 

After roll-out of the new program, we expect initial participation to match those surveyed who were willing to share (**19%**). In the competitive model, assuming clinics see 5% of their client base per week, we expect to reach 76.5% opt-in after 2.5 years. This motivates designing the new program to incentivise opt-in, to not only achieve >80% but do so in a shorter time-frame.

If we model β as a competitive visibility multiplier, as the number of additional clinics drawn in per current participating clinics, the importance of incentives becomes clear: when β = 5%, the plateau goes from 76.5% to 86.7%. 

Incentive design is also important to influence the rates of sharing, and increase the desire to receive patient data. The interactive plot below shows that a modest 5% increase to intrinsic sharing desire, receiving desire and competitive visibility, achieves the desired 80% opt-in by 94 Weeks. 

> **Interactive version of this model — with adjustable α, γ, and β sliders and a live chart — is in `index.html`.**

The following describes how the program has been designed to enforce these incentives to achieve the desired opt-in rates.

### 4 — How incentives are enforced by application design

The success of the proposed program hinges on how well the competitive advantage of data sharing is illustrated to the clinic. Several design decisions in Kinetic ensure that sharing is a selfish act rather than an altruistic one.

At the top of each patient record, the system indicates whether that patient has opted in to share records. This reframes the value proposition around the patient rather than the competitor. With this framing, a practitioner is not sharing their client data with competitors, it is gaining insight that their patient is offering. This patient-centric contextualisation encourages participation as a competitive act.

When sharing is enabled, intake data is pre-filled from prior records, saving time and improving completeness. Should the practitioner decide to opt-in at any point, a confirmation window enforces clarity about which data will be gained and shared.

Whether or not the practitioner selects sharing, available clinical metadata is shown. This signals their availability and relevance. However, it is made clear that these records are only available once data sharing is enabled. These design decisions address the primary fear, that the practitioners do not want to help their patients move to competitors, by reframing the data availability as patient-centric, and then offering the practitioner the ability to capitalise on what the patient is already willing to provide.

To address the secondary concern, about judgment by other practitioners, clinical notes are omitted from sharing and shared patient data is de-identified. Only the dates and geographical region are presented to the user as metadata for a structured summary of the patient information (diagnosis, treatment type, and outcome). The "save" button at the bottom of the document changes to a "save & share" button when sharing is selected. 

The design choices above enforce the incentive to participate, both in sharing and receiving, as well as illustrate the competitive advantage available to the practitioner, influencing the β-coefficient in the model above. I expect that even modest program performance will achieve the desired outcome. 

---

## File Guide

| File | What it is |
|------|------------|
| `index.html` | This explainer with interactive payoff matrix and live simulation. |
| `clinic-view.html` | The system from a single clinic's perspective. Three patient scenarios showing what access looks like at different sharing levels. |
=======
# heidi_project_challenge_product_growth
Project challenge response (Product growth project 1)
>>>>>>> 77b812774244179c7663ff460f9b8649074d3e5c
