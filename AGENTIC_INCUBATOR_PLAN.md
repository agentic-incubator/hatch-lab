# Hatch Lab: Claude Skills for Product Strategy Development

## Vision

Transform the systematic product strategy methodologies from the MIT Capstone workbook into a curated collection of Claude Skills that enable AI agents to guide innovators through new product development across any industry.

## Core Value Proposition

These skills convert Claude into a specialized product strategy consultant that can:

- Guide systematic problem discovery and validation
- Evaluate market opportunities and competitive dynamics
- Select appropriate AI technologies and architectures
- Design sustainable business models and revenue strategies
- Plan and execute pilots for product-market fit validation
- Measure success and guide strategic pivots

## Skills Architecture

### 1. Foundation Layer - Discovery & Validation

These skills help users understand problems deeply before jumping to solutions:

**product-discovery**

- Maps customer journeys and pain points
- Applies jobs-to-be-done framework
- Generates opportunity matrices
- Creates validated problem statements

**market-validation**

- Calculates TAM/SAM/SOM
- Analyzes competitive landscapes
- Validates willingness to pay
- Assesses market timing

**customer-research** (planned)

- Designs research protocols
- Creates interview guides
- Analyzes qualitative data
- Synthesizes insights

### 2. Design Layer - Solution & Model Creation

These skills help design the right solution and business approach:

**ai-technology-selector**

- Maps problems to AI capabilities
- Evaluates build vs. buy decisions
- Assesses technical feasibility
- Creates implementation roadmaps

**business-model-architect**

- Designs revenue models
- Calculates unit economics
- Creates value propositions
- Plans scaling strategies

**hci-designer** (planned)

- Creates user personas
- Designs interaction flows
- Applies usability heuristics
- Produces wireframes

### 3. Execution Layer - Build & Measure
These skills guide implementation and optimization:

**pilot-planner**

- Defines MVP scope
- Structures pilot programs
- Establishes success criteria
- Creates rollout strategies

**metrics-evaluator** (planned)
- Defines KPIs
- Creates dashboards
- Analyzes performance
- Recommends optimizations

**pivot-advisor** (planned)

- Identifies pivot triggers
- Evaluates strategic options
- Guides transitions
- Manages stakeholder communication

### 4. Orchestration Layer - Journey Navigation

The master skill that coordinates all others:

**product-strategy-navigator**

- Assesses starting point
- Routes to appropriate skills
- Maintains context across skills
- Synthesizes outputs
- Guides complete journey

## Implementation Strategy

### Phase 1: Core Skills (Complete)

✅ Created 6 foundational skills:
- product-discovery
- market-validation
- ai-technology-selector
- business-model-architect
- pilot-planner
- product-strategy-navigator

### Phase 2: Enhanced Capabilities (Next Steps)

- [ ] Add remaining execution skills (metrics-evaluator, pivot-advisor)
- [ ] Create industry-specific variations
- [ ] Develop advanced orchestration patterns
- [ ] Build skill composition templates

### Phase 3: Intelligence Layer (Future)
- [ ] Adaptive skill selection based on context
- [ ] Learning from user interactions
- [ ] Automated workflow optimization
- [ ] Community skill contributions

## Technical Specifications

### Skill Structure

Each skill follows Anthropic's specification:

```yaml
---
name: skill-name
description: Purpose and capabilities (50-200 chars)
---
# Skill Content
[Comprehensive instructions and frameworks]
```

### Progressive Disclosure Pattern

1. **Metadata**: ~100 tokens in system prompt
2. **Core Instructions**: Loaded when relevant
3. **Deep Resources**: Additional files on demand

### Integration Methods

- **Claude.ai**: Upload to settings
- **Claude API**: Include in API calls
- **Claude Code**: Install as plugins

## Usage Scenarios

### Scenario 1: Startup Founder

"I have an idea for a productivity app"

- Navigator assesses idea maturity
- Routes through discovery → validation → design
- Outputs: Problem validation, market size, MVP plan

