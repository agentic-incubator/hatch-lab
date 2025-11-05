---
name: tech-stack-advisor
description: Recommends optimal technology stacks based on project requirements, team expertise, scalability needs, and industry best practices while considering trade-offs between different technologies and frameworks
---

# Tech Stack Advisor Skill

This skill helps you select the optimal technology stack for your project by evaluating options across frontend, backend,
database, infrastructure, and tooling layers while considering technical and business constraints.

## Core Capabilities

I can help you:

- Select appropriate programming languages and frameworks
- Choose databases and storage solutions
- Recommend infrastructure and deployment options
- Evaluate build tools and development workflows
- Assess technology trade-offs and risks
- Plan technology migrations
- Ensure stack compatibility and integration
- Consider team expertise and hiring factors

## Tech Stack Selection Framework

### Step 1: Requirements Assessment

#### Project Requirements Matrix

```
PROJECT TYPE
├─ Web Application
│   ├─ SPA (React, Vue, Angular)
│   ├─ SSR (Next.js, Nuxt, SvelteKit)
│   └─ MPA (Rails, Django, Laravel)
├─ Mobile Application
│   ├─ Native (Swift, Kotlin)
│   ├─ Cross-platform (React Native, Flutter)
│   └─ Hybrid (Ionic, Capacitor)
├─ API/Backend
│   ├─ REST (Express, FastAPI, Spring)
│   ├─ GraphQL (Apollo, Graphene)
│   └─ gRPC (protobuf-based)
└─ Data/AI
    ├─ Analytics (Python, R, Spark)
    ├─ ML/AI (TensorFlow, PyTorch)
    └─ Streaming (Kafka, Pulsar)
```

#### Constraint Analysis

```
TECHNICAL CONSTRAINTS
├─ Performance requirements
├─ Scalability needs
├─ Security requirements
├─ Integration needs
└─ Platform limitations

BUSINESS CONSTRAINTS
├─ Budget limitations
├─ Timeline pressure
├─ Team expertise
├─ Vendor preferences
└─ Compliance requirements

OPERATIONAL CONSTRAINTS
├─ Deployment environment
├─ Maintenance capacity
├─ Monitoring needs
├─ Support requirements
└─ DevOps maturity
```

### Step 2: Frontend Stack Selection

#### JavaScript Frameworks

```
REACT
├─ Pros: Large ecosystem, flexible, reusable
├─ Cons: Learning curve, decision fatigue
├─ Best for: Complex UIs, large teams
└─ Ecosystem: Next.js, Redux, MUI

VUE
├─ Pros: Gentle learning, progressive, elegant
├─ Cons: Smaller ecosystem, less corporate
├─ Best for: Rapid prototyping, small teams
└─ Ecosystem: Nuxt, Vuex, Vuetify

ANGULAR
├─ Pros: Full framework, TypeScript, enterprise
├─ Cons: Complexity, verbose, heavy
├─ Best for: Enterprise apps, large teams
└─ Ecosystem: RxJS, Angular Material

SVELTE
├─ Pros: No runtime, fast, simple
├─ Cons: Smaller community, fewer libraries
├─ Best for: Performance-critical, small apps
└─ Ecosystem: SvelteKit, Svelte Store
```

#### Mobile Frameworks

```
NATIVE
├─ iOS: Swift + SwiftUI/UIKit
├─ Android: Kotlin + Jetpack Compose
├─ Pros: Best performance, platform features
└─ Cons: Dual codebases, specialized skills

REACT NATIVE
├─ Language: JavaScript/TypeScript
├─ Pros: Code reuse, web developer friendly
├─ Cons: Performance overhead, native modules
└─ Best for: Content apps, rapid deployment

FLUTTER
├─ Language: Dart
├─ Pros: Hot reload, consistent UI, performance
├─ Cons: Large app size, Dart learning
└─ Best for: Beautiful UIs, cross-platform

KOTLIN MULTIPLATFORM
├─ Language: Kotlin
├─ Pros: Native performance, code sharing
├─ Cons: Newer, smaller community
└─ Best for: Business logic sharing
```

### Step 3: Backend Stack Selection

#### Programming Languages

```
JAVASCRIPT/TYPESCRIPT (Node.js)
├─ Frameworks: Express, NestJS, Fastify
├─ Pros: Full-stack JS, async, npm ecosystem
├─ Cons: CPU-intensive tasks, callback hell
└─ Best for: Real-time, I/O heavy, APIs

PYTHON
├─ Frameworks: Django, FastAPI, Flask
├─ Pros: Readable, ML/AI libs, rapid dev
├─ Cons: GIL, performance, deployment
└─ Best for: Data apps, ML/AI, prototypes

JAVA/KOTLIN
├─ Frameworks: Spring, Micronaut, Ktor
├─ Pros: Performance, enterprise, mature
├─ Cons: Verbose, memory usage, complexity
└─ Best for: Enterprise, microservices

GO
├─ Frameworks: Gin, Echo, Fiber
├─ Pros: Performance, concurrency, simple
├─ Cons: Less expressive, smaller ecosystem
└─ Best for: Microservices, CLI tools, DevOps

RUST
├─ Frameworks: Actix, Rocket, Axum
├─ Pros: Performance, safety, systems
├─ Cons: Learning curve, compile times
└─ Best for: Systems, performance-critical

C#/.NET
├─ Frameworks: ASP.NET Core, Minimal APIs
├─ Pros: Microsoft ecosystem, cross-platform
├─ Cons: Windows-centric history, licensing
└─ Best for: Enterprise, Windows, games
```

