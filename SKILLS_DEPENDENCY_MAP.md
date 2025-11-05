# Hatch Lab Skills Dependency Map

This document visualizes the relationships, dependencies, and typical sequencing of all 15 Hatch Lab skills.

## Master Orchestration Flow

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│          PRODUCT-STRATEGY-NAVIGATOR (Master)                │
│                                                             │
│  Coordinates all skills below based on user needs and       │
│  product development stage                                  │
│                                                             │
└────────────────┬────────────────────────────────────────────┘
                 │
                 │ Routes to appropriate skills
                 │
                 ▼
         [See flows below]
```

## Complete Dependency Graph

```
                    START HERE
                         │
                         ▼
              ┌──────────────────┐
              │ problem-framing  │ ◄─── Can start here for any unclear problem
              └─────────┬────────┘
                        │
                        ├──────────────────────────┐
                        ▼                          ▼
            ┌────────────────────┐    ┌──────────────────────┐
            │ product-discovery  │    │ customer-research    │
            └─────────┬──────────┘    └──────────┬───────────┘
                      │                           │
                      └───────────┬───────────────┘
                                  ▼
                      ┌───────────────────────┐
                      │  market-validation    │
                      └───────────┬───────────┘
                                  │
                ┌─────────────────┼─────────────────┐
                ▼                 ▼                 ▼
    ┌──────────────────┐  ┌─────────────────┐  ┌─────────────────┐
    │ value-proposition│  │ business-model- │  │ ai-technology-  │
    │                  │  │    architect    │  │   selector      │
    └──────────────────┘  └──────┬──────────┘  └────────┬────────┘
                                 │                      │
                                 │         ┌────────────┴────────┐
                                 │         ▼                     ▼
                                 │  ┌──────────────────┐  ┌────────────────┐
                                 │  │ tech-stack-      │  │ architecture-  │
                                 │  │   advisor        │  │   designer     │
                                 │  └──────────┬───────┘  └────────┬───────┘
                                 │             │                   │
                                 │             └──────┬────────────┘
                                 │                    ▼
                                 │            ┌──────────────┐
                                 │            │ hci-designer │
                                 │            └──────┬───────┘
                                 │                   │
                    ┌────────────┴──────────────┬────┘
                    ▼                           ▼
          ┌──────────────────┐        ┌─────────────────┐
          │ regulatory-      │        │ pilot-planner   │
          │   analyzer       │        │                 │
          └──────────────────┘        └────────┬────────┘
                    │                          │
                    └───────────┬──────────────┘
                                ▼
                    ┌──────────────────────┐
                    │ metrics-evaluator    │
                    └───────────┬──────────┘
                                │
                                ├───── Success ────────► Continue/Scale
                                │
                                └───── Issues ─────────► pivot-advisor
                                                              │
                                                              └─► Loop back to
                                                                  appropriate
                                                                  stage
```

## Skill Relationships by Type

### 1. Sequential Dependencies (Must Follow Order)

#### Path A: Problem → Solution Discovery

```
problem-framing → product-discovery → customer-research → market-validation
```

**Why Sequential:** Each skill builds on insights from the previous step. You can't validate a market without first
understanding the problem and discovering potential solutions.

#### Path B: Validation → Design

```
market-validation → business-model-architect → pilot-planner
```

**Why Sequential:** You need market understanding before designing business models, and you need business models
before planning pilots.

#### Path C: Technology Stack Selection

```
ai-technology-selector → tech-stack-advisor → architecture-designer
```

**Why Sequential:** High-level technology decisions inform specific stack choices, which inform architectural patterns.

### 2. Parallel Opportunities (Can Run Simultaneously)

#### Parallel Set 1: Market Understanding

```
┌─ market-validation
├─ value-proposition
└─ customer-research
```

**When to Use:** Early stage, need comprehensive market understanding quickly.

#### Parallel Set 2: Design Phase

```
┌─ hci-designer
├─ architecture-designer
└─ business-model-architect
```

**When to Use:** Have validated problem, moving to solution design. Different teams can work simultaneously.

#### Parallel Set 3: Compliance & Planning

```
┌─ regulatory-analyzer
└─ pilot-planner
```

**When to Use:** Preparing for launch, need both compliance strategy and pilot structure.

### 3. Cross-Cutting Skills (Can Apply Anytime)

These skills can be invoked at any stage:

- **problem-framing**: Whenever problem definition is unclear
- **regulatory-analyzer**: Whenever compliance questions arise
- **pivot-advisor**: Whenever strategy needs reassessment
- **product-strategy-navigator**: Whenever guidance on next steps is needed

## Common Journey Patterns

### Pattern 1: New Product from Scratch

```
Duration: 8-12 hours
Certainty: High structure, comprehensive coverage

