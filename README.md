# Hatch Lab: Product Strategy Skills Framework

**Transform Claude into a specialized product strategy consultant through 15 production-ready skills.**

Hatch Lab provides systematic, AI-guided frameworks for product discovery, validation, design, and launch.
Built on Anthropic's Agent Skills specification and inspired by MIT's product development curriculum.

---

## Quick Start

### Installation

**Option 1: Claude.ai**

1. Upload the `skills/` folder to Claude.ai Settings → Skills
2. Skills activate automatically based on your queries

**Option 2: Claude API**

```python
client.messages.create(
    model="claude-opus-4-1-20250805",
    messages=[{"role": "user", "content": "Analyze market for..."}],
    skills=[{"type": "custom", "path": "./skills/market-validation"}]
)
```

### Your First Session

- **New to product strategy?** → Start with `product-strategy-navigator` (guides you through entire journey)
- **Have specific question?** → Jump to a specific skill (see catalog below)
- **Need workflow guidance?** → See [SKILLS_DEPENDENCY_MAP.md](./SKILLS_DEPENDENCY_MAP.md)

---

## Skills Catalog

**15 production-ready skills organized by product development stage:**

### 🎯 Discovery & Strategy (6 skills)

- **problem-framing** - Systematically define problems using root cause analysis
- **product-discovery** - Explore problem spaces and identify opportunities
- **customer-research** - Design and execute research programs, develop personas
- **market-validation** - Validate demand, analyze competition, size markets (TAM/SAM/SOM)
- **value-proposition** - Craft compelling positioning and messaging
- **pivot-advisor** - Guide strategic pivots based on data and feedback

### 🏗️ Design & Architecture (4 skills)

- **hci-designer** - Create human-centered interfaces and experiences
- **architecture-designer** - Design scalable technical architectures
- **tech-stack-advisor** - Recommend optimal technology stacks
- **ai-technology-selector** - Match AI/ML capabilities to business problems

### 💼 Business & Operations (3 skills)

- **business-model-architect** - Design revenue models and unit economics
- **pilot-planner** - Structure pilot programs and define MVPs
- **regulatory-analyzer** - Analyze compliance requirements (GDPR, HIPAA, etc.)

### 📊 Measurement & Orchestration (2 skills)

- **metrics-evaluator** - Define KPIs and track performance
- **product-strategy-navigator** ⭐ - Orchestrate complete product journeys (master skill)

**→ [View detailed skill descriptions](./SKILLS_CATALOG.md)**

---

## Common Use Cases

| Scenario                     | Recommended Path                                                    | Est. Time   |
| ---------------------------- | ------------------------------------------------------------------- | ----------- |
| **New product from scratch** | product-strategy-navigator                                          | 11-18 hours |
| **Validate existing idea**   | market-validation → business-model-architect → pilot-planner        | 2-3 hours   |
| **Technical architecture**   | ai-technology-selector → tech-stack-advisor → architecture-designer | 3-6 hours   |
| **Product struggling**       | metrics-evaluator → pivot-advisor                                   | 3-4 hours   |
| **Specific question**        | Jump to relevant skill                                              | 20-120 min  |

**→ [View detailed workflows and dependencies](./SKILLS_DEPENDENCY_MAP.md)**

---

## Documentation

| Document                                                   | Purpose                                      |
| ---------------------------------------------------------- | -------------------------------------------- |
| **[SKILLS_CATALOG.md](./SKILLS_CATALOG.md)**               | Complete skill descriptions, success metrics |
| **[SKILLS_DEPENDENCY_MAP.md](./SKILLS_DEPENDENCY_MAP.md)** | Workflows, dependencies, journey patterns    |
| **[CONTRIBUTING.md](./CONTRIBUTING.md)**                   | Contribution guidelines and standards        |

---

## Quick Examples

**Startup founder:**

```
"I want to build a SaaS platform for supply chain sustainability"
→ Start with product-strategy-navigator
→ Get complete strategy in 11-18 hours
```

**Product manager:**

```
"Help me validate demand for this new feature"
→ Use market-validation
→ Get TAM/SAM/SOM analysis in 45-90 min
```

**Engineering lead:**

```
"Should we use microservices or monolith?"
→ Use architecture-designer
→ Get architecture decision in 60-120 min
```

---

## Project Status

- **Version**: 1.0 (November 2025)
- **Skills**: 15/15 production-ready
- **Status**: Active development
- **License**: MIT

---

## Contributing

We welcome contributions! See **[CONTRIBUTING.md](./CONTRIBUTING.md)** for:

- Skill development guidelines
- Testing requirements
- Submission process
- Style guide

---

## Support & Community

- **Issues**: Report bugs or request features via GitHub Issues
- **Discussions**: Ask questions or share use cases in GitHub Discussions
- **Documentation**: All guides available in this repository

---

## Acknowledgments

Built on [Anthropic's Agent Skills framework](https://docs.anthropic.com/claude/docs) and inspired by
MIT's [Designing and Building AI Products and Services](https://xpro.mit.edu/courses/course-v1:xPRO+AIPSx+R1/) curriculum.

---

## License

MIT - See [LICENSE](./LICENSE) file for details.