#### API Paradigms

```
REST
├─ Pros: Simple, cacheable, standard
├─ Cons: Over/under-fetching, versioning
└─ Tools: OpenAPI, Postman

GraphQL
├─ Pros: Flexible queries, typed, efficient
├─ Cons: Complexity, caching harder
└─ Tools: Apollo, Relay, GraphiQL

gRPC
├─ Pros: Performance, streaming, typed
├─ Cons: Browser support, debugging
└─ Tools: protobuf, grpcurl

WebSockets
├─ Pros: Real-time, bidirectional
├─ Cons: Stateful, scaling complexity
└─ Tools: Socket.io, ws
```

### Step 4: Database Selection

#### Database Decision Tree

```
STRUCTURED DATA?
├─ Yes → Relationships?
│   ├─ Yes → ACID Required?
│   │   ├─ Yes → PostgreSQL/MySQL
│   │   └─ No → MongoDB/DynamoDB
│   └─ No → Query Complexity?
│       ├─ High → PostgreSQL
│       └─ Low → Key-Value Store
└─ No → Data Type?
    ├─ Documents → MongoDB/CouchDB
    ├─ Time-series → InfluxDB/TimescaleDB
    ├─ Graph → Neo4j/Amazon Neptune
    └─ Search → Elasticsearch/Solr
```

#### Database Comparisons

```
RELATIONAL
PostgreSQL: Feature-rich, extensions, reliable
MySQL: Fast, simple, widely supported
SQLite: Embedded, serverless, simple
SQL Server: Microsoft ecosystem, enterprise

NoSQL DOCUMENT
MongoDB: Flexible, scalable, popular
DynamoDB: Managed, scalable, AWS
CouchDB: Sync, offline-first, REST API
RavenDB: .NET friendly, ACID, multi-model

KEY-VALUE
Redis: In-memory, fast, data structures
Memcached: Simple, fast, caching only
DynamoDB: Managed, scalable, consistent

TIME-SERIES
InfluxDB: Purpose-built, SQL-like, efficient
TimescaleDB: PostgreSQL extension, SQL
Prometheus: Metrics, monitoring, pull-based

GRAPH
Neo4j: Mature, Cypher query, visualization
Amazon Neptune: Managed, multiple models
ArangoDB: Multi-model, flexible, ACID
```

### Step 5: Infrastructure & DevOps

#### Deployment Options

```
TRADITIONAL
├─ VPS (DigitalOcean, Linode, Vultr)
├─ Pros: Control, predictable cost
├─ Cons: Management overhead, scaling
└─ Best for: Small apps, fixed load

CONTAINERIZED
├─ Docker + Kubernetes
├─ Pros: Portable, scalable, standard
├─ Cons: Complexity, learning curve
└─ Best for: Microservices, scale

SERVERLESS
├─ AWS Lambda, Vercel, Netlify
├─ Pros: No ops, auto-scale, pay-per-use
├─ Cons: Vendor lock-in, cold starts
└─ Best for: Variable load, event-driven

PAAS
├─ Heroku, Render, Railway
├─ Pros: Simple, fast deployment
├─ Cons: Cost at scale, less control
└─ Best for: Prototypes, small teams
```

#### CI/CD Tools

```
VERSION CONTROL
├─ Git (GitHub, GitLab, Bitbucket)
├─ Branching strategies (GitFlow, GitHub Flow)
└─ Code review process

CI/CD PLATFORMS
├─ GitHub Actions: Integrated, simple
├─ GitLab CI: Full DevOps platform
├─ Jenkins: Flexible, self-hosted
├─ CircleCI: Fast, cloud-native
└─ BuildKite: Hybrid, scalable

DEPLOYMENT TOOLS
├─ Terraform: Infrastructure as code
├─ Ansible: Configuration management
├─ ArgoCD: GitOps for Kubernetes
└─ Helm: Kubernetes package manager
```

### Step 6: Supporting Tools

#### Development Tools

