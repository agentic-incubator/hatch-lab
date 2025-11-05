# Hatch Lab Implementation Guide

## Executive Summary

Hatch Lab is a comprehensive collection of Claude Skills designed to transform AI agents into specialized
product strategy consultants. By converting proven product development methodologies into executable skills, this framework
enables users to systematically develop, validate, and launch innovative products across any industry.

## Framework Architecture

### Core Design Principles

1. **Progressive Disclosure**: Skills load information incrementally to optimize token usage
2. **Composability**: Skills work independently or orchestrated together
3. **Domain Agnostic**: Applicable across industries with contextual adaptation
4. **Evidence-Based**: Grounded in proven product development methodologies
5. **Actionable Outputs**: Each skill produces concrete deliverables

### Skills Hierarchy

```
┌─────────────────────────────────────────┐
│     Product Strategy Navigator          │
│         (Master Orchestrator)           │
└─────────────┬───────────────────────────┘
              │
    ┌─────────┴──────────────────┐
    │                            │
┌───▼─────┐                  ┌───▼─────┐
│Discovery│                  │Execution│
│ Skills  │                  │ Skills  │
└─────────┘                  └─────────┘
    │                          │
    ├─ product-discovery       ├─ pilot-planner
    ├─ market-validation       ├─ metrics-evaluator
    ├─ customer-research       └─ pivot-advisor
    └─ problem-framing
              │
    ┌─────────┴───────────────┐
    │                         │
┌───▼─────┐               ┌───▼─────┐
│ Design  │               │Technical│
│ Skills  │               │ Skills  │
└─────────┘               └─────────┘
    │                           │
    ├─ hci-designer             ├─ ai-technology-selector
    ├─ business-model-architect ├─ architecture-designer
    └─ value-proposition        ├─ tech-stack-advisor
                                └─ regulatory-analyzer
```

## Skill Specifications

### Required SKILL.md Structure

```yaml
---
name: skill-name # Hyphen-separated, lowercase
description: Clear description of skill purpose and capabilities
allowed-tools: # Optional: Pre-approved tools for Claude Code
  - tool1
  - tool2
metadata: # Optional: Custom key-value pairs
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

   ```
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

```
User: "Help me validate market demand for a sustainable packaging solution"
System: Activates market-validation skill
Output: TAM/SAM/SOM analysis, competitive landscape, validation report
```

### Pattern 2: Sequential Workflow

```
User: "I want to build a new B2B SaaS product"
System: Orchestrates multiple skills in sequence
Flow: discovery → validation → technology → business model → pilot
```

### Pattern 3: Parallel Processing

```
User: "Analyze this opportunity from multiple angles"
System: Activates multiple skills simultaneously
Parallel: market-validation + ai-technology-selector + business-model-architect
```

### Pattern 4: Adaptive Navigation

```
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

| Metric                   | Target              | Measurement Method          |
| ------------------------ | ------------------- | --------------------------- |
| Skill Load Time          | < 2 seconds         | Timer from trigger to ready |
| Token Efficiency         | < 2000 tokens/skill | Context window usage        |
| Output Quality           | > 8/10 rating       | User feedback scores        |
| Task Success Rate        | > 80%               | Completion tracking         |
| Multi-skill Coordination | > 75% success       | Workflow completion         |

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

| Metric           | Description                             | Target |
| ---------------- | --------------------------------------- | ------ |
| Activation Rate  | % of relevant queries triggering skills | > 85%  |
| Completion Rate  | % of started workflows completed        | > 70%  |
| Value Score      | User rating of output value             | > 8/10 |
| Time Saved       | Hours saved vs. manual process          | > 50%  |
| Decision Quality | % of go/no-go decisions validated       | > 80%  |

### Business Impact Metrics

| Metric          | Description                            | Target    |
| --------------- | -------------------------------------- | --------- |
| Ideas Validated | # of concepts evaluated                | 100/month |
| Pivot Rate      | % of projects successfully pivoted     | > 60%     |
| Time to Market  | Reduction in development time          | -30%      |
| Success Rate    | % of pilots meeting criteria           | > 40%     |
| ROI             | Return on skill development investment | > 5x      |

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

The Hatch Lab Skills Framework transforms AI agents into powerful product strategy consultants. By following this
implementation guide, organizations can systematically build, validate, and launch innovative products with reduced risk
and increased speed to market.

The modular, composable nature of skills ensures flexibility and scalability, while the evidence-based methodologies provide
confidence in decision-making. As the framework evolves, it will continue to incorporate best practices and emerging
patterns in product development.

## Appendices

### A. Skill Development Template

```markdown
---
name: your-skill-name # Hyphen-separated, lowercase
description: Clear 50-200 character description of skill purpose and capabilities
allowed-tools: # Optional: Pre-approved tools
  - tool1
  - tool2
metadata: # Optional
  version: 1.0
  author: Your Name
  category: discovery|strategy|architecture|business|measurement
---

# Skill Name

## Overview

[Brief introduction to what this skill does and when to use it]

## Core Capabilities

- Capability 1
- Capability 2
- Capability 3
- Capability 4
- Capability 5

## Core Framework

### Step 1: [Name]

[Detailed instructions for this step]

### Step 2: [Name]

[Detailed instructions for this step]

### Step 3: [Name]

[Detailed instructions for this step]

## Key Artifacts

1. **[Artifact Name]**: [Description]
2. **[Artifact Name]**: [Description]
3. **[Artifact Name]**: [Description]

## Advanced Techniques (Optional)

### Technique 1: [Name]

[When and how to use this technique]

### Technique 2: [Name]

[When and how to use this technique]

## Example Output
```

[Example of what the skill produces]

```

## Quality Checklist

