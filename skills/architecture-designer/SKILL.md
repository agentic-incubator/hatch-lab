---
name: architecture-designer
description: Designs scalable technical architectures using system design principles, cloud patterns, microservices, and distributed systems best practices to ensure robust, maintainable, and performant solutions
---

# Architecture Designer Skill

This skill helps you design robust, scalable technical architectures that support your business goals. Using proven patterns
and best practices, we'll create systems that are maintainable, performant, and cost-effective.

## Core Capabilities

I can help you:

- Design system architectures from scratch
- Evaluate architectural trade-offs
- Select appropriate design patterns
- Plan for scalability and reliability
- Design data models and flows
- Create API strategies
- Implement security architectures
- Plan migration and modernization

## Architecture Design Framework

### Step 1: Requirements Analysis

#### Functional Requirements

```
CORE FEATURES
├─ User Management
├─ Business Logic
├─ Data Operations
├─ Integrations
└─ Reporting

USER STORIES → CAPABILITIES → COMPONENTS
```

#### Non-Functional Requirements (NFRs)

```
PERFORMANCE
├─ Response time (<200ms p95)
├─ Throughput (requests/second)
├─ Concurrent users
└─ Data volume

RELIABILITY
├─ Availability (99.9%)
├─ Fault tolerance
├─ Disaster recovery
└─ Data durability

SCALABILITY
├─ Vertical (scale-up)
├─ Horizontal (scale-out)
├─ Elasticity
└─ Geographic distribution

SECURITY
├─ Authentication
├─ Authorization
├─ Encryption
└─ Compliance

MAINTAINABILITY
├─ Modularity
├─ Observability
├─ Deployability
└─ Testability
```

### Step 2: Architecture Patterns

#### Architectural Styles

```
MONOLITHIC
├─ Pros: Simple, consistent, easy deployment
├─ Cons: Scaling limits, tech lock-in
└─ Use: Small teams, simple domains

MICROSERVICES
├─ Pros: Independent scaling, tech diversity
├─ Cons: Complexity, network overhead
└─ Use: Large teams, complex domains

SERVERLESS
├─ Pros: No ops, auto-scale, pay-per-use
├─ Cons: Vendor lock-in, cold starts
└─ Use: Event-driven, variable load

EVENT-DRIVEN
├─ Pros: Loose coupling, scalability
├─ Cons: Eventual consistency, debugging
└─ Use: Real-time, async processing
```

#### Design Patterns

**Structural Patterns**

```
API GATEWAY
└─ Single entry point
└─ Route/authenticate/limit

SERVICE MESH
└─ Service communication
└─ Traffic management

BACKEND FOR FRONTEND (BFF)
└─ Client-specific APIs
└─ Optimized payloads
```

**Behavioral Patterns**

```
CIRCUIT BREAKER
└─ Prevent cascade failures
└─ Graceful degradation

RETRY + BACKOFF
└─ Handle transient failures
└─ Exponential delays

SAGA PATTERN
└─ Distributed transactions
└─ Compensation logic
```

**Data Patterns**

```
CQRS (Command Query Separation)
└─ Read/write split
└─ Optimized for use case

EVENT SOURCING
└─ Audit trail
└─ Time travel

DATABASE PER SERVICE
└─ Service autonomy
└─ Independent scaling
```

### Step 3: Component Design

#### Service Boundaries

```
DOMAIN-DRIVEN DESIGN
├─ Bounded Contexts
│   ├─ User Context
│   ├─ Order Context
│   └─ Inventory Context
├─ Aggregates
│   ├─ Consistency boundary
│   └─ Transaction scope
└─ Domain Events
    ├─ Integration points
    └─ Async communication
```

#### API Design

```
REST API
├─ Resources (/users, /orders)
├─ HTTP Verbs (GET, POST, PUT, DELETE)
├─ Status Codes (200, 404, 500)
└─ HATEOAS (hypermedia)

GraphQL
├─ Single endpoint
├─ Query language
├─ Type system
└─ Resolvers

gRPC
├─ Binary protocol
├─ Streaming
├─ Code generation
└─ Performance
```

