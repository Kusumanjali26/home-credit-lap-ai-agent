# Home Credit - Loan Against Property (LAP) AI Voice Agent

## Overview
An AI Voice Agent (**Priya**) engineered on Retell AI to pre-qualify customers for a Loan Against Property (LAP) up to ₹75 Lakhs. The agent dynamically handles a 7-point eligibility checklist, out-of-order conversational responses, immediate disqualification conditions, and balance transfer branching.

## Candidate & Submission Details
- **Candidate Name:** Kusumanjali Kurasala
- **Platform:** Retell AI (Single-Prompt / Conversational Flow)
- **Verified Call Record ID:** `call_0f09ed52bd91ee9f6f67b2cd5e5`

## Core Architecture & System Prompt Specification

### 1. 7 Eligibility Checklist Parameters
1. **Property Type:** Residential / Commercial (Agricultural = Auto-Disqualify)
2. **Ownership:** Sole or Joint Owner
3. **Documents:** Original Property Title Deeds Available
4. **Loan Amount:** Standard up to ₹75 Lakhs (Higher amounts routed to manual review)
5. **Income Mode:** Salaried / Self-Employed via Direct Bank Transfer or Cheque (Cash Income = Auto-Disqualify)
6. **Property Value:** Fair market valuation for LTV ratio assessment
7. **Tenure:** Valid range strictly between 3 and 15 years

### 2. Disqualification Hard-Stops
- **Cash Income:** Direct rejection due to lack of verifiable bank credits.
- **Agricultural Land:** Non-eligible collateral class.
- **Missing Original Documents:** Mandatory compliance requirement.
- **Invalid Tenure:** Outside 3 to 15 years range.

### 3. Loan Transfer Branching
Handles active existing loans by offering Balance Transfer options with reduced EMIs and additional top-up funds before routing to a Senior Loan Specialist.

## Verification & Test Scenarios Executed
- **TC-01:** Perfect Qualification Flow (Passed)
- **TC-02:** Multi-Variable Out-of-Order Extraction (Passed)
- **TC-03:** Cash Income Hard-Stop (Passed)
- **TC-04:** Agricultural Property Rejection (Passed)
- **TC-05:** High Loan Amount (>₹75L) Manual Routing (Passed)
- **TC-06:** Active Existing Loan Balance Transfer Branching (Passed)
