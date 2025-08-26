Power BI Sample Dataset (Transactions)
Columns:
- Date (YYYY-MM-DD)
- Product (Product A/B/C/D)
- Region (North/South/East/West)
- Channel (Online/Retail)
- Units (integer)
- Sales (currency; Units * product price with small noise)

Suggested Tutorial Steps:
1) Import this dataset (CSV or Excel).
2) In Power Query: set data types (Date, Text, Whole Number, Decimal), remove errors/blanks, trim/clean text if needed.
3) Create a Date table in DAX and relate Date -> Date.
4) Measures to try: Total Sales, Total Units, AOV, Sales MTD, Sales YoY %.
5) Visuals: Cards (Sales/Units/AOV), Bar by Product, Line by Month, Map by Region, Slicers for Date/Channel.

Attribution: @_thedatanerd
