![[CPS 402 1.jpeg]]

#### **1. Database Operations & Security**  
**d) SQL Query to Filter Cars Due for Service**  
```sql
SELECT * FROM cars 
WHERE service_due_date BETWEEN '2023-12-01' AND '2023-12-31';
```  
**MongoDB Equivalent**:  
```javascript
db.cars.find({
  service_due_date: { $gte: ISODate("2023-12-01"), $lte: ISODate("2023-12-31") }
});
```

**e) Database Security Methods**  
1. **Encryption** (e.g., TLS for data in transit, AES for data at rest).  
2. **Role-Based Access Control (RBAC)** to limit user permissions.  
3. **Regular Backups** to prevent data loss.  
4. **Audit Logging** to track unauthorized access.  
5. **Firewall Rules** to restrict database access to trusted IPs.  
*Why?* Prevents breaches, ensures compliance, and maintains customer trust.  

#### **2. Database Comparisons & Architecture**  
**a) Relational vs. NoSQL**  

| **Feature**       | **Relational (SQL)**          | **NoSQL (MongoDB)**          |  
|-------------------|-----------------------------|----------------------------|  
| **Schema**        | Fixed (predefined tables)    | Flexible (dynamic documents)|  
| **Scalability**   | Vertical (scale-up)          | Horizontal (scale-out)      |  
| **Query Language**| SQL                          | JSON-like queries           |  

**b) Database System Architecture**  
*(Diagram: Users → Application → Query Processor → Database Manager → File Manager → Disk Storage)*  
![[Pasted image 20231212094514.png|300]]
**c) Key Components**  
1. **Query Processor**: Optimizes and executes queries.  
2. **Database Manager**: Ensures ACID compliance.  
3. **File Manager**: Manages disk storage.  
4. **Data Dictionary**: Stores metadata (schemas, indexes).  

**d) Client-Server Architectures**  
1. **2-Tier**: Client ↔ Server (e.g., desktop app + database).  
2. **3-Tier**: Client ↔ Application Server ↔ Database Server (e.g., web apps).  
3. **N-Tier**: Multiple specialized layers (e.g., microservices).  

#### **3. MongoDB Features & Issues**  
**a) Attractive Features**  
1. **Schema-less Design**: Flexible JSON documents.  
2. **Horizontal Scalability**: Sharding for large datasets.  
3. **High Performance**: Indexing and in-memory processing.  
4. **Aggregation Pipeline**: Complex data transformations.  

**b) Common Technical Issues**  
1. **Memory Usage**: High RAM consumption.  
2. **Joins**: No native joins (use `$lookup`).  
3. **Transactions**: Limited multi-document ACID support.  
4. **Schema Design**: Poor design hurts performance.  
5. **Sharding Complexity**: Requires careful planning.  

**c) ACID Properties**  
- **Atomicity**: All-or-nothing transactions.  
- **Consistency**: Valid state transitions.  
- **Isolation**: Concurrent transactions don’t interfere.  
- **Durability**: Survives crashes once committed.  

#### **4. MongoDB Practical Example**  
**a) Create & Populate Database**  
```javascript
use FountainUniversity;
db.STUDIEC.insertMany([
  { MATRIC_NUM: "FLU_07005", NAME: "BANDI", LEVEL: 400, DEPARTMENT: "MATHS & COMP", CCPA: 4.79 },
  { MATRIC_NUM: "FLU_08001", NAME: "MUZZ", LEVEL: 200, DEPARTMENT: "MICROBIOLOGY", CCPA: 2.65 },
  // Add other records...
]);
```

**b) Filter Students (CGPA > 4.5)**  
```javascript
db.STUDIEC.find({ CCPA: { $gt: 4.5 } });
```

**c) Alternative NoSQL Databases**  
1. **Cassandra** (Column-family).  
2. **Redis** (Key-Value).  
3. **Couchbase** (Document).  

**d) DBA Roles**  
1. Schema design and optimization.  
2. Backup/recovery planning.  
3. User access management.  
4. Performance tuning.  