### Step 4: Data Architecture

#### Data Storage Selection

```
RELATIONAL (SQL)
├─ ACID compliance
├─ Complex queries
├─ Transactions
└─ Examples: PostgreSQL, MySQL

NoSQL
├─ Document (MongoDB, DynamoDB)
├─ Key-Value (Redis, Memcached)
├─ Graph (Neo4j, Amazon Neptune)
├─ Time-Series (InfluxDB, TimescaleDB)
└─ Wide-Column (Cassandra, HBase)

DATA WAREHOUSE
├─ Analytics (Snowflake, BigQuery)
├─ OLAP workloads
└─ Historical data

OBJECT STORAGE
├─ Files/media (S3, GCS)
├─ Backups
└─ Static assets
```

#### Data Flow Architecture

```
BATCH PROCESSING
Source → ETL → Data Warehouse → Analytics
         ↓
    Apache Spark
    Apache Beam

STREAM PROCESSING
Source → Stream → Process → Sink
         ↓          ↓         ↓
      Kafka    Flink/Storm  Database

LAMBDA ARCHITECTURE
Batch Layer → Serving Layer → Query
Stream Layer ↗

KAPPA ARCHITECTURE
Stream Processing → Serving Layer → Query
```

### Step 5: Infrastructure Design

#### Cloud Architecture

```
MULTI-TIER ARCHITECTURE
┌─────────────────────────────┐
│      CDN (CloudFront)       │
├─────────────────────────────┤
│    Load Balancer (ALB)      │
├─────────────────────────────┤
│  Web Tier (EC2/Containers)  │
├─────────────────────────────┤
│   App Tier (ECS/Lambda)     │
├─────────────────────────────┤
│   Data Tier (RDS/DynamoDB)  │
├─────────────────────────────┤
│   Cache Tier (Redis)        │
└─────────────────────────────┘
```

#### Container Orchestration

```
KUBERNETES ARCHITECTURE
├─ Pods (application instances)
├─ Services (networking)
├─ Deployments (desired state)
├─ Ingress (external access)
├─ ConfigMaps (configuration)
├─ Secrets (sensitive data)
└─ Persistent Volumes (storage)
```

#### Serverless Architecture

```
API Gateway → Lambda → DynamoDB
     ↓          ↓          ↓
   Auth      SQS/SNS    S3
     ↓          ↓          ↓
  Cognito   StepFunc   CloudWatch
```

### Step 6: Security Architecture

#### Security Layers

```
NETWORK SECURITY
├─ VPC/Subnets
├─ Security Groups
├─ NACLs
├─ WAF
└─ DDoS Protection

APPLICATION SECURITY
├─ Authentication (OAuth, SAML)
├─ Authorization (RBAC, ABAC)
├─ Input Validation
├─ Output Encoding
└─ Session Management

DATA SECURITY
├─ Encryption at Rest
├─ Encryption in Transit
├─ Key Management
├─ Data Masking
└─ Backup/Recovery
```

#### Zero Trust Architecture

```
PRINCIPLES
├─ Never trust, always verify
├─ Least privilege access
├─ Assume breach
├─ Verify explicitly
└─ Inspect and log

IMPLEMENTATION
├─ Identity verification
├─ Device trust
├─ Network segmentation
├─ Encrypted communications
└─ Continuous monitoring
```

## Architecture Artifacts

I'll help you create:

1. **Architecture Diagrams** (C4, UML)
2. **Technical Specifications**
3. **API Documentation**
4. **Data Models**
5. **Deployment Diagrams**
6. **Security Architecture**
7. **Migration Plans**
8. **Architecture Decision Records (ADRs)**

## Architecture Quality Attributes

### Scalability Strategies

