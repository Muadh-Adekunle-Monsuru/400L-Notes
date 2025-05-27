# Understanding MongoDB and NoSQL Databases

## Student Management System Implementation Guide

---

## Slide 1: What is MongoDB?

- A NoSQL database that stores data in JSON-like documents
- Flexible schema - documents in a collection can have different fields
- Scalable and high-performance
- Perfect for applications with changing data requirements

---

## Slide 2: NoSQL vs Traditional Databases

### NoSQL Databases:

- Schema-less/flexible schema
- Horizontally scalable
- Better for unstructured data
- Examples: MongoDB, Cassandra, Redis

### Traditional (SQL) Databases:

- Fixed schema
- Vertically scalable
- Better for complex queries
- Examples: MySQL, PostgreSQL

---

## Slide 3: MongoDB Basic Concepts

- **Database**: Container for collections
- **Collection**: Group of documents (like SQL tables)
- **Document**: Individual record (JSON-like)
- **Field**: Key-value pair in a document

Example Document:

```json
{
	"_id": "507f1f77bcf86cd799439011",
	"firstName": "John",
	"lastName": "Doe",
	"email": "john@example.com"
}
```

---

## Slide 4: Prisma Overview

### What is Prisma?

- Modern database toolkit
- Type-safe database access
- Auto-generated query builder
- Schema-first development approach

### Benefits:

- Better TypeScript integration
- Simplified database operations
- Reduced boilerplate code
- Automatic migrations

---

## Slide 5: Project Implementation

### Schema Definition (Prisma vs MongoDB)

#### Prisma Schema:

```prisma
model Student {
  id          String   @id @default(auto()) @map("_id") @db.ObjectId
  firstName   String
  lastName    String
  email       String
  courses     String[]
}
```

#### Regular MongoDB:

```javascript
{
  firstName: String,
  lastName: String,
  email: String,
  courses: Array
}
```

---

## Slide 6: Common Methods Used in Project

### Create Operations:

```typescript
// Using Prisma
await prisma.student.create({
	data: {
		firstName: 'John',
		lastName: 'Doe',
	},
});

// Regular MongoDB
db.students.insertOne({
	firstName: 'John',
	lastName: 'Doe',
});
```

---

## Slide 7: Query Operations

### Reading Data:

```typescript
// Using Prisma
const student = await prisma.student.findUnique({
	where: { id: studentId },
});

// Regular MongoDB
db.students.findOne({ _id: ObjectId(studentId) });
```

---

## Slide 8: Project Setup Steps

1. Install dependencies:

```bash
npm install @prisma/client prisma
```

2. Initialize Prisma:

```bash
npx prisma init
```

3. Configure MongoDB connection:

```env
DATABASE_URL="mongodb+srv://username:password@cluster.mongodb.net/database"
```

4. Generate Prisma Client:

```bash
npx prisma generate
```

---

## Slide 9: Project Structure

### Key Components:

```
prisma/
  ├── schema.prisma    # Database schema
lib/
  ├── actions.ts       # Server actions
  └── client.ts        # Prisma client
app/
  ├── students/        # Student management
  └── courses/         # Course management
```

---

## Slide 10: Key Features Implemented

1. Student Management

   - Registration
   - Profile updates
   - Course enrollment

2. Course Management

   - Course creation
   - Student enrollment
   - Course listing

3. Dashboard
   - Statistics
   - Recent registrations
   - Active courses

---

## Slide 11: Best Practices

1. Use Prisma's type safety
2. Implement error handling
3. Keep schema definitions clean
4. Use environment variables
5. Regular database backups
6. Implement proper indexing

---

## Slide 12: Resources

