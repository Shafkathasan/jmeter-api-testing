# JMeter Booking & Dmoney API Tests

### This repository contains JMeter scripts for performance testing a booking API (Task 1) and functional testing for a Dmoney API (Task 2).

---

## 📋 Description

- **Task 1 (Booking API)**:
  - Load & stress testing for 120,000 users over 12 hours (simulated in 20 minutes).
  - Generates HTML reports and Excel summaries for throughput, response times, and bottlenecks.
- **Task 2 (Dmoney API)**:
  - Simulates agents, customers, and merchants performing deposits, money transfers, and payments.
  - Uses CSV files for data-driven testing with dynamic amounts and assertions.

---

## 🛠 Prerequisites

- **JMeter 5.6+** ([Download](https://jmeter.apache.org/download_jmeter.cgi))
- **Java 8+** (Required for JMeter)
- **Git** (Optional, for cloning the repo)
- **Excel** (Optional, for viewing test reports)

---

## 🚀 Steps to Run

### **Task 1: Booking API Performance Tests**

1. **Clone the repo**:

   ```bash
   git clone https://github.com/Shafkathasan/jmeter-api-testing.git
   ```

2. **Run Load Test (20 minutes)**:

   ```bash
   jmeter -n -t A03_Booking_b14.jmx -l A03_Booking_b14.jtl -e -o LoadReport
   ```

3. **Run Stress Test**:
   ```bash
   jmeter -n -t A03_Booking_b14.jmx -l A03_Booking_b14.jtl -e -o StressReport
   ```
4. **View Reports**:

- Open `LoadReport/index.html` or `StressReport/index.html`.
- Update `A03_Booking_Api_Test_Report.xlsx` manually with metrics.

### **Task 2: Dmoney API Functional Tests**

1. **Run the test**:

   ```bash
   jmeter -n -t A03_dmoney_b14.jmx -l A03_dmoney_b14.jtl -e -o DmoneyReport
   ```

2. **View Report**:

- Open `DmoneyReport/index.html`.

---

## 📸 Reports Screenshots

#### Task 1: Booking API

**Load Test Report**
![LoadTest_20250311_162237_chrome](https://github.com/user-attachments/assets/f3a27796-51c7-48a3-9e23-d6ef97a99e7c)

**Stress Test Report**
![StressTest_20250315_152446_chrome](https://github.com/user-attachments/assets/22198f5d-4823-4a4e-af91-2f9e27833c72)

#### Task 2: Dmoney API

**Request Summary**
![Assignment-on-Jmeter-B14-DmoneyReport-2025-03-15-15_19_28](https://github.com/user-attachments/assets/0868374b-b203-4355-8864-1ee50e8b5b99)

---

## 🖥 Technology Used
- JMeter - Performance & functional testing.
- Java - Runtime environment for JMeter.
- GitHub - Version control & hosting.
- CSV - Data-driven test inputs.

---

## 📝 Notes
- .gitignore: Excludes `*.jtl`, `Reports/`, and `SS/`.
- Excel Reports: Update manually from HTML metrics.
- CSV (text format) UserIDs are created with Postman
- If Agents can't deposit because of insufficient balance create new Agents with Postman
