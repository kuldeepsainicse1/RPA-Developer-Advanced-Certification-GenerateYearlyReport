# RPA-Developer-Advanced-Certification-GenerateYearlyReport

In this Certification for RPA Developer Advanced, you will create a UiPath automation that performs the steps below. 

To achieve this, you will use the REFrameWork as the starting template and follow the UiPath development best practices.

The solution has to be scalable, so create two separate projects (sub-processes):

One for the Dispatcher (add to queue);
Another one for the Performer (consume queue). 
Make sure you use a connection to an UiPath Orchestrator for testing.
Create Queue and update the name in Config.xlsx and Create ACME_Cred as Asset in Orchestrator with your username and password for ACME access.


Here are the steps performed by the Robot in the Dispatcher:

1. Log in to https://www.acme-test.com
2. On the landing page, Check for Dashboard, click Work Items menu. crape the data from the table displayed and add data with type as WI4 in array of DataRow.
3. For each row in the DataRow, Add a queue item containing the WIID
4. Close ACME System 1.


Steps performed by the Robot in the Performer:

1. Log in to https://www.acme-test.com.
2. For each Queue Item:
3. Open the Details page of the selected activity to retrieve the Vendor Tax ID.
4. Download Monthly Report section in the Reports menu. 
5. Fill in the Vendor TaxID and download ALL the corresponding monthly reports for 2020.
6. Group all the downloaded monthly reports into a single Excel yearly report with the “YearlyReport-2020-TAXID.xlsx” name
7. Upload the resulting Excel yearly report in the “Upload Yearly Report” section in the Reports menu.
8. Fill in the Vendor TaxID, set the year as 2020, and select the file on your hard drive. This will return a unique upload ID. Output: upload ID
9. Go back to Work Item Details and open Update Work Item
10. Set the status to “Completed”. Add the following comment: “Uploaded with ID [uploadID]” 

Note: Navigation can be achieved in multiple ways by the robot - choose whichever you find best.
