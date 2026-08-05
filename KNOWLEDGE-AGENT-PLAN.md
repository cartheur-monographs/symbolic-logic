# Knowledge Agent Plan

Date: 2026-08-05

This plan describes how to turn this repository into a bounded knowledge agent focused on Berkeley, his comparison set, and the problem of living embodied machine intelligence.

## Goal

Build a domain-specific knowledge agent that can answer questions about:

- Berkeley's `Symbolic Logic and Intelligent Machines`
- Berkeley's `Machine "Intelligence"` and related `1951-1952` machine writings
- the comparison set `Berkeley, Ashby, Heiserman, Walter, Turing, Shannon`
- the relation between symbolic logic, control, embodiment, adaptation, and machine intelligence
- the paper's present critical question: what current LLM-centered robotics still leaves architecturally underdescribed

The agent should be a research assistant for this corpus, not a general-purpose AI explainer.

## Scope

The first version of the agent should stay inside the classed source set already prepared in this repo:

- Berkeley
- Ashby
- Heiserman
- Walter
- Turing
- Shannon

Optional secondary context can be added later, but only when clearly labeled as secondary.

## Product definition

The agent should be able to do four things well:

1. Answer source-grounded questions about Berkeley and the comparison set.
2. Explain influence, comparison, and architectural difference across the corpus.
3. Compare Berkeley with Heiserman-style embodied or adaptive machine intelligence without collapsing them into the same thing.
4. Retrieve passages, concepts, and structured summaries with citations back to the corpus.

The agent should not pretend to be an expert in all of AI, robotics, logic, or cybernetics.

## Current repository status

The repository already has the most important corpus-preparation step completed:

- classed text extractions in `sources-classed/` and `literature-classed/`
- project-level notes in root markdown files
- an active paper bundle in `arxiv/v.2/`

The next agent work should build on that state rather than assuming an untouched PDF-only repo.

## Phase 1: Corpus preparation

The main extraction work is now done for the high-priority comparison set.

Remaining work is:

- clean OCR noise where it materially harms retrieval
- split each classed source into stable chunks
- store chunk metadata with source name, section, approximate page range, and theme tags

### Chunking guidance

Use chunks that are:

- large enough to preserve argument flow
- small enough to retrieve precise evidence

A good initial target is:

- `800` to `1500` words per chunk
- `100` to `200` words of overlap

For Berkeley specifically, special indexing should be added around these themes:

- intelligent machines
- inputs, outputs, storage, calculation, control
- Boolean algebra
- states and events
- robot examples
- programming and subroutines
- learning from experience
- persistence, maintenance, reproduction

## Phase 2: Concept map and ontology

Build a small domain ontology so the agent can reason consistently about repeated concepts.

### Core entities

- `Berkeley`
- `Shannon`
- `Ashby`
- `Heiserman`
- `Walter`
- `Turing`

### Core concepts

- `symbolic logic`
- `Boolean algebra`
- `intelligent machines`
- `control`
- `memory`
- `inputs`
- `outputs`
- `states`
- `events`
- `robot`
- `behavior`
- `adaptation`
- `embodiment`
- `persistence`
- `recovery`
- `maintenance`
- `learning from experience`

### Relationships to encode

- `influenced_by`
- `extends`
- `contrasts_with`
- `applies_to`
- `embodies_in_hardware`
- `anticipates`
- `falls_short_of`

The ontology does not need to be complex. It just needs to make the agent's comparisons stable.

## Phase 3: Retrieval design

The most important capability is source-bounded retrieval.

### Retrieval strategy

Use hybrid retrieval if possible:

- lexical search for exact names and terms
- vector retrieval for semantic similarity

### Retrieval rules

- Prefer Berkeley first when the question is about Berkeley's own claims.
- Prefer Shannon when the question is about the logic-to-circuit bridge.
- Prefer Ashby and Walter when the question is about adaptation, feedback, or embodiment.
- Prefer Heiserman when the question is about reflex, memory, generalization, or confidence-bearing revision.
- Prefer Turing when the question is about child machines, learning machines, or unorganized machines.

### Ranking priorities

Rank passages higher when they:

- directly answer the question
- contain named authors or named concepts
- define a concept
- contain examples of machines, robots, control, states, events, feedback, or learning
- offer explicit historical attribution

## Phase 4: Prompt design

The agent needs a strict system prompt to avoid drifting into generic AI chatter.

### Prompt requirements

- Stay inside the provided corpus unless the user explicitly requests external context.
- Distinguish between direct evidence and inference.
- When comparing Berkeley with later AI or robotics, state clearly that those are cross-period interpretations.
- Prefer Berkeley's wording and examples over modern paraphrase when possible.
- Avoid flattening Berkeley into a generic "symbolic AI" figure.
- Avoid overstating direct historical lineage where only architectural continuity has been established.

### Voice

The voice should be:

- scholarly but readable
- explicit about uncertainty
- careful with chronology
- able to compare lineages without overstating influence

## Phase 5: Internal note library

Priority notes should include:

- Berkeley as subject overview
- Shannon as the logic-to-circuit bridge
- Ashby as adaptive middle pressure point
- Walter as embodied seam
- Berkeley and embodied machine intelligence
- Berkeley versus Heiserman
- Turing as nearby developmental alternative

These notes now exist in partial form in the root markdown files and should be formalized into reusable agent notes later.

## Phase 6: Evaluation

The agent should be tested with questions that stress retrieval discipline and historical accuracy.

### Evaluation categories

- direct factual questions
- influence questions
- comparison questions
- chronology questions
- interpretation questions

### Example evaluation prompts

- `How does Berkeley define an intelligent machine?`
- `What role does Shannon play in Berkeley's machine theory?`
- `How does Ashby clarify Berkeley's learning problem?`
- `Why does Walter matter for the paper's account of embodiment?`
- `How does Berkeley differ from Heiserman on adaptation and learning?`
- `How does Turing's child-machine route differ from Berkeley's control architecture?`
