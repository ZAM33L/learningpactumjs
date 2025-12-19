# learningpactumjs

A learning and practice repository for **API testing using PactumJS**. This project contains simple, incremental examples to understand how PactumJS works for validating REST APIs, handling test data, using templates, and generating reports.

---

## 📌 Purpose of This Repository

This repository is meant for **revision and hands‑on learning** of PactumJS concepts, including:

* Writing basic API tests
* Using Pactum `spec()` for requests and assertions
* Managing test data using JSON files
* Using **stash & data templates**
* Generating test execution reports

It is ideal for anyone starting with **API automation testing in Node.js**.

---

## 🧰 Tech Stack

* **Node.js**
* **PactumJS** (API testing library)
* **JavaScript**
* **Mocha/Jest** (test runner – depending on setup)

---

## 📁 Project Structure

```
learningpactumjs/
│
├── testsPactum01/        # PactumJS test cases
│   └── *.js              # API test files
│
├── data/                 # Test data & templates (JSON)
│   └── *.json
│
├── reports/              # Test execution reports
│
├── db1.json               # Sample/mock data file
├── package.json           # Project dependencies & scripts
├── package-lock.json      # Dependency lock file
└── .gitignore             # Ignored files
```

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/ZAM33L/learningpactumjs.git
cd learningpactumjs
```

### 2️⃣ Install Dependencies

```bash
npm install
```

### 3️⃣ Run Tests

```bash
npm test
```

(or use the script defined in `package.json`)

---

## 🧪 What You Will Learn

* Creating API tests using `spec()`
* Validating:

  * Status codes
  * Response body
  * JSON fields
* Using **stash** for sharing data across tests
* Loading **data templates** from JSON files
* Structuring test cases cleanly
* Viewing test execution reports

---

## 🧠 Example Pactum Test

```js
const { spec } = require('pactum');

it('should return 200 status', async () => {
  await spec()
    .get('https://jsonplaceholder.typicode.com/posts/1')
    .expectStatus(200)
    .expectJsonLike({ id: 1 });
});
```

---

## 📚 Reference

* PactumJS Documentation: [https://pactumjs.github.io/](https://pactumjs.github.io/)

---


Happy Testing 🚀
