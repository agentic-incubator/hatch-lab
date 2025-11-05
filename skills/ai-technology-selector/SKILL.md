---
name: ai-technology-selector
description: Matches AI technologies to business problems, evaluates technical feasibility, assesses build-vs-buy decisions, and creates implementation roadmaps considering intellectual property, ethics, and scalability
---

# AI Technology Selector Skill

This skill helps you identify and select the right AI technologies for your product, evaluate technical feasibility, and
create implementation strategies that balance innovation with practical constraints.

## Core Capabilities

I can help you:

- Map business problems to AI capabilities
- Evaluate different AI approaches (ML, DL, Gen AI, Classical AI)
- Assess build vs. buy vs. partner decisions
- Analyze intellectual property implications
- Create technical implementation roadmaps
- Identify data requirements and constraints
- Evaluate ethical and regulatory considerations

## AI Technology Selection Framework

### Step 1: Problem-Technology Mapping

#### Cognitive Process Alignment

```
BUSINESS NEED → COGNITIVE CAPABILITY → AI TECHNOLOGY
```

**Core Cognitive Processes**:

1. **SENSE** (Perception)
   - Technologies: Computer Vision, Speech Recognition, NLP
   - Use Cases: Quality inspection, voice interfaces, document processing

2. **LEARN** (Pattern Recognition)
   - Technologies: Machine Learning, Deep Learning, Reinforcement Learning
   - Use Cases: Prediction, classification, anomaly detection

3. **REASON** (Logic & Planning)
   - Technologies: Expert Systems, Knowledge Graphs, Constraint Solvers
   - Use Cases: Diagnosis, scheduling, configuration

4. **CREATE** (Generation)
   - Technologies: Generative AI, GANs, Transformers
   - Use Cases: Content creation, design, synthesis

5. **INTERACT** (Communication)
   - Technologies: Conversational AI, NLU, Dialog Systems
   - Use Cases: Customer service, virtual assistants, collaboration

### Step 2: Technology Deep Dive

#### Machine Learning Taxonomy

```
┌─────────────────────────────────┐
│         Supervised              │
│  ├─ Regression                  │
│  ├─ Classification              │
│  └─ Time Series                 │
├─────────────────────────────────┤
│         Unsupervised            │
│  ├─ Clustering                  │
│  ├─ Dimensionality Reduction    │
│  └─ Anomaly Detection           │
├─────────────────────────────────┤
│         Reinforcement           │
│  ├─ Policy Optimization         │
│  ├─ Value Learning              │
│  └─ Multi-Agent                 │
└─────────────────────────────────┘
```

#### Generative AI Options

```
TEXT                    IMAGE                   CODE
├─ GPT-4/Claude        ├─ Stable Diffusion    ├─ Codex/Copilot
├─ Llama/Mistral       ├─ Midjourney          ├─ CodeLlama
├─ Domain-Specific     ├─ DALL-E              ├─ StarCoder
└─ Fine-tuned          └─ Custom GANs         └─ Domain Models
```

### Step 3: Build vs. Buy Decision Matrix

| Factor               | Build                      | Buy                          | Hybrid                    |
| -------------------- | -------------------------- | ---------------------------- | ------------------------- |
| **When Appropriate** | Core differentiator        | Commodity capability         | Some customization needed |
| **Time to Market**   | 6-18 months                | 1-3 months                   | 3-6 months                |
| **Cost Structure**   | High upfront, low marginal | Low upfront, per-use pricing | Moderate both             |
| **Control**          | Full                       | Limited                      | Partial                   |
| **IP Ownership**     | Full                       | None/Limited                 | Shared                    |
| **Maintenance**      | Internal team              | Vendor                       | Shared                    |

### Step 4: Technical Feasibility Assessment

#### Data Requirements Evaluation

```
DATA AVAILABILITY
     ├─ Volume: [Sufficient?]
     ├─ Quality: [Clean/Labeled?]
     ├─ Variety: [Representative?]
     ├─ Velocity: [Real-time needs?]
     └─ Privacy: [Compliance?]
```

#### Infrastructure Needs

- **Compute**: GPU/TPU requirements
- **Storage**: Data lake/warehouse needs
- **Networking**: Latency requirements
- **Deployment**: Edge/Cloud/Hybrid

### Step 5: Implementation Roadmap

#### Phase 1: Proof of Concept (Months 1-3)

```markdown
- [ ] Data collection and preparation
- [ ] Model selection and baseline
- [ ] Initial training and validation
- [ ] Technical feasibility confirmed
```

#### Phase 2: Pilot Development (Months 4-6)