#### **5. Database Setup & Selection**  
**a) Steps to Establish a Database**  
1. **Requirement Analysis**.  
2. **Schema Design**.  
3. **DBMS Selection** (e.g., MongoDB vs. MySQL).  
4. **Deployment & Monitoring**.  

**b) Database Manager Roles**  
1. Transaction management (ACID).  
2. Buffer/pool management.  
3. Concurrency control.  
4. Query optimization.  

**c) Database Selection Factors**  
1. **Data Structure** (structured vs. unstructured).  
2. **Scalability Needs** (vertical/horizontal).  
3. **Budget** (open-source vs. proprietary).  
4. **Query Complexity** (joins vs. aggregations).  

#### **6. Short Notes**  
**i) Database Schema**  
Blueprint defining tables, fields, relationships (e.g., `CREATE TABLE` in SQL).  

**ii) SQLite Database**  
Lightweight, serverless SQL DB for embedded systems (e.g., mobile apps).  

**iii) Physical View**  
How data is stored on disk (blocks, indexes, files).  

**iv) Database Normalization**  
Process to eliminate redundancy (1NF, 2NF, 3NF).  

---


![[CPS 402 20-21.jpeg]]

#### **Question 1: Enterprise Database Design for Online Shopping Company**  

**a) Step-by-Step Database Design Approach**  
1. **Requirement Analysis**:  
   - Identify business needs (e.g., track purchases, inventory, employees).  
2. **Conceptual Design**:  
   - Create ER diagrams to define entities (Products, Suppliers, Employees) and relationships.  
3. **Logical Design**:  
   - Convert ER diagrams to schema (tables for SQL, collections for NoSQL).  
4. **DBMS Selection**:  
   - Choose based on scalability, cost, and data structure (e.g., MongoDB for flexibility).  
5. **Implementation**:  
   - Create tables/collections, populate data, and set up indexes.  
6. **Security & Backup**:  
   - Configure access controls and backup schedules.  

**b) Recommended Database: MongoDB**  
**Justifications**:  
1. **Schema Flexibility**: Adapts to evolving product/purchase structures.  
2. **Scalability**: Handles high-volume transactions (e.g., sales spikes).  
3. **JSON Support**: Aligns with web/app data formats.  
4. **Horizontal Scaling**: Sharding for distributed data.  
5. **Aggregation Framework**: Complex analytics (e.g., sales trends).  

**c) Simplified 4-Table Schema (MongoDB Collections)**  
1. **Products**:  
   ```json
   { 
     "product_id": "P100", 
     "product_name": "Laptop", 
     "supplier_name": "TechDistributors",
     "retailer_name": "QuickShop"
   }
   ```
2. **Purchases**:  
   ```json
   {
     "purchase_id": "PU101",
     "product_id": "P100",
     "purchase_date": ISODate("2023-12-01"),
     "cost": 1200
   }
   ```
3. **Employees**:  
   ```json
   {
     "employee_id": "E202",
     "name": "Alice",
     "department": "Logistics",
     "salary": 50000
   }
   ```
4. **Sales**:  
   ```json
   {
     "sale_id": "S303",
     "product_id": "P100",
     "employee_id": "E202",
     "quantity": 5,
     "sale_date": ISODate("2023-12-10")
   }
   ```

**d) DDL Commands to Populate Tables**  
```javascript
// Insert into Products
db.products.insertOne({
  product_id: "P100",
  product_name: "Laptop",
  supplier_name: "TechDistributors"
});

// Insert into Employees
db.employees.insertOne({
  employee_id: "E202",
  name: "Alice",
  department: "Logistics"
});

// Insert into Sales
db.sales.insertOne({
  sale_id: "S303",
  product_id: "P100",
  quantity: 5
});
```

