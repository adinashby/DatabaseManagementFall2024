# Lecture 3: Relationship between tables

#### **Topic: Relationship Between Tables**

1. **Introduction to Relational Databases**
   - **What is a Relational Database?:**  
     A relational database is a type of database that stores data in tables that are related to each other. Unlike flat databases, relational databases allow for organizing data across multiple tables, making it easier to manage complex data sets efficiently.
   - **Importance of Relationships in Databases:**  
     Relationships between tables reduce data redundancy and improve consistency by storing related information in different tables. For example, customer information is stored in one table, while order information is stored in another. This allows for linking customer records with their corresponding orders.

2. **Types of Relationships Between Tables**
   - **One-to-One (1:1) Relationship:**  
     A one-to-one relationship exists when each record in Table A has exactly one matching record in Table B and vice versa. This is often used when dividing a table for security or organizational purposes. For example, a "Users" table can have a corresponding "UserDetails" table, where each user has one set of details.
   - **One-to-Many (1:N) Relationship:**  
     The most common type of relationship where one record in Table A can have multiple related records in Table B. For example, a "Customers" table can have a one-to-many relationship with an "Orders" table because one customer can have multiple orders.
   - **Many-to-Many (M:N) Relationship (Using a Junction Table):**  
     A many-to-many relationship occurs when multiple records in Table A can relate to multiple records in Table B. Since databases can't handle many-to-many relationships directly, a junction table (also called a linking or bridge table) is used. For example, "Students" and "Courses" tables have a many-to-many relationship because each student can enroll in multiple courses, and each course can have multiple students.

3. **Creating Relationships in Microsoft Access**
   - **Step 1: Setting Up Tables with Primary Keys:**  
     Start by ensuring that each table involved in the relationship has a primary key. The primary key uniquely identifies each record in a table. For example, in a "Customers" table, the primary key could be "CustomerID," and in an "Orders" table, the primary key could be "OrderID."
   - **Step 2: Linking Tables with Foreign Keys:**  
     A foreign key is a field in Table B that corresponds to the primary key in Table A. It establishes the relationship between the two tables. For instance, the "Orders" table would have a "CustomerID" as a foreign key to link each order with the corresponding customer from the "Customers" table.
   - **Step 3: Using the Relationships Window in Access:**  
     The Relationships window allows you to visually create and manage relationships between tables. Demonstrate how to open the Relationships window, add tables, and drag the primary key from one table to the foreign key in another to establish a relationship.
   - **Step 4: Enforcing Referential Integrity:**  
     Referential integrity ensures that relationships between tables remain consistent. When enabled, it prevents adding a record to the "Orders" table without a corresponding "CustomerID" in the "Customers" table. It also ensures that deleting a record in one table doesn’t leave orphaned records in related tables.

4. **Types of Join Operations in Relationships**
   - **Inner Join (Default):**  
     An inner join shows only the records where there is a matching value in both tables. For example, it shows only the orders where there is a corresponding customer in the "Customers" table.
   - **Left Join (Left Outer Join):**  
     A left join shows all the records from the first (left) table, along with matching records from the second (right) table. If there are no matches, it shows NULL values for the second table. This is useful when you want to see all customers, even those who haven't placed any orders.
   - **Right Join (Right Outer Join):**  
     A right join is the opposite of a left join. It shows all records from the second (right) table and matching records from the first (left) table. If there are no matches, NULL values will appear for the first table.
   - **Full Outer Join (Not Directly Supported in Access):**  
     While Microsoft Access doesn't directly support full outer joins, you can create queries that simulate them by combining left and right joins. This will return all records from both tables, with NULLs for missing matches.

5. **Practical Applications of Relationships**
   - **Linking Customers and Orders:**  
     Explain how to create a real-world example of a one-to-many relationship by linking a "Customers" table to an "Orders" table. Each customer can have multiple orders, but each order is linked to a single customer.
   - **Creating a Many-to-Many Relationship Using a Junction Table:**  
     Demonstrate how to create a many-to-many relationship between "Students" and "Courses" using a junction table called "StudentCourses." Each record in the junction table would have a "StudentID" and a "CourseID," linking a student to the courses they are enrolled in.
   - **Combining Data from Multiple Tables in Queries:**  
     Once relationships are established, show how to create queries that pull data from multiple tables. For example, pulling customer names from the "Customers" table and their related order details from the "Orders" table.

6. **Maintaining Relationships**
   - **Cascading Updates and Deletes:**  
     When creating relationships, Access allows you to enforce cascading updates and deletes:
     - **Cascading Updates:** Automatically updates foreign key values in related tables if the primary key value changes. For example, if a "CustomerID" changes in the "Customers" table, all related records in the "Orders" table will be updated.
     - **Cascading Deletes:** Automatically deletes related records when a primary record is deleted. For instance, if a customer is deleted from the "Customers" table, all their related orders are also deleted from the "Orders" table.
   - **Managing Relationship Conflicts:**  
     Discuss common conflicts that can arise in relationships, such as orphaned records (records in one table with no matching records in another). Show how to troubleshoot and fix these issues by adjusting relationships or data entry practices.

7. **Exercise: Creating and Managing Relationships**
   - **Step-by-Step Example of Creating Relationships Between Tables:**  
     Students will create a one-to-many relationship between two tables ("Customers" and "Orders"), set up foreign keys, and enforce referential integrity. 
   - **Building a Many-to-Many Relationship Using a Junction Table:**  
     In a more advanced exercise, students will create three tables: "Students," "Courses," and "StudentCourses" (junction table). They will establish relationships between these tables and practice creating queries that pull data from all three.
   - **Applying Cascading Updates and Deletes:**  
     Students will enable cascading updates and deletes and perform operations to see how changes in one table impact related records in another.

