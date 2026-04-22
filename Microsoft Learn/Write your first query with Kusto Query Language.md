# Write your first query with Kusto Query Language

## What's a Kusto query?

A Kusto query is a read-only request to process data and return results. The request is stated in plain text that's easy to read, author, and automate. A Kusto query has one or more query statements and returns data in a tabular or graph format.

Tabular query satements contain zero or more _operators_. Eeach operator starts with a tabular input and returns a tabular output. Operators are sequenced by a pipe (`|`). Data flows-or is _piped_-from one operator to the next. The data is filtered or manipulated at each step and fed into the following step.

Think of it like a funnel, where you start out with an entire data table. Each time the data passes through another operator, it's filtered, rearranged, or summarized. Because the piping of information from one operator to another is sequential, the query's operator order is important. At the end of the funnel, you're left with a refined output.

These operators are KQL-specific, although they often have parallels to SQL or other languages.

Let's look at an example query:

```
StormEvents
| where StartTime between (datatime(2007-11-01) .. datetime(2007-12-01))
| where State == "FLORIDA"
| count
```
