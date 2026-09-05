# Tool Calling & MCP Cheat Sheet

## Tool Calling

Tool calling lets a model request execution of an external capability.

Conceptually:

```text
User
 ↓
Model
 ↓
Tool Request
 ↓
Tool
 ↓
Tool Result
 ↓
Model
 ↓
Answer / Next Tool
```

## Function Calling

A structured mechanism where the model produces arguments for a predefined function.

Example concept:

```json
{
  "name": "get_weather",
  "arguments": {
    "location": "Hyderabad"
  }
}
```

The exact schema depends on the platform.

## Tool

A capability available to the model.

Examples:

- Search
- Calendar
- Database
- File system
- CRM
- Calculator

## MCP — Model Context Protocol

A protocol designed to standardize how AI applications connect models with external tools and data sources.

The protocol defines a structured way for compatible clients and servers to exchange context and capabilities.

## MCP Mental Model

```text
AI Application
      ↓
MCP Client
      ↓
MCP Server
 ┌────┼──────────────┐
 ↓    ↓              ↓
Tools Resources   Prompts
```

Exact capabilities depend on the implementation.

## Security Considerations

Tool-enabled AI systems need controls around:

- Authentication
- Authorization
- Input validation
- Output validation
- Secret handling
- Tool scope
- Audit logging
- Prompt injection
- Data exfiltration

## Principle of Least Privilege

A tool should receive only the permissions it needs.

For example, a read-only database tool should not automatically have write access.
