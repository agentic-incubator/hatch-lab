---
name: metrics-evaluator
description: Defines success metrics, creates measurement frameworks, analyzes performance data, and provides optimization recommendations using KPI design, analytics, and data-driven decision making methodologies
---

# Metrics Evaluator Skill

This skill helps you define, track, and optimize the metrics that matter most for your product's success. Using proven
measurement frameworks, we'll create a data-driven approach to product development and growth.

## Core Capabilities

I can help you:

- Define North Star metrics and KPIs
- Create measurement frameworks and dashboards
- Analyze performance data and trends
- Identify optimization opportunities
- Design experiments and interpret results
- Build attribution models
- Create automated alerting systems
- Develop data-driven decision frameworks

## Metrics Framework

### Step 1: Metrics Architecture

#### Metrics Hierarchy

```
NORTH STAR METRIC
    ├─ Primary KPIs
    │   ├─ Leading Indicators
    │   └─ Lagging Indicators
    ├─ Secondary KPIs
    │   ├─ Operational Metrics
    │   └─ Health Metrics
    └─ Supporting Metrics
        ├─ Input Metrics
        └─ Process Metrics
```

#### North Star Selection Criteria

**Characteristics of Good North Star Metrics**:

1. **Customer Value**: Reflects value delivered
2. **Revenue Correlation**: Predicts business success
3. **Actionable**: Teams can influence it
4. **Measurable**: Can track accurately
5. **Understandable**: Simple to communicate
6. **Non-Gameable**: Hard to manipulate

**Common North Star Metrics by Model**:

```
B2B SaaS: Weekly Active Teams
Marketplace: GMV (Gross Merchandise Value)
Consumer App: Daily Active Users
E-commerce: Monthly Purchases per User
Media: Total Time Reading
Fintech: Assets Under Management
```

### Step 2: KPI Definition

#### SMART KPI Framework

```
Specific    → What exactly are we measuring?
Measurable  → How do we quantify it?
Achievable  → Is the target realistic?
Relevant    → Does it drive business value?
Time-bound  → What's the timeframe?
```

#### KPI Categories

**Growth Metrics**

```
Acquisition → Activation → Retention → Revenue → Referral
├─ CAC      ├─ Time to   ├─ Churn   ├─ LTV    ├─ Viral
├─ CPL      │  Value     ├─ DAU/MAU ├─ ARPU   │  Coeff
└─ Channels └─ Aha Rate  └─ Cohorts └─ MRR    └─ NPS
```

**Engagement Metrics**

```
DEPTH               BREADTH           FREQUENCY
Sessions/User       Feature Adoption  DAU/MAU Ratio
Time in App        Users/Feature     Return Rate
Actions/Session    Feature Usage %    Session Interval
```

**Quality Metrics**

```
PRODUCT            USER              TECHNICAL
Error Rate         Satisfaction      Uptime %
Load Time         Support Tickets    Response Time
Crash Rate        Task Success       API Latency
Bug Escape Rate   Effort Score       Query Time
```

### Step 3: Measurement Design

#### Data Collection Strategy

```
EVENT TRACKING
├─ User Actions (clicks, views, submits)
├─ System Events (errors, loads, API calls)
├─ Business Events (purchases, upgrades)
└─ Custom Events (features, workflows)

PROPERTIES TO CAPTURE
├─ User Properties (segment, cohort, persona)
├─ Event Properties (context, value, source)
├─ Session Properties (device, location, time)
└─ Product Properties (version, variant, test)
```

#### Attribution Models

**Types of Attribution**:

1. **First Touch**: Credits initial interaction
2. **Last Touch**: Credits final interaction
3. **Linear**: Equal credit to all touches
4. **Time Decay**: Recent touches weighted more
5. **Position Based**: U-shaped attribution
6. **Data-Driven**: ML-based attribution

### Step 4: Dashboard Creation

#### Dashboard Architecture

```
EXECUTIVE DASHBOARD
├─ North Star Trend
├─ Revenue Metrics
├─ Key Health Indicators
└─ Alerts & Anomalies

OPERATIONAL DASHBOARD
├─ Real-time Metrics
├─ Funnel Analysis
├─ Cohort Performance
└─ Experiment Results

DIAGNOSTIC DASHBOARD
├─ Deep Dive Metrics
├─ Segment Analysis
├─ Root Cause Tools
└─ Correlation Analysis
```

#### Visualization Best Practices

**Chart Selection Guide**:

```
Comparison      → Bar Chart
Trend          → Line Chart
Composition    → Pie/Stacked Bar
Distribution   → Histogram
Relationship   → Scatter Plot
Performance    → Gauge/Bullet
```

### Step 5: Analysis Techniques

#### Cohort Analysis Framework

```
ACQUISITION COHORTS
Week 0  Week 1  Week 2  Week 3  Week 4
100%    60%     45%     35%     30%
100%    62%     46%     37%     32%
100%    65%     48%     38%     33%
        ↑ Improving Retention
```

#### Funnel Analysis

```
Step 1: Landing Page     → 10,000 (100%)
Step 2: Sign Up         → 2,000 (20%)
Step 3: Activation      → 800 (8%)
Step 4: Purchase        → 240 (2.4%)
Step 5: Retention       → 144 (1.44%)

Biggest Drop-off: Step 1→2 (80% loss)
```

