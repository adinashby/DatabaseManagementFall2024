# Lecture 1: Table and Query

#### **Topic 1: What is a Table and Query**

1. **Introduction to Microsoft Access**
   - **Overview of Database Management Systems (DBMS):**  
     Introduction to what a DBMS is and how it manages data. Explain the difference between flat file databases (like spreadsheets) and relational databases (like Access). Discuss the benefits of using a DBMS.
   - **Importance of Access in Small to Mid-Scale Databases:**  
     Highlight how Microsoft Access is commonly used by individuals and small to medium-sized businesses to manage data without needing large-scale enterprise solutions like SQL Server or Oracle.

2. **Understanding Tables in Access**
   - **Definition of a Table:**  
     A table in Microsoft Access is a structured set of data that is organized in rows (records) and columns (fields). Each row represents a unique record, and each column represents a specific data attribute.
   - **Structure of a Table: Rows and Columns:**  
     Explain how rows contain individual records and columns (fields) store specific data points. For example, a "Customer" table might have columns like Name, Address, and Phone Number.
   - **Differences Between Tables and Spreadsheets:**  
     Discuss key differences between a database table and a spreadsheet, such as data relationships, normalization, and data integrity.
   - **Creating and Modifying Tables:**  
     Demonstrate how to create a table from scratch or use existing templates in Access. Explain how to add or delete fields, set field properties, and adjust table structures.
   - **Navigating the Datasheet View:**  
     Introduce the Datasheet View, where users can interact with table data, edit records, and modify table structures easily.
   - **Adding and Deleting Records:**  
     Practical steps to add or delete records from tables in Access. This includes both manual entry and importing data from external sources.

3. **Queries in Microsoft Access**
   - **Definition and Purpose of Queries:**  
     A query is a request for information from a database table or a combination of tables. It helps users filter, sort, and retrieve specific data based on criteria.
   - **Different Types of Queries:**  
     - **Select Queries:** Used to retrieve data based on conditions. No changes are made to the database.
     - **Action Queries:** Includes Update, Delete, Append, and Make-Table queries that modify data or structure.
     - **Parameter Queries:** A dynamic query that prompts the user to input values before execution.
     - **Aggregate Queries:** Used to calculate summary statistics (e.g., SUM, AVG) across grouped records.
   - **Creating Queries: Query Design View:**  
     Step-by-step instructions on using Query Design View to build custom queries. Discuss the visual interface where fields and criteria can be added.
   - **Running and Modifying Queries:**  
     Show how to execute queries, modify their criteria, and save them for later use.
   - **Saving and Managing Queries:**  
     Explain best practices for saving queries in Access, organizing them in the database, and managing multiple queries for different use cases.

4. **Practical Applications of Tables and Queries**
   - **How Tables and Queries Work Together:**  
     Show how tables store raw data and queries retrieve and manipulate that data for reporting, analysis, or updates.
   - **Use Cases of Tables and Queries in Real-World Scenarios:**  
     Provide examples such as customer databases, inventory systems, and financial recordkeeping to demonstrate the practical use of tables and queries.

5. **Exercise: Building Simple Tables and Queries**
   - **Step-by-Step Example: Creating a Table and Query from Scratch:**  
     A hands-on exercise where students create a simple table (e.g., "Students" with fields for Name, Grade, and Age) and then build a query to filter students by a specific grade range.

---

#### **Topic 2: Fields and Primary Key**

1. **Introduction to Fields in Microsoft Access**
   - **What is a Field?:**  
     A field is the smallest unit of data in a table, representing a single piece of information. Each field corresponds to a column in a table, such as "Name" or "Date of Birth."
   - **Different Field Types (Text, Number, Date/Time, etc.):**  
     Fields in Access can hold different data types:
     - **Text:** Used for alphanumeric data, like names or descriptions.
     - **Number:** Stores numerical data, used for calculations.
     - **Date/Time:** Stores dates and times.
     - **Currency, Boolean (Yes/No), Hyperlinks, etc.:** These specialized fields serve different purposes in data management.
   - **Creating and Modifying Fields in Tables:**  
     A tutorial on how to add fields when designing tables, change their properties (name, size, format), and modify them to meet the needs of the database.
   - **Field Properties: Field Size, Format, Input Mask:**  
     Explanation of key field properties:
     - **Field Size:** Determines the maximum number of characters for text fields or the range of values for number fields.
     - **Format:** Specifies how data is displayed (e.g., date formats like MM/DD/YYYY).
     - **Input Mask:** Sets rules for data entry (e.g., phone number formats).

2. **Understanding the Importance of Data Types**
   - **Assigning Appropriate Data Types to Fields:**  
     Discuss the importance of selecting correct data types for ensuring data integrity and efficient storage. For example, choosing "Date/Time" for dates instead of "Text."
   - **Data Integrity and Field Type Selection:**  
     Data types enforce rules on what kind of data can be entered, ensuring consistency and reliability of database operations.

3. **Primary Key in Access**
   - **What is a Primary Key?:**  
     The primary key is a unique identifier for each record in a table. No two records can have the same primary key, which ensures data uniqueness.
   - **Purpose of a Primary Key in Database Tables:**  
     Primary keys ensure that each record can be uniquely identified, preventing duplicate data and helping in relationships between tables.
   - **Guidelines for Choosing a Primary Key:**  
     Primary keys should be unique, stable (not subject to frequent changes), and concise. Examples include AutoNumber fields or existing identifiers like Social Security Numbers or Employee IDs.
   - **AutoNumber vs Manual Assignment of Primary Keys:**  
     Compare AutoNumber, where Access automatically assigns a sequential number, to manually assigned primary keys, where you define your own unique identifier.
   - **Setting Up a Primary Key in Access:**  
     Step-by-step guide on selecting or creating a primary key for a table during design.

4. **Relationship Between Primary Key and Foreign Key**
   - **Linking Tables Through Primary Keys:**  
     Explain how primary keys in one table can be linked to foreign keys in another to create relationships between tables (e.g., customer orders linked to customer records).
   - **Importance of Foreign Keys in Relational Databases:**  
     Foreign keys help maintain data integrity by establishing relationships between different tables, allowing for data retrieval through queries that join tables.

5. **Exercise: Setting Fields and Primary Keys**
   - **Creating a Table with Proper Field Types:**  
     Students will create a table and assign appropriate field types based on the type of data (e.g., text for names, number for age).
   - **Defining a Primary Key for Your Table:**  
     Students will set a primary key for their table, ensuring that each record has a unique identifier.
   - **Building Relationships Between Tables Using Primary and Foreign Keys:**  
     Hands-on exercise in which students create multiple tables, set primary and foreign keys, and build relationships between tables (e.g., "Orders" and "Customers").

