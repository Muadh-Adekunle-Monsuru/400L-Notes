![[Pasted image 20231212094514.png]]
### **1. Users & Interfaces**  
- **Application Users**: Use front-end applications (e.g., web/mobile apps) that indirectly access the database.  
- **Application Interfaces**: GUIs or APIs that translate user actions into database queries.  
- **Database Administrator (DBA)**: Manages schema, security, and performance via DDL (e.g., `CREATE TABLE`).  

---

### **2. Application Layer**  
- **Application Program**: Contains business logic and embeds DML (e.g., SQL `INSERT`, `SELECT`) for data operations.  
- **DML Precompiler**:  
  - Translates embedded SQL in application code into executable calls.  
  - Checks syntax and validates queries before execution.  

---

### **3. Core Database Modules**  
- **Query Processor**:  
  - **Parses** and **optimizes** queries (e.g., `SELECT * FROM users`).  
  - Generates efficient execution plans using indexes and statistics.  
- **DDL Compiler**:  
  - Processes schema definitions (e.g., `CREATE TABLE`).  
  - Updates metadata in the **Data Dictionary**.  
- **Database Manager**:  
  - Coordinates transactions (ensures ACID properties).  
  - Manages buffers and interfaces with the **File Manager**.  
- **File Manager**:  
  - Handles physical storage (reads/writes data to disk).  
  - Manages space allocation for tables/indexes.  

---

### **4. Storage Layer**  
- **Data Files**: Store actual data (e.g., rows of a table).  
- **Disk Storage**: Physical hardware where data persists.  
- **Data Dictionary**:  
  - Metadata repository (table schemas, constraints, user permissions).  
  - Used by all modules for validation and optimization.  

---

### **Key Interactions**  
1. **Application Flow**:  
   - User → Application Interface → DML Precompiler → Query Processor → Database Manager → File Manager → Data Files.  
2. **Admin Flow**:  
   - DBA → DDL Compiler → Updates Data Dictionary → Schema changes propagate to storage.  

---

### **Summary of Functions**  
| **Module**           | **Role**                                                             |
| -------------------- | -------------------------------------------------------------------- |
| **DML Precompiler**  | Translates embedded SQL into executable calls.                       |
| **Query Processor**  | Optimizes and executes queries (e.g., joins, filters).               |
| **DDL Compiler**     | Defines/modifies database schemas (metadata).                        |
| **Database Manager** | Ensures transaction integrity (ACID) and memory buffering.           |
| **File Manager**     | Manages physical data storage on disk.                               |
| **Data Dictionary**  | Stores metadata (schemas, indexes, users) for system-wide reference. |

---

### **Why This Matters**  
This modular design ensures:  
- **Efficiency**: Optimized query execution and storage.  
- **Security**: Controlled access via the DBA and Data Dictionary.  
- **Flexibility**: Supports both ad-hoc queries (native users) and application-driven operations.  

For example, when an app user submits a form:  
1. The **DML Precompiler** converts the app’s SQL into a call.  
2. The **Query Processor** picks the fastest path to retrieve data.  
3. The **Database Manager** fetches results from disk (via **File Manager**) and returns them.  
