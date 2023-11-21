# Nodes reference

How to use each node in workflows.

Our detailed guide to each node in workflows. _Over time, we'll expand each node into a separate page with a detailed description, examples, and comparison to spreadsheets and SQL._

## Get data

**Select** the data sources you want to transform in your workflow. They can come from results from other workflows or integrations.

## Save data

Make the results of your workflow available for other workflows or use them in dashboards by connecting the appropriate nodes with a **Save data** node.

## Select columns

Use the **select columns** node to choose a subset of columns from the input table.

You can choose whether the selected columns are **kept** or **excluded** with the _select mode_ dropdown.

## Join

Use the **join** node to merge together two tables that share a common column (e.g. an internal id or email address).

You'll need to specify which column you're using from each of the two tables (**Left join** and **Right join**). You can always preview the two tables.

💡 A join node needs to have two input nodes. Inputs 1 and 2 are assigned in the order that you connected them to the join node. By convention, the Input 1 is the _left table_ and Input 2 is the _right table_.

Optionally, you can decide what happens to rows that don't match with the **How** condition. Your four options are:

*   **Inner:** Only keep matching rows (default)
    
*   **Left:** Keep all rows from the **left table**
    
*   **Right:** Keep all rows from the **right table**
    
*   **Outer:** Keep all rows
    

For the **Left**, **Right** and **Outer** joins, any non-matching rows are filled with _null values_. Usually you'll want to use **Inner**, unless you know you have missing data and you want to handle this as a special case.

## Group and Aggregate

Use the **group and aggregate** node to generate summary statistics for groups of rows.

You'll start with the group columns, which are used to place the rows from the input table into groups:

*   If you choose **one** group column, then the rows are grouped by _each unique value_ in that column.
    
*   If you choose **multiple** group columns, then the rows are grouped by _each unique combination of values_ across the columns.
    
*   If you **don't** choose a group column, all rows will go in one group.
    

💡 For certain columns, all the values will be unique and grouping won't do anything. E.g. if you have decimal numbers, you'll need to round them to whole numbers before grouping.

For the next step, you decide what metrics to calculate to summarise each group. These will be _aggregation metrics_ like SUM or MEAN. You can compute as many aggregations as you like. By default, we'll show the size (COUNT) of each group.

The output table will show each group column, along with each aggregation.

## Union

Use the **union** node to stack data from multiple input nodes with the same schema.

💡 A union node can have unlimited inputs, but they all need to have the same schema (i.e. column names and data types), otherwise it will return an error.

Optionally, you can decide to do with duplicate rows. By default, they are kept, but you can remove them with the _distinct_ option.

## Except

Use the **except** node to remove rows that exist in a second table.

💡 Like the union node, an except node can have unlimited inputs, but they all need to have the same schema (i.e. column names and data types), otherwise it will return an error.

## Sort

Use the **sort** node to sort the rows based on column values.

For each column, you can decide if rows should be sorted in **ascending** (default) or **descending** order.

💡 The priority of the sort is determined by the order of the sort columns.

## Limit

Use the **limit** node to choose a fixed number of rows.

The **Limit** option to choose how many rows to keep. By default, you'll start from the first row, but you can use the **Offset** option to change this.

💡 The order of the rows is not guaranteed unless you use a sort node before a limit node.

## Filter

Use the **filter** node to filter rows from the input node by a condition.

Rows are kept if the condition is true. If you provide multiple conditions, rows are kept if **all** of them are true.

💡 We don't currently support **OR** filters. For now, the workaround is to use multiple filter nodes, and combine together with a union node.

## Distinct

Use the **distinct** node to remove duplicate rows.

By default, all the columns will be used to compare rows, to decide if there are duplicate values.

Optionally, you can choose to compare only a subset of columns.

## Pivot

Use the **pivot** node to summarise the relationship between two columns.

To build a pivot table, you'll need to specify the two columns to compare:

*   The **Pivot index** is the vertical axis of the pivot table
    
*   The **Pivot column** is the horizontal axis of the pivot table
    

You'll then need to decide what metric to summarise (**Pivot value**), and how to aggregate it.

💡 Currently you can only summarise by a single metric. If you need to summarise multiple metrics, take a look at the group and aggregate node.

The output will show the relationship of each unique combination of the two columns, in a 2D layout.

## Unpivot

Use the **unpivot** node to reverse data that is pivoted.

Pivoted data is great for presentation, but is not a good format for data analytics. You can use the **Unpivot** node to combine multiple columns into separate row values.  
  
First provide the new column names for the **category** column and the **value** column.  
The **categories** will be the different column names from the **selected** columns and the **values** will be taken from the rows of these columns.

You can also select **specific** columns you would like to keep **without** unpivotting them.

## Intersect

Use the **intersect** node to only include rows that appear in all the input nodes.

💡 An intersect node can have unlimited inputs, but they all need to have the same schema (i.e. column names and data types), otherwise it will return an error.

## Edit

Use the **edit** node to transform columns using pre-defined functions.

You'll need to choose the column, the function to apply and (in certain cases) the value for the function.

Edits are useful for common operations like basic maths, manipulating strings or extracting parts of dates.

💡 For more custom logic, take a look at the formula node.

## Add

Use the **add** node to create new columns using pre-built functions.

The behaviour is identical to the edit node, except that the output creates _new columns_ instead of replacing existing columns.

## Convert (coming soon 🚀 )

Use the convert node to change the data type of columns, for example, turning numbers into text.

💡 If a conversion fails, it means that the current column contains data whose format cannot be converted. Often this happens when otherwise numerical columns contain bits of text like letters or hyphens. You will need to clean these cases before by using the _edit_ or _formula_ node.

## Rename

Use the **rename node** to rename the columns from the input node.

Keep in mind that column names:

*   can only contain letters, numbers and underscores
    
*   must start with a letter or underscore
    
*   are limited to 300 characters in length
    

## Formula

Use the **formula node** to create new columns using spreadsheet-like formulas.

You reference columns using their name, and formulas are applied automatically to all rows in the table. You have access to arithmetic operations, and a library of functions.

Example 1: Calculate payable tax on your profits

    (revenue-cost)*(tax/100)

Example 2: Create full names from first and last names, removing extra whitespace

    join(strip(first_name)," ",strip(last_name))

The formula editor will help you write your formulas with:

*   **autocompletion** for column names, functions and brackets
    
*   **syntax highlighting** to differentiate numbers, text, columns and functions
    
*   **error checking** (wavy red lines) for mistakes in your formulas
    

Take a look at the help tab for more examples, and a full reference with all functions.

💡 Functions typically one work for one type of input (e.g. number, text, date & time). We're working on making this more explicit, with better error messages as well.

**If you think we've missed any important functions, please reach out and let us know!**

## Window and Calculate

Use the **window and calculate** node to calculate a metric for each row, by looking at other rows in the chosen window.

For example:

*   _7 day moving average_: order the rows by date, and for each row, take the average of a 7 row window.
    
*   _Cumulative sum over time:_ order the rows by time, and for each row, take sum of all the preceding rows
    
*   _Best ranking collateral in each campaign_: group by campaign, order by performance, generate the rank number for each one, then use a filter node to select rows with rank number = 1.
    

_The window node is powerful, but we appreciate it's difficult to get your head around. More content and explanations are coming soon._

## Sentiment Analysis (coming soon 🚀)

Get a sentiment estimation between -1 (bad) to +1 (good) of your text column.

## Text

Use the **text node** to write text at any point on the canvas.

Text nodes help you explain your reasoning behind parts of the workflow, and communicate with collaborators.

💡 Text node position is not preserved when you click the format button. We're working on a solution to this.