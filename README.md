# Smart Electricity Bill Calculator

A beginner-friendly Python console program that calculates and displays an
electricity bill. It uses only Python's built-in features and does not use a
database, files, APIs, external libraries, or classes.

## Run the program

From this folder, run:

```text
python smart_electricity_bill_calculator.py
```

The program asks for the customer's name, customer ID, and electricity units
consumed. Units may be entered as a whole number or a decimal. If the units are
not a valid number or are negative, the program explains the problem and asks
again.

## Program flow

1. `get_customer_details()` collects the customer information and validates the
   units consumed. It returns the name, ID, and units.
2. `calculate_bill(units_consumed)` calculates the energy charge using
   progressive slabs, adds the fixed service charge, and returns all three
   amounts.
3. `display_bill(...)` prints the customer details and a formatted breakdown
   of the bill.
4. `main()` calls these functions in order to run the program.

## Electricity rates

The rates are progressive: each rate applies only to the units in that slab.

| Units | Rate |
| --- | ---: |
| First 100 units | ₹2 per unit |
| Next 100 units (101–200) | ₹4 per unit |
| Next 300 units (201–500) | ₹6 per unit |
| Units above 500 | ₹8 per unit |

A fixed service charge of **₹100** is added to the energy charge. Bill amounts
are displayed to two decimal places. The console uses `Rs.` as the currency
marker so the bill displays correctly in Windows terminals that do not support
the rupee symbol.