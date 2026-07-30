---
title: Excel Field Notes July 2026
date: 2026-07-30 08:28:SS +/-TTTT
categories: ["Field Notes"]
tags: [excel, spreadsheet, productivity, keyboard-shortcuts, definitions, learning, field-notes ]
pin: true
---

## What I Learned
I continued my dive into Excel, but with family in town, it was more important to me to spend time with them. This month I dove into V, H, and XLOOKUP.

### Definitions
- Relative cell reference: a cell reference adjusts based on the position of the formula when copied to another cell. It changes according to the relative position of the rows and columns
- Absolute: cell reference remains constant, regardless of where the formula is copied or moved. It is indicated by a dollar sign ($) before the column letter and row number. Eg: =$A$1+$B$1
- Mixed: combines relative and absolute, can lock either column or row. Eg: =$A1+B$1
- VLOOKUP: vertical lookup, search value in first col of a range or table and returns a value in the same row from another specified col
-- Syntax: =VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
-- Example: In a table where column A contains product IDs and column B contains product names, =VLOOKUP(101, A2:B10, 2, FALSE) searches for product ID 101 in column A and returns the corresponding product name from column B. The last parameter is not mandatory, and Excel sets the default to FALSE.
- HLOOKUP: horizontal lookup, searches a value in the first row of a range or table and returns a value in the same column from another specified row
-- Syntax: =HLOOKUP(lookup_value, table_array, row_index_num, [range_lookup])
-- Example: In a table where row 1 contains months and row 2 contains sales data, =HLOOKUP("January", A1:H2, 2, FALSE) searches for January in row 1 and returns the corresponding sales data from row 2. The last parameter is not mandatory, and Excel sets the default to FALSE. 
- XLOOKUP: extended lookup, more flexible and powerful that can perform both horizontal and vertical lookups. Great for more complex searches and returns results from any column or row, regardless of position
-- Syntax: =XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found], [match_mode], [search_mode])
-- Example: =XLOOKUP(101, A2:A10, B2:B10, "Not Found", 0) searches for product ID 101 in column A and returns the corresponding product name from column B. If the ID is not found, it returns "Not Found." The last three parameters in the formula are not mandatory. 
...

### Tips

- Use relative for repetitive calculations across multiple rows or columns where the formula needs to adapt to its new location
- Use absolute when you need to refer to a fixed value or cell that shouldn’t change when the formula is copied
- Use mixed when one part of the reference should remain fixed, while the other part should change
- VLOOKUP: when you need to search for a value in the first column and retrieve data in another column in the same row
-- EG: looking up prices in a product list or finding employee names based on ID numbers. 
- HLOOKUP: when data is organized horizontally and you need to search for a value in the first row and return data from a specific row in another column
-- EG: finding quarterly sales data when your data is structured with months in the first row and sales figures in subsequent rows or in a dataset with multiple column headings. 
- XLOOKUP: when VLOOKUP and HLOOKUP can’t handle your data structure
-- EG: ideal for matching data across different tables, or returning results from columns or rows that are not adjacent to the lookup column or row. 

