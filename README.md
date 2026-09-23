# RPA UI Interaction Patterns

A vendor-independent collection of 13 user interface (UI) interaction patterns for Robotic Process Automation (RPA). The patterns capture recurring UI interaction requirements and connect them to alternative automation Methods, helping developers reason about how a bot can interact with web, desktop, and screen-based interfaces.

## Explore the research

- **[Read the full pattern collection (PDF)](RPA_UI_Interaction_Patterns%20%281%29.pdf)** — pattern descriptions, motivations, variants, applicability conditions, operations, and examples.
- **[Inspect the prototype source code](https://github.com/chester713/rpa-ui-log-analyzer)** — the RPA UI Log Analyzer, a research prototype demonstrating a pattern-guided recommendation approach, with setup instructions and a sample UI event log.

## About the patterns

The collection uses the **Action–Object–Method–Context (AOMC)** model to describe UI interactions:

- **Action:** what the bot needs to do, such as find, read, write, or activate.
- **Object:** what the bot interacts with, such as an HTML element, a UI element exposed through an accessibility interface, or a visual element on screen.
- **Method:** how the interaction can be implemented, such as DOM parsing or manipulation, UI Automation tree parsing or manipulation, visual recognition, or hardware input simulation.
- **Context:** the environment in which the interaction takes place, such as a web, desktop, or screen environment.

An interaction requirement combines an Action, an Object, and a Context. Each pattern links that requirement to one or more automation Methods, with variants and applicability conditions explaining when a method can be used. This provides a common vocabulary for discussing UI automation across RPA tools.

## Pattern collection

| Category | Pattern | Purpose |
| --- | --- | --- |
| Extraction | **Find Element** | Locate a target UI element and establish a reference for subsequent interactions. |
| Extraction | **Read Element** | Retrieve content, attributes, or properties from a target element. |
| Extraction | **Observe** | Monitor a target object for changes over time. |
| Modification | **Write Element** | Insert or update data, values, or properties in a target element. |
| Modification | **Delete Element** | Remove an element from the underlying interface structure where supported. |
| Modification | **Disable Element** | Suppress or deactivate an interfering element so the task can proceed. |
| Control | **Open** | Establish a new execution context through a UI interaction to access a resource. |
| Control | **Activate** | Invoke the functional behaviour of an interactive control. |
| Control | **Hover** | Trigger hover-dependent content or behaviour, such as a tooltip or menu. |
| Control | **Switch Context** | Move the bot's active execution context to another application or window. |
| Control | **Scroll** | Adjust the viewport to reveal elements for subsequent interaction. |
| Control | **Focus** | Assign input focus to a designated element. |
| Control | **Refresh** | Update or reload an interface element or view to show current information. |

For the full definitions and the conditions governing each variant, see the [pattern collection PDF](RPA_UI_Interaction_Patterns%20%281%29.pdf).

## Recommendation prototype

The [RPA UI Log Analyzer](https://github.com/chester713/rpa-ui-log-analyzer) demonstrates how the patterns can guide automation-Method recommendations from recorded UI interaction logs. Its approach has two stages:

1. **Task interpretation:** group recorded events and infer the activities they represent.
2. **Method recommendation:** match interpreted activities to patterns and recommend automation Methods based on the identified context.

The PDF documents the pattern collection; the separate prototype repository contains the implementation of the recommendation approach. Recommendations support design decisions and require checking against the target application and the applicable pattern conditions. See the prototype's README for usage instructions and known limitations.