#### Segmentation Analysis

```
SEGMENTATION VARIABLES
├─ Demographic (age, location, industry)
├─ Behavioral (usage, engagement, path)
├─ Psychographic (motivation, values)
├─ Technographic (device, browser, OS)
└─ Transactional (plan, spend, frequency)
```

### Step 6: Optimization Framework

#### Experiment Design

```
HYPOTHESIS
├─ Change: What we'll modify
├─ Impact: Expected outcome
├─ Metric: How we'll measure
└─ Reason: Why we believe it

EXPERIMENT SETUP
├─ Sample Size: Statistical power
├─ Duration: Significance timeline
├─ Segments: Test/Control split
└─ Success Criteria: Decision rules
```

#### Statistical Significance

```
Confidence Level: 95% (p < 0.05)
Power: 80% (β = 0.20)
Effect Size: Minimum detectable
Sample Size: n = f(effect, power, α)
```

## Metrics Artifacts

I'll help you create:

1. **Metrics Strategy Document**
2. **KPI Definition Library**
3. **Dashboard Specifications**
4. **Tracking Plans**
5. **Analysis Templates**
6. **Alert Configurations**
7. **Experiment Designs**
8. **Performance Reports**

## Advanced Analytics Techniques

### Predictive Analytics

```
CHURN PREDICTION
Input Features → ML Model → Risk Score → Intervention
- Usage patterns
- Engagement metrics
- Support interactions
- Payment history
```

### Revenue Analytics

```
LTV MODELING
Historical Data → Cohort Analysis → Prediction Model
├─ Retention Curves
├─ Revenue Expansion
├─ Churn Patterns
└─ Segment Multipliers
```

### Product Analytics

```
FEATURE IMPACT ANALYSIS
Pre/Post → Difference-in-Differences → Causal Impact
├─ Usage Metrics
├─ Engagement Lift
├─ Revenue Impact
└─ Retention Effect
```

## Example Metrics Implementation

**Product**: B2B Collaboration Platform

**Metrics Framework**:

```markdown
### North Star Metric

**Weekly Active Teams**: Teams with 3+ members active/week

### Primary KPIs

1. **Team Activation Rate**: 40% (target: 50%)
   - Definition: Teams completing first project
   - Measured: Within 7 days of signup
2. **Team Retention**: 75% month-over-month
   - Definition: Teams active in consecutive months
   - Leading indicator: Weekly engagement
3. **Revenue per Team**: $450/month
   - Components: Seats × Price × Usage tier
   - Growth driver: Seat expansion

### Dashboard Views

1. **Executive**: North Star trend, MRR, churn
2. **Product**: Feature adoption, engagement, NPS
3. **Growth**: Funnel conversion, CAC, LTV

### Alert Rules

- North Star drops >10% WoW → Immediate
- Churn spike >2 std dev → Investigation
- CAC:LTV ratio >1:3 → Strategy review
```

## Performance Optimization Playbook

### Metric Investigation Process

1. **Identify Anomaly**: Statistical deviation
2. **Segment Analysis**: Find affected groups
3. **Root Cause**: Trace to source
4. **Hypothesis**: Formulate fix
5. **Test**: Run experiment
6. **Implement**: Roll out if successful

### Optimization Levers

**Acquisition Optimization**

- Channel performance
- Landing page conversion
- Signup friction
- Onboarding flow

**Activation Optimization**

- Time to value
- Feature discovery
- Initial success
- Aha moments

**Retention Optimization**

- Engagement drivers
- Value reinforcement
- Habit formation
- Re-engagement

## Questions I'll Ask You

To design your metrics:

- What's your business model?
- What constitutes success for your product?
- What decisions need data support?
- What tools do you have for tracking?
- What's your analytics maturity?
- Who needs access to metrics?

## Output Templates

### Metrics Strategy Document

```markdown
## Metrics Strategy: [Product Name]

### North Star Metric

- **Metric**: [Name]
- **Definition**: [Precise calculation]
- **Current**: [Value]
- **Target**: [Value by date]

### KPI Framework

| KPI | Definition | Current | Target | Owner |
| --- | ---------- | ------- | ------ | ----- |

### Measurement Plan

- Tracking: [Tools and events]
- Reporting: [Frequency and format]
- Review: [Cadence and process]
```

### Performance Report

```markdown
## Performance Report: [Period]

### Executive Summary

- North Star: [Value] ([↑↓]% vs prior)
- Health: [Status]
- Action Required: [Yes/No]

### KPI Performance

| Metric | Actual | Target | Status | Trend |
| ------ | ------ | ------ | ------ | ----- |

### Key Insights

1. [Insight with data support]
2. [Insight with data support]

### Recommendations

1. [Action based on data]
2. [Action based on data]
```

## Integration Points

- **Inputs from**: All product skills
- **Critical for**: `pilot-planner`, `pivot-advisor`
- **Informs**: `product-strategy-navigator`

## Common Pitfalls

⚠️ **Vanity Metrics**: Impressive but not actionable
⚠️ **Too Many Metrics**: Analysis paralysis
⚠️ **Gaming**: Optimizing metric not value
⚠️ **Lagging Focus**: Not enough leading indicators
⚠️ **No Action**: Metrics without decisions

Let's define your success metrics. What does winning look like for your product?
