# mongoDB-aggregation-hard

i was assigned some tasks and asked to perform them and attach the screenshots this is a readme for easy tasks -->

**1. Category Value and Classification:**

- **Task:** For each `category`, calculate its total inventory value (sum of `price * quantity` for all products in that category). Then, classify each category: if total value > 10000, it's "High Value"; if > 5000, it's "Medium Value"; otherwise, it's "Standard Value".
- **Output:** Display `category` (as `categoryName`), `totalInventoryValue`, and `valueClassification`.
- **Hint:** First `$group` by category to sum `price * quantity`. Then use `$project` with `$cond` (possibly nested or using `$switch`) for classification.

![image](https://github.com/user-attachments/assets/0954f9ae-05e2-4a2e-9d95-6ed6c8982143)

![image](https://github.com/user-attachments/assets/bcdd71e7-b209-49dc-8472-ea7e8253c896)

**2. Suppliers and Their Most Expensive Product:**

- **Task:** For each `supplier.name`, find the name and price of the most expensive product they supply.
- **Output:** Display `supplierName`, `mostExpensiveProductName`, and `maxPrice`.
- **Hint:** You might need to `$sort` first within groups or use `$max` carefully. One approach: `$sort` by price, then `$group` using `$first` to pick the top item's details for each supplier.

![image](https://github.com/user-attachments/assets/8af77956-03d5-4c80-abbb-6f204ce643cb)

![image](https://github.com/user-attachments/assets/449045bb-fe98-473a-84bd-a6f8b9476ad9)

3. Products with "portable" tag but NOT "computer" tag:
*   Task: Find products that have the "portable" tag but DO NOT have the "computer" tag. Display their name and tags.
*   Hint: Use $match. You'll need to match for inclusion of one tag and exclusion of another. Consider $all and $nin or a combination of $elemMatch and $not. A simple $and with two conditions on the tags array is often effective.

![image](https://github.com/user-attachments/assets/43877b10-4c0e-4b9d-8b62-cfa98e168dd7)

I have attached queries and their outputs in the screenshots and copy pasted the questions from the provided notion file.
