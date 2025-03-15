**Task 1:**   
Create a JMeter collection (**booking.jmx**): (Score: 10)  
● Add the following properties to the Header Controller:  
○ Accept: \*/\*  
● Login:  
○ URL: [https://restful-booker.herokuapp.com/auth](https://restful-booker.herokuapp.com/auth)  
○ Body:  
{  
"username": "admin",  
"password": "password123"  
}  
●  
Create Booking:  
○ URL: [https://restful-booker.herokuapp.com/booking](https://restful-booker.herokuapp.com/booking)  
○ Body:  
{  
"firstname": "Generate Random FirstName",  
"lastname": "Generate Random LastName",  
"totalprice": Generate random amount,  
"depositpaid": true,  
"bookingdates": {  
"checkin": "2024-01-01",  
"checkout": "2024-01-02"  
}  
}  
  
Search Booking:  
○ URL: [https://restful-booker.herokuapp.com/booking/<booking\_id&gt](https://restful-booker.herokuapp.com/booking/%3Cbooking_id&gt);  
Now, perform performance testing for the following scenario:  
  
**Scenario:**  
120,000 users over a 12-hour period log in, create a booking, and search for the  
booking.   
**Todo 1 (Score 15):**  
Find the throughput and perform a load test (you can limit the load test to a maximum of  
20 minutes to save time) to ensure the server can handle the load. Create a load test  
report.   
  
Use a Gaussian Random Timer (Deviation 2000ms, Constant delay 500ms). Do it in 3 step  
1st step: 5 min load  
2nd step: 10 min load  
3rd step: 20 min load  
**Todo 2 (Score 15):**  
If the load test passes, identify the bottleneck throughput by conducting a stress test.  
Create a stress test report. (Step is not mentioned because try to breakdown the server in several steps to gradually increase the users for create booking.)  
**Todo 3 (Score 10):**  
Generate an HTML report for both the load test and the stress test. Also add the steps for both load test and stress test into 2 excel tab named load test report, stress test report. (If you want replace previous generated report, delete the Report folder and log file to generate new report)  
   
  
**Task 2:**  
From the dmoney API collection, create another JMeter collection (**dmoney.jmx**) for the  
following scenario: (Score: 50)  
  
**Scenario:**  
○ 5 agents perform deposits for 10 customers.  
○ 5 customers send money to another 10 customers.  
○ 5 customers make payments to 2 merchants.  
  
*HINT:*  
Log in as an admin once and generate a token to use for each of the threads. **Create 3 threads** for each type of  
transaction and set up agent, customer, and merchant accounts in 3 different CSV files  
(e.g., **deposit.csv**, **sendMoney.csv** and **payment.csv**).   
The amount must be dynamic using the Random Variable Controller. Use small amounts so that balance can't become empty. Each thread should have a ramp-up time of 120 seconds. Must add assertion to ensure that all transactions are successful.  
  
**Submission Process:**  
1\. Upload your folder to GitHub. The folder must include the following files:  
○ booking.jmx  
○ dmoney.jmx  
Resources:  
  ○ deposit.csv  
  ○ sendMoney.csv  
  ○ payment.csv  
booking-api-test-report.xlsx  
  
2\. Add dmoney.jtl and the HTML report folder to .gitignore.  
3\. Write the necessary information in the README.md file, including what you have done,  
prerequisites, and instructions on how to run the tests.  
4\. For Question 1, Add the screenshots of the request summary, statistics from the generated HTML, and the two reports (load test  
and stress test from the excel file) in the README.md  
5\. For Question 2, add only the screenshots of the request summary and statistics from  
the generated HTML report. No need to write steps in excel as we are not performing performance test here.
