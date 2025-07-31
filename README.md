# 🧪 API Testing – ServeRest with Postman & Newman

> This repository contains automated API tests for the public **ServeRest.dev** API, written using **Postman** and executed via **Newman**, following best practices for test design, reporting, and GitHub documentation.

---

## 📌 Project Overview

| Item          | Description                                                                          |
|-------------  |--------------------------------------------------------------------------------------|
| **Platform**  | Public API ServeRest.dev                                                             |
| **Tools**     | Postman (for test creation), Newman (for CLI execution)                              |
| **Goal**      | Practice API automation with authentication, dynamic data, environments, and reports |

---

## 📁 Repository Structure

```bash
api-test-serverest/  
├── collections/  
│   └── ServeRest.postman_collection.json  
├── environments/  
│   └── Serverest_Dev.postman_environment.json  
├── reports/    
├── README.md  
└── package.json
```  

---

## 🚀 How to Run Tests

### Prerequisites
- Node.js installed

```bash
### Clone the repository

git clone https://github.com/marcusphillipe/postman-serverest-api-tests.git  
cd postman-serverest-api-tests

### Install Newman locally

npm install newman --save-dev

### Run basic test suite

npm run test:api

### Run with HTML report

npm run test:html

### Make sure your `package.json` includes:

"scripts": {
  "test:api": "newman run collections/ServeRest.postman_collection.json -e environments/Serverest_Dev.postman_environment.json",
  "test:html": "newman run collections/ServeRest.postman_collection.json -e environments/Serverest_Dev.postman_environment.json -r cli,html --reporter-html-export reports/report.html"
}
```

---

## ✅ Test Coverage

- User registration and login with Bearer Token  
- Full product CRUD (POST, GET, PUT, DELETE)  
- Cart creation, listing and cancellation  
- Status code, response message and performance validations  
- Dynamic data via Postman variables (`token`, `userId`, `productId`)  
- Use of pre-request scripts, conditional logic, and reusable environments  

---

## 📈 HTML Report

```bash
### To generate a visual HTML report using Newman:

npm run test:html

### Open it from your browser at:

reports/report.html
```

---

## 💡 Good Practices Applied

- Collections and environments are version-controlled (.json files)  
- CLI execution enabled via npm scripts  
- HTML reports allow clear test insights  
- Code uses reusable variables, performance thresholds, and status-based assertions  

---

## 👨‍💻 Author

Project developed for learning, professional growth, and showcasing QA automation skills.

**Marcus Phillipe**  
🔗 [LinkedIn](https://www.linkedin.com/in/marcusparamos/)  
📁 [GitHub Repo](https://github.com/marcusphillipe/postman-serverest-api-tests.git)

## 📬 Contributions

Suggestions and feedback are welcome!
