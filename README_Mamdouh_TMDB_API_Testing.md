<div align="center">

# 🎬 TMDB API Testing Project

**End-to-end API testing suite for The Movie Database (TMDB) API**  
Built and executed with Postman — from test design to automated assertions and defect reporting.

</div>

---

## 📌 Overview

This project is a complete **API Testing project** for the TMDB API, covering different API testing activities including request validation, automated assertions, environment management, collection execution, and defect identification.

The project was built to demonstrate practical hands-on skills in API testing using **Postman** and JavaScript-based test scripts.

**What this project shows:**

- ✅ API request and response validation
- ✅ Automated assertions using Postman's `pm.test`
- ✅ Authentication using Bearer Token
- ✅ Environment and variable management
- ✅ Validation of status codes, response structure, data types, and business rules
- ✅ Collection execution using Postman Runner
- ✅ Identification and documentation of failed test cases and defects

---

## 🗂️ Project Structure

```text
TMDB-API-Testing/
├── README.md
├── TMDB-API-Proj.postman_collection.json
├── TMDBEnv.postman_environment.json
├── bug-reports/
│   └── TMDB_Bug_Reports.xlsx
└── screenshots/
    └── Collection_Run_Results.png
```

> The environment file should not contain real credentials when uploaded to a public repository.

---

## 🎯 Test Scope

| Area | Endpoints / Features Covered |
|---|---|
| **Authentication** | Verify Authentication |
| **Search** | Search Movies by Keyword |
| **Search** | Search TV Shows by Name |
| **Movies** | Get Movie Details by Movie ID |
| **Movies** | Get Movie Credits (Cast & Crew) |
| **Movies** | Get Popular Movies |
| **Movies** | Get Now Playing Movies |
| **Movies** | Discover Movies by Genre |
| **TV Shows** | Get TV Show Details by ID |
| **People** | Get Person Details (Actor/Director) |
| **Account** | Get Account ID |
| **Watchlist** | Add Movie to Watchlist – First Request |
| **Watchlist** | Add Same Movie to Watchlist – Idempotency |

The project includes **multiple API testing scenarios** with automated assertions for response validation.

---

## ⚙️ Tech Stack

| Tool / Technology | Purpose |
|---|---|
| **Postman** | API request design, testing, scripting, and collection execution |
| **JavaScript** | Writing automated Postman test scripts |
| **TMDB API** | API under test |
| **Excel / Google Sheets** | Bug and defect reporting |
| **Git & GitHub** | Version control and project hosting |

---

## 🧪 Test Validations

The automated tests validate:

- HTTP status codes
- Response body structure
- Required response fields
- Data types
- Array validation
- Empty and non-empty response data
- Authentication behavior
- Movie and TV show details
- Cast and crew information
- Release date validation
- Watchlist request behavior
- API response business rules

Example Postman test:

```javascript
pm.test("Status code is 200 OK", function () {
    pm.response.to.have.status(200);
});
```

---

## 🚀 How to Run

### 1. Clone or download the project

Download the repository and open Postman.

### 2. Import the collection

Import:

- `TMDB-API-Proj.postman_collection.json`
- `TMDBEnv.postman_environment.json`

### 3. Configure the environment

Add your TMDB credentials and required variables.

Example variables:

```text
base_url
token
api_key
movie_id
series_id
person_id
account_id
```

### 4. Select the environment

Select **TMDB Environment** from the Postman environment selector.

### 5. Run the collection

Open the Postman Collection Runner and run the complete collection.

---

## 📊 Test Results

The latest collection execution produced the following results:

| Metric | Result |
|---|---|
| Total Tests | 65 |
| ✅ Passed | 61 |
| ❌ Failed | 4 |
| Errors | 0 |
| Average Response Time | 101 ms |
| Total Run Duration | 2.323 seconds |

### Collection Run Summary

```text
Total Tests: 65
Passed:      61
Failed:      4
Errors:      0
```

---

## 🐞 Failed Test Cases / Issues Found

The latest execution identified the following failed assertions:

| ID | Test Case / Issue | Status |
|---|---|---|
| BUG-001 | Movie Cast list is empty | Open |
| BUG-002 | TV Show Genres array is empty | Open |
| BUG-003 | Now Playing movie release date is outside the expected date range | Open |
| BUG-004 | Repeated Watchlist request returns `201` instead of expected `200` | Open |

### Example Failed Assertions

**BUG-001**

```text
Cast list is not empty
AssertionError: expected +0 to be above +0
```

**BUG-002**

```text
Genres array is not empty
AssertionError: expected +0 to be above +0
```

**BUG-003**

```text
Movie release dates are within valid date range
AssertionError: expected 2026-06-17T00:00:00.000Z
to be at least 2026-07-15T00:00:00.000Z
```

**BUG-004**

```text
Second request returns 200 OK
AssertionError: expected response to have status code 200 but got 201
```

> Some failed assertions may require further investigation to determine whether they represent actual API defects, test data issues, or test assertion/business-rule issues.

---

## 🔐 Security Note

No real API credentials should be committed to a public repository.

Before uploading the project to GitHub:

- Remove API keys
- Remove Bearer Tokens
- Clear sensitive environment variable values
- Use placeholders or empty values in the environment file

Example:

```json
{
    "key": "token",
    "value": "",
    "enabled": true
}
```

---

## 👨‍💻 About Me

**Mamdouh Abdelaziz** — Junior Software QA Engineer | ISTQB® CTFL Certified

Interested in:

- Manual Testing
- API Testing
- Database Testing
- Test Case Design
- Bug Reporting
- SQL
- Postman
- Java
- Agile / Scrum

Actively building hands-on QA projects to strengthen practical software testing skills.

📍 Egypt  

🔗 [LinkedIn](https://www.linkedin.com/in/mamdouh-abdelaziz180297/)  
📧 [mamdouhabdelaziz305@gmail.com](mailto:mamdouhabdelaziz305@gmail.com)

---

<div align="center">

⭐ If you found this project useful, feel free to explore the collection and test cases.

</div>