**e) Preventive Measures for Data Security**  
1. **Encryption**: Encrypt data at rest (AES-256) and in transit (TLS).  
2. **Access Control**: RBAC to limit employee/department access.  
3. **Regular Backups**: Automated daily backups to offsite/cloud storage.  
4. **Audit Logs**: Monitor unauthorized access or changes.  

#### **Question 2: Crime Reporting System **  
**Key Actions**:  
1. **Use MongoDB** for flexible citizen reports (JSON documents).  
2. **Geospatial Indexing** to map crime hotspots.  
3. **Role-Based Access** for police vs. public users.  
4. **Real-Time Analytics** to identify crime trends.  

---
![[CPS 402 21-22.jpeg]]
#### **Question 1: Community Bank Database Solution**  

**a) Database Schema (Relational Model)**  
1. **Branch** (`bname` [PK], `bcity`, `assets`)  
2. **Customer** (`cname` [PK], `street`, `ccity`, `phone`)  
3. **Account** (`account_num` [PK], `bname` [FK], `balance`)  
4. **Depositor** (`cname` [FK], `account_num` [FK])  
5. **Loan** (`loan_num` [PK], `bname` [FK], `amount`)  

**b) DDL Commands (SQL)**  
```sql
-- Create Branch Table
CREATE TABLE Branch (
    bname VARCHAR(50) PRIMARY KEY,
    bcity VARCHAR(50),
    assets DECIMAL(12,2)
);

-- Create Customer Table
CREATE TABLE Customer (
    cname VARCHAR(50) PRIMARY KEY,
    street VARCHAR(100),
    ccity VARCHAR(50),
    phone VARCHAR(15)
);

-- Create Account Table
CREATE TABLE Account (
    account_num VARCHAR(20) PRIMARY KEY,
    bname VARCHAR(50),
    balance DECIMAL(10,2),
    FOREIGN KEY (bname) REFERENCES Branch(bname)
);
```

**c) Populate Tables with INSERT**  
```sql
-- Insert into Branch
INSERT INTO Branch VALUES 
('Main Branch', 'Osogbo', 5000000.00),
('North Branch', 'Ikirun', 3000000.00);

-- Insert into Customer
INSERT INTO Customer VALUES 
('John Doe', '12 Oke-Baale', 'Osogbo', '08012345678'),
('Jane Smith', '45 Olorunda', 'Ikirun', '08087654321');

-- Insert into Account
INSERT INTO Account VALUES 
('ACC001', 'Main Branch', 250000.00),
('ACC002', 'North Branch', 150000.00);
```

**d) SELECT Query for Customer Details**  
```sql
SELECT cname, street, ccity, phone 
FROM Customer;
```

**e) Recommended Client-Server Architecture: 3-Tier**  
1. **Presentation Tier**: Web/mobile interface for bank staff/customers.  
2. **Application Tier**: Business logic (e.g., transaction processing).  
3. **Database Tier**: MongoDB or MySQL for data storage.  
*Justification*: Balances security, scalability, and maintainability.  

**f) Potential Database Performance Issues**  
1. **Poor Indexing**: Slows query performance.  
2. **Network Latency**: Delays in distributed systems.  
3. **Hardware Limitations**: Insufficient RAM/CPU.  
4. **Concurrency Conflicts**: Multiple transactions causing locks.  
5. **Data Corruption**: Due to inadequate backups.  

#### **Question 2: Database System Architecture**  

**a) Labeled Architecture Diagram**  
*(Typical Components: Users → Application → Query Processor → Database Manager → File Manager → Disk Storage)*  

**Key Components & Functions**:  
1. **Query Processor**: Optimizes and executes SQL queries.  
2. **Database Manager**: Ensures ACID compliance (transactions).  
3. **File Manager**: Manages disk I/O and storage.  
4. **Data Dictionary**: Stores metadata (table schemas).  
5. **Buffer Manager**: Caches frequently accessed data.  

**Interrelation**:  
- Users submit queries → Query Processor optimizes → Database Manager retrieves data via File Manager → Results returned to users.  

