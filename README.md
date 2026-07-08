## Product OS v1

A Framework for Vibe Coding & AI-Native Development

---

📋 Table of Contents

· Overview
· Philosophy
· Repository Structure
· Documentation Standards
· File Naming Convention
· Document Types
· Versioning Strategy
· Cross-Reference System
· Development Workflow
· Getting Started
· Contributing
· License

---

🎯 Overview

Product OS v1 is a comprehensive framework and knowledge base for building software products using Vibe Coding — a development approach optimized for collaboration with AI assistants like ChatGPT, Claude, and similar tools.

This repository serves as your single source of truth for product development, containing:

· Standardized documentation that works with any AI assistant
· Executable checklists and templates for each development phase
· Prompt library for consistent AI interactions
· Decision logs to prevent recurring discussions
· Playbooks for rapid product launches

What is Vibe Coding?

Vibe Coding is a development methodology where you:

1. Think in layers: Understand → Decide → Execute
2. Work in small, atomic steps: Each file = one concept
3. Use AI as pair programmer: Clear prompts for consistent outputs
4. Build incrementally: Sprint-based development with stable releases
5. Document everything: Every decision has a home

---

🧠 Philosophy

Core Principles

1. Single Source of Truth

Every concept has exactly one definitive file. Other files reference it rather than repeating content.

2. Atomic Files

Each file covers one topic only. If a file grows too large (700-1000 words), split it into multiple files.

3. Action First

Every file must answer: "After reading this, what exactly should I do?" Knowledge without action is incomplete.

4. Build vs Buy

Always evaluate existing solutions before building custom ones:

· ✅ Use existing services
· ✅ Use starter kits
· ✅ Use open source
· ❌ Build from scratch only when necessary

5. AI Native

All processes are designed to be executed by AI assistants. Wherever needed, dedicated Prompt files are provided.

6. Vibe Coding Friendly

· No 5000-line files
· No academic documentation
· Step-by-step progression
· Clear action items

7. Living Document

This repository is a living system, not a static book. Real product development improves Product OS over time.

---

📁 Repository Structure

```
Product-OS/
│
├── Sprint-00/          # Foundation & Standards
│   ├── SPR-README-001-Repository-Overview.md
│   ├── SPR-ARCH-001-Repository-Architecture.md
│   ├── SPR-STD-001-Document-Standards.md
│   ├── SPR-STD-004-Authoring-Protocol.md
│   └── SPR-TOC-001-Repository-TOC.md
│
├── Sprint-01/          # Product Thinking & Canvas
│   ├── PRN-*-*.md      # Product Principles
│   ├── CAN-*-*.md      # Canvas Components
│   └── ...
│
├── Sprint-02/          # Blueprint & Design
│   ├── BP-DISC-*.md    # Discovery
│   ├── BP-DES-*.md     # Design
│   ├── BP-ARCH-*.md    # Architecture
│   └── ...
│
├── Sprint-03/          # Foundation
│   ├── FD-AUTH-*.md    # Authentication
│   ├── FD-BILL-*.md    # Billing
│   ├── FD-DB-*.md      # Database
│   └── ...
│
├── Sprint-04/          # Development Workflow
│   ├── PRM-*-*.md      # Prompts
│   ├── TMP-*-*.md      # Templates
│   └── QA-*-*.md       # Quality Assurance
│
└── Sprint-05/          # Execution & Playbooks
    ├── EX-*-*.md       # Example Projects
    └── PLY-*-*.md      # Playbooks
```

---

📝 Documentation Standards

File Header

Every file starts with a standard header:

```markdown
# Title of File

**File ID:** CAT-TOPIC-001
**Version:** 1.0
**Sprint:** Sprint-03
**Status:** Stable
**Last Update:** YYYY-MM-DD

---
```

File Structure

Most files follow this structure (some sections may be omitted):

Section Purpose
Purpose What this file is about
Why Why this concept matters
When When to use this file
Inputs What you need before starting
Outputs What you'll have after completion
Checklist Step-by-step action items
Best Practices Recommended approaches
Common Mistakes What to avoid
Tools Recommended tools and services
Prompt AI prompt (only in PRM-* files)
Related Files Cross-references to other files

The 3-Layer Structure

Every file follows the Understand → Decide → Execute pattern:

1. Understand - What is this concept?
2. Decide - What decision do I need to make?
3. Execute - What exactly should I do?

---

🏷️ File Naming Convention

Format

```
[Category]-[Topic]-[Number]-[Title].md
```

Categories

Code Category Description
SPR Sprint Sprint-specific files (only Sprint-00)
PRN Principle Core principles and philosophies
CAN Canvas Product Canvas components
BP Blueprint Product design and architecture
FD Foundation Technical foundations
PRM Prompt AI prompts and interactions
TMP Template Reusable templates
QA Quality Testing and quality standards
EX Example Case studies and examples
PLY Playbook Execution guides

Examples

```
FD-AUTH-001-Authentication-Overview.md
BP-ARCH-001-Architecture.md
PRM-BE-001-Backend-Prompt.md
CAN-PRB-001-Problem.md
```

