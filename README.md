# reasonable

_Building on the shoulders of giants..._

Rough notes that led to these ideas are https://notes.strangemonad.com/Building+AI+Applications for now. 

## Assumptions of things we believe to be true

- Lots of the current ideas being explored to create systems that reason aren't unique to AI

- Workflows and workflow orchestration is ubiquitous and not unique to AI agents.
  - All successful technologies retrieve (bridge) something from the past
- Open world vs closed world
  - We don't want to have to specify all the tools we know about up front (before we even know what we're trying to solve)
- Leverage robotics
  -  decomposable hierarchical Sense-Plan-Act loops e.g. T-REX style teleo-reactor architectures and control loops generally.
- Leverage Operations Research, planning, constraint solving and symbolic systems where that makes sense either directly (e.g. have an LLM call out to a solver) or indirectly by using similar ideas
- Surface stuck-ness and ask for help
  - being stuck can be a good thing for a co-pilot (we don't need to be building a Mars rover).
- The core ideas of automated theorem provers historically stem from a shared philosophy - make a machine that can reason automatically. Recent work on automated theorem proving has built up a large number of approaches to make humans more efficient at proving theorems. We should leverage those ideas for making AI seasons efficient at reasoning.
- It's unlikely that a single LLM in a single call or chat interaction solves complex, multistep reasoning problems. LLMs are probably not the right architecture on many fronts.
  - Context windows are a scarce resource and always will be. That's a good thing because it can help focus just like our executive functions help to focus
  - That LLMs can remember facts seems like a neat quirk rather than a core feature. We should be able to make much, much smaller LLMs if we don't expect them to remember facts. We should instead use external storage for memory and retrieval (both short term and long term).
- Evals are great. Reasoning systems should be able to self-introspect and self-critique.
  - Always? As part of evaluating convergence? 


## Design Questions
- How nested should workflows get? Should reasoning loops be separate from "pure" workflow execution loops? How?
- chat history vs re-phrasing from scratch.
  - Chat history makes sense for a human input, but we can automate re-phrasing from scratch.


## Ideas

### Workflows
- Workflows are ubiquitous and not unique to AI agents.
- Successful new technologies retrieve (bridge) something from the past ^[Marshall McLuhan's media tetrad]
- Injecting AIs to augment existing workflow automation will be very powerful.
- Workflow execution is just a flavor of incremental, async computation. We should leverage that heavily rather than entangling that with interactions to the AI agent.

#### Tasks and Actions
See temporal.io

### Tactics and Tacticals
Even though deep learning reasoning seems to be pulling ahead of symbolic reasoning on many fronts, there are many 
good ideas from work on automated theorem provers about how to make humans more efficient. We should leverage those ideas for


### Interfaces and Protocols
Protocols are good, we should share them and allow multiple different implementations.


### Dependency injection
Matching workflows and problem-solving steps to dependencies is an ideal fit for dependency injection.


### Other ideas
- deliberate planning
- workflows and workflow runs need identity
- per-step caching of results and meta-reasoning
- Goals and fronts
- Budgets
- Convergence
- Timelines
- Hypotheticals
- Conflicting evidence and resolution strategies
- Executive - what should we surface to a human in what order?
- Goal refinement (and refinement strategies)
  - pause, reword, iterate, augment
  - what history should stay around, what answers should come from cache, what should be from scratch
- Context chains
  - do we need separate execution and reasoning contexts?
- Goal-directed extraction (salient extraction) vs summarization
- Speech acts
- Society of mind / Minsky
- Blueprints
- causal meta-inference
- tasks, projects, artifacts
- task complexity measurements
  - could token level prediction probability be used as a proxy for task complexity or flagging a generating model "getting confused"?
- majority voting
  - ELBO?


## TODO
- Jupyter magic