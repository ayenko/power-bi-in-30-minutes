# Power BI Template Setup (TheDataNerd)

This bundle helps you create a PBIX file in ~2 minutes with a clean model, measures, and theme.

## Files
- `powerbi_sample_dataset.csv` / `powerbi_sample_dataset.xlsx` — Transactions fact data
- `DateTable.dax` — Date table DAX
- `DAX_Measures.dax` — Core reusable measures
- `PowerBI_Theme.json` — Navy & Gold theme
- `powerbi_dataset_README.txt` — Short notes

## Steps (create your PBIX)
1. Open **Power BI Desktop** → **Get Data** → CSV or Excel (import the Transactions table).
2. **Power Query**: set data types (Date, Text, Whole Number, Decimal). Remove blanks/errors if any. Close & Apply.
3. **Model**: Create Date table → *Modeling > New table* → paste contents of `DateTable.dax`.
4. In **Modeling**, select **DateTbl** → **Mark as date table** (choose Date column).
5. Create relationships: `Transactions[Date]` → `DateTbl[Date]` (Many-to-one, single direction).
6. (Optional) Create dim tables (Product, Region, Channel) via **Transform Data** (Reference & Remove other columns), or keep as a single fact for the tutorial.
7. Create a **Measures** table (Modeling > New table) and paste `DAX_Measures.dax` measures.
8. Apply the theme: **View > Themes > Browse for themes** → select `PowerBI_Theme.json`.
9. Build visuals: Cards (Total Sales, Total Units, AOV). Bar by Product, Line by YearMonth, Map by Region. Slicers: Date, Channel.
10. Sort Month axis: **Sort by column** → `YearMonth` to avoid alphabetic order.
11. Add interactivity: Drill-through to Product detail page; Bookmarks + Buttons for slicer panel; Edit Interactions for cross-highlighting.
12. **Publish** to My Workspace; in Service, set **Scheduled refresh** Daily. Document data source & refresh time in the report description.

> Tip: Name bookmarks clearly: *Slicer Panel – Open/Close*.
