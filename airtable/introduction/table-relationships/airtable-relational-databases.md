---
author: kapnobatai136

category: must-know

aspects:
  - introduction

type: normal

---

# Relational Databases

---
## Content

When thinking of a definition for relational databases, the first thing that comes to mind is that tables in a database contain rows that communicate, hence the relational part. This is not entirely true. The relation is between the column (field), the row, and the data (or type to be more specific) that is inserted.

You can have a base with multiple tables, each holding a different type of data. Consider this, you're a movie theater manager and have recently started to store your data digitally (mostly interested in ticket sales). In your first attempt, you created a new table that holds all data, which looked something like this:

| Identification | Movie Name | Movie Duration | ... | Buyer Name | Buy Date   | ... |
|----------------|------------|----------------|-----|------------|------------|-----|
| 1              | Peter Pan  | 107            | ... | Andrei     | 25/02/2004 | ... |
| ...            | ...        | ...            | ... | ...        | ...        | ... |


A better way of doing this is having two separate tables, one for movies that are showing, and one for ticket buyers. Both tables would communicate through a movie identifier.

| Identification | Movie Name | Movie Duration | ... |
|----------------|------------|----------------|-----|
| 1              | Peter Pan  | 107            | ... |
| ...            | ...        | ...            | ... |

| Buyer Name | Buy Date   | Movie ID | ... |
|------------|------------|----------|-----|
| Andrei     | 25/02/2004 | 1        | ... |
| ...        | ...        | ...      | ... |