# 🧪 API Testing with Apache JMeter – RESTful API Demo

This project demonstrates manual and automated **API testing using JMeter** against the public endpoint [https://api.restful-api.dev](https://api.restful-api.dev).
Developed as part of the **Digital Skola QA Bootcamp Batch 12** by **Putri Stephanie Lesilolo.**

---

## 📁 Project Structure
```
jmeterRestfulAPI/
├── jmeter_testplan_putristphn.jmx
├── report/
│   ├── html/
│   │   └── index.html
│   └── results.jtl
├── screenshots/
│    ├── post_body.png
│    ├── post_header.png
│    ├── get_body.png
│    ├── get_header.png
│    └── report_dashboard.png
└── README.md
```

--- 
  
## 🚀 Test Scenarios

| Method | Endpoint | Description |
|--------|-----------|--------------|
| POST | `/objects` | Create new object |
| GET | `/objects/{id}` | Retrieve object by ID |

---

## 🧰 Tools & Setup

- **Apache JMeter 5.6.3**
- **Java 21**
- **macOS Terminal**
- **Assertions:**
  - HTTP Response Code validation 
  - JSON Field Validation (`id`,`name`, `data.year`, `data.price`, `data.color`)
- Reports generated using JMeter CLI and HTML Dashboard

---

## 📊 Test Flow

1. **POST – Add Object**
   - Creates new object and extracts `id`
2. **PUT – Update Object**
   - Updates object using dynamic `${createdId}`
3. **GET – Validate Object**
   - Verifies updated data through assertions
4. **HTML Report**
   - Generated via command line:
     ```bash
     jmeter -n -t jmeter_testplan_putristphn.jmx -l report/results.jtl
     jmeter -g report/results.jtl -o report/html
     ```
5. **Open report**
   ```bash
   open report/html/index.html

--- 

## 🧠 Key Learnings

- Through this project, I practiced and strengthened:
- Designing modular API test plans using JMeter components.
- Writing Response & JSON Assertions for validation.
- Running JMeter tests via CLI mode and exporting HTML reports.
- Analyzing test performance and debugging failed samples.
- Differentiating between functional testing vs performance testing focus in APIs.

🧭 This exercise enhanced my understanding of backend validation, data accuracy, and automation-ready API testing.

---

## 👩🏻‍💻 Author

**Putri Stephanie Lesilolo**  
*Quality Assurance Engineer*  
📍 Jakarta, Indonesia  

🔗 [LinkedIn](https://www.linkedin.com/in/putrilesilolo/) | [GitHub](https://github.com/putristphn)