- [MongoDB Documentation](https://docs.mongodb.com/)
- [Prisma Documentation](https://www.prisma.io/docs/)
- [Next.js Documentation](https://nextjs.org/docs)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)

---

## Slide 13: Actual Project Schema Implementation

```prisma
model Student {
  id          String   @id @default(auto()) @map("_id") @db.ObjectId
  address     String
  firstName   String
  lastName    String
  email       String
  semester    String
  middleName  String
  matricNo    String
  phone       String
  dateOfBirth DateTime
  gender      String
  city        String
  state       String
  program     String
  createdAt   DateTime @default(now())
  courses     String[]
}

model Courses {
  id          String    @id @default(auto()) @map("_id") @db.ObjectId
  title       String    
  code        String?
  credits     String?
  semester    String?
  department  String?
  students    String[]
  createdAt   DateTime  @default(now())
}
```

---

## Slide 14: Server Actions Implementation

### Student Registration:
```typescript
export async function registerStudent(values: any) {
  const res = await prisma.student.create({
    data: {
      ...values,
    },
  });
}
```

### Course Management:
```typescript
export async function addCourse(courseId: string, studentId: string) {
  const student = await prisma.student.findUnique({
    where: {
      id: studentId,
    },
  });

  const res = await prisma.student.update({
    where: {
      id: studentId,
    },
    data: {
      courses: [...(student?.courses || []), courseId],
    },
  });
  return res;
}
```

---

## Slide 15: CRUD Operations Implementation

### Update Operation:
```typescript
export async function updateStudent(id: string, values: any) {
  const res = await prisma.student.update({
    where: {
      id,
    },
    data: {
      ...values,
    },
  });
  return res;
}
```

### Delete Operation:
```typescript
export async function deleteStudent(id: string) {
  const res = await prisma.student.delete({
    where: {
      id,
    },
  });
  return res;
}
```

---

## Slide 16: Course Management Implementation

### Course Creation:
```typescript
export async function createCourse(values: any) {
  const res = await prisma.courses.create({
    data: {
      ...values,
    },
  });
  return res;
}
```

### Drop Course:
```typescript
export async function dropCourse(courseId: string, studentId: string) {
  const student = await prisma.student.findUnique({
    where: {
      id: studentId,
    },
  });

  const updatedCourses = (student?.courses || []).filter(
    (id) => id !== courseId
  );

  const res = await prisma.student.update({
    where: {
      id: studentId,
    },
    data: {
      courses: updatedCourses,
    },
  });
  return res;
}
```

---

## Slide 17: Project Setup in Action

### Prisma Client Setup:
```typescript
// filepath: lib/client.ts
import { PrismaClient } from '@prisma/client';

const globalForPrisma = globalThis as unknown as {
  prisma: PrismaClient | undefined;
};

export const prisma = globalForPrisma.prisma ?? new PrismaClient();

if (process.env.NODE_ENV !== 'production') globalForPrisma.prisma = prisma;
```

---

## Slide 18: Key Differences from Traditional MongoDB

1. Type Safety:
   - Prisma provides TypeScript interfaces
   - Automatic type generation
   - Compile-time error checking

2. Query Building:
   - Prisma: Structured, type-safe queries
   - MongoDB: Raw queries with more flexibility but less safety

3. Schema Management:
   - Prisma: Centralized schema definition
   - MongoDB: Optional schema validation

4. Relationships:
   - Prisma: Built-in relationship handling
   - MongoDB: Manual relationship management
---
# Common Challenges in Creating and Running the Student Management System

## Database Configuration Challenges

1. **MongoDB Connection Issues**
- Connection string format errors
- Network connectivity problems
- Authentication failures

```env
DATABASE_URL="mongodb+srv://<username>:<password>@cluster.mongodb.net/database?retryWrites=true&w=majority"
```

2. **Prisma Setup Issues**
- Schema synchronization errors
- Client generation problems
```bash
# Common error resolution steps
npx prisma generate
npx prisma db push
```

## Type Safety Challenges

1. **TypeScript Integration**
```typescript
// Common type error in actions.ts
// Incorrect
export async function registerStudent(values: any) // avoid using 'any'

// Correct
export async function registerStudent(values: StudentFormValues) {
  // ...existing code...
}
```

2. **Schema Type Mismatches**
```prisma
// Common schema issues
model Student {
  dateOfBirth DateTime // Often received as string from forms
  courses     String[] // Array handling can be tricky
}
```

## Performance Issues

1. **Query Optimization**
```typescript
// Inefficient query
const student = await prisma.student.findMany({
  include: { courses: true }
});

// Optimized query
const student = await prisma.student.findMany({
  select: {
    id: true,
    firstName: true,
    courses: true
  }
});
```

2. **Connection Pooling**
```typescript
// Add connection pooling configuration
const prisma = new PrismaClient({
  connectionPool: {
    min: 2,
    max: 10
  }
});
```

## Error Handling Challenges

```typescript
// Better error handling implementation
export async function registerStudent(values: StudentFormValues) {
  try {
    const res = await prisma.student.create({
      data: values,
    });
    return { success: true, data: res };
  } catch (error) {
    if (error instanceof PrismaClientKnownRequestError) {
      // Handle Prisma-specific errors
      return { success: false, error: 'Database operation failed' };
    }
    return { success: false, error: 'Unknown error occurred' };
  }
}
```

## Environment Setup Issues

1. **Development vs Production**
```bash
# Development environment setup
npm run dev
# Production build issues
npm run build
```

2. **Environment Variables**
```env
NODE_ENV=development
DATABASE_URL=...
# Must be added to both .env and .env.local
```

## Data Validation Challenges

```typescript
// Implementation of proper validation
import { z } from 'zod';

const StudentSchema = z.object({
  firstName: z.string().min(2),
  email: z.string().email(),
  dateOfBirth: z.date(),
  // ...other fields
});
```

## Deployment Challenges

1. **Build Process**
```json
{
  "scripts": {
    "postinstall": "prisma generate",
    "build": "next build",
    "start": "next start"
  }
}
```

2. **Database Migration**
```bash
# Generate migration
npx prisma migrate dev --name init

# Apply migration in production
npx prisma migrate deploy
```

These challenges require careful consideration during development and deployment phases.