**b) Database Manager Roles**  
1. **Transaction Management**: Ensures atomicity/consistency.  
2. **Concurrency Control**: Manages multi-user access.  
3. **Buffer Pool Management**: Optimizes memory usage.  
4. **Recovery**: Handles crash recovery via logs.  

#### **Question 3: Crime Reporting System with MongoDB**  

**a) Unique Features of MongoDB**  
1. **Document Model**: JSON-like documents for flexible data.  
2. **Horizontal Scaling**: Sharding for large datasets.  
3. **Aggregation Pipeline**: Complex analytics (e.g., crime trends).  
4. **Geospatial Indexes**: Track crime hotspots.  
5. **Replication**: High availability with replica sets.  

**b) Technical Issues in MongoDB**  
1. **Memory Usage**: High RAM consumption for large datasets.  
2. **Joins**: Limited native join support (use `$lookup`).  
3. **Schema Design**: Poor design leads to performance bottlenecks.  

---
![[CPS 402 a.jpeg]]

#### **Question 3c: MySQL vs. MongoDB (4 Key Differences)**  
| **Feature**       | **MySQL (Relational)**               | **MongoDB (NoSQL)**               |  
|-------------------|------------------------------------|----------------------------------|  
| **Data Model**    | Tables with rows/columns           | JSON-like documents              |  
| **Schema**        | Fixed schema (predefined structure)| Dynamic schema (flexible fields) |  
| **Scalability**   | Vertical (scale-up with hardware)  | Horizontal (scale-out via sharding) |  
| **Query Language**| SQL (structured queries)           | JSON-based queries               |  

#### **Question 4**  
**a) Database Definition**  
A **database** is an organized collection of structured data stored electronically, enabling efficient retrieval, updating, and management.  

**b) 4 Business Applications**  
1. **E-commerce**: Product catalogs, customer orders.  
2. **Banking**: Transaction records, account management.  
3. **Healthcare**: Patient records, appointment scheduling.  
4. **HR Systems**: Employee data, payroll processing.  

**c) Database System vs. DBMS**  
- **Database System**: Includes data + software (DBMS) + users.  
- **DBMS**: Software that manages databases (e.g., MySQL, MongoDB).  

**d) 3 Common DBMS Software**  
1. **MySQL** (Relational)  
2. **MongoDB** (NoSQL)  
3. **Oracle Database** (Enterprise RDBMS)  

#### **Question 5: Database Concepts**  
**(i) Database Schema**  
Blueprint defining tables, fields, relationships (e.g., `CREATE TABLE` in SQL).  

**(ii) Client-Server Database**  
Architecture where clients request data from a central database server (e.g., web apps).  

**(iii) Logical View**  
How users/applications perceive data (e.g., tables in SQL, documents in MongoDB).  

**(iv) One-to-Many Relationship**  
One record in Table A links to multiple records in Table B (e.g., one customer → many orders).  

**(v) Denormalization**  
Intentionally adding redundancy to improve read performance (trade-off with update efficiency).  


#### **Question 6**  
**a) Steps to Design a Large Database System**  
1. **Requirement Analysis**: Identify business needs (e.g., entities like students, courses).  
2. **Conceptual Design**: Create ER diagrams to model relationships.  
3. **Logical Design**: Convert ER diagrams to schema (tables/collections).  
4. **Physical Design**: Optimize storage (indexes, partitioning).  
5. **Implementation**: Deploy using DDL commands.  

**b) STUDREC Table Operations**  
**i) DDL to Create Table (SQL)**  
```sql
CREATE TABLE STUDREC (
    MATRIC_NUM VARCHAR(10) PRIMARY KEY,
    NAME VARCHAR(50),
    LEVEL INT,
    DEPARTMENT VARCHAR(50),
    CGPA FLOAT
);
```

**ii) INSERT Command**  
```sql
INSERT INTO STUDREC VALUES 
('FUO/07063', 'SALAAM', 400, 'MATHS & COMP', 4.8),
('FUO/08001', 'LATEEFAT', 200, 'MICROBIOLOGY', 3.2);
```

