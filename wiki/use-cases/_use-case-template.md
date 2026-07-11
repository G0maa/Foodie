<!--
Use-case template. Copy this file into a new folder under use-cases/
(e.g. remove-cart-item/remove-cart-item.md) and fill it in.
Guidance is in HTML comments — delete them as you go.
-->

# Goal

<!-- One sentence: the outcome the ACTOR wants. Not "manage X" — a single goal. -->

## Actor

<!-- Primary actor. Note secondary/system actors only if they participate. -->

## Preconditions

<!-- States ASSUMED TRUE before the use case starts and NOT re-checked inside it
     (guaranteed by something else, e.g. auth middleware). If the flow has to
     check it, it's not a precondition — it's a step. -->
1.

## Business Rules

<!-- Invariants / domain constraints this use case must honor
     (uniqueness keys, single-restaurant carts, limits...). Drives the ERD. -->
1.

## Main Success Scenario

<!-- The happy path only. Every line is an ACTOR or SYSTEM action.
     Write checks as actions ("System verifies ..."); on this path they pass. -->
1. <Actor> ...
2. System verifies ...
3. System ... (and any side effects / recalculations)

## Exception Flows

<!-- Branch from a Main Flow step: "Na" = an extension of step N.
     Describe only what differs — do NOT re-list the preamble steps. -->
- **2a. <condition>:** <system response>.
- **3a. <condition>:** <system response>.

## Postconditions

<!-- States true after success. Cover create AND update variants where relevant. -->
1.

## Diagram

1. Flowchart
2. Sequence Diagram
3. Pseudocode

# Notes

<!-- Open questions, decisions to make, ADR candidates. -->
1.