- [ ] Criteria 1
- [ ] Criteria 2
- [ ] Criteria 3
- [ ] Criteria 4

## Common Mistakes to Avoid

- Mistake 1 and how to avoid it
- Mistake 2 and how to avoid it
- Mistake 3 and how to avoid it

## Key Questions to Ask

1. Question 1?
2. Question 2?
3. Question 3?

## Output Templates

### Template 1: [Name]

```

[Template structure]

```

### Template 2: [Name]

```

[Template structure]

```

## Integration Points

**Inputs from:**
- skill-name-1: What it provides
- skill-name-2: What it provides

**Outputs to:**
- skill-name-3: What you provide
- skill-name-4: What you provide

**Coordinates with:**
- skill-name-5: How you work together
```

### B. Common Orchestration Patterns

#### Pattern 1: Sequential Discovery → Validation → Design

**Use When:** Starting a new product from scratch

```
1. problem-framing (20-40 min)
2. product-discovery (30-60 min)
3. customer-research (45-90 min)
4. market-validation (45-90 min)
5. value-proposition (30-60 min)
6. business-model-architect (60-90 min)
7. pilot-planner (45-90 min)
8. metrics-evaluator (30-60 min)
```

**Total Duration:** 4-8 hours

#### Pattern 2: Parallel Market Analysis

**Use When:** Need fast market insights

```
Launch simultaneously:
- market-validation
- value-proposition
- customer-research

Then consolidate findings into:
- business-model-architect
```

**Total Duration:** 1-2 hours

#### Pattern 3: Technical Deep Dive

**Use When:** Technology choices are critical

```
1. problem-framing (20-40 min)
2. ai-technology-selector (45-90 min)
3. tech-stack-advisor (30-60 min)
4. architecture-designer (60-120 min)
5. regulatory-analyzer (30-60 min)
```

**Total Duration:** 3-6 hours

#### Pattern 4: Pivot Analysis

**Use When:** Product isn't working, need new direction

```
1. metrics-evaluator (analyze current state)
2. pivot-advisor (evaluate options)
3. market-validation (reassess market)
4. value-proposition (refine messaging)
5. customer-research (validate new direction)
6. pilot-planner (test pivot)
```

**Total Duration:** 3-5 hours

### C. Industry-Specific Guidance

#### Healthcare & Medical Devices

**Critical Skills:**

- regulatory-analyzer (HIPAA, FDA, medical device classifications)
- customer-research (clinical workflows, patient safety)
- pilot-planner (clinical trials, IRB approval)

**Special Considerations:**

- Extended validation timelines (12-24 months typical)
- Regulatory approval paths
- Clinical evidence requirements
- Patient safety protocols

#### Financial Services & Fintech

**Critical Skills:**

- regulatory-analyzer (PCI-DSS, SOC 2, financial regulations)
- architecture-designer (security, audit trails)
- business-model-architect (transaction economics)

**Special Considerations:**

- Security and compliance first
- Audit trail requirements
- Transaction cost modeling
- Partnership with regulated entities

#### Consumer Software & SaaS

**Critical Skills:**

- hci-designer (user experience critical)
- metrics-evaluator (growth metrics)
- business-model-architect (pricing, LTV:CAC)

**Special Considerations:**

- Fast iteration cycles
- User experience paramount
- Viral growth potential
- Freemium models common

#### Enterprise B2B

**Critical Skills:**

- customer-research (buying committees, long sales cycles)
- value-proposition (ROI justification)
- pilot-planner (POCs, enterprise pilots)

**Special Considerations:**

- Long sales cycles (6-18 months)
- Multiple stakeholders
- Integration requirements
- Security and compliance

### D. Troubleshooting Common Issues

#### Issue: Skills not activating correctly

**Symptoms:** Skill doesn't load when expected

**Solutions:**

1. Check YAML frontmatter format
2. Verify file naming (hyphen-separated, lowercase)
3. Ensure description is 50-200 characters
4. Check file permissions
5. Restart Claude or reload skills

#### Issue: Context overload / token limits

**Symptoms:** Performance degradation, incomplete responses

**Solutions:**

1. Use progressive disclosure pattern
2. Break work into smaller sessions
3. Use product-strategy-navigator for routing
4. Clear context between major sections
5. Focus on one skill at a time

#### Issue: Skills producing inconsistent outputs

**Symptoms:** Variable quality, different formats

**Solutions:**

1. Review skill templates and examples
2. Be more specific in prompts
3. Use quality checklists
4. Provide more context about project
5. Iterate on outputs with follow-up prompts

#### Issue: Integration between skills failing

**Symptoms:** Context loss, repeated information requests

**Solutions:**

1. Use product-strategy-navigator for orchestration
2. Explicitly reference previous skill outputs
3. Maintain project context document
4. Use structured handoff formats
5. Document key decisions and findings

#### Issue: Skill selection unclear

**Symptoms:** Unsure which skill to use

**Solutions:**

1. Start with product-strategy-navigator
2. Review skills summary table in README
3. Check "Integrates with" sections
4. Follow common workflow patterns
5. Use multiple skills for complex questions

#### Issue: Output not actionable enough

**Symptoms:** Too generic, not specific to your context

**Solutions:**

1. Provide more project details
2. Share actual data/examples
3. Request specific templates
4. Ask for step-by-step guidance
5. Iterate with clarifying questions

#### Issue: Performance/speed concerns

**Symptoms:** Skills taking too long to respond

**Solutions:**

1. Use haiku model for simpler tasks
2. Break complex analyses into phases
3. Cache common reference materials
4. Parallel process independent skills
5. Use summary mode for large documents

---

_Version 1.0 - November 2025_
_Based on MIT's Designing and Building AI Products and Services curriculum_
_Aligned with Anthropic's Agent Skills specification_