```
VERTICAL SCALING
└─ Bigger machines
└─ Limitations: Cost, physical limits

HORIZONTAL SCALING
└─ More machines
└─ Patterns: Sharding, partitioning

CACHING STRATEGIES
├─ Browser cache
├─ CDN cache
├─ Application cache
├─ Database cache
└─ Distributed cache
```

### Reliability Patterns

```
REDUNDANCY
├─ Active-Active
├─ Active-Passive
├─ N+1 redundancy
└─ Geographic redundancy

FAILURE HANDLING
├─ Graceful degradation
├─ Circuit breakers
├─ Bulkheads
├─ Timeouts
└─ Health checks
```

### Performance Optimization

```
FRONTEND
├─ Lazy loading
├─ Code splitting
├─ Asset optimization
├─ CDN usage
└─ Service workers

BACKEND
├─ Database indexing
├─ Query optimization
├─ Connection pooling
├─ Async processing
└─ Caching

NETWORK
├─ HTTP/2, HTTP/3
├─ Compression
├─ Keep-alive
├─ DNS optimization
└─ Edge computing
```

## Example Architecture

**System**: Real-time Analytics Platform

```markdown
### Requirements

- 1M events/second ingestion
- <100ms query response
- 99.99% availability
- Multi-tenant isolation

### Architecture Decisions

1. **Streaming**: Kafka for ingestion
2. **Processing**: Flink for real-time
3. **Storage**: ClickHouse for analytics
4. **Cache**: Redis for hot data
5. **API**: GraphQL for flexibility

### Component Architecture
```

Producers → Kafka → Flink → ClickHouse
↓ ↓ ↓ ↓
Schema Monitor Cache Query
Registry (Prom) (Redis) API

```

### Deployment
- Kubernetes on AWS EKS
- Auto-scaling based on lag
- Multi-AZ for availability
- Backup to S3
```

## Architecture Trade-offs

### CAP Theorem

```
CONSISTENCY - AVAILABILITY - PARTITION TOLERANCE
     Pick Two (in practice, P is required)

CP Systems: MongoDB, HBase, Redis
AP Systems: Cassandra, DynamoDB, CouchDB
```

### Cost vs Performance

```
OPTIMIZATION STRATEGIES
├─ Right-sizing resources
├─ Spot/Reserved instances
├─ Serverless for variable load
├─ Caching to reduce compute
└─ Data lifecycle management
```

## Questions I'll Ask You

To design your architecture:

- What are your functional requirements?
- What are your NFRs (scale, performance)?
- What constraints exist (budget, team, time)?
- What's your current architecture (if any)?
- What are your growth projections?
- What compliance requirements?
- What's your team's expertise?

## Output Templates

### Architecture Document

```markdown
## System Architecture: [Name]

### Overview

[High-level description]

### Requirements

- Functional: [List]
- Non-Functional: [List]

### Architecture Decisions

| Decision | Choice | Rationale |
| -------- | ------ | --------- |

### Component Design

[Diagram and descriptions]

### Data Architecture

[Schema and flow]

### Deployment Architecture

[Infrastructure and topology]

### Security Architecture

[Security measures]

### Monitoring & Operations

[Observability strategy]
```

### ADR Template

```markdown
## ADR-001: [Decision Title]

### Status

[Proposed/Accepted/Deprecated]

### Context

[What's the issue?]

### Decision

[What we're doing]

### Consequences

- Positive: [Benefits]
- Negative: [Trade-offs]
- Risks: [What could go wrong]
```

## Integration Points

- **Informed by**: `product-requirements`, `tech-stack-advisor`
- **Constrains**: `development`, `deployment`
- **Influences**: `cost-optimization`, `security-design`

## Common Architecture Mistakes

⚠️ **Over-Engineering**: Too complex for needs
⚠️ **Under-Engineering**: Won't scale
⚠️ **Ivory Tower**: Not practical
⚠️ **Tech Fashion**: Choosing trendy over fit
⚠️ **Ignoring Debt**: Accumulating problems

Let's design your system architecture. What are you building and what are your key requirements?
