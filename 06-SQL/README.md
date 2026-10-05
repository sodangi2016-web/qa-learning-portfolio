# SQL for QA

SQL was practiced as part of the QA learning plan.

## Tables
- customers
- transactions
- transaction_types

## Skills Practiced
- SELECT
- WHERE
- AND / OR
- ORDER BY
- INSERT / UPDATE / DELETE
- COUNT / SUM / MAX / MIN / AVG
- GROUP BY / HAVING
- INNER JOIN
- LEFT JOIN
- CASE
- COALESCE
- Subqueries
- EXISTS
- CTEs
- Window functions
- ROW_NUMBER
- RANK / DENSE_RANK
- LAG / LEAD
- Running totals
- Running balance and overdraft detection

## Example

```sql
SELECT 
    c.name,
    SUM(t.amount) AS total_transaction_amount
FROM customers c
JOIN transactions t
    ON c.id = t.customer_id
GROUP BY c.id, c.name
ORDER BY total_transaction_amount DESC
LIMIT 1;
```

This returns the customer with the highest total transaction amount.