Document ID

Each file has a unique Document ID: CAT-TOPIC-XXX

This ID remains constant even if the file moves between sprints. All references use this ID.

---

📚 Document Types

1. Knowledge (PRN, CAN, BP, FD)

Teaches concepts and provides understanding. Must include Action First section.

2. Decision (SPR-STD-010, BP-GNG-*)

Documents important decisions. Includes context, alternatives considered, and final decision.

3. Checklist (QA-*, -CHK-)

Step-by-step execution guides. Each item should be verifiable.

4. Template (TMP-*)

Reusable templates for PRDs, features, APIs, decisions, tests, releases.

5. Prompt (PRM-*)

AI-specific prompts. Never include prompts inside Knowledge files.

---

🔢 Versioning Strategy

Status Levels

Status Meaning
Draft Initial version, in progress
Stable Complete and reviewed, ready for use
Reviewed Final version, approved and frozen

Version Numbers

· Format: MAJOR.MINOR
· Example: 1.0, 1.1, 2.0
· Increment version when content changes significantly
· Major version changes indicate breaking changes

---

🔗 Cross-Reference System

How to Reference

```markdown
> For details on Authentication, refer to [FD-AUTH-001](Sprint-03/FD-AUTH-001-Authentication-Overview.md).
```

Related Files Section

Every file ends with:

```markdown
## Related Files

- [FD-AUTH-001](Sprint-03/FD-AUTH-001-Authentication-Overview.md)
- [FD-AUTH-002](Sprint-03/FD-AUTH-002-Authentication-Providers.md)
- [PRM-AUTH-001](Sprint-04/PRM-AUTH-001-Auth-Prompt.md)
```

Important Rules

1. No duplicate content - Reference instead of repeating
2. Always link - Include document ID and path
3. Keep relationships - Maintain related files sections

---

🔄 Development Workflow

Sprint Structure

Each Sprint has:

1. Goal - What we achieve this sprint
2. Outputs - Specific files created
3. Result - State after completion

Sprint 00: Foundation

Goal: Design Product OS system and repository standards
Output: Repository structure, standards, protocols, TOC
Result: Ready to start producing files

Sprint 01: Product Thinking

Goal: Define product before starting development
Output: Principles, Canvas, Problem definition
Result: Clear decision on product viability

Sprint 02: Blueprint

Goal: Design product before writing code
Output: Discovery, Validation, Architecture, Planning
Result: Complete product design ready for development

Sprint 03: Foundation

Goal: Build common foundation for all projects
Output: Starter Kit, Auth, Database, Billing, etc.
Result: Shared infrastructure defined once

Sprint 04: Development Workflow

Goal: Standardize AI-powered development process
Output: Prompts, Templates, QA, Git Workflow
Result: Reproducible development process

Sprint 05: Execution

Goal: Turn Product OS into an executable system
Output: Example projects, Playbooks
Result: New products built by running playbooks

No Changes to Previous Sprints

Once a Sprint is complete, it is frozen. New ideas go to:

· Decision Log (if important)
· Product OS v2 (if requires breaking changes)

---

🚀 Getting Started

Using This Repository

1. Start with Sprint 00 - Read the standards and protocols
2. Follow the sprint order - Each sprint builds on previous ones
3. Use the file IDs - Request files by ID (e.g., "FD-AUTH-001")
4. Stay atomic - One file = one concept
5. Keep it alive - Update based on real project experience

Working with AI Assistants

Simply request a file by its ID:

```
"Show me FD-AUTH-001"
"Update BP-ARCH-001 to version 1.1"
"Create a new file FD-NEW-001 with [description]"
```

The AI will respond with exactly that file's content, following all standards.

Creating New Files

1. Choose the right category (PRN/CAN/BP/FD/PRM/TMP/QA/EX/PLY)
2. Select a topic code
3. Assign the next available number
4. Use the standard file structure
5. Add cross-references
6. Set status to "Draft"
7. Include in the TOC

Avoiding Scope Creep

· Don't change completed sprints
· Log new ideas in Decision Log
· Save breaking changes for v2
· Keep each sprint focused

---

🤝 Contributing

Guidelines

1. Follow all documentation standards
2. Maintain atomic files (one topic = one file)
3. Keep content actionable (Understand → Decide → Execute)
4. Add cross-references, not duplicate content
5. Update version and status when modifying
6. Never change frozen sprints

Pull Request Process

1. Review existing content to avoid duplication
2. Ensure your file follows all standards
3. Add related files section
4. Update the repository TOC
5. Request review from maintainers

---

📄 License

Product OS v1 is licensed under the MIT License.

This means you can:

· ✅ Use it commercially
· ✅ Modify it
· ✅ Distribute it
· ✅ Use it in your own products

With the condition that you include the original copyright notice.

---

🙏 Acknowledgments

This framework was developed through collaboration between human product thinkers and AI assistants, proving that Vibe Coding is not just possible but powerful.

---