### Scenario 2: Corporate Innovation Team

"We need to explore AI opportunities in supply chain"

- Parallel activation of discovery + AI selector
- Identifies high-value use cases
- Outputs: Opportunity matrix, technology recommendations

### Scenario 3: Product Manager

"Help me pivot our failing product"

- Pivot-advisor analyzes current state
- Routes to appropriate interventions
- Outputs: Pivot options, transition plan

## Key Differentiators

### vs. Generic AI Assistants

- **Structured Methodology**: Proven frameworks, not ad-hoc advice
- **Progressive Depth**: Right level of detail at each stage
- **Actionable Outputs**: Concrete deliverables, not just text

### vs. Human Consultants

- **Always Available**: 24/7 guidance
- **Consistent Quality**: Best practices every time
- **Cost Effective**: Fraction of consulting fees
- **Scalable**: Serve unlimited users simultaneously

### vs. Static Frameworks

- **Interactive**: Adapts to user context
- **Integrated**: Skills work together seamlessly
- **Current**: Updated with latest methodologies
- **Intelligent**: Learns from patterns

## Success Metrics

### Skill Performance

- Activation accuracy > 85%
- Task completion > 70%
- User satisfaction > 8/10
- Time saved > 50%

### Business Impact

- Ideas validated: 100+/month
- Successful pivots > 60%
- Time to market -30%
- ROI > 5x investment

## Risk Mitigation

### Technical Risks

- **Token Limits**: Progressive disclosure design
- **Skill Conflicts**: Clear boundaries and handoffs
- **Performance**: Optimize for common paths

### User Risks

- **Over-reliance**: Emphasize human judgment
- **Misapplication**: Clear scope boundaries
- **Quality**: Continuous improvement cycles

## Development Roadmap

### Q4 2025

- Complete core skill set
- Initial user testing
- Performance optimization

### Q1 2026

- Industry variations
- Advanced orchestration
- Integration tools

### Q2 2026

- Marketplace launch
- Community skills
- Enterprise features

### Q3 2026

- Intelligence layer
- Automated workflows
- Scale to 1000+ users

## Call to Action

### For Developers

1. Clone the repository
2. Test with your use cases
3. Contribute improvements
4. Create specialized skills

### For Organizations

1. Pilot with innovation teams
2. Customize for your industry
3. Integrate with existing tools
4. Measure impact on innovation velocity

### For Entrepreneurs

1. Use skills for your next idea
2. Validate before building
3. Share success stories
4. Request new capabilities

## Conclusion

The Hatch Lab transforms how products are conceived, validated, and launched. By encoding proven methodologies into Claude Skills, we democratize access to world-class product strategy expertise.

These skills don't replace human creativity and judgment - they amplify it. They handle the frameworks, analysis, and structure, freeing innovators to focus on vision, creativity, and execution.

The future of product development is human creativity augmented by AI-powered methodology. The Hatch Lab makes that future accessible today.

---

## Resources

### Documentation

- [Implementation Guide](./IMPLEMENTATION_GUIDE.md)
- [Skill Specifications](./README.md)
- Individual skill documentation in `/skills/`

### Repository Structure

```text
agentic-incubator/
├── README.md                    # Framework overview
├── IMPLEMENTATION_GUIDE.md      # Detailed implementation
├── AGENTIC_INCUBATOR_PLAN.md   # This document
└── skills/                      # Individual skills
    ├── product-discovery/
    ├── market-validation/
    ├── ai-technology-selector/
    ├── business-model-architect/
    ├── pilot-planner/
    └── product-strategy-navigator/
```

### Contact & Contribution

- GitHub: [your-repo-url]
- Issues: Report bugs and request features
- Discussions: Share use cases and patterns
- Pull Requests: Contribute improvements

---

*Built on Anthropic's Agent Skills framework*
*Inspired by MIT's Designing and Building AI Products and Services*
*Version 1.0 - October 2025*
