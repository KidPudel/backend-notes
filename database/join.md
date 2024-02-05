# Different Types of SQL JOINs

Here are the different types of the JOINs in SQL:

- `(INNER) JOIN`: Returns records that have matching values in both tables
- `LEFT (OUTER) JOIN`: Returns all records from the left table, and the matched records from the right table
- `RIGHT (OUTER) JOIN`: Returns all records from the right table, and the matched records from the left table
- `FULL (OUTER) JOIN`: Returns all records when there is a match in either left or right table

    

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/c312b26c-2049-4a41-8dca-aa90f900b9e4/929f0654-9b0e-42dd-88ee-c702502487a1/Untitled.png)

**Note:** The `INNER JOIN` keyword returns only rows with a match in both tables. Which means that if you have a product with no CategoryID, or with a CategoryID that is not present in the Categories table, that record would not be returned in the result.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/c312b26c-2049-4a41-8dca-aa90f900b9e4/cad258dd-df16-498a-8bf8-1ba51ef8c9dc/Untitled.png)

**Note:** The `LEFT JOIN` keyword returns all records from the left table (Customers), even if there are no matches in the right table (Orders).

If there is no matches for the right side, a null value will be returned for that field

CutomerID: 1902, OrderID: 9211

CustomerID: 5401, OrderID: // because there is no match
![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/c312b26c-2049-4a41-8dca-aa90f900b9e4/292088f7-98e6-414a-bb10-2e0f2b6af798/Untitled.png)
![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/c312b26c-2049-4a41-8dca-aa90f900b9e4/9f56f450-6b18-489a-8ec3-ba435569eee5/Untitled.png)