**iii) SELECT for CGPA > 4.5**  
```sql
SELECT * FROM STUDREC WHERE CGPA > 4.5;
```

**MongoDB Equivalent**  
```javascript
db.STUDREC.find({ CGPA: { $gt: 4.5 } });
```

---
![[CPS 402 u.jpeg]]


#### **Question 1: Database Engine Comparison**  
**a) Preferred Database: MongoDB**  
**Justifications**:  
1. **Flexible Schema**: Adapts to changing data structures (e.g., adding new fields without altering tables).  
2. **Scalability**: Horizontal scaling via sharding for high-volume data.  
3. **JSON Support**: Native compatibility with modern web/app development.  

**b) MongoDB Technical Issues**  
1. **Memory Usage**: High RAM consumption for large datasets.  
2. **Joins**: Limited native join support (requires `$lookup` aggregation).  
3. **Transaction Complexity**: Multi-document ACID transactions are resource-intensive.  

**c) Recommended Database: Distributed**  
**Reasons**:  
1. **Fault Tolerance**: Data replicated across nodes ensures availability.  
2. **Performance**: Parallel processing reduces latency for global users.  
3. **Scalability**: Easily add nodes to handle growth.  

**d) Client-Server Database System**  
- **Definition**: Centralized database server processes requests from multiple clients (e.g., web browsers, mobile apps).  
- **How It Works**:  
  - **Clients** send queries (e.g., `SELECT * FROM students`).  
  - **Server** processes queries, returns results.  
- **Diagram**:  
  ```plaintext
  Clients → Network → Database Server → Storage
  ```

---

#### **Question 2: SQL Fundamentals**  
**a) SQL Overview**  
- **Purpose**: Standard language for managing relational databases (create, read, update, delete data).  

**b) DDL vs. DML**  

| **Type** | **Purpose**               | **Syntax Example**                     |  
|----------|---------------------------|---------------------------------------|  
| **DDL**  | Define schema             | `CREATE TABLE Students (id INT, ...);` |  
| **DML**  | Manipulate data           | `INSERT INTO Students VALUES (1, 'Alice');` |  

**c) University Database Operations**  
**i) DDL to Create Table**:  
```sql
CREATE TABLE STUDREC (
    MATRIC_NUM VARCHAR(10) PRIMARY KEY,
    NAME VARCHAR(50),
    LEVEL INT,
    DEPARTMENT VARCHAR(50),
    CGPA FLOAT
);
```

**ii) SELECT for CGPA > 4.5**:  
```sql
SELECT * FROM STUDREC WHERE CGPA > 4.5;
```

**iii) INSERT New Record**:  
```sql
INSERT INTO STUDREC VALUES 
('FUO/09023', 'MARXAM', 200, 'BIOCHEMISTRY', 3.97);
```

**iv) DELETE Record**:  
```sql
DELETE FROM STUDREC WHERE MATRIC_NUM = 'FUO/03033';
```

**v) Why Relational DBMS Dominates**:  
1. **ACID Compliance**: Ensures data integrity.  
2. **Standardization**: SQL is universally adopted.  
3. **Mature Ecosystem**: Robust tools (e.g., MySQL Workbench).  
4. **Complex Queries**: Efficient joins and aggregations.  
5. **Structured Data**: Ideal for business applications.  

#### **Question 3: Database System Architecture**  

**b) 5 Key Components & Functions**:  
1. **Query Processor**: Optimizes and executes SQL queries.  
2. **Database Manager**: Ensures ACID compliance (transactions).  
3. **File Manager**: Manages disk I/O (reads/writes).  
4. **Data Dictionary**: Stores metadata (table schemas).  
5. **Buffer Manager**: Caches frequently accessed data.  

**c) Database Manager Roles**:  
1. **Transaction Control**: Commit/rollback operations.  
2. **Concurrency Management**: Handles simultaneous user access.  
3. **Recovery**: Restores data after crashes using logs.  

---

