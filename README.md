[![Claude Code Project](https://img.shields.io/badge/Claude%20Code-Project-blue?style=flat-square&logo=github)](https://github.com/danielrosehill/Claude-Code-Repos-Index)

# Agent Reference Workflows

**An index of repositories that each demonstrate one agentic workflow, end to end.**

These are not tutorials and not templates. Each one is a record of an agentic
workflow actually being run on a real task — the sequence that worked, the wrong
turns, and the places the process fell short.

## Why keep these as an index

I write a lot of Claude Code plugins. The hard part of designing a plugin is
almost never the mechanics; it is knowing **what the workflow should actually
be** — which steps exist, what order they go in, where a human has to intervene,
and which step quietly does most of the work.

That knowledge only comes from having run the workflow properly at least once,
in the open, with the mess left in. So these repos are kept as **working context
for plugin design**. Specifically, each one is meant to supply:

| | |
|---|---|
| **The intended workflow** | The stages, in order, as they turned out to be — not as they were first imagined |
| **Where it broke** | The steps that ran too late, the constraints that turned out not to discriminate, the assumptions that survived too long |
| **Where a human is still required** | Which is usually the most interesting line in the whole repo, because it is the line that moves |
| **Candidate automation** | The steps that are mechanical enough to become a command, a skill, or an agent |

A plugin designed from a tidy imagined workflow encodes the imagined version. A
plugin designed from one of these encodes what the work is actually like.

## The index

### Purchasing and evaluation

**[Agentic-Purchase-Pipeline](https://github.com/danielrosehill/Agentic-Purchase-Pipeline)**
An eight-stage process for evaluating any purchase over roughly $50, with a full
worked example — a hardware purchase researched, specified, reversed four times,
and ordered.

- *Demonstrates:* spec capture with evidence tagging · identifying the
  load-bearing requirement no vendor publishes · classifying a market by failure
  mode · driving a logged-in storefront to confirm variant-level availability
- *Exposes:* the spec-revision loop is the whole game and most tooling omits it;
  landed cost was computed one stage too late and overturned the recommendation
  at the last step; execution is still manual for authorisation reasons rather
  than capability ones

### Development process

**[Research-Decide-Implement](https://github.com/danielrosehill/Research-Decide-Implement)**
A deterministic Research → Decide → Implement pattern that deliberately overrides
the default collaborative loop of coding agents: stay on the defined path and no
approval gates are needed.

- *Demonstrates:* trading interactivity for autonomy under an explicit contract;
  artifacts as the communication channel between phases
- *Companion:* **[rdi-template](https://github.com/danielrosehill/rdi-template)**
  — the canonical seed scaffold planted into a target repo

**[Document-As-You-Go](https://github.com/danielrosehill/Document-As-You-Go)**
A system prompt and slash command that make coding agents capture what they
discovered, not just what they changed.

- *Demonstrates:* treating knowledge as an output of the work rather than a
  byproduct; routing a finding by its reach — this task, this project, or a
  standalone knowledge repo
- *Exposes:* capture reliably loses to task completion unless it is made an
  explicit obligation before reporting done

### Decision-making under a spec

**[Spec-Led-Certification](https://github.com/danielrosehill/Spec-Led-Certification)**
Choosing a professional certification spec-first: write the requirements, then
survey and score the options against them.

- *Demonstrates:* the same shape as the purchase pipeline applied to a decision
  with no product to buy — evidence that the pattern generalises past shopping
- *Related:* **[Spec-Standard-Research](https://github.com/danielrosehill/Spec-Standard-Research)**
  — background research into specification standards for spec-driven agentic work

### Reasoning and research

**[Perspective-Finder-Prompt](https://github.com/danielrosehill/Perspective-Finder-Prompt)**
A prompt for mapping the real nuances in a debate rather than flattening it to
two sides.

- *Demonstrates:* structured disagreement-mapping as a repeatable agent task

## Not currently published

Listed because they are part of the same collection and are relevant context,
even though the repositories are private or local-only:

| Repo | Workflow | Status |
|---|---|---|
| Claude-Shopping-Eval-Demo | Screenshot store catalogues → multimodal agent → ranked PDF. Complements the purchase pipeline: better when the constraint is *price across local stores* rather than *fit* | Local only — remote 404s |
| Ezra-Travel-Bot | Proof of concept for a flight-booking agent — the same execution boundary problem as stage 6 of the purchase pipeline | Private |
| Claude-Geolocation-Helper | Claude Code pattern for assisting with geolocation tasks | Private |
| Scraping-Notes | Verified web-access routes per site — what worked, what did not, and why | Private |
| Habits-Of-Claude | Standing habits for a coding agent, one file per habit | Private |

## What qualifies for this index

A repo belongs here if it:

1. Documents **one** workflow, not a grab-bag of prompts
2. Was **actually run** on a real task, with a worked example attached
3. Records **where it went wrong**, not only where it went right
4. Names the point at which a **human is still required**

A repo that is only a prompt, only a template, or only a finished result belongs
elsewhere — see [Claude-Code-Repos-Index](https://github.com/danielrosehill/Claude-Code-Repos-Index)
for the full collection, and [Subindices](https://github.com/danielrosehill/Subindices)
for the other indexes.
