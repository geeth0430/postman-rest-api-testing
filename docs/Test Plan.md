# Test Plan - RESTful User API Testing

## 1. Document Information

| Item | Details |
|---|---|
| Project | RESTful User API Testing |
| Document | Test Plan |
| Version | 1.0 |
| Tool | Postman |
| API | ReqRes |
| Testing Type | API Functional Testing |
| Prepared By | Geeth |
| Date | 08 September 2026 |
| Status | Active |

---

## 2. Introduction

This test plan describes the approach used to test the RESTful User API using Postman.

The testing focuses on API functionality, status code validation, response validation, positive testing, negative testing, automated assertions, and defect reporting.

---

## 3. Testing Objectives

- Verify REST API functionality.
- Validate HTTP status codes.
- Validate JSON responses.
- Perform positive and negative testing.
- Validate response time.
- Create automated Postman assertions.
- Execute API test cases.
- Identify and document defects.
- Generate test execution and Newman reports.

---

## 4. Scope of Testing

### In Scope

- GET Users
- POST Create User
- PUT Update User
- DELETE User
- Invalid User testing
- Invalid Endpoint testing
- Status code validation
- Response body validation
- JSON validation
- Response time validation
- Postman automated assertions
- Collection Runner execution

### Out of Scope

- UI testing
- Mobile testing
- Performance/load testing
- Database testing
- Security penetration testing
- Production testing

---

## 5. Test Strategy

Both positive and negative testing will be performed.

### Positive Testing

Testing valid API requests such as:

- Retrieve users
- Create a user
- Update a user
- Delete a user

### Negative Testing

Testing invalid requests such as:

- Non-existing user
- Invalid endpoint
- Invalid authentication conditions where applicable

### Automated Testing

Postman JavaScript assertions will be used to validate status codes, response data, JSON format, and response time.

Example:

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

---

## 6. API Endpoints Under Test

| ID | Method | Endpoint | Purpose |
|---|---|---|---|
| TC-001 | GET | `/api/users?page=2` | Retrieve users |
| TC-002 | POST | `/api/users` | Create user |
| TC-003 | PUT | `/api/users/2` | Update user |
| TC-004 | DELETE | `/api/users/2` | Delete user |
| TC-005 | GET | `/api/users/999999` | Test invalid user |
| TC-006 | GET | `/api/invalidendpoint` | Test invalid endpoint |

---

## 7. Expected Results

| ID | Scenario | Expected Result |
|---|---|---|
| TC-001 | Get Users | 200 OK |
| TC-002 | Create User | 201 Created |
| TC-003 | Update User | 200 OK |
| TC-004 | Delete User | 204 No Content |
| TC-005 | Invalid User | 404 Not Found |
| TC-006 | Invalid Endpoint | Based on API documentation/authentication requirements |

---

## 8. Test Data

### Create User

```json
{
    "name": "Geeth",
    "job": "QA Engineer"
}
```

### Update User

```json
{
    "name": "Geeth Updated",
    "job": "Senior QA Engineer"
}
```

### Invalid User

```text
User ID: 999999
```

---

## 9. Test Environment

| Component | Details |
|---|---|
| Operating System | Windows |
| Testing Tool | Postman |
| API | ReqRes |
| Protocol | HTTPS |
| API Style | REST |
| Data Format | JSON |
| Execution | Postman Collection Runner |

---

## 10. Pass / Fail Criteria

### PASS

A test passes when:

- Expected status code is returned.
- Response structure is correct.
- Required data is present.
- All relevant assertions pass.

### FAIL

A test fails when:

- An unexpected status code is returned.
- Required data is missing.
- Response data is incorrect.
- An automated assertion fails.

### BLOCKED

A test is blocked when testing cannot continue because of issues such as:

- API unavailable
- Authentication problems
- Environment configuration problems

---

## 11. Defect Management

Confirmed defects will be documented in:

```text
Bug-Reports/
```

Each defect should include:

- Bug ID
- Title
- Endpoint
- HTTP method
- Steps to reproduce
- Expected result
- Actual result
- Severity
- Priority
- Status
- Evidence

---

## 12. Test Execution

The Postman collection will be executed using the Collection Runner.

Test cases:

```text
TC-001
TC-002
TC-003
TC-004
TC-005
TC-006
```

Execution results will be recorded in:

```text
Test-Reports/Test_Execution_Report.md
```

The automated Newman report will be stored in:

```text
Test-Reports/Newman_Report.html
```

---

## 13. Evidence

Testing evidence will be stored in:

```text
Screenshots/
```

Evidence may include:

- API request
- Request data
- Response status
- Response body
- Postman test results
- Defect screenshots

---

## 14. Test Deliverables

The main project deliverables are:

```text
README.md
Postman/User_API_Collection.json
Postman/User_API_Environment.json
Test-Cases/Test_Cases.xlsx
Bug-Reports/
Test-Reports/Test_Execution_Report.md
Test-Reports/Newman_Report.html
Screenshots/
docs/Test-Plan.md
```

---

## 15. Security

API keys, passwords, and other sensitive information must not be committed to GitHub.

Sensitive values should be managed using Postman environment variables.

---

## 16. Conclusion

This test plan provides a structured approach for testing REST APIs using Postman.

The project demonstrates practical SQA skills including API functional testing, positive and negative testing, automated assertions, test execution, defect reporting, evidence collection, and test reporting.