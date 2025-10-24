# Hatch Lab Implementation Guide

## Executive Summary

The Hatch Lab is a comprehensive collection of Claude Skills designed to transform AI agents into specialized product strategy consultants. By converting proven product development methodologies into executable skills, this framework enables users to systematically develop, validate, and launch innovative products across any industry.

## Framework Architecture

### Core Design Principles

1. **Progressive Disclosure**: Skills load information incrementally to optimize token usage
2. **Composability**: Skills work independently or orchestrated together
3. **Domain Agnostic**: Applicable across industries with contextual adaptation
4. **Evidence-Based**: Grounded in proven product development methodologies
5. **Actionable Outputs**: Each skill produces concrete deliverables

### Skills Hierarchy

```text
┌─────────────────────────────────────────┐
│     Product Strategy Navigator          │
│         (Master Orchestrator)           │
└─────────────┬───────────────────────────┘
              │
    ┌─────────┴─────────┐
    │                   │
┌───▼─────┐        ┌───▼─────┐
│Discovery│        │Execution│
│ Skills  │        │ Skills  │
└─────────┘        └─────────┘
    │                       │
    ├─ product-discovery       ├─ pilot-planner
    ├─ market-validation       ├─ metrics-evaluator
    ├─ customer-research       └─ pivot-advisor
    └─ problem-framing
              │
    ┌─────────┴─────────┐
    │                   │
┌───▼─────┐        ┌───▼─────┐
│ Design  │        │Technical│
│ Skills  │        │ Skills  │
└─────────┘        └─────────┘
    │                      │
    ├─ hci-designer           ├─ ai-technology-selector
    ├─ business-model-architect├─ architecture-designer
    └─ value-proposition       └─ tech-stack-advisor
```

## Skill Specifications

### Required SKILL.md Structure

```yaml
---
name: skill-name  # Hyphen-separated, lowercase
description: Clear description of skill purpose and capabilities
allowed-tools:  # Optional: Pre-approved tools for Claude Code
  - tool1
  - tool2
metadata:  # Optional: Custom key-value pairs
  version: 1.0
  author: creator
---

# Skill Name

[Skill content following Markdown format]
```

### Skill Development Standards

1. **Naming Convention**: Use hyphen-separated lowercase (e.g., `product-discovery`)
2. **Description Length**: 50-200 characters for optimal context loading
3. **File Organization**:

   ```text
   skill-name/
   ├── SKILL.md          # Primary instructions
   ├── templates/        # Optional: Output templates
   │   ├── canvas.md
   │   └── report.md
   ├── examples/         # Optional: Case studies
   │   └── example1.md
   └── resources/        # Optional: Additional tools
       └── checklist.md
   ```

## Implementation Phases

### Phase 1: Foundation (Weeks 1-4)

#### Objectives

- Deploy core discovery and validation skills
- Test with 3-5 pilot users
- Refine skill interactions

#### Deliverables

- [ ] 6 core skills operational
- [ ] Basic orchestration patterns
- [ ] Initial user feedback
- [ ] Performance baselines

#### Success Metrics

- Skill activation accuracy > 80%
- User task completion > 70%
- Positive feedback score > 7/10

### Phase 2: Enhancement (Weeks 5-8)

#### Objectives

- Add specialized skills
- Implement advanced orchestration
- Create industry templates

#### Deliverables

- [ ] 12+ total skills available
- [ ] Industry-specific variations
- [ ] Advanced composition patterns
- [ ] Integration examples

#### Success Metrics

- Multi-skill workflow success > 75%
- Time-to-insight reduction > 40%
- User retention > 60%

### Phase 3: Intelligence (Weeks 9-12)

#### Objectives

- Implement adaptive skill selection
- Add learning mechanisms
- Create skill marketplace

#### Deliverables

- [ ] Intelligent routing system
- [ ] Performance optimization
- [ ] Skill recommendation engine
- [ ] Community contributions

#### Success Metrics

- Autonomous skill selection accuracy > 85%
- User productivity improvement > 50%
- Community skill contributions > 10

## Usage Patterns

### Pattern 1: Single Skill Invocation

```text
User: "Help me validate market demand for a sustainable packaging solution"
System: Activates market-validation skill
Output: TAM/SAM/SOM analysis, competitive landscape, validation report
```

### Pattern 2: Sequential Workflow

```text
User: "I want to build a new B2B SaaS product"
System: Orchestrates multiple skills in sequence
Flow: discovery → validation → technology → business model → pilot
```

### Pattern 3: Parallel Processing

```text
User: "Analyze this opportunity from multiple angles"
System: Activates multiple skills simultaneously
Parallel: market-validation + ai-technology-selector + business-model-architect
```

### Pattern 4: Adaptive Navigation

```text
User: "Guide me through product development"
System: Navigator skill assesses and routes
Dynamic: Adjusts path based on intermediate results
```

## Integration Guidelines

### With Claude.ai

1. **Installation**: Settings → Skills → Upload folder
2. **Activation**: Automatic based on user query
3. **Visibility**: Skills appear in chain of thought
4. **Output**: Formatted deliverables and artifacts

### With Claude API

```python
from anthropic import Client

client = Client()
response = client.messages.create(
    model="claude-opus-4-1-20250805",
    messages=[{"role": "user", "content": "Analyze market for AI tutoring"}],
    skills=[
        {"type": "custom", "path": "./skills/market-validation"},
        {"type": "custom", "path": "./skills/ai-technology-selector"}
    ]
)
```

### With Claude Code

```bash
# Install from marketplace
/plugin install product-strategy@agentic-incubator

# Manual installation
cp -r ./skills/* ~/.claude/skills/

# Verify installation
/skills list
```

