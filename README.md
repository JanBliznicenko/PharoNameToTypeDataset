# Pharo name-to-type dataset
Dataset of name to type regularities from Pharo 13, along with original unprocessed logged types with circumstances

Dataset was created with TypeInfoTools: https://github.com/JanBliznicenko/TypeInfoTools

Produced by using run-time type logging using Metalinks while executing tests and examples.

Date: 2025-08-12

# Contents

* *unprocessed*: STON format - Original outputs merged into a single file without any other changes, contains most context data
* *name-to-type-with-origin*: STON format - Grouped by names, with lists of all types, some context info dropped
* *name-to-type-statistics*: CSV format with semicolon delimiter - aggregations per name, contain name, most common type, ratio to all distinct recordings of all types, amount of distinct recordings of all types
* *analysis*: CSV format with semicolon delimiter - Ad-hoc analysis of disagreements between methods and vars

## Notes

* Amount of baselines processed: 177
* Applied on return types and variables (including temporary, not including shared/pool)
* Analysis only contains results with at least 80 % ratio and 30 distinct recordings
* Distinct recoding = unique referencing class
* Referencing class for methods = sender's class
* Referencing class for vars = receiver's class when doing the assignment (or message send for method parameters)