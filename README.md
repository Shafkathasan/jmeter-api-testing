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
- Update `A03 Booking Api Test Report.xlsx` manually with metrics.

### **Task 2: Dmoney API Functional Tests**

1. **Run the test**:

   ```bash
   jmeter -n -t A03_dmoney_b14.jmx -l A03_dmoney_b14.jtl -e -o DmoneyReport
   ```

2. **View Report**:

- Open `DmoneyReport/index.html`.

---

## 📸 Screenshots

#### Task 1: Booking API

**Load Test Report**

**Stress Test Report**

#### Task 2: Dmoney API

**Request Summary**
