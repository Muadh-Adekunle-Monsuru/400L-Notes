### **SQL vs. MongoDB: Commands Comparison**  

#### **What is SQL?**  
SQL (Structured Query Language) is used in **relational databases** (e.g., MySQL, PostgreSQL) to manage structured data stored in **tables** with fixed schemas.  

#### **What is MongoDB?**  
MongoDB is a **NoSQL document database** that stores data in flexible **JSON-like documents** (BSON format) with dynamic schemas.  

---

### **Common SQL Commands & MongoDB Equivalents**  

| **Operation**  | **SQL Command**                          | **MongoDB Command**                          |
|--------------|--------------------------------------|------------------------------------------|
| **Create Database** | `CREATE DATABASE db_name;`          | `use db_name` (implicitly creates DB)    |
| **Create Table/Collection** | `CREATE TABLE users (id INT, name VARCHAR(50));` | `db.createCollection("users")` (optional) |
| **Insert Data** | `INSERT INTO users (id, name) VALUES (1, "Alice");` | `db.users.insertOne({ id: 1, name: "Alice" });` |
| **Select (Read) Data** | `SELECT * FROM users;` | `db.users.find();` |
| **Select with Condition** | `SELECT * FROM users WHERE id = 1;` | `db.users.find({ id: 1 });` |
| **Update Data** | `UPDATE users SET name = "Bob" WHERE id = 1;` | `db.users.updateOne({ id: 1 }, { $set: { name: "Bob" } });` |
| **Delete Data** | `DELETE FROM users WHERE id = 1;` | `db.users.deleteOne({ id: 1 });` |
| **Delete All Rows/Documents** | `DELETE FROM users;` | `db.users.deleteMany({});` |
| **Drop Table/Collection** | `DROP TABLE users;` | `db.users.drop();` |
| **Drop Database** | `DROP DATABASE db_name;` | `db.dropDatabase();` |

---

### **Key Differences in Querying**  
1. **Joins (SQL) vs. Embedded Documents (MongoDB)**  
   - SQL: Uses `JOIN` to combine tables.  
     ```sql
     SELECT users.name, orders.product 
     FROM users 
     JOIN orders ON users.id = orders.user_id;
     ```
   - MongoDB: Stores related data in nested documents (no joins).  
     ```javascript
     db.users.find({}, { name: 1, "orders.product": 1 });
     ```

2. **Aggregation (SQL) vs. MongoDB Aggregation Pipeline**  
   - SQL:  
     ```sql
     SELECT COUNT(*) FROM users WHERE age > 30;
     ```
   - MongoDB:  
     ```javascript
     db.users.aggregate([
       { $match: { age: { $gt: 30 } } },
       { $count: "total_users" }
     ]);
     ```

---

### **When to Use SQL vs. MongoDB?**  
- **SQL (RDBMS)**: Best for structured data, complex queries, and transactions requiring **ACID compliance** (e.g., banking systems).  
- **MongoDB (NoSQL)**: Best for **flexible schemas**, scalability, and handling unstructured data (e.g., social media, IoT, real-time analytics).  
