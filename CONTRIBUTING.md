# Contributing to Hatch Lab

Thank you for your interest in contributing to Hatch Lab! This document provides guidelines and instructions
for contributing to the project.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Types of Contributions](#types-of-contributions)
- [Skill Development Guidelines](#skill-development-guidelines)
- [Testing Requirements](#testing-requirements)
- [Submission Process](#submission-process)
- [Style Guide](#style-guide)
- [Review Process](#review-process)

## Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inclusive environment for all contributors, regardless of:

- Experience level
- Background or identity
- Personal characteristics
- Technical preferences

### Expected Behavior

- Be respectful and professional
- Focus on constructive feedback
- Prioritize user value and quality
- Respect intellectual property
- Maintain ethical AI practices
- Ensure accessibility in all contributions

### Unacceptable Behavior

- Harassment or discrimination
- Destructive criticism without constructive alternatives
- Publishing others' private information
- Other conduct inappropriate for a professional setting

## Getting Started

### Prerequisites

1. **Familiarity with Claude Skills**: Read the [Anthropic Agent Skills documentation](https://docs.anthropic.com/claude/docs)
2. **Understanding of Product Strategy**: Review existing skills to understand the framework
3. **Markdown Proficiency**: All skills are written in Markdown
4. **Git/GitHub Knowledge**: Basic understanding of pull requests and version control

### Setting Up Your Environment

```bash
# Clone the repository
git clone https://github.com/yourusername/hatch-lab.git
cd hatch-lab

# Create a new branch for your contribution
git checkout -b feature/your-skill-name

# Install markdown linter (optional but recommended)
npm install -g markdownlint-cli
```

## Types of Contributions

We welcome several types of contributions:

### 1. New Skills

Create entirely new skills that complement the existing framework.

**Examples:**

- Industry-specific variations (healthcare, fintech, retail)
- Regional adaptations (market-specific considerations)
- Advanced specialized skills (AI ethics auditor, sustainability analyzer)

### 2. Skill Improvements

Enhance existing skills with:

- Better examples
- Additional frameworks
- Improved templates
- Clearer instructions
- Bug fixes

### 3. Documentation

Improve project documentation:

- Clarify usage instructions
- Add tutorials and guides
- Create video walkthroughs
- Translate documentation

### 4. Templates and Resources

Contribute supporting materials:

- Output templates
- Case studies
- Example projects
- Integration guides

### 5. Bug Reports and Feature Requests

Help improve the project by:

- Reporting issues with existing skills
- Suggesting new features
- Identifying documentation gaps
- Proposing improvements

## Skill Development Guidelines

### Skill Structure Requirements

Every skill MUST follow this structure:

```markdown
---
name: your-skill-name
description: Clear 50-200 character description
metadata: # Optional
  version: 1.0
  author: Your Name
  category: discovery|strategy|architecture|business|measurement
  tags: [tag1, tag2]
---

# Skill Name

## Overview

[2-3 paragraphs explaining the skill]

## Core Capabilities

[5-8 bullet points of key capabilities]

## Core Framework

[Step-by-step methodology with 3-7 major steps]

## Key Artifacts

[List of deliverables the skill produces]

## Advanced Techniques (Optional)

[Deeper methods for experienced users]

## Example Output

[Real-world example of skill output]

## Quality Checklist

[Validation criteria for outputs]

## Common Mistakes to Avoid

[Typical pitfalls and how to avoid them]

## Key Questions to Ask

[Discovery questions to guide the process]

## Output Templates

[2-3 practical templates users can fill in]

## Integration Points

[How this skill connects to others]
```

### Naming Conventions

- **Skill Names**: Lowercase, hyphen-separated (e.g., `market-validation`)
- **File Names**: `SKILL.md` in capital letters
- **Folder Names**: Match skill name exactly (e.g., `market-validation/`)
- **Avoid**: Spaces, underscores, special characters, CamelCase

### Description Guidelines

**Good Descriptions (50-200 characters):**

```yaml
description: Validates market demand and competitive positioning using TAM/SAM/SOM frameworks, competitive intelligence, and customer segmentation methodologies
```

**Bad Descriptions:**

```yaml
# Too short
description: Analyzes markets

# Too vague
description: Helps with understanding your market and what customers want

# Too long (> 200 characters)
description: This skill provides comprehensive market validation capabilities including total addressable market analysis, serviceable addressable market calculations, detailed competitive landscape assessment, customer segment identification and prioritization, and validation of willingness to pay through multiple research methodologies
```

### Content Quality Standards

1. **Clarity**: Instructions should be clear to someone new to the framework
2. **Completeness**: Include all required sections
3. **Actionability**: Provide concrete steps, not just concepts
4. **Examples**: Include real-world examples relevant to multiple industries
5. **Integration**: Clearly explain how skill connects to others
6. **Accessibility**: Use plain language, avoid jargon where possible

### Skill Categories

Place your skill in one of these categories:

- **Discovery**: Problem exploration, research, understanding needs
- **Strategy**: Planning, positioning, competitive analysis
- **Architecture**: Technical design, system architecture, technology selection
- **Business**: Business models, pricing, revenue strategies
- **Measurement**: Metrics, analytics, performance tracking
- **Orchestration**: Meta-skills that coordinate other skills

## Testing Requirements

Before submitting a skill, test it with:

### 1. Self-Testing Checklist

- [ ] YAML frontmatter is valid
- [ ] Description is 50-200 characters
- [ ] All required sections present
- [ ] At least 2 example outputs included
- [ ] At least 2 output templates provided
- [ ] Integration points documented
- [ ] Markdown is properly formatted
- [ ] No broken links or references
- [ ] No spelling or grammar errors

### 2. Functional Testing

Test your skill with at least 3 different scenarios:

1. **Beginner Use Case**: Someone new to the domain
2. **Intermediate Use Case**: Someone with some experience
3. **Advanced Use Case**: Complex real-world situation

Document your test results:

```markdown
## Test Results

### Test 1: Beginner - Startup Founder

**Scenario**: First-time founder with no market research experience
**Outcome**: Successfully produced TAM/SAM/SOM analysis
**Feedback**: Needed more explanation of terminology
**Changes Made**: Added glossary section

### Test 2: Intermediate - Product Manager

**Scenario**: PM launching new product line
**Outcome**: Completed competitive analysis in 45 minutes
**Feedback**: Templates were very helpful
**Changes Made**: None needed

### Test 3: Advanced - Innovation Consultant

**Scenario**: Multi-market expansion analysis
**Outcome**: Used advanced techniques for complex scenario
**Feedback**: Appreciated depth and flexibility
**Changes Made**: Added emerging markets considerations
```

### 3. Integration Testing

Test how your skill integrates with existing skills:

- [ ] Inputs from predecessor skills work correctly
- [ ] Outputs to successor skills are properly formatted
- [ ] No conflicts with similar skills
- [ ] Orchestration via product-strategy-navigator works

### 4. Markdown Linting

Run markdown linter:

```bash
markdownlint skills/your-skill-name/SKILL.md
```

Fix all errors and warnings.

## Submission Process

### Step 1: Prepare Your Contribution

1. Ensure all tests pass
2. Update relevant documentation
3. Add your skill to SKILLS_CATALOG.md
4. Update README.md if needed
5. Create examples in your skill's `/examples` folder (optional)

### Step 2: Commit Your Changes

```bash
# Add your files
git add skills/your-skill-name/

# Commit with clear message
git commit -m "Add [skill-name]: [brief description]

- Core capabilities: [list main features]
- Integrates with: [list related skills]
- Tested with: [list test scenarios]"

# Push to your branch
git push origin feature/your-skill-name
```

### Step 3: Create Pull Request

1. Go to GitHub repository
2. Click "New Pull Request"
3. Select your branch
4. Fill out the PR template (see below)
5. Request review from maintainers

### Pull Request Template

```markdown
## Description

[Describe what this PR adds or changes]

## Type of Change

- [ ] New skill
- [ ] Skill improvement
- [ ] Documentation
- [ ] Bug fix
- [ ] Template/resource

## Skill Information (if applicable)

- **Skill Name**: your-skill-name
- **Category**: [category]
- **Related Skills**: [list]
- **Duration**: [estimated completion time]

## Testing

- [ ] Self-testing checklist completed
- [ ] Functional testing with 3+ scenarios
- [ ] Integration testing passed
- [ ] Markdown linting passed

## Test Scenarios

1. [Scenario 1 description and outcome]
2. [Scenario 2 description and outcome]
3. [Scenario 3 description and outcome]

## Documentation Updates

- [ ] Added to SKILLS_CATALOG.md
- [ ] Updated README.md (if needed)
- [ ] Created examples (if applicable)
- [ ] Updated IMPLEMENTATION_GUIDE.md (if needed)

## Breaking Changes

- [ ] No breaking changes
- [ ] Breaking changes (describe below)

[If breaking changes, describe impact and migration path]

## Additional Notes

[Any other information reviewers should know]
```

## Style Guide

### Markdown Formatting

- Use ATX-style headings (`#` not `===`)
- Add blank lines around headings
- Add blank lines around code blocks
- Use fenced code blocks with language specifiers
- Use consistent list formatting
- Maximum line length: 120 characters (except code blocks)

### Language and Tone

- **Active Voice**: "Analyze the market" not "The market should be analyzed"
- **Present Tense**: "The skill produces" not "The skill will produce"
- **Direct Instructions**: "Do X" not "You might want to consider doing X"
- **Professional but Approachable**: Avoid both overly formal and overly casual language

### Code Examples

````markdown
# Good: Specific, actionable

```
TAM (Total Addressable Market): $12.5B
- Global enterprise software market for AI-powered analytics
- Based on Gartner 2024 report
```

# Bad: Vague, not actionable

```
TAM: Very large market
- Lots of companies need this
- Market is growing
```
````

### Technical Terms

- Define acronyms on first use
- Provide examples for abstract concepts
- Link to external resources for deep dives
- Include glossary for complex skills

## Review Process

### What Reviewers Look For

1. **Quality**: Does it meet standards?
2. **Value**: Does it add value to users?
3. **Completeness**: Are all sections included?
4. **Integration**: Does it work with existing skills?
5. **Originality**: Is it sufficiently different from existing skills?
6. **Maintainability**: Can it be maintained long-term?

### Review Timeline

- **Initial Review**: Within 5 business days
- **Feedback Cycle**: 3-5 days per round
- **Approval**: 2 maintainer approvals required
- **Merge**: Within 2 days of approval

### Addressing Feedback

- Respond to all review comments
- Make requested changes promptly
- Explain if you disagree with feedback
- Request clarification if needed
- Update PR description as you make changes

### After Merge

- Your contribution will be included in the next release
- You'll be added to CONTRIBUTORS.md
- You can promote your skill in discussions
- Consider creating a blog post or tutorial

## Recognition

Contributors are recognized in:

- CONTRIBUTORS.md file
- Skill metadata (author field)
- Release notes
- Project website (if applicable)

## Questions?

- **General Questions**: Open a GitHub Discussion
- **Bug Reports**: Open a GitHub Issue
- **Private Inquiries**: Email maintainers (see README)
- **Real-Time Help**: Join Discord community (link in README)

## License

By contributing, you agree that your contributions will be licensed under the Apache 2.0 License.

---

Thank you for contributing to Hatch Lab! Your contributions help democratize access to world-class product strategy expertise.
