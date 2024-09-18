# Lecture 4: Queries with Calculated Fields

### **Topic 1: Selection Queries with Criteria, Calculated Fields, Grouping Functions, etc.**

1. **Introduction to Selection Queries**
   - **What is a Selection Query?:**  
     A selection query retrieves data from one or more tables based on specific criteria. It allows users to view, filter, and analyze subsets of data without modifying the underlying tables.
   - **Why Use Selection Queries?:**  
     Selection queries are essential for extracting meaningful insights from large datasets. They help to focus on the specific data needed for reports or analysis without the need to sift through entire tables.

2. **Creating a Basic Selection Query**
   - **Using the Query Design View:**  
     Step-by-step instructions on opening the Query Design View, selecting tables or queries, and choosing fields to include in the query.
   - **Running a Simple Query:**  
     Once the fields are selected, show how to run the query to retrieve the data. Discuss how the results are displayed in Datasheet View and how they relate to the original table.

3. **Using Criteria in Queries**
   - **Adding Criteria to Filter Data:**  
     Criteria are conditions that data must meet to be included in the query results. For example, using the criteria `>= 100` in the "Price" field will only show records where the price is equal to or greater than 100.
   - **Using Logical Operators in Criteria:**  
     Demonstrate how to apply logical operators (AND, OR, NOT) in criteria to filter data:
     - **AND:** Both conditions must be true. For example, `Country = "USA" AND City = "New York"` will return records where both the country is USA and the city is New York.
     - **OR:** Either condition must be true. For example, `City = "London" OR City = "Paris"` will return records from either London or Paris.
     - **NOT:** Excludes data matching the condition. For example, `NOT "USA"` will exclude all records where the country is USA.
   - **Using Wildcards in Criteria:**  
     Wildcards allow for flexible matching of text patterns:
     - **Asterisk (*) for multiple characters:** `*Street*` will match any record containing the word "Street."
     - **Question mark (?) for a single character:** `Sm?th` will match records like "Smith" and "Smyth."

4. **Working with Calculated Fields in Queries**
   - **What is a Calculated Field?:**  
     A calculated field is a field that derives its value from an expression rather than directly from a table. It allows you to perform calculations or concatenate values based on existing fields.
   - **Creating a Simple Calculated Field:**  
     Demonstrate how to add a calculated field in Query Design View. For example, adding a calculated field `TotalPrice: [Quantity] * [UnitPrice]` will multiply the "Quantity" field by the "UnitPrice" field to get the total price for each order.
   - **Using Mathematical Operators in Calculated Fields:**  
     Explain basic arithmetic operations that can be performed in calculated fields: addition (+), subtraction (-), multiplication (*), and division (/).
   - **Concatenating Fields:**  
     Show how to concatenate text fields. For example, `FullName: [FirstName] & " " & [LastName]` will create a full name by combining the first and last names.

5. **Using Grouping Functions in Queries**
   - **What is Grouping in Queries?:**  
     Grouping allows you to aggregate data based on a specific field, creating summary reports. It helps in calculating totals, averages, counts, and other statistics over groups of records.
   - **Common Grouping Functions:**
     - **SUM:** Adds up all values in a group. For example, `SUM([TotalPrice])` will calculate the total sales for each group.
     - **AVG:** Calculates the average of all values in a group. For example, `AVG([Quantity])` will return the average quantity sold per group.
     - **COUNT:** Counts the number of records in each group. For example, `COUNT([OrderID])` will count how many orders were placed by each customer.
     - **MIN and MAX:** Returns the minimum or maximum value within each group.
   - **Creating a Query with Grouping Functions:**  
     Step-by-step guide on how to apply grouping in queries. For example, grouping data by "Category" and applying a `SUM([Sales])` to calculate total sales per category.
   - **Using the "Totals" Option in Query Design:**  
     Show how to use the "Totals" button in the query design toolbar to group data and apply aggregate functions.

