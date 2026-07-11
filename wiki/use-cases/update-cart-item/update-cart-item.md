# Goal

Update item in the customer's cart.

## Actor

Customer

## Preconditions

1. Customer is logged in / registered.
2. Item is in the cart.

## Business Rules

1. A `CartItem` is unique by **(item + selected options)**. The same item with *different* options is a separate line, not an increment.

## Main Success Scenario

1. Customer updates an item in the cart (with quantity and options).
2. System verifies the restaurant is open.
3. System verifies the item is in stock for the requested quantity.
4. System updates the `CartItem` and recalculates totals.

## Exception Flows

Each branch is labelled by the Main Flow step it extends.

- **2a. Restaurant is closed:** reject — "Restaurant is closed".
- **3a. Item is out of stock:** reject — "Item is not in stock".

## Postconditions

1. `CartItem` is updated in `Cart`.
2. Totals are recalculated.

## Diagram

1. Flowchart
2. Sequence Diagram
3. Pseudocode

# Notes
- src: Claude.
1. Does update include remove (qty → 0)?
2. Option change can collide with the uniqueness key. Editing options may make `(item + options)` match an existing line (e.g. "Burger [no onions]" → "[extra cheese]" when that line already exists). Add an exception flow — merge quantities or reject.
3. Stock check should only gate an increase. Step 3 currently verifies stock unconditionally; lowering the quantity (or removing) must not be blocked by stock. Only check stock for the added delta when qty increases.
4. Restaurant-open check on edits? Blocking cart *edits* while the restaurant is closed is debatable — the open-check arguably belongs at checkout. Decide consciously rather than inheriting it from `add-cart-item`.
5. Postconditions must mirror the decisions above (line removed if qty→0, lines merged on option collision).
