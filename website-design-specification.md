# Sovereign CLI — AI Assistant Marketing Website

## Design Specification Document

### Version 1.0 | Architectural Blueprint for Implementation

---

## Table of Contents

1. [Website Overview & URL Structure](#1-website-overview--url-structure)
2. [Global Visual Language](#2-global-visual-language)
3. [Page 1: Landing Page](#3-page-1-landing-page)
4. [Page 2: CLI Specification](#4-page-2-cli-specification)
5. [Page 3: Vision & Roadmap](#5-page-3-vision--roadmap)
6. [Page 4: Research Team](#6-page-4-research-team)
7. [Page 5: Upcoming Projects & LLM Scaling](#7-page-5-upcoming-projects--llm-scaling)
8. [Global Content & Style Guidelines](#8-global-content--style-guidelines)

---

## 1. Website Overview & URL Structure

### Site Map

| Page | URL Route | Purpose |
|------|-----------|---------|
| Landing | `/` | Coming Soon + Waitlist capture |
| CLI Spec | `/cli-spec` | Technical reference for developers |
| Vision | `/vision` | Long-term product story + principles |
| Team | `/team` | Research team + expertise |
| Roadmap | `/roadmap` | Product phases + LLM scaling details |

### Navigation Architecture

Primary navigation (persistent across all pages):

- **Product** — Links to CLI Spec
- **Vision** — Links to Vision page  
- **Research** — Links to Team page
- **Roadmap** — Links to Roadmap page
- **CTA** — "Join Waitlist" button (gold, prominent)

Footer navigation (persistent across all pages):

- Product column: CLI Spec, Features, Integrations
- Vision column: Roadmap, Principles, Research
- Company column: Team
- Legal column: Privacy, Terms, Security

---

## 2. Global Visual Language

### Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#0A0A0B` | Main page backgrounds |
| `--bg-secondary` | `#111113` | Card backgrounds, section alternation |
| `--bg-tertiary` | `#18181B` | Terminal windows, code blocks |
| `--accent-gold` | `#F5A623` | Primary accent, buttons, highlights |
| `--accent-amber` | `#D4883B` | Secondary accent, gradients |
| `--accent-neon` | `#B8FF57` | Success states, code output, hover accents |
| `--text-primary` | `#FAFAFA` | Headlines, body text |
| `--text-secondary` | `#A1A1AA` | Subtitles, descriptions |
| `--text-muted` | `#52525B` | Captions, timestamps, meta |

### Typography

- **Headlines**: Inter, 700 weight, -0.02em letter-spacing
- **Body**: Inter, 400/500 weight
- **Code/Terminal**: JetBrains Mono, 400 weight
- **Scale**: Clamp-based fluid typography (mobile to desktop)

### Visual Effects

- **Background**: Subtle particle field (gold-tinted dots, slow drift)
- **Glows**: Radial gold gradients behind hero elements
- **Cards**: Dark cards with 1px gold border, neon glow on hover
- **Terminals**: macOS-style window chrome with colored dots
- **Animations**: 
  - Fade-in on scroll (300ms ease-out)
  - Cursor blink in terminal outputs
  - Subtle pulse on CTA bands
  - Particles floating upward continuously

### Component Patterns

1. **Cards**: Dark bg-secondary, gold border (20% opacity), hover → neon glow
2. **Buttons**: 
   - Primary: Gold bg, dark text, neon hover + glow
   - Outline: Transparent, gold border, gold text
3. **Terminal Windows**: bg-tertiary, gold prompt, neon output, blinking cursor
4. **Badges**: Small gold border + text, used for phases/versions

---

## 3. Page 1: Landing Page

**URL**: `/`  
**Goal**: Capture waitlist signups by communicating core value proposition clearly

---

### 3.1 Hero Section

#### Headline

> **Your Terminal. Your Models. Your AI.**

#### Subheadline

A CLI assistant powered by open-source LLMs that you control. No vendor lock-in. No API rate limits. Just sovereign, privacy-first coding infrastructure that lives where you work.

#### Primary CTA Button

> **Join the Waitlist — Get 2 Months Free**

#### Secondary Note (below CTA)

> Waitlist users receive 2 months of free access at launch. Non-waitlist users start directly on paid plans.

#### Hero Visual — Centerpiece

**Concept**: Glowing "AI Core" orb with terminal mockup overlaid

**Implementation**:
- Position: Center of hero, slightly offset to create depth
- Orb: 400px radial gradient (gold glow, pulsing animation)
- Terminal mock: Positioned in front of orb, max-width 560px
- Terminal chrome: 3 colored dots (red/yellow/green), dark bg-tertiary
- Terminal content:
  - Prompt line: `~/dev/my-project $ ai "refactor this API endpoint for pagination"`
  - Output line (typewriter effect): `I'll analyze the endpoint structure and create a paginated version...`

**Animations**:
- Orb: Slow pulse (8s cycle, scale 1.0 → 1.05)
- Particles: Drift upward in background (continuous)
- Terminal cursor: Blink (1s step-end, infinite)
- Terminal output: Typewriter character reveal on load

**Color treatment**:
- Headline: Gradient from text-primary to accent-gold
- Subtitle: text-secondary
- CTA: Primary button (accent-gold bg)
- Orb glow: glow-gold (rgba 245, 166, 35, 0.15)

---

### 3.2 "Why Sovereign AI?" Section

#### Section Heading

> **Why Sovereign AI Matters**

#### Content (2-3 paragraphs)

**Paragraph 1** (problem statement):

Relying on a single AI API vendor means your coding workflow is one outage, pricing change, or policy shift away from disruption. Every query sends your code—often your most valuable intellectual property—through third-party infrastructure you cannot inspect or audit.

**Paragraph 2** (solution statement):

Self-hosted open-source models change that equation. You decide which model runs where. You control the data flow. You optimize costs by running on your own GPU infrastructure, and you can swap or upgrade models without rewriting a single line of your workflow.

**Paragraph 3** (principle statement):

This isn't about rejecting AI. It's about owning the stack that powers your productivity.

#### Value Props — Bullet List

| Icon | Title | Description |
|------|-------|-------------|
| ✓ | **No Lock-In** | Route between OpenAI, Gemini, Qwen, GLM, DeepSeek, or your own fine-tuned models with a single config change. |
| ✓ | **Data Privacy** | Sensitive code, config, and architecture never leave infrastructure you control. |
| ✓ | **Cost Control** | Start with hosted APIs. Migrate to self-hosted as your team scales. Predictable infrastructure costs replace per-token metered billing. |
| ✓ | **Full Observability** | Log every prompt, every response, every routing decision. Know exactly what your AI is doing. |
| ✓ | **Enterprise Ready** | SSO, audit logs, on-prem deployment options. This is built for teams shipping real software. |

#### Visual Layout

- **Desktop**: 2-column grid (text left, bullets right)
- **Mobile**: Single column, stacked
- **Icons**: ✓ symbol in accent-neon
- **Section bg**: bg-primary (no alternation)

---

### 3.3 "What the CLI Can Do" Section

#### Section Heading

> **What the CLI Can Do**

#### Intro Paragraph

The assistant reads your entire workspace—repo structure, git history, dependencies, config files—before answering. It understands the context of your project, not just the prompt you type.

#### Capabilities Grid (2x2 on desktop)

| Capability | Description | Example Command |
|------------|-------------|-----------------|
| **Generate** | Describe what you need in plain English. The CLI outputs idiomatic code that matches your project's style, imports, and conventions. | `ai "add a REST endpoint for user profile"` |
| **Debug** | Paste an error or describe a failure. The CLI analyzes stack traces, relevant source files, and proposes fixes with explanation. | `ai "why is this Promise.all failing?"` |
| **Document** | Ask for API docs, README updates, or code comments. The CLI reads your existing docs style and maintains consistency. | `ai "write docs for this module"` |
| **Architect** | Describe a system requirement. The CLI proposes component diagrams, data flow, and implementation suggestions. | `ai "design a caching layer for this service"` |

#### Workspace Context Explanation

> **How workspace context works:** When you invoke the CLI, it automatically indexes your current directory—reading `package.json`, `Cargo.toml`, `pyproject.toml`, `.git/`, `docker-compose.yml`, and other config files. This context is injected into the prompt so the model understands your stack, naming conventions, and existing patterns. You can customize which files or directories are included or excluded via a local config file.

#### Visual Layout

- **Section bg**: bg-secondary (alternates from previous)
- **Cards**: 2-column grid, each card has title (gold), description, code snippet (neon text on dark bg)
- **Hover state**: Neon glow border
- **Context explanation**: Centered text block, max-width 600px

---

### 3.4 Waitlist & Social Proof Strip

#### Section Content

**Headline**:

> **Join the early access cohort.**

**Copy**:

We're opening the waitlist to a limited number of teams. Early adopters shape the product through direct feedback and get 2 months of free access when we launch. This isn't a marketing list—it's a founding community.

**Social proof line**:

> Built by developers who've shipped infrastructure at scale. Designed for teams who care about what runs under the hood.

#### Email Capture

- Input field: "your@email.com" placeholder
- Button: "Join Waitlist"
- Layout: Horizontal form, max-width 400px, centered

#### Visual Treatment

- **Background**: Gradient floor (transparent → gold 10% opacity, top to bottom)
- **Border**: 1px gold top and bottom (20% opacity)
- **Headline**: accent-gold
- **Social proof**: text-muted, small font (13px)

---

### 3.5 Integrations / Future-Ready Section

#### Section Heading

> **Your Stack. Your Models.**

#### Intro Paragraph

The CLI launches with support for OpenAI and Gemini APIs—so you can start immediately. As our self-hosted models come online, you'll be able to point the same CLI at Qwen, GLM, DeepSeek, or any open-source model running on your own GPU VMs. Same interface. Evolving backend. Full sovereignty.

#### Visual Diagram

**Concept**: Orbital/routing layout

**Elements**:
- Left side (2 nodes): OpenAI, Gemini (gold border cards)
- Center: Router/Engine node (gold border, glowing, "⚙" icon)
- Right side (2 nodes): Qwen, DeepSeek (gold border cards)
- Connections: Arrows from outer nodes through center router

**Node style**:
- Each node: Square card with model abbreviation in large gold text, model name below
- Center node: Slightly larger, neon glow effect
- Hover: Individual node glows on hover

#### Visual Layout

- **Desktop**: Horizontal row of 5 elements (2 - 1 - 2)
- **Mobile**: Wrap to 2 rows (2 on top, 3 on bottom)
- **Section bg**: bg-primary

---

### 3.6 Footer

#### Brand Column

- Logo: `$` symbol in gold square + "AI CLI" text
- Tagline: "Sovereign AI infrastructure for developers who ship."

#### Link Columns

| Product | Vision | Company | Legal |
|---------|--------|---------|-------|
| CLI Spec | Roadmap | Team | Privacy |
| Features | Principles | | Terms |
| Integrations | Research | | Security |

#### Bottom Row

- **Left**: "A developer-first tool. Privacy by design. No telemetry, no data leaves your infrastructure."
- **Right**: "Join Waitlist" outline button

---

## 4. Page 2: CLI Specification

**URL**: `/cli-spec`  
**Goal**: Provide developers with precise technical reference — not marketing fluff

---

### 4.1 Hero Block

#### Headline

> **CLI Specification**

#### Description

A precise reference for what the CLI does, how it routes requests, and how to configure it for your workflow. This is a living spec—it evolves with each release.

#### Version Badge

> v0.1 — Coming Soon

---

### 4.2 Core Capabilities Section

#### Section Heading

> **Core Capabilities**

#### Capabilities Grid (3x2 on desktop)

| Capability | Description | Example Command | Best Model |
|------------|-------------|-----------------|------------|
| **Generate** | Produces idiomatic code from natural language descriptions. Handles file creation, function stubs, full modules, and test scaffolding. | `ai "create a React hook for debounced search"` | Small-medium model (fast, precise) |
| **Debug** | Analyzes error messages, stack traces, and source context to propose fixes. Explains the root cause in developer-friendly terms. | `ai "debug: TypeError Cannot read property 'id' of undefined"` | Medium-large model (reasoning depth) |
| **Document** | Generates or updates documentation—README, API docs, JSDoc, docstrings—matching your project's existing style. | `ai "write a README for this service"` | Medium model (style awareness) |
| **Architect** | Proposes system designs, component structures, data flows, and implementation plans for complex features. | `ai "design a message queue architecture for this microservices app"` | Large model (deep reasoning) |
| **Review** | Performs code review on diffs or files. Flags issues, suggests improvements, checks for security anti-patterns. | `ai "review: ./src/auth/login.ts"` | Medium-large model |
| **Explain** | Breaks down complex code, error messages, or architectural decisions into plain English. | `ai "explain this regex pattern"` | Small model (fast Q&A) |

#### Workspace Context Subsection

> **Workspace Context**  
> The CLI automatically indexes your project on invocation. It reads your dependency files (`package.json`, `Cargo.toml`, `requirements.txt`), git metadata, config files (`.eslintrc`, `tsconfig.json`, `docker-compose.yml`), and file tree structure. This context is summarized and prepended to every prompt. You control what gets included via the config file.

---

### 4.3 Model Routing Section

#### Section Heading

> **Model Routing**

#### Intro Paragraph

The CLI doesn't use a single model for everything. It routes each request based on three criteria: task type (generation vs. reasoning vs. Q&A), latency tolerance (fast answers vs. deep analysis), and sensitivity (public code vs. proprietary logic). You can override these defaults in your config.

#### Routing Flow Diagram (Textual Description)

```
User Prompt → Router → Decision Engine → Model Selection
```

**Visual representation**:
- Horizontal flow: 4 boxes connected by arrows
- Each box: Dark card with gold border
- "Router" and "Decision Engine" highlighted as gold

#### Routing Examples Table

| Scenario | Routing Logic | Model Used |
|----------|---------------|------------|
| Quick question about a function | Task = Q&A, Low latency → Fast model | ai-small (hosted) |
| Refactor a 500-line module | Task = Generation, Medium latency → Medium model | ai-medium (hosted or self-hosted) |
| Security-critical auth code review | Sensitivity = High → Self-hosted model only | ai-secure (self-hosted) |

---

### 4.4 Runtime & Integrations Section

#### Section Heading

> **Runtime & Integrations**

#### Runtime Support (3 cards, horizontal)

| Platform | Status | Notes |
|----------|--------|-------|
| macOS | Supported | Universal binary, Apple Silicon optimized |
| Linux | Supported | Debian, RPM, AUR packages |
| WSL | Supported | Full parity with Linux build |

#### Editor Integrations (4 cards, horizontal)

| Integration | Description |
|-------------|-------------|
| **Neovim** | Native plugin that pipes buffer content to the CLI and inserts responses. |
| **VS Code** | Extension that adds a sidebar panel for CLI interaction. |
| **GitHub Actions** | Action for automated code review on PRs. |
| **GitLab CI** | CI template for running documentation generation on merge. |

---

### 4.5 Configuration Section

#### Section Heading

> **Configuration**

#### Intro Paragraph

A local `ai.toml` file in your project root controls everything—model preferences, context paths, routing rules, and style guidelines. It lives in your repo so your team shares the same config.

#### Config Example (Code Block)

```toml
# ~/.ai/config.toml (global)

[defaults]
model = "balanced"          # fast | balanced | deep
self_hosted_only = false    # true forces self-hosted routes

[context]
include = ["src/", "tests/"]
exclude = ["node_modules/", "dist/", ".git/"]
max_files = 50

[models]
hosted = ["openai", "gemini"]
self_hosted = ["qwen-coder", "glm-4", "deepseek"]

[security]
audit_log = true
prompt_log = "local-only"
```

> **Note**: Example config — your actual config will vary.

---

### 4.6 CTA Band

**Headline**: "Ready to try the CLI?"  
**Subline**: "Join the waitlist to get early access and 2 months free at launch."  
**Button**: "Join the Waitlist"

---

## 5. Page 3: Vision & Roadmap

**URL**: `/vision`  
**Goal**: Tell the long-term product story, establish credibility

---

### 5.1 Vision Hero

#### Headline

> **From Terminal to Sovereign AI Infrastructure**

#### Subheadline

We start with a CLI. We end with a fully self-hosted AI coding stack—purpose-built for developers who demand control over every layer of their tooling.

---

### 5.2 Product Roadmap Narrative

#### Section Heading

> **Product Roadmap**

#### Subheadline

This isn't a single product. It's a platform that evolves with your needs.

#### Timeline (5 phases, vertical)

| Phase | Name | Description | Developer Experience |
|-------|------|-------------|---------------------|
| **Phase 1** | CLI Assistant | Terminal-based AI that reads your workspace and assists with code, debug, docs, and architecture. Context-aware prompts, model routing, local config. | "I type a question, I get an answer that knows my project." |
| **Phase 2** | AI-Powered IDE | A code editor where AI is a first-class citizen—not a plugin, but the editing surface itself. Inline refactoring, semantic code search, intelligent autocomplete. | "The editor reads my intent and writes the code for me." |
| **Phase 3** | Multi-Agent AI | Multiple specialized AI agents coordinate on complex tasks—one for backend, one for frontend, one for DevOps. Agent orchestration, task decomposition, shared context. | "I describe a feature, and agents split the work and execute in parallel." |
| **Phase 4** | Terminal Agent | A command-line agent that acts as your "second brain" in the shell—handles deployments, debugging, infra queries. Shell command generation, log analysis, kubectl/terraform understanding. | "I ask the terminal a question about my infra, it answers and acts." |
| **Phase 5** | Data Breach Security Tool | An AI that monitors your codebase for leaked secrets, vulnerable patterns, and compliance gaps. Secret scanning, vulnerability detection, audit reporting. | "My AI catches a leaked API key before it leaves my machine." |

---

### 5.3 Coding Specialist LLM Section

#### Section Heading

> **The Coding Specialist LLM**

#### Subheadline

We're training a model purpose-built for coding—not a general LLM that happens to write code, but a specialist that understands software engineering at its core.

#### Scaling Stages (4 columns, horizontal)

| Stage | Parameters | Name | Purpose | Trade-off |
|-------|------------|------|---------|-----------|
| Stage 1 | **30B** | Fast Iteration | Single-GPU deployment, quick code generation, low latency. | Limited context window (~32K). Best for focused, single-file tasks. |
| Stage 2 | **180B** | Enhanced | Deeper reasoning for architecture and security reviews. | Multi-file context, complex refactoring. Higher latency (2-3x vs Stage 1). Requires multi-GPU. |
| Stage 3 | **250B** | Primary | Primary backbone for IDE and multi-agent workflows. | Agent coordination, large codebase reasoning. Significant compute. |
| Stage 4 | **1T** | Frontier-Scale | Multi-agent coordination, enterprise-wide codebases, system-level reasoning. | Highest compute requirements. Reserved for large teams with dedicated GPU infrastructure. |

#### Visual: Staircase/Bar Chart

- 4 vertical bars, increasing height left to right
- Bar 1: 30B (30% height, gold)
- Bar 2: 180B (50% height, gold)
- Bar 3: 250B (70% height, neon)
- Bar 4: 1T (100% height, neon + glow)
- Each bar has parameter count label above, stage name below

---

### 5.4 Philosophy & Principles

#### Section Heading

> **Our Principles**

#### Principles List (vertical, text-only with dot pattern background)

| Principle | Description |
|-----------|-------------|
| **Sovereign by default** | Every component runs on your infrastructure. No data leaves without your explicit permission. |
| **Developer-first** | We build tools we'd use ourselves. We ship what we need, not what sounds good in a pitch deck. |
| **Open-source aligned** | We contribute back. We use open models. We believe in collective progress. |
| **Observable and controllable** | You see every decision, every prompt, every route. You are never in the dark. |

#### Visual Treatment

- Background: Dot pattern (gold dots at 5% opacity, 24px spacing)
- Layout: Centered, max-width 700px
- Each principle: Title in gold, description in text-secondary

---

### 5.5 CTA Band

**Headline**: "Join the Journey"  
**Subline**: "Be part of building the future of sovereign AI infrastructure."  
**Button**: "Join the Waitlist"

---

## 6. Page 4: Research Team

**URL**: `/team`  
**Goal**: Build trust with enterprise buyers and serious developers

---

### 6.1 Hero Introduction

#### Headline

> **The Team Behind the Stack**

#### Subheadline

Researchers and engineers who've spent years building AI tools, training large models, and operating GPU infrastructure at scale. We're building the tool we wanted to use.

---

### 6.2 Team Member Cards

#### Section Heading

> **Meet the Team**

#### Team Grid (3x2 on desktop, 2x3 on tablet)

| Avatar | Name | Role | Bio |
|--------|------|------|-----|
| AC | **Alex Chen** | Founder & Architect | Former staff engineer at a major AI company. Led the design of developer tools used by thousands of engineers. Obsessed with UX and infrastructure. |
| SP | **Samira Patel** | Research Engineer | PhD in ML. Previously trained open-source coding models. Focuses on model routing, fine-tuning, and evaluation pipelines. |
| JK | **Jordan Kelley** | Infrastructure Engineer | Built GPU clusters for a top-tier AI lab. Expert in distributed training, inference optimization, and cloud-native deployments. |
| RG | **Ravi Gupta** | Applied Scientist | Works on multi-agent orchestration. Previously built autonomous coding agents at a devtools startup. |
| EV | **Elena Voss** | Security & Privacy Lead | Former security researcher at a cloud provider. Specializes in threat modeling for AI systems and data privacy engineering. |

#### Card Visual

- **Avatar**: 80px circle, gold-to-amber gradient, initials centered
- **Name**: 18px, text-primary
- **Role badge**: Small pill with gold border, gold text, uppercase
- **Bio**: 14px, text-secondary
- **Hover**: Neon glow border

---

### 6.3 Research Focus Areas

#### Section Heading

> **Research Focus**

#### Focus Grid (3x2 on desktop)

| Focus Area | Description |
|------------|-------------|
| **Routing Across Open-Source Models** | Building the intelligent router that picks the right model (Qwen, GLM, DeepSeek, etc.) based on task, latency, and privacy requirements. |
| **Multi-Agent Orchestration** | Designing systems where multiple AI agents collaborate on a single codebase—splitting work, sharing context, and resolving conflicts. |
| **Efficient Fine-Tuning** | Distilling large models into compact, task-specific variants that run on single-GPU or consumer hardware without sacrificing quality. |
| **Guardrails & Evaluation** | Creating robust evaluation frameworks for code correctness, security, and maintainability. Building guardrails that prevent harmful outputs. |
| **Context Compression** | Novel techniques for injecting repo-scale context into limited-size model prompts without losing fidelity. |
| **Self-Hosted Inference** | Optimizing inference stacks for open-source models on bare-metal GPUs, with minimal latency and maximum throughput. |

---

### 6.4 Open Work & Transparency

#### Section Heading

> **Open Work**

#### Subheadline

We believe trust is earned through transparency. As we build, we'll publish:

#### Publication Categories (3 columns)

| Papers | Benchmarks | Blog |
|--------|------------|------|
| Coming Q2 2026 | Coming Q2 2026 | Coming Q2 2026 |
| Coming Q3 2026 | Coming Q3 2026 | Coming Q3 2026 |
| Coming Q4 2026 | Coming Q4 2026 | Coming Q4 2026 |

#### Closing Statement

> We'll also release open-source tools, configs, and evaluation pipelines over time. Transparency isn't a marketing tactic—it's how we build trust.

---

### 6.5 CTA Band

**Headline**: "Join the Team"  
**Subline**: "We're hiring. Help us build the future of sovereign AI infrastructure."  
**Button**: "Join the Waitlist"

---

## 7. Page 5: Upcoming Projects & LLM Scaling

**URL**: `/roadmap`  
**Goal**: Detailed phase + scaling information for serious planners

---

### 7.1 Roadmap Hero

#### Headline

> **Upcoming Projects & LLM Scaling**

#### Subheadline

Phased rollout from CLI to full sovereign AI stack. Parameter scaling from 30B to 1T. Every stage unlocks new capabilities for your team.

---

### 7.2 Product Phases Section

#### Section Heading

> **Product Phases**

#### Timeline (vertical, same as Vision page but with "Unlocks" highlighted)

| Phase | Name | Description | Unlocks |
|-------|------|-------------|---------|
| Phase 1 | CLI Assistant | Terminal-based AI with workspace context, model routing, and local config. | Immediate productivity — code gen, debug, docs, architecture. |
| Phase 2 | AI-Powered IDE | A new code editor built with AI as the core primitive—not an extension, the editor itself. | Inline refactoring, semantic search, intelligent autocomplete. |
| Phase 3 | Multi-Agent AI | Coordinated agents for backend, frontend, DevOps—each specialized, sharing context. | Complex features shipped faster — agents parallelize work. |
| Phase 4 | Terminal Agent | An AI that lives in your shell—handles deployments, debugging, log analysis, infra queries. | "Ask my terminal" workflow — natural language interaction with your dev environment. |
| Phase 5 | Data Breach Security Tool | Continuous scanning for leaked secrets, vulnerable patterns, and compliance gaps in your codebase. | Proactive security — catch leaks before they're committed. |

#### Phase 1 Callout

> **Note**: Phase 1 (CLI) is what we're promoting as "Coming Soon"

---

### 7.3 LLM Scaling Roadmap Section

#### Section Heading

> **LLM Scaling Roadmap**

#### Subheadline

Four clear stages of parameter scaling, each unlocking new capabilities.

#### Scaling Stages (4 columns, horizontal)

| Stage | Parameters | Name | Purpose | Trade-off |
|-------|------------|------|---------|-----------|
| Stage 1 | **30B** | Initial | Initial coding model, good for single-GPU deployments. | Limited context (~32K). Best for single-file tasks. |
| Stage 2 | **180B** | Enhanced | Deeper reasoning for architecture and security reviews. | Multi-file context, complex refactoring. Higher latency (2-3x vs Stage 1). Requires multi-GPU. |
| Stage 3 | **250B** | Primary | Primary backbone for IDE and multi-agent workflows. | Agent coordination, large codebase reasoning. Significant compute. Best for high-value complex tasks. |
| Stage 4 | **1T** | Frontier | Frontier-scale model for complex, multi-system enterprises. | System-level reasoning, enterprise-wide coordination. Highest compute requirements. Reserved for dedicated infrastructure. |

#### Visual: Staircase/Bar Chart

- 4 bars with increasing height
- Labels: Stage number (badge), parameter count (large), stage name, purpose, trade-off
- Bar colors: Stages 1-2 in gold, Stages 3-4 in neon

---

### 7.4 CTA Band

**Headline**: "Build the Future of Sovereign AI"  
**Subline**: "Join the waitlist to be part of Phase 1. Shape the product. Get 2 months free at launch."  
**Button**: "Join the Waitlist — Get 2 Months Free"

---

## 8. Global Content & Style Guidelines

### Writing Principles

1. **Developer-first**: Use precise technical language. No fluff.
2. **Confident but accurate**: State capabilities clearly. Don't overpromise.
3. **Minimal marketing**: Facts over hype. Let the product speak.
4. **Privacy-conscious**: Always emphasize data sovereignty.

### Voice & Tone

- **Headlines**: Bold, declarative, forward-looking
- **Body**: Clear, concise, technical
- **CTAs**: Direct action, benefit-focused
- **Microcopy**: Helpful, not playful

### Consistency Rules

| Element | Rule |
|---------|------|
| Product name | "AI CLI" or "the CLI" — never "the tool" |
| Waitlist benefit | Always mention "2 months free" |
| Self-hosted messaging | Use "sovereign" as primary adjective |
| Model names | OpenAI, Gemini, Qwen, GLM, DeepSeek (capitalized) |
| CTA buttons | Gold bg, dark text, "Join the Waitlist" |
| Section alternation | bg-primary → bg-secondary → bg-primary |

### Visual Patterns

1. **Cards**: Dark bg, 1px gold border (20% opacity), hover = neon glow
2. **Terminals**: macOS chrome, gold prompt, neon output, blinking cursor
3. **Gradients**: Gold to amber for logos/branding
4. **Glows**: Radial gold behind hero elements
5. **Particles**: Gold-tinted dots, slow upward drift

### Animation Guidelines

| Element | Animation | Duration |
|---------|-----------|----------|
| Page sections | Fade in + slide up | 300ms |
| Cards on hover | Border glow | 200ms |
| CTA buttons | Glow pulse + lift | 150ms |
| Terminal cursor | Blink | 1s loop |
| Hero orb | Pulse scale | 8s loop |
| Particles | Float up | 20s linear infinite |

### Responsive Breakpoints

- **Desktop**: 1200px+ (4-column grids)
- **Tablet**: 768px-1199px (2-column grids)
- **Mobile**: <768px (1-column, stacked)

---

## Document Metadata

| Field | Value |
|-------|-------|
| Version | 1.0 |
| Created | 2026-03-16 |
| Purpose | Design specification for CLI AI Assistant marketing website |
| Audience | Frontend developers, UX designers, implementation team |
| Format | Markdown (ready for handoff to code generation system) |

---

*End of Design Specification*