Built with ❤️ for Vibe Coders everywhere

---

🔗 Quick Reference

Most Important Files to Read First

1. SPR-STD-004 - Authoring Protocol (The Constitution)
2. SPR-TOC-001 - Complete Table of Contents
3. PRN-PRD-001 - Product Thinking Principles
4. BP-ARCH-001 - Architecture Overview
5. FD-START-001 - Starter Kit Foundation
6. PRM-SYS-001 - System Prompt Template
7. PLY-PRD-001 - New Product Playbook

Common File Requests

Request File
New product planning CAN-OVR-001
Customer definition CAN-CUS-001
MVP scope CAN-MVP-001
Architecture design BP-ARCH-001
Authentication setup FD-AUTH-001
Database selection FD-DB-002
Billing integration FD-BILL-001
System prompt PRM-SYS-001
PRD template TMP-PRD-001

---

Repository Version: v1.0
Last Updated: 2026-01-09
Status: Stable

---
Decision Log System

🎯 Purpose

A lightweight system to capture decisions and ideas without breaking momentum. Every thought goes to the Decision Log, not into active development.

---

📋 How It Works

1. One File = One Decision

Every decision gets its own file:

```
Sprint-00/SPR-DEC-XXX-Short-Title.md
```

2. Decision File Structure

```markdown
# Decision: [Title]

**Decision ID:** SPR-DEC-001
**Date:** YYYY-MM-DD
**Status:** Proposed | Approved | Rejected | Postponed
**Related Files:** [FD-AUTH-001]

---

## Context
What triggered this decision?

## Options Considered
1. Option A - Pros/Cons
2. Option B - Pros/Cons
3. Option C - Pros/Cons

## Decision
What we chose and why.

## Impact
What changes because of this.

## Action
- [ ] What to do now
- [ ] What to defer

## For Future
How this affects v2 or later sprints.
```

3. Simple Rules

Rule Description
Log First Any idea → Create decision file immediately
Don't Act Never implement during current sprint
Review Later Evaluate decisions during sprint planning
Keep Simple Max 200 words per decision

---

🔄 Decision Lifecycle

```
💡 Idea → 📝 Log it → 🔍 Review → ✅ Approve → 🚀 Implement (next sprint)

                ↓
            ❌ Reject
                ↓
            ⏸️ Postpone (v2)
```

---

📁 Decision Log Location

```
Sprint-00/
└── Decisions/
    ├── SPR-DEC-001-Use-Supabase.md
    ├── SPR-DEC-002-Vibe-Coding-Standards.md
    ├── SPR-DEC-003-Pricing-Strategy.md
    └── ...
```

---

✨ Benefits

· ✅ No interruption - Keep writing, just log it
· ✅ No duplication - All decisions in one place
· ✅ No forgetting - Every idea is captured
· ✅ No regret - Review decisions properly later
· ✅ No scope creep - Current sprint stays focused

---

🎮 Quick Command

Just write:

```
"Log: [your decision or idea]"
```

Example:

```
"Log: Should we use Firebase instead of Supabase for auth?"
```

The system creates:

```
Sprint-00/Decisions/SPR-DEC-XXX-Firebase-vs-Supabase.md
```

---

📊 Decision Status Tracker

Status Meaning Next Action
Proposed New idea, needs review Review in next sprint planning
Approved Ready for implementation Add to next sprint backlog
Rejected Won't implement Document why, close
Postponed Good idea, but for v2 Move to v2 backlog

---

🚨 Important

1. Never implement a decision in the current sprint
2. Decisions are evaluated during sprint planning
3. Each decision is independent (no cross-referencing between decisions)
4. If it's urgent, discuss with team, still log it

---

📝 Example

SPR-DEC-001-Use-Supabase.md

```markdown
# Decision: Use Supabase as Primary Database

**Decision ID:** SPR-DEC-001
**Date:** 2026-01-09
**Status:** Proposed
**Related Files:** FD-DB-002

---

## Context
Need a database solution for all products. Considering managed vs self-hosted.

## Options Considered
1. **Supabase** - Pros: Managed, built-in auth, realtime. Cons: Vendor lock-in
2. **AWS RDS** - Pros: Full control. Cons: More setup, higher cost
3. **PlanetScale** - Pros: Serverless, scale. Cons: Limited free tier

## Decision
Supabase for all projects.

**Why:** Balances ease of use with features. Free tier sufficient for MVPs. Realtime works great for our use cases.

## Impact
- Database selection files need updating
- All future projects use Supabase by default

## Action
- [x] Log decision
- [ ] Update FD-DB-002 with Supabase as default
- [ ] Create FD-DB-003 for Supabase setup

## For Future
- Consider migration strategy if we need to leave Supabase
- Evaluate self-hosted Supabase option for v2
```

---

🔗 Related Files

· SPR-STD-010 - Detailed Decision Log Standard
· SPR-ARCH-002 - Architecture

---

Created: 2026-01-09 | Status: Stable | Version: 1.0

---

"Product OS is not a book. It's a living system. Every real product built improves it." 
