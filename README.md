# Retail Billing with Multiple Discount Rules

Builds an itemized sample invoice with bulk discounts, an order-level discount, a maximum discount cap, and category-based tax.

## What it demonstrates

Variables, numbers, strings, tuples, lists, nested loops, conditions, arithmetic and comparison operators, indexing, and list operations. No imports or user-defined functions are used.

## Sample assumptions

- Quantity of at least three for an item gives 5% off that item.
- Gross merchandise total of at least 5000 gives an additional 10% off the post-bulk subtotal.
- Combined discounts cannot exceed 20% of gross merchandise value.
- Tax rates are selected by product category and applied after discounts.
- The order discount is allocated proportionally across the remaining item values before tax.

Edit the product list, category tax rates, and rules near the top of `main.py`.

## Algorithm

1. Calculate each line's gross amount and applicable bulk discount.
2. Find each line's category tax rate and store the line values in lists.
3. Calculate the order discount, then enforce the total discount cap.
4. Allocate the order discount proportionally to each line.
5. Apply category tax and add the item totals to produce the amount due.

## Pseudocode

```text
FOR each product
    calculate gross and bulk discount
    find category tax rate and save line data
calculate order discount and enforce maximum discount
FOR each saved line
    allocate order discount proportionally
    calculate category tax and line total
print invoice totals
```

## Flowchart

```text
START -> Read products and tax rates -> Calculate gross and bulk discounts
       -> Calculate order discount and cap -> For each item allocate discount
       -> Apply tax -> Add line totals -> Print invoice -> END
```

## Run

```powershell
python main.py
```

## Live Streamlit deployment

https://retail-billing-discounts-ntlnbfgwjappdmnhrnketbr.streamlit.app/
