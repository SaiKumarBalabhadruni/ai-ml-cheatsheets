# AI Agents Cheat Sheet

## What Is an AI Agent?

An AI agent is a system that uses a model to pursue a goal by reasoning over state, using tools, and taking actions.

A useful abstraction:

```text
Model
+
Tools
+
State / Memory
+
Control Loop
=
Agent
```

## Agent Loop

```text
Observe
 ↓
Reason
 ↓
Plan
 ↓
Act
 ↓
Observe Result
 ↓
Continue / Finish
```

Not every agent needs every step explicitly.

## Tool Calling

The model requests an external function or tool.

Examples:

- Search
- Database query
- Calculator
- Code execution
- API request
- File operation

## Function Calling

A structured representation of a requested function and its arguments.

## State

Information needed to continue the current workflow.

## Memory

Information retained beyond a single immediate model operation.

## Planning

Breaking a goal into smaller steps.

## Orchestration

Coordinating models, tools, data, and workflows.

## Agent vs Chatbot

A chatbot may simply generate responses.

An agentic system can:

```text
Understand Goal
 ↓
Choose Action
 ↓
Use Tool
 ↓
Inspect Result
 ↓
Take Another Action
```

## Common Agent Failure Modes

- Tool misuse
- Bad planning
- Infinite loops
- Incorrect assumptions
- Stale state
- Prompt injection
- Excessive tool calls
- Lack of verification

## Agent Design Principle

Give an agent the smallest set of tools that reliably supports its goal.

More tools do not automatically make an agent better.
