# Restful-Booker API Testing

Manual and automated API testing project for the Restful-Booker API (https://restful-booker.herokuapp.com), built as part of my QA portfolio.

## Tools Used
- Postman — manual test execution and collection design
- Newman — command-line automated test runner
- newman-reporter-htmlextra — HTML test reports
- Jira — bug tracking

## What's Included
- Restful-Booker.postman_collection.json — Postman collection covering all 10 endpoints (Ping, Auth, Get/Create/Update/Delete Booking)
- API_Testing_Test_Cases.xlsx — 48 test cases covering Functional, Input Validation, Security, Edge Case, and Non-Functional testing
- report.html — Newman automated test execution report

## How to Run

1. Install Node.js from nodejs.org
2. Install Newman: npm install -g newman newman-reporter-htmlextra
3. Run the collection: newman run Restful-Booker.postman_collection.json -r htmlextra --reporter-htmlextra-export report.html

## Bugs Found
| ID | Endpoint | Issue | Severity |
|----|----------|-------|----------|
| SCRUM-5 | GET /booking/{id} | Returns 404 despite ID appearing in booking list | Medium |
| SCRUM-6 | POST /auth | Returns 200 OK instead of 401 for invalid credentials | Medium |
| — | POST /booking | Missing required field causes 500 Internal Server Error instead of 400 | High |

## Author
Merna — Senior QA Engineer
