1. Error, fault and failure are often used interchangeably with a diffused meaning, discuss them
**1. Error:**
*   **Definition:** An *error* is a human action that results in a system containing a *fault*.
*   **Source:** Errors are made by people (developers, designers, testers, operators, etc.)
*   **Examples:**
    *   A programmer writing the wrong operator in a conditional statement (e.g., using `<` instead of `<=`).
*   **Key Characteristic:** It is the *cause* of the issue. The error *introduces* the problem into the system.

**2. Fault:**
*   **Definition:** A *fault* (also called a *defect* or a *bug*) is a static condition in a system that can cause a system to fail to perform its required function. It is an anomaly in the code, data, or documentation.
*   **Origin:** Faults are the *result* of errors.
*   **Examples:**
    *   Incorrect code in a software program.
    *   Missing or incorrect data in a database.
*   **Key Characteristic:** The fault is a *manifestation* of the error, representing the actual problem within the system. A fault does not always lead to failure.

**3. Failure:**
*   **Definition:** A *failure* occurs when the system deviates from its specified or expected behavior. This occurs when a *fault* is exercised under particular conditions.
*   **Origin:** Failures are the *result* of a *fault* being activated.
*   **Examples:**
    *   The system giving the wrong answer to a query.
    *   The system taking much longer to process a request than specified.
*   **Key Characteristic:** A failure is an *observable event*. It's what the user or operator experiences when the system isn't working correctly.

**Summary in a Table:**

| Term    | Definition                                                | Source          | Manifestation                    | Observable Event |
| ------- | --------------------------------------------------------- | --------------- | -------------------------------- | ---------------- |
| Error   | Human action resulting in a fault                         | Human           | N/A                              | NO               |
| Fault   | An anomaly in the system that can cause failure.          | Error           | Incorrect code, data, etc.       | Potentially      |
| Failure | Deviation from specified/expected behavior due to a fault | Fault Activated | System malfunction, wrong result | YES              |

---
![[403 TEST 2023.jpeg]]