## Quality Assurance

### Testing Framework

#### Unit Testing (Per Skill)

- [ ] Activation triggers correctly
- [ ] Outputs match expected format
- [ ] Edge cases handled
- [ ] Error messages clear

#### Integration Testing

- [ ] Skills share context properly
- [ ] Orchestration patterns work
- [ ] No conflicts between skills
- [ ] Performance within limits

#### User Acceptance Testing

- [ ] Tasks completed successfully
- [ ] Outputs valuable and actionable
- [ ] Learning curve acceptable
- [ ] Feedback incorporated

### Performance Benchmarks

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| Skill Load Time | < 2 seconds | Timer from trigger to ready |
| Token Efficiency | < 2000 tokens/skill | Context window usage |
| Output Quality | > 8/10 rating | User feedback scores |
| Task Success Rate | > 80% | Completion tracking |
| Multi-skill Coordination | > 75% success | Workflow completion |

## Security Considerations

### Skill Validation Checklist

- [ ] No external API calls from skill code
- [ ] No sensitive data storage
- [ ] No arbitrary code execution
- [ ] Input sanitization present
- [ ] Output filtering active
- [ ] Resource limits defined

### Trust Model

1. **Trusted Sources**: Anthropic, verified developers
2. **Community Skills**: Review before use
3. **Private Skills**: Internal audit required
4. **Skill Permissions**: Explicitly granted

## Example Implementations

### Example 1: Tech Startup Journey

```markdown
## Journey: AI-Powered Code Review Tool

### Phase 1: Discovery (Week 1)
**Skill**: product-discovery
**Output**: Developers waste 30% of time on code reviews
**Validation**: 200+ developers confirm pain point

### Phase 2: Market Validation (Week 2)
**Skill**: market-validation
**Output**: $1.2B TAM, fragmented competition
**Decision**: Proceed with development

### Phase 3: Technology Selection (Week 3)
**Skill**: ai-technology-selector
**Output**: Claude API + Tree-sitter for AST analysis
**Architecture**: Microservices on AWS

### Phase 4: Business Model (Week 4)
**Skill**: business-model-architect
**Output**: Per-seat SaaS, $50/developer/month
**Economics**: LTV:CAC = 4.2:1

### Phase 5: Pilot Planning (Week 5-6)
**Skill**: pilot-planner
**Output**: 8-week pilot with 5 companies
**Success Criteria**: 50% reduction in review time
```

### Example 2: Healthcare Innovation

```markdown
## Journey: Remote Patient Monitoring Platform

### Parallel Discovery & Validation
**Skills**: product-discovery + market-validation
**Insight**: Chronic disease management gap in rural areas
**Market**: $4.5B opportunity, regulatory pathway clear

### Technology & Compliance Assessment
**Skills**: ai-technology-selector + regulatory-analyzer
**Decision**: FDA Class II medical device software
**Stack**: HIPAA-compliant cloud, ML for predictions

### Business Model & Pilot Design
**Skills**: business-model-architect + pilot-planner
**Model**: B2B2C through health systems
**Pilot**: 3 rural clinics, 500 patients, 6 months
```

## Metrics & KPIs

### Skill Performance Metrics

| Metric | Description | Target |
|--------|-------------|--------|
| Activation Rate | % of relevant queries triggering skills | > 85% |
| Completion Rate | % of started workflows completed | > 70% |
| Value Score | User rating of output value | > 8/10 |
| Time Saved | Hours saved vs. manual process | > 50% |
| Decision Quality | % of go/no-go decisions validated | > 80% |

### Business Impact Metrics

| Metric | Description | Target |
|--------|-------------|--------|
| Ideas Validated | # of concepts evaluated | 100/month |
| Pivot Rate | % of projects successfully pivoted | > 60% |
| Time to Market | Reduction in development time | -30% |
| Success Rate | % of pilots meeting criteria | > 40% |
| ROI | Return on skill development investment | > 5x |

## Continuous Improvement

### Feedback Loops

1. **User Feedback**: Collected after each skill use
2. **Performance Data**: Automated tracking of metrics
3. **Outcome Tracking**: Long-term success monitoring
4. **Community Input**: Feature requests and contributions

### Update Cycle

- **Weekly**: Bug fixes and minor improvements
- **Monthly**: New features and skills
- **Quarterly**: Major upgrades and architecture changes
- **Annually**: Framework evolution and strategy review

## Support & Resources

### Documentation

- Skill specifications and templates
- Integration guides
- Example implementations
- Video tutorials

### Community

- Discord channel for users
- GitHub for contributions
- Monthly webinars
- Case study library

### Professional Services

- Custom skill development
- Enterprise integration
- Training workshops
- Strategy consulting

## Conclusion

The Hatch Lab Skills Framework transforms AI agents into powerful product strategy consultants. By following this implementation guide, organizations can systematically build, validate, and launch innovative products with reduced risk and increased speed to market.

The modular, composable nature of skills ensures flexibility and scalability, while the evidence-based methodologies provide confidence in decision-making. As the framework evolves, it will continue to incorporate best practices and emerging patterns in product development.

## Appendices

### A. Skill Development Template

[See SKILL_TEMPLATE.md]

### B. Orchestration Patterns Catalog

[See ORCHESTRATION_PATTERNS.md]

### C. Industry-Specific Customizations

[See INDUSTRY_GUIDE.md]

### D. Troubleshooting Guide

[See TROUBLESHOOTING.md]

---

*Version 1.0 - October 2025*
*Based on MIT's Designing and Building AI Products and Services curriculum*
*Aligned with Anthropic's Agent Skills specification*
