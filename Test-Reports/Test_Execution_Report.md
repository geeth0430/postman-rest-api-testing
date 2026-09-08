# 🧪 API Test Execution Report

## 📌 Project Information

| Item | Details |
|---|---|
| Project | RESTful User API Testing |
| Tool | Postman |
| API | ReqRes |
| Tester | Geeth |
| Date | 08 September 2026 |

## 📊 Test Summary

| Metric | Result |
|---|---:|
| Total Test Cases | 6 |
| ✅ Passed | 5 |
| ❌ Failed | 1 |
| Pass Rate | 83.33% |

## 🔎 Test Results

| ID | Test Scenario | Expected | Actual | Result |
|---|---|---:|---:|---|
| 🔍 TC-001 | Get Users | 200 | 200 | ✅ PASS |
| 👤 TC-002 | Create User | 201 | 201 | ✅ PASS |
| ✏️ TC-003 | Update User | 200 | 200 | ✅ PASS |
| 🗑️ TC-004 | Delete User | 204 | 204 | ✅ PASS |
| ⚠️ TC-005 | Invalid User | 404 | 404 | ✅ PASS |
| 🚫 TC-006 | Invalid Endpoint | 404 | 401 | ❌ FAIL |

## 🐞 Defect

**BUG-001 — Invalid Endpoint**

- Expected: `404 Not Found`
- Actual: `401 Unauthorized`
- Severity: Medium
- Priority: Medium
- Status: Open / Needs Verification

Details: `Bug-Reports/BUG-001.md`

## 🎯 Testing Covered

- GET, POST, PUT and DELETE APIs
- HTTP status code validation
- JSON response validation
- Positive testing
- Negative testing
- Postman automated assertions
- Bug reporting

## 📸 Evidence

```text
Screenshots/
├── BUG-001.png
├── TC-001-Get-Users.png
├── TC-002-Create-User.png
├── TC-003-Update-User.png
├── TC-004-Delete-User.png
├── TC-005-Get-Invalid-User.png
└── TC-006-Invalid-Endpoint.png
```

## 🏁 Conclusion

**6 test cases** were executed.

**5 passed** and **1 failed**.

TC-006 failed because the invalid endpoint returned `401 Unauthorized` instead of the expected `404 Not Found`. The issue is documented as **BUG-001** and requires further verification.

**Overall Status:** ⚠️ Partially Passed