6. **Exercise: Creating Queries with Criteria, Calculated Fields, and Grouping**
   - **Step-by-Step Example:**  
     Students will create a query based on a "Sales" table, applying filters to show sales greater than $100, adding a calculated field to show total sales (Quantity * Price), and grouping the results by region to show the total sales per region.

---

### **Topic 2: How to Write Simple Regular Expressions for Queries**

1. **Introduction to Regular Expressions (RegEx)**
   - **What is a Regular Expression?:**  
     A regular expression (RegEx) is a sequence of characters that defines a search pattern. It is commonly used for pattern matching in strings, allowing users to search for specific formats or text patterns in a database.
   - **Why Use Regular Expressions in Queries?:**  
     Regular expressions provide powerful, flexible search capabilities, especially when searching for data with specific patterns (e.g., email addresses, phone numbers, postal codes) or cleaning data with inconsistent formats.

2. **Basic Syntax of Regular Expressions**
   - **Literals and Special Characters:**  
     Literal characters match exactly what you type. For example, the expression `"Smith"` will only match records that contain "Smith."
   - **Special Characters in RegEx:**  
     - **Dot (.) for any single character:** Matches any single character except a newline. For example, `Smi.h` will match "Smith" and "SmitH."
     - **Asterisk (*) for zero or more occurrences:** Matches zero or more of the preceding character. For example, `ab*` will match "a," "ab," "abb," and so on.
     - **Plus (+) for one or more occurrences:** Matches one or more of the preceding character. For example, `ab+` will match "ab," "abb," but not "a."
     - **Question mark (?) for zero or one occurrence:** Matches zero or one of the preceding character. For example, `ab?` will match "a" and "ab," but not "abb."
   - **Character Classes (Square Brackets):**  
     Character classes allow matching any one of a set of characters. For example, `[abc]` matches "a," "b," or "c." You can also define ranges, such as `[a-z]` to match any lowercase letter.
   - **Escape Special Characters:**  
     If you need to match a literal special character (e.g., a dot or asterisk), escape it with a backslash (`\`). For example, `\.` matches a literal period.

3. **Writing Simple Regular Expressions for Queries**
   - **Matching Specific Patterns in Data:**  
     Demonstrate how to write RegEx patterns for specific data formats:
     - **Email Addresses:** Use a regular expression like `[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}` to match email addresses in a database.
     - **Phone Numbers:** Use a pattern like `\(\d{3}\) \d{3}-\d{4}` to match phone numbers in the format "(123) 456-7890."
     - **Postal Codes:** Use a pattern like `^[A-Z]\d[A-Z] \d[A-Z]\d$` to match Canadian postal codes in the format "A1B 2C3."
   - **Using RegEx in Query Criteria:**  
     In Microsoft Access, regular expressions aren't natively supported in standard queries, but you can use VBA functions or expressions to perform similar pattern matching tasks. Show how to create a query where criteria use functions or patterns for validating or extracting text.
   
4. **Advanced Regular Expressions**
   - **Anchors (Start and End of Strings):**  
     Use `^` for the start of a string and `$` for the end of a string. For example, `^Smith$` matches only the entire word "Smith," but not any record that has "Smith" as part of a larger string.
   - **Repetitions and Ranges:**  
     Demonstrate how to define a specific number of occurrences. For example, `\d{3}-\d{2}-\d{4}` matches a social security number in the format "123-45-6789."
   - **Optional and Required Characters:**  
     Use `?` to specify that a character is optional. For example, `colou?r` matches both "color" and "colour."
   - **Capturing Groups:**  
     Explain capturing groups and how to extract parts of a match. For example, `(abc|def)` matches either "abc" or "def."

5. **Exercise: Writing Regular Expressions for Queries**
   - **Step-by-Step Example:**  
     Students will create a query to search for data that matches specific patterns, such as finding all email addresses from a "Customers" table using a simple regular expression. They will also apply RegEx to validate phone numbers in a "Contacts" table.
