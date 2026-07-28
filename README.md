# 🚀 REST API Test Automation & Validation Suite

An open-source, automated **REST API Testing Repository** validating CRUD endpoints, HTTP status codes, JSON schema response structures, environment variables, and API performance metrics.

---

### 📌 Project Overview
This repository contains end-to-end automated test suites built using **Postman** and executed via **Newman CLI / Postman Runner**. It demonstrates industry-standard practices for API Quality Assurance, including dynamic assertion testing, data-driven testing, and JSON schema structural verification.

---

### 🛠️ Tech Stack & Tools
- **API Testing Client:** Postman
- **Scripting Language:** JavaScript (`pm.test`, `pm.expect`)
- **CLI Runner:** Newman CLI
- **Supported Formats:** REST, JSON, Multipart/form-data
- **CI/CD Integration:** GitHub Actions / CLI Execution

---

### 🧪 Key Testing Capabilities Covered

1. **CRUD Endpoint Validation:**
   - `POST` — Record creation, token generation, payload authorization.
   - `GET` — Retrieval of data records, pagination, query parameters.
   - `PUT` / `PATCH` — Partial & complete resource updates.
   - `DELETE` — Resource deletion and verifying subsequent 404 status.

2. **Assertions & Checks:**
   - **Status Code Verification:** `200 OK`, `201 Created`, `400 Bad Request`, `401 Unauthorized`, `404 Not Found`.
   - **Response Time & Latency Metrics:** Ensuring API response times stay below 500ms threshold.
   - **JSON Schema Validation:** Verifying data types, required fields, and nested JSON structures.
   - **Dynamic Environment Variables:** Auto-extracting Auth Tokens (`Bearer Token`) and saving IDs dynamically for chained requests.

---

### 💻 Sample Postman Test Scripts (JavaScript)

#### 1. Status Code & Response Time Validation
```javascript
pm.test("Status code is 200 OK", function () {
    pm.response.to.have.status(200);
});

pm.test("Response time is less than 500ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});
