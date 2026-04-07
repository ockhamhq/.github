# ockham

**Intelligence infrastructure.**  
**No ghosts. Just machines.**

---

## The Problem

Most AI infrastructure asks you to believe in ghosts.

It wraps an LLM call in a persona, gives it a name and a memory, calls it an *agent*, and charges you for the privilege of sending the same context tokens to every ghost in the room.

Strip the metaphor and look at the computation:

- processes  
- state  
- API calls  

---

## The Thesis

> An agent is a process with a system prompt, tool access, and shared state.  
> **There is no further entity.**

LLM calls are not special components.

They are:

- stateless functions  
- high latency  
- loosely typed outputs  
- non-trivial cost per invocation  

Everything else is distributed systems engineering.

---

## The Replacement

Ockham replaces agents with explicit machinery.

| Instead of | Use |
|------------|-----|
| agents | processes |
| memory | state |
| collaboration | shared data structures |
| orchestration | task graphs |
| context stuffing | context selection |

---

## The Stack

Each component removes one layer of abstraction.

```text
razor   → task graph runtime
fabric  → state + memory
forge   → distributed execution
lattice → contracts
plexus  → graph/vector IR
sieve   → caching
sim     → deterministic simulation
corvus  → observability
```

---

## Core Ideas

### Task Graphs

A mutable DAG of computation.

Nodes:
- LLM calls  
- tool invocations  
- gates  
- forks / merges  

Structure is not fixed.  
Execution can rewrite the graph.

---

### Context Selection

Each step declares what it needs.

Not:
> “give me everything”

But:
> “give me this projection of state”

This is how you reduce tokens:
- not truncation  
- not compression  
- selection  

---

### No Ghosts

There is no identity.

There is no agent.

There is only:
- process  
- state  
- transitions  

---

## Status

Early.

Building in the open.

---

## Repositories

- https://github.com/ockhamhq/razor  
- https://github.com/ockhamhq/fabric  
- https://github.com/ockhamhq/forge  
- https://github.com/ockhamhq/lattice  
- https://github.com/ockhamhq/plexus  
- https://github.com/ockhamhq/sieve  
- https://github.com/ockhamhq/sim  
- https://github.com/ockhamhq/corvus  

---

## Links

- https://noghosts.dev

---

## Lineage

- William of Ockham — don't multiply entities beyond necessity  
- Gilbert Ryle — the ghost in the machine  
- Vienna Circle — verify your claims  

---

**Exorcise your agents.**
