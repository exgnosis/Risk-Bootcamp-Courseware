# Quantative Exercise

## Scenario

Your team is responsible for assessing risk for a critical internal application used for customer onboarding
- Historical assessments have relied only on qualitative ratings such as “Likely / Major”, based on SME interviews
- Now a quantative risk evaluation that will be used as an input into a strategic planning process.

## Part 1: Identify Input Data

### Risk Event:
- A cybersecurity breach caused by stolen employee credentials.

### Given Data:

Asset Value (AV):
- Customer Onboarding System is valued at $2,000,000
- This includes data, functionality, and reputational exposure.

Exposure Factor (EF):
- Using impact guidance, SMEs estimate a breach could compromise 40% of the system’s value.

Historical Frequency Data:
- Reviewing the last five years incident logs show:
  - 4 credential-related compromise attempts
  - 1 successful breach in that period
  - Industry reports suggest a typical rate of ~0.5 breaches per year for similar institutions.
- Control Environment:

Multi-factor authentication (MFA) has been deployed across 80% of the environment.

Log correlation and monitoring tools detect 60% of intrusion attempts.

Password policy is outdated.

## Part 2: Step-by-Step Calculations    

#### Step 1: Calculate the Single Loss Expectancy (SLE)
- SLE = Asset Value × Exposure Factor
- Compute the SLE and record your answer.

#### Step 2: Determine the Annual Rate of Occurrence (ARO)
- ARO = (Number of events) / (Years of observation)
- From scenario data:
  - 1 successful breach in 5 years → 1/5 = 0.2
  - Industry rate suggests ~0.5
- Propose an ARO value combining both of these values:
  - Option A: Use your judgment and choose one
  - Option B: Average them
  - Option C: Use a range (low: 0.2, high: 0.5)
- Write down your chosen ARO and the reasoning behind it

#### Step 3: Calculate the Annualized Loss Expectancy (ALE)
- ALE = SLE × ARO
- Compute the ALE using your SLE and ARO.

## Part 3: Residual Risk

#### Step 4: Estimate Inherent Risk
- Start with your inherent (pre-control) values you used or calculated previously:
  - Asset Value (AV) = $2,000,000
  - Inherent Exposure Factor (EF_inherent) = 0.40
  - Inherent ARO (ARO_inherent) = the value you chose in Part 2
- From these calculate:
  - SLE_inherent = AV × EF_inherent
  - ALE_inherent = SLE_inherent × ARO_inherent

#### Step 5: Quantify the Effect of Controls on Frequency (ARO)
- Based on expert analysis and historical performance of controls:
  - Multi-factor authentication (MFA) and monitoring together are estimated to reduce successful credential breaches by 70% compared to the no-control baseline.
- We treat this as a 70% reduction in ARO (frequency of successful events).
- Compute the residual ARO_Residual:
  - ARO_Residual = ARO × (1−0.70)
- Record your ARO_residual.

#### Step 6: Quantify the Effect of Controls on Impact (SLE)
- Because detection and response have improved:
- Faster detection and response are estimated to reduce financial impact per breach by 25% compared to the inherent case.
- Model this as a 25% reduction in the Exposure Factor:
  - EF_Residual= RF_Inherent * .75
- Compute EF_residual using EF_inherent = 0.40.
- Compute SLE_residual = AV × EF_residual.
- Record your SLE_residual.

#### Step 7: Compute Residual ALE and Risk Reduction
- Compute the absolute reduction in ALE:
  - ΔALE = ALE_Inherent − ALE_Residual
- Compute the percentage reduction in risk:
  - %Reduction = (ΔALE/ALE_Inherent)×100%
- Write a 2–3 sentence interpretation in business language, for example including
  - How much expected loss per year did we remove?
  - Is this magnitude of reduction financially meaningful?