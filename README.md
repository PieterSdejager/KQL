Sure, here's your KQL cheatsheet rewritten in markup language:

```markdown
# KQL Cheatsheet

## Basic Operators
- **AND**: Combines two conditions and returns results that match both.
  ```kql
  "error" AND "failure"
  ```
- **OR**: Combines two conditions and returns results that match either.
  ```kql
  "error" OR "failure"
  ```
- **NOT**: Excludes results that match the condition.
  ```kql
  "error" NOT "failure"
  ```

## Wildcards
- **Asterisk (*)**: Represents zero or more characters.
  ```kql
  "erro*"
  ```
- **Question Mark (?)**: Represents a single character.
  ```kql
  "err?r"
  ```

## Proximity Searches
- **NEAR**: Finds terms that are close to each other.
  ```kql
  "error" NEAR "failure"
  ```

## Ranges
- **Numeric Range**: Searches for values within a specified range.
  ```kql
  "price:[100 TO 200]"
  ```
- **Date Range**: Searches for dates within a specified range.
  ```kql
  "date:[2023-01-01 TO 2023-12-31]"
  ```

## Field Searches
- **Specific Field**: Searches within a specific field.
  ```kql
  "title:error"
  ```

## Boosting
- **Boost**: Increases the relevance score of a term.
  ```kql
  "error^2 failure"
  ```

## Grouping
- **Parentheses**: Groups terms or clauses to form sub-queries.
  ```kql
  (error OR failure) AND (price:[100 TO 200])
  ```

## Fuzzy Searches
- **Tilde (~)**: Searches for terms that are similar to the specified term.
  ```kql
  "error~"
  ```

## Examples
- **Find documents containing "error" and "failure" within the title field**:
  ```kql
  "title:(error AND failure)"
  ```
- **Find documents containing "error" within the last 30 days**:
  ```kql
  "error AND date:[now-30d TO now]"
  ```

## Useful Resources
- **Microsoft Learn**: *An external link was removed to protect your privacy.*
```
