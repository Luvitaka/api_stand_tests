# API Test Automation | Urban Grocers

## Project Description

This project was completed as part of the **QA Engineer Bootcamp** during the **Introduction to Test Automation** module.

The objective was to automate API testing for the **Urban Grocers** application using Python and the Requests library. The project focuses on validating the **Create Kit** endpoint by executing positive and negative test scenarios based on a predefined checklist.

The automation creates a new user, retrieves the authentication token, and uses it to create product kits while verifying the API behavior under different input conditions.

---

## Objectives

- Automate REST API testing using Python.
- Send GET and POST requests with the Requests library.
- Validate API responses using Pytest assertions.
- Apply positive and negative test design techniques.
- Organize automation code following a modular project structure.

---

## Technologies Used

- Python 3
- PyCharm
- Pytest
- Requests
- REST API
- JSON
- Git
- GitHub

---

## Project Structure

```text
qa-project/
│
├── configuration.py
├── data.py
├── sender_stand_request.py
├── create_kit_name_kit_test.py
└── README.md
```

### File Description

| File | Purpose |
|------|---------|
| `configuration.py` | Stores the base URL and API endpoints. |
| `data.py` | Contains request headers and request bodies used during testing. |
| `sender_stand_request.py` | Implements reusable API request functions. |
| `create_kit_name_kit_test.py` | Contains all automated test cases for the Create Kit endpoint. |

---

## Test Scenarios

The automated tests validate the **name** field when creating a product kit.

### Positive Tests

- Name with 1 character
- Name with 511 characters
- Special characters
- Spaces
- Numeric values

Expected Result:

- HTTP Status Code **201**
- Response body contains the same **name** value sent in the request

### Negative Tests

- Empty name
- Name longer than 511 characters
- Missing name parameter
- Incorrect data type (integer)

Expected Result:

- HTTP Status Code **400**

---

## Test Workflow

Each automated test performs the following steps:

1. Create a new user.
2. Retrieve the authentication token.
3. Send a request to create a new product kit.
4. Validate the response status code.
5. Verify the response body when applicable.

---

## Running the Tests

Clone the repository:

```bash
git clone <repository-url>
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run all tests:

```bash
pytest
```

Or execute the specific test file:

```bash
pytest create_kit_name_kit_test.py
```

---

## Skills Demonstrated

- API Test Automation
- REST API Testing
- Test Case Design
- Positive and Negative Testing
- Authentication Token Handling
- JSON Request Validation
- Assertions with Pytest
- Modular Test Architecture
- Python Functions
- Code Reusability
- Version Control with Git

---

## Learning Outcomes

Through this project, I gained hands-on experience designing and automating API tests using Python and Requests. I learned how to work with authentication tokens, build reusable request functions, organize test data, and implement maintainable automated tests following QA best practices.

---

## Author

**Karina Luvianos**
QA Engineer | Career Switcher
