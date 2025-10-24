# Hatch Lab: Product Strategy Skills Framework

## Overview

A comprehensive collection of Claude Skills that guide innovators, entrepreneurs, and product teams through systematic product strategy development and evaluation. These skills transform Claude into a specialized product strategy consultant, supporting new product development and innovation across industries.

## Architecture Philosophy

### Progressive Disclosure Pattern

Following Anthropic's Agent Skills design principles, each skill operates with three levels of context loading:

1. **Metadata Level**: Brief name and description in YAML frontmatter (~100 tokens)
2. **Primary Instructions**: Core SKILL.md content loaded when relevant
3. **Deep Context**: Additional files and resources loaded on demand

### Skill Orchestration Model

```text
┌─────────────────────────────────────┐
│     Product Strategy Navigator      │
│         (Master Skill)              │
└────────────┬────────────────────────┘
             │
    ┌────────┴────────┐
    │                 │
┌───▼──────┐    ┌────▼──────┐
│Discovery │    │Validation │
│  Skills  │    │  Skills   │
└──────────┘    └───────────┘
    │                 │
┌───▼──────┐    ┌────▼──────┐
│  Design  │    │Development│
│  Skills  │    │  Skills   │
└──────────┘    └───────────┘
```

## Skills Catalog

### 1. Core Strategy Skills

#### product-discovery

- **Purpose**: Guide systematic exploration of problem spaces and opportunity identification
- **Key Components**: Customer journey mapping, jobs-to-be-done analysis, problem framing
- **Outputs**: Problem statements, opportunity matrices, initial hypotheses

#### market-validation

- **Purpose**: Validate market demand and competitive positioning
- **Key Components**: TAM/SAM/SOM analysis, competitive analysis, customer segment definition
- **Outputs**: Market size estimates, competitive positioning maps, validation metrics

#### ai-technology-selector

- **Purpose**: Match AI capabilities to business problems
- **Key Components**: Technology readiness assessment, IP evaluation, build-vs-buy analysis
- **Outputs**: Technology recommendations, implementation roadmaps, risk assessments

### 2. Design & Development Skills

#### hci-designer

- **Purpose**: Create human-centered interfaces and experiences
- **Key Components**: User persona development, interaction design, usability heuristics
- **Outputs**: Wireframes, user flows, interaction specifications

#### business-model-architect

- **Purpose**: Design sustainable business models and revenue strategies
- **Key Components**: Value proposition canvas, revenue model design, unit economics
- **Outputs**: Business model canvas, pricing strategies, financial projections

#### pilot-planner

- **Purpose**: Structure pilot programs to validate product-market fit
- **Key Components**: MVP definition, success criteria, rollout planning
- **Outputs**: Pilot roadmap, measurement framework, go/no-go criteria

### 3. Evaluation & Iteration Skills

#### metrics-evaluator

- **Purpose**: Define and track success metrics
- **Key Components**: KPI selection, measurement frameworks, analysis templates
- **Outputs**: Metrics dashboards, performance reports, optimization recommendations

#### pivot-advisor

- **Purpose**: Guide strategic pivots based on market feedback
- **Key Components**: Pivot patterns, decision frameworks, risk assessment
- **Outputs**: Pivot recommendations, transition plans, stakeholder communications

## Implementation Patterns

### 1. Skill Composition Pattern

Skills can be composed for complex workflows:

```yaml
workflow: new-product-launch
  steps:
    - product-discovery
    - market-validation
    - business-model-architect
    - pilot-planner
```

### 2. Context Sharing Pattern

Skills share context through structured outputs:

```markdown
## Context Output
- problem_statement: [from product-discovery]
- market_size: [from market-validation]
- technology_stack: [from ai-technology-selector]
```

### 3. Progressive Enhancement Pattern

Skills build upon each other's outputs:

- Basic: Single skill execution
- Enhanced: Multi-skill workflow
- Advanced: Adaptive skill selection based on context

## Usage Examples

### Example 1: SaaS Product Innovation

```text
User: "I want to create a SaaS platform for sustainable supply chain management"
Skills Activated:
1. product-discovery → Identifies pain points in current supply chain sustainability tracking
2. market-validation → Analyzes $2.8B market opportunity
3. ai-technology-selector → Recommends predictive analytics and optimization algorithms
4. business-model-architect → Designs tiered subscription model
```

### Example 2: Healthcare AI Application

```text
User: "Help me design an AI-powered diagnostic assistant for rural clinics"
Skills Activated:
1. product-discovery → Maps clinical workflow inefficiencies
2. hci-designer → Creates intuitive interface for non-technical users
3. pilot-planner → Structures 3-month pilot with 5 rural clinics
4. metrics-evaluator → Defines clinical accuracy and adoption metrics
```

## Security & Best Practices

### Skill Validation

- All skills undergo security review before publication
- No external API calls from within skills
- Sandboxed execution environment
- Clear data handling guidelines

### Quality Assurance

- Structured testing framework
- Example scenarios for each skill
- Performance benchmarks
- User feedback integration

## Development Roadmap

### Phase 1: Foundation (Current)

- Core strategy skills
- Basic composition patterns
- Documentation and examples

### Phase 2: Enhancement

- Industry-specific variations
- Advanced composition patterns
- Integration with external tools

### Phase 3: Intelligence

- Adaptive skill selection
- Learning from user interactions
- Automated skill composition

## Contributing Guidelines

### Skill Development Standards

1. Follow SKILL.md specification
2. Include comprehensive examples
3. Provide clear success criteria
4. Document dependencies
5. Test with diverse scenarios

### Code of Conduct

- Focus on user value
- Maintain professional quality
- Respect intellectual property
- Prioritize accessibility
- Ensure ethical AI practices

## License

Apache 2.0 - See LICENSE file for details

## Acknowledgments

Built on Anthropic's Agent Skills framework and inspired by MIT's Designing and Building AI Products and Services curriculum.