1. problem-framing (30 min)
   └─► 2. product-discovery (60 min)
        └─► 3. customer-research (90 min)
             └─► 4. market-validation (60 min)
                  ├─► 5a. value-proposition (45 min)
                  └─► 5b. business-model-architect (90 min)
                       └─► 6. ai-technology-selector (60 min)
                            └─► 7. tech-stack-advisor (45 min)
                                 └─► 8. architecture-designer (120 min)
                                      └─► 9. hci-designer (90 min)
                                           └─► 10. regulatory-analyzer (60 min)
                                                └─► 11. pilot-planner (60 min)
                                                     └─► 12. metrics-evaluator (45 min)
```

### Pattern 2: Fast Validation (MVP Mode)

```
Duration: 2-3 hours
Certainty: Lower, but faster to market

1. problem-framing (20 min)
   └─► 2. [Parallel]
        ├─► market-validation (45 min)
        ├─► customer-research (45 min)
        └─► value-proposition (30 min)
             └─► 3. pilot-planner (45 min)
                  └─► 4. metrics-evaluator (30 min)
```

### Pattern 3: Technical Deep Dive

```
Duration: 4-6 hours
Certainty: High technical confidence

1. problem-framing (30 min)
   └─► 2. ai-technology-selector (90 min)
        └─► 3. tech-stack-advisor (60 min)
             └─► 4. architecture-designer (120 min)
                  ├─► 5. regulatory-analyzer (60 min)
                  └─► 6. hci-designer (90 min)
```

### Pattern 4: Pivot/Optimization

```
Duration: 3-4 hours
Certainty: Depends on findings

1. metrics-evaluator (analyze current state, 60 min)
   └─► 2. pivot-advisor (identify options, 90 min)
        └─► 3. [Based on pivot type]
             ├─► Customer Pivot: customer-research + value-proposition
             ├─► Market Pivot: market-validation + business-model-architect
             ├─► Technology Pivot: ai-technology-selector + architecture-designer
             └─► Feature Pivot: product-discovery + hci-designer
                  └─► 4. pilot-planner (test new direction, 60 min)
                       └─► 5. metrics-evaluator (measure results, 30 min)
```

### Pattern 5: Enterprise B2B Launch

```
Duration: 10-14 hours
Certainty: High, comprehensive

1. problem-framing (45 min)
   └─► 2. customer-research (emphasis on buying committees, 120 min)
        └─► 3. market-validation (60 min)
             └─► 4. value-proposition (emphasis on ROI, 90 min)
                  └─► 5. business-model-architect (60 min)
                       └─► 6. architecture-designer (emphasis on enterprise, 120 min)
                            └─► 7. regulatory-analyzer (SOC 2, GDPR, etc., 90 min)
                                 └─► 8. hci-designer (admin interfaces, 90 min)
                                      └─► 9. pilot-planner (POC strategy, 90 min)
                                           └─► 10. metrics-evaluator (60 min)
