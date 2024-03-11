# DB__Assignment

Q1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
It is many-to-one relationship between table Product and other table Product_Category.
Many products can belong to the same product category. The category_id column in the "Product" table is a foreign key that references the id column in the "Product_Category" table. This relationship allows multiple products to share the same category.

Q2. How could you ensure that each product in the "Product" table has a valid category assigned to it?
=>Using foreign key constraint 
category_id INT NOT NULL REFERENCES product_category(id)
This line of code establishes a foreign key relationship between the "Product" table's category_id column and the "product_category" table's id column. With this foreign key constraint, the database ensures that each value in the category_id column of the "Product" table must exist in the id column of the "product_category" table. If there is an attempt to insert or update a record in the "Product" table with a category_id that does not exist in the "product_category" table, the database will reject the operation, maintaining referential integrity.
The foreign key constraint is what ensures that each product in the "Product" table has a valid category assigned to it. The constraint guarantees that the category_id values must match existing id values in the "product_category" table
=>By keeping Constraint like NOT NULL that allow not keep any null value as category_id is primary key for table id column in product_category.



