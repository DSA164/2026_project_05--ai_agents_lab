# 2026 Project 06 — AI Agents Lab

## Purpose

This project is part of the `AI-Engineering-Lab` learning roadmap.

It introduces AI agents in a controlled and educational way. The goal is to understand tools, state, planning, validation, and failure modes without falling into uncontrolled automation.

This is not a vibecoding project. Every agent behavior should be inspectable and explainable.

## Why this project exists

After learning LLMs, local serving, workflows, and RAG, I can begin to connect models to tools.

The core agent loop is:

```text
user objective
  ↓
state
  ↓
reasoning / planning
  ↓
tool selection
  ↓
tool execution
  ↓
observation
  ↓
state update
  ↓
human validation when needed
```

This project teaches how to make that loop explicit.

## Learning focus

This project focuses on:

- tool calling;
- explicit state;
- planning;
- state machines;
- LangGraph-style architecture;
- human-in-the-loop validation;
- decision logging;
- guardrails;
- agent failure modes;
- testing agent behavior.

## Minimal milestone

Build a minimal agent that can use exactly one safe tool and log its decision before using it.

## Final deliverable

A controlled stateful agent prototype with:

- a small set of tools;
- explicit state;
- logged decisions;
- human validation before sensitive actions;
- simple tests for state transitions;
- documented failure modes.

## Repository structure

Recommended structure:

```text
notes/              agent concepts and failure modes
src/tools/           safe tool definitions
src/state/           state objects and transitions
src/agents/          agent prototypes
src/guards/          validation and safety checks
tests/               state and tool behavior tests
experiments/         agent behavior experiments
MENTORING.md         guided exercises and validation checklist
learning_log.md      session-by-session observations
```

## Success criteria

By the end of this project, I should be able to explain:

- what tools the agent can use;
- what state the agent keeps;
- why the agent chooses an action;
- when human validation is required;
- how decisions are logged;
- how to test an agent without trusting it blindly.

## Relation to the next project

This project prepares `2026_project_07--business_watch_agent`.

Once agent behavior is controlled, I can apply it to a useful watch system that combines sources, retrieval, scoring, and alerts.
