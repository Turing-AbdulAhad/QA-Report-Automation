Documentation for QA Report Automation

Project Owner : Abdul Ahad Khan
Created Date : Aug 18, 2023
Project Overview:
This project is designed to automate the process of fetching, analyzing, and visualizing Quality Analysis scores from a Google Sheet. The results are then compiled into an informative email, complete with visual aids, and sent to the specified recipient. This automation ensures that the team is consistently updated on their performance metrics in a timely and efficient manner.
Key Features:
Google Sheets Integration: The script fetches data directly from a Google Sheet using the gspread library.
Data Analysis with Pandas: The data is processed and analyzed using the pandas library to derive meaningful insights.
Visualization with Matplotlib: The script generates bar charts to visually represent the data, making it easier to understand and interpret.
Email Notification: The results, along with the generated charts, are sent via email to the specified recipient.
Detailed Breakdown:
1. Setup and Authentication:
Necessary libraries are imported.
Google Sheets API scope is defined.
Service account credentials are loaded from a JSON key file.
Authentication with Google Sheets is established.
2. Data Extraction:
The specified Google Sheet is opened by its URL.
Data from the desired worksheet is fetched and converted into a Pandas DataFrame.
3. Data Analysis:
The data is filtered based on specific agents.
The current week, previous week, and current month are determined.
Average scores for the current week, previous week, and current month are calculated.
The number of audits conducted in the current month is determined.
Agents' scores are sorted for consistent plotting.
4. Data Visualization:
A bar chart is generated to display agents' average scores and the number of audits for the current month.
A comparison bar chart is created to compare scores from the previous month to the current month.
Both charts are saved as PNG files.
5. Email Compilation:
Profiles with scores below 85% for the current week are identified.
An HTML table is created for these profiles.
An email body is constructed, incorporating the analysis results and the HTML table.
The generated bar charts are attached to the email.
6. Email Sending:
The email is sent to the specified recipient using the SMTP protocol.
How to Use:
Ensure you have the necessary libraries installed.
Update the path to the JSON key file for Google Sheets API authentication.
Update the Google Sheet URL.
Specify the desired agents for filtering.
Update the email details (sender, recipient, SMTP server, etc.).
Run the script.
**An automatic Email with the data will be sent to the recipient every week on Friday at 11 PM IST.

Conclusion:
This automation script provides a streamlined way to keep the team updated on their Quality Analysis scores. By fetching data directly from Google Sheets, analyzing it, and sending out an informative email, the process becomes efficient and reduces manual intervention.