```markdown
- [ ] Production pipeline design
- [ ] Model optimization
- [ ] Integration planning
- [ ] Limited deployment
```

#### Phase 3: Scale Implementation (Months 7-12)

```markdown
- [ ] Full production deployment
- [ ] Monitoring and feedback loops
- [ ] Performance optimization
- [ ] Continuous improvement
```

## Technology Selection Artifacts

I'll help you create:

1. **AI Technology Recommendation Report**
2. **Technical Architecture Diagram**
3. **Data Requirements Specification**
4. **Risk Assessment Matrix**
5. **Implementation Roadmap**
6. **IP Strategy Document**

## Advanced Considerations

### Intellectual Property Strategy

**IP Opportunities**:

- Proprietary algorithms
- Novel architectures
- Domain-specific models
- Unique data combinations
- Integration patterns

**IP Risks**:

- Model provider dependencies
- Training data ownership
- Output rights
- Patent landscapes
- Open source obligations

### Ethical AI Framework

**Principles to Address**:

1. **Fairness**: Bias detection and mitigation
2. **Explainability**: Model interpretability
3. **Privacy**: Data protection and consent
4. **Safety**: Failure modes and fallbacks
5. **Accountability**: Governance and oversight

### Regulatory Compliance

**Key Regulations**:

- GDPR (Data Privacy)
- CCPA (California Privacy)
- AI Act (EU AI Regulation)
- Industry-specific (HIPAA, FINRA, etc.)

## Example Technology Selection

**Problem**: Automated customer support for technical products

**Selected Technologies**:

```markdown
### Primary Stack

- **NLU Engine**: Claude API for understanding
- **Knowledge Base**: Vector DB (Pinecone) + RAG
- **Dialog Management**: Langchain orchestration
- **Voice (Optional)**: Whisper + ElevenLabs

### Architecture

- **Deployment**: Serverless (AWS Lambda)
- **Monitoring**: Langfuse for LLM ops
- **Feedback**: Human-in-the-loop for improvements

### Build vs Buy Decision

- **Buy**: LLM capabilities (Claude API)
- **Build**: Domain knowledge layer
- **Hybrid**: Dialog orchestration
```

## Technology Evaluation Checklist

### Technical Readiness

- [ ] Technology maturity level
- [ ] Available skills/expertise
- [ ] Integration complexity
- [ ] Scalability potential
- [ ] Performance requirements met

### Business Alignment

- [ ] Cost-benefit positive
- [ ] Acceptable time to market
- [ ] Risk tolerance match
- [ ] Strategic fit
- [ ] Competitive advantage

### Operational Readiness

- [ ] Data pipeline ready
- [ ] Infrastructure available
- [ ] Team training plan
- [ ] Maintenance strategy
- [ ] Monitoring approach

## Questions I'll Ask You

To recommend the best AI technology:

- What specific problem are you solving?
- What data do you have available?
- What's your budget and timeline?
- What technical expertise exists in your team?
- What are your accuracy/performance requirements?
- What regulatory constraints apply?
- Is this a core differentiator or supporting feature?

## Output Templates

### Technology Recommendation

```markdown
## AI Technology Recommendation

### Problem Statement

[Description of business problem]

### Recommended Approach

**Primary Technology**: [e.g., Transformer-based NLP]
**Specific Implementation**: [e.g., Fine-tuned Claude]
**Architecture Pattern**: [e.g., RAG with vector store]

### Rationale

- **Why This Technology**:
- **Alternatives Considered**:
- **Key Tradeoffs**:

### Implementation Plan

**Phase 1**: [Timeline & Milestones]
**Phase 2**: [Timeline & Milestones]
**Phase 3**: [Timeline & Milestones]
```

### Risk Assessment

```markdown
## Technical Risk Analysis

### High Risks

- **Risk**: [Description]
  **Mitigation**: [Strategy]

### Medium Risks

- **Risk**: [Description]
  **Mitigation**: [Strategy]

### Dependencies

- External APIs
- Data availability
- Regulatory approval
```

## Integration Points

- **Inputs from**: `product-discovery`, `market-validation`
- **Outputs to**: `pilot-planner`, `metrics-evaluator`
- **Coordinates with**: `business-model-architect` (cost implications)

## Red Flags

⚠️ **Insufficient Data**: <1000 quality examples
⚠️ **Unrealistic Expectations**: 100% accuracy required
⚠️ **Technical Mismatch**: Wrong tool for problem
⚠️ **Regulatory Blocker**: Non-compliant approach
⚠️ **Cost Prohibitive**: ROI < 0

Let's select the right AI technology for your product. What problem are you trying to solve with AI?