```
IDE/EDITORS
├─ VS Code: Universal, extensible
├─ JetBrains: Language-specific, powerful
├─ Vim/Neovim: Terminal, efficient
└─ Sublime/Atom: Lightweight, customizable

TESTING
├─ Unit: Jest, pytest, JUnit
├─ Integration: Postman, Supertest
├─ E2E: Cypress, Playwright, Selenium
└─ Performance: K6, JMeter, Gatling

MONITORING
├─ APM: DataDog, New Relic, AppDynamics
├─ Logging: ELK Stack, Splunk, CloudWatch
├─ Metrics: Prometheus + Grafana
└─ Errors: Sentry, Rollbar, Bugsnag
```

## Stack Evaluation Matrix

### Evaluation Criteria

```
TECHNICAL FIT (40%)
├─ Performance requirements
├─ Scalability potential
├─ Security capabilities
├─ Integration options
└─ Feature completeness

TEAM FIT (30%)
├─ Current expertise
├─ Learning curve
├─ Available talent
├─ Community support
└─ Documentation quality

BUSINESS FIT (20%)
├─ Cost (licenses, hosting, development)
├─ Time to market
├─ Vendor stability
├─ Future-proofing
└─ Exit strategy

OPERATIONAL FIT (10%)
├─ Deployment complexity
├─ Maintenance burden
├─ Monitoring capabilities
├─ Debugging tools
└─ Upgrade path
```

## Stack Recommendations by Use Case

### SaaS Application

```yaml
Frontend: React + Next.js + TypeScript
Backend: Node.js + NestJS
Database: PostgreSQL + Redis
Infrastructure: AWS/GCP + Kubernetes
Monitoring: DataDog + Sentry
```

### E-commerce Platform

```yaml
Frontend: Vue + Nuxt.js
Backend: Python + Django
Database: PostgreSQL + Elasticsearch
Infrastructure: AWS + CloudFront
Payments: Stripe/PayPal
```

### Real-time Collaboration

```yaml
Frontend: React + Socket.io client
Backend: Node.js + Socket.io
Database: MongoDB + Redis
Infrastructure: AWS + ALB + ECS
WebRTC: Daily.co/Twilio
```

### Mobile-First Social App

```yaml
Mobile: React Native + Expo
Backend: Go + Gin
Database: PostgreSQL + DynamoDB
Infrastructure: AWS + Lambda
Push: Firebase Cloud Messaging
```

### Data Analytics Platform

```yaml
Frontend: React + D3.js/Recharts
Backend: Python + FastAPI
Database: ClickHouse + PostgreSQL
Processing: Apache Spark + Kafka
Infrastructure: AWS + EMR
```

## Migration Strategies

### Incremental Migration

```
STRANGLER FIG PATTERN
Old System → Facade → New System
     ↓          ↓         ↑
  Gradual    Route    Build
  Decline   Traffic   Features
```

### Big Bang Migration

```
PARALLEL RUN
Old System → Compare → New System
     ↓         ↓          ↑
   Keep      Verify    Deploy
  Running    Results    Ready
```

## Questions I'll Ask You

To recommend your tech stack:

- What type of application?
- What are your performance requirements?
- What's your team's expertise?
- What's your budget?
- What's your timeline?
- What integrations are needed?
- What's your scaling projection?

## Output Templates

### Tech Stack Recommendation

```markdown
## Recommended Tech Stack

### Summary

[Overview of recommended stack]

### Frontend

- Framework: [Choice + rationale]
- State Management: [Choice]
- UI Library: [Choice]
- Build Tool: [Choice]

### Backend

- Language: [Choice + rationale]
- Framework: [Choice]
- API Style: [REST/GraphQL/gRPC]

### Database

- Primary: [Choice + rationale]
- Cache: [Choice]
- Search: [If needed]

### Infrastructure

- Hosting: [Choice]
- Deployment: [Strategy]
- Monitoring: [Tools]

### Trade-offs

- Pros: [Benefits]
- Cons: [Limitations]
- Risks: [Mitigation]
```

### Technology Comparison

```markdown
## Technology Comparison: [Options]

| Criteria       | Option A | Option B | Option C |
| -------------- | -------- | -------- | -------- |
| Performance    | [Rating] | [Rating] | [Rating] |
| Scalability    | [Rating] | [Rating] | [Rating] |
| Team Expertise | [Rating] | [Rating] | [Rating] |
| Cost           | [Rating] | [Rating] | [Rating] |
| Community      | [Rating] | [Rating] | [Rating] |

### Recommendation

[Choice with detailed rationale]
```

## Integration Points

- **Informed by**: `architecture-designer`, `requirements`
- **Influences**: `development-planning`, `hiring`
- **Coordinates with**: `ai-technology-selector`

## Common Stack Selection Mistakes

⚠️ **Resume-Driven Development**: Choosing for learning
⚠️ **Hype-Driven Decisions**: Following trends blindly
⚠️ **Over-Engineering**: Too complex for needs
⚠️ **Under-Specifying**: Missing critical requirements
⚠️ **Ignoring TCO**: Only considering initial cost

Let's select your technology stack. What are you building and what are your constraints?
