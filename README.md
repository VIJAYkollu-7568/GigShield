<img width="1536" height="1024" alt="ChatGPT Image Mar 20, 2026, 10_22_23 AM" src="https://github.com/user-attachments/assets/2d1d0dc2-619b-4d43-83b1-fdb18d8789b7" />

# GigShield

**GigShield** is an **AI-enabled parametric income protection platform** for **food-delivery gig workers** who lose earnings because of **verified external disruptions** such as **heavy rainfall, flooding, curfews, zone shutdowns, traffic restrictions, and platform outages**.

It is designed as a **low-friction, weekly protection model** that combines **dynamic premium pricing, trigger-based claims, automated validation, fraud checks, and payout workflows**.


## 1. Core Requirement

GigShield is designed to solve **disruption-led income loss** for food-delivery partners working in urban micro-zones.

### Key requirements
- Protect **loss of income only**
- Use a **weekly premium model**
- Support **parametric trigger-based claims**
- Minimize manual claim filing
- Include **eligibility validation and fraud checks**
- Be scalable for future insurer and platform integration


## 2. Target Persona

### Primary Persona: Ravi
- **Age:** 24  
- **Occupation:** Food-delivery partner  
- **Platform:** Zomato / Swiggy  
- **City:** Hyderabad  
- **Income Type:** Variable weekly earnings  
- **Pain Point:** Income stops when weather, outages, or local restrictions affect his zone  
- **Need:** Fast, simple protection without paperwork-heavy claims  



## 3. Persona-Based Scenarios

### Scenario 1: Heavy Rainfall
Ravi starts his evening shift in Hyderabad. Heavy rainfall causes waterlogging in his delivery zone, reducing order movement and making deliveries unsafe. Since the event crosses the trigger threshold in his active zone, GigShield flags the disruption and starts claim evaluation.

### Scenario 2: Platform Outage
Meena begins her dinner shift in Pune during peak hours. A platform outage lasts for two hours, stopping all order flow. GigShield verifies the outage, checks whether her protected shift overlaps with the disruption window, and marks the claim as eligible.

### Scenario 3: Curfew / Zone Restriction
A local restriction shuts down a dense delivery area during working hours. Partners assigned to that micro-zone lose earning opportunities. GigShield validates the impacted zone and covered time window, then processes the payout workflow automatically.


## 4 Workflow Diagram
<img width="1420" height="742" alt="Screenshot 2026-03-19 192626" src="https://github.com/user-attachments/assets/404e6698-db8f-435a-b966-b9e395257e32" />



## 5. Application Workflow

GigShield follows a simple trigger-based workflow:

1. Worker signs up and enters profile, zone, and weekly income details  
    2. System calculates a **zone-based risk score**  
    3. A **weekly premium** is generated  
    4. Coverage is activated for the selected week  
    5. External disruption signals are monitored  
    6. When a verified trigger occurs, the system identifies impacted workers  
    7. Eligibility validation and fraud checks are applied  
    8. If valid, payout is approved and processed 



## 6. Weekly Premium Model

GigShield uses a weekly premium model because gig-worker risk changes frequently based on location, disruption frequency, and income patterns. Weekly pricing better matches how delivery workers earn and how their exposure changes over time.

### Premium Logic:

    
    Weekly Premium=Base Rate+(Zone Risk×W1​)+(Disruption Frequency×W2​)+(Income Factor×W3​)

    Base Rate: standard minimum premium
    Zone Risk: disruption exposure of the worker’s delivery micro-zone
    Income Factor: worker’s average weekly earnings
    W1,W2,W3: pricing weights

Example

    If:

    Base Rate = ₹20

    Zone Risk = 3

    Disruption Frequency = 2

    Income Factor = 12

    Then:
    20 +(3×10)+(2×5)+12=72
    

Weekly Premium = ₹72


## 7. Parametric Triggers

GigShield uses parametric triggers, meaning claims are activated by verified external events instead of reimbursement-based manual proofs.

Proposed Triggers

Heavy Rainfall

Flood Alert / Waterlogging

Curfew / Local Restriction

Zone Shutdown

Traffic Restriction

Platform Outage

### Trigger Conditions

A valid parametric trigger must be:

externally verifiable

time-bound

zone-specific

measurable

directly linked to earning disruption


## 8. AI/ML Integration Plan

Model 1 — Premium Calculator (XGBoost)

Model 2 — Fraud Detection Engine (Isolation Forest)
<img width="628" height="411" alt="image" src="https://github.com/user-attachments/assets/21ee0650-6c92-4121-8ef6-02e057c00fac" />


 Model 3 — Risk Forecaster (Prophet by Meta)

 Model 4 — Income Baseline (EWMA Rolling Average)

 ### AIML Workflow Diagram



 ## 9. Tech Stack


Frontend: Next.js, React, Tailwind CSS, TypeScript

Backend: Node.js, NestJS / Express.js

Database: PostgreSQL, Prisma

AI/ML Layer: Python, FastAPI, scikit-learn / XGBoost

Caching / Rules: Redis

Payment Layer: RazorPay SandBox , UPI payout API 




## How to Run

### Prerequisites
- **Node.js** 18 or above
- **npm** or **yarn**

### Installation

```bash
git clone https://github.com/your-username/GigShield.git
cd GigShield
npm install

Install Dependencies : npm install
Run the dev Server   : npm run dev
Open in browser      : http://localhost:3000