```

## Dependency Matrix

| Skill                      | Strong Dependencies (Must precede)           | Weak Dependencies (Should precede)       | Can Run Parallel With                           |
| -------------------------- | -------------------------------------------- | ---------------------------------------- | ----------------------------------------------- |
| problem-framing            | None (starting skill)                        | None                                     | None (should be first)                          |
| product-discovery          | problem-framing                              | None                                     | customer-research                               |
| customer-research          | problem-framing                              | product-discovery                        | market-validation, product-discovery            |
| market-validation          | product-discovery OR customer-research       | problem-framing                          | customer-research, value-proposition            |
| value-proposition          | market-validation                            | customer-research                        | business-model-architect                        |
| business-model-architect   | market-validation                            | value-proposition                        | hci-designer, architecture-designer             |
| ai-technology-selector     | problem-framing                              | product-discovery, market-validation     | None (sequential in tech path)                  |
| tech-stack-advisor         | ai-technology-selector                       | None                                     | regulatory-analyzer                             |
| architecture-designer      | tech-stack-advisor OR ai-technology-selector | business-model-architect                 | hci-designer, business-model-architect          |
| hci-designer               | customer-research                            | architecture-designer                    | architecture-designer, business-model-architect |
| regulatory-analyzer        | None (can run anytime)                       | market-validation, architecture-designer | Any skill                                       |
| pilot-planner              | market-validation, business-model-architect  | All design skills                        | regulatory-analyzer                             |
| metrics-evaluator          | pilot-planner OR (for pivots: none)          | None                                     | None (typically last)                           |
| pivot-advisor              | metrics-evaluator                            | All prior skills                         | None (decision point)                           |
| product-strategy-navigator | None (orchestrator)                          | None                                     | All (manages all)                               |

## Input/Output Relationships

### Problem Framing

- **Inputs**: User's initial problem description
- **Outputs to**: All other skills (foundational problem definition)

### Product Discovery

- **Inputs from**: problem-framing (problem definition)
- **Outputs to**: market-validation, customer-research (opportunity areas)

### Customer Research

- **Inputs from**: product-discovery (opportunity areas), problem-framing (problem statement)
- **Outputs to**: market-validation (segment insights), hci-designer (personas), value-proposition (needs)

### Market Validation

- **Inputs from**: product-discovery (opportunities), customer-research (segments)
- **Outputs to**: business-model-architect (market size, segments), value-proposition (competitive context)

### Value Proposition

- **Inputs from**: market-validation (competitive landscape), customer-research (needs)
- **Outputs to**: business-model-architect (positioning), pilot-planner (value messaging)

### Business Model Architect

- **Inputs from**: market-validation (market data), value-proposition (positioning)
- **Outputs to**: pilot-planner (business model), metrics-evaluator (key metrics)

### AI Technology Selector

- **Inputs from**: problem-framing (problem definition), product-discovery (requirements)
- **Outputs to**: tech-stack-advisor (high-level tech choices), architecture-designer (AI/ML components)

### Tech Stack Advisor

- **Inputs from**: ai-technology-selector (technology direction), architecture-designer (architecture patterns)
- **Outputs to**: architecture-designer (specific technologies), pilot-planner (technical constraints)

### Architecture Designer

- **Inputs from**: tech-stack-advisor (technology stack), ai-technology-selector (AI components)
- **Outputs to**: hci-designer (system capabilities), pilot-planner (technical architecture)

### HCI Designer

- **Inputs from**: customer-research (personas), architecture-designer (system capabilities)
- **Outputs to**: pilot-planner (user experience design), metrics-evaluator (UX metrics)

### Regulatory Analyzer

- **Inputs from**: market-validation (target markets), architecture-designer (system design)
- **Outputs to**: pilot-planner (compliance requirements), architecture-designer (regulatory constraints)

### Pilot Planner

- **Inputs from**: business-model-architect (business model), architecture-designer (architecture), hci-designer (UX design)
- **Outputs to**: metrics-evaluator (success criteria)

### Metrics Evaluator

- **Inputs from**: pilot-planner (success criteria), business-model-architect (key metrics)
- **Outputs to**: pivot-advisor (performance data) OR continue/scale decision

### Pivot Advisor

- **Inputs from**: metrics-evaluator (performance data)
- **Outputs to**: Relevant skills based on pivot type (loops back into flow)

## Decision Points

### Decision 1: After Problem Framing

```
Have a clear problem?
├─ YES → product-discovery
└─ NO → More problem-framing or customer-research
```

### Decision 2: After Market Validation

```
Market opportunity viable?
├─ YES → Continue to business-model-architect
└─ NO → pivot-advisor OR stop
```

### Decision 3: After Metrics Evaluator

```
Pilot meeting success criteria?
├─ YES → Scale and continue
├─ PARTIAL → Optimize with relevant skills
└─ NO → pivot-advisor
```

### Decision 4: Technology Approach

```
Is AI/ML core to solution?
├─ YES → ai-technology-selector → tech-stack-advisor → architecture-designer
└─ NO → tech-stack-advisor → architecture-designer
```

### Decision 5: Compliance Critical?

```
Highly regulated industry? (healthcare, finance, etc.)
├─ YES → regulatory-analyzer early (after market-validation)
└─ NO → regulatory-analyzer late (before pilot-planner)
```

## Tips for Navigating Dependencies

### 1. Use product-strategy-navigator

Let the navigator guide you through the appropriate sequence based on your specific situation.

### 2. Start with Problem Framing

Unless you have crystal-clear problem definition, always start with problem-framing.

### 3. Parallelize When Possible

Don't wait unnecessarily. If skills don't have strong dependencies, run them in parallel.

### 4. Document Handoffs

When moving between skills, explicitly reference outputs from previous skills.

### 5. Revisit When Needed

Don't treat this as one-way flow. Loop back when you discover new information.

### 6. Skip What You Have

If you already have solid market validation data, don't redo it. Jump to the next needed skill.

## Anti-Patterns (What to Avoid)

### ❌ Jumping to Solutions

```
BAD: business-model-architect → pilot-planner (without validation)
GOOD: problem-framing → discovery → validation → business-model
```

### ❌ Excessive Parallelization

```
BAD: Running all 15 skills simultaneously
GOOD: Run 2-3 skills in parallel at appropriate stages
```

### ❌ Ignoring Dependencies

```
BAD: architecture-designer before tech-stack-advisor
GOOD: Follow sequential tech path
```

### ❌ Skipping Validation

```
BAD: product-discovery → pilot-planner
GOOD: product-discovery → market-validation → pilot-planner
```

### ❌ Over-Planning

```
BAD: Spending 20 hours on perfect strategy before any validation
GOOD: Fast validation cycle, then deeper planning
```

---

_For questions about skill dependencies or sequencing, start with product-strategy-navigator or consult IMPLEMENTATION_GUIDE.md_
