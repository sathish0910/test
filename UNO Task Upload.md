[[_TOC_]]

# 1. Overview

## 1.1 Objective

UNO chatbot will helps users to know the pending task and update into database.

## 1.2 User Stories
1. As a user, I can download the excel template file in “UNO Template” document library.
2. As a user, I can upload the updated excel file in “Task Upload” document library.
3. As a power automate flow bot, I can get the data from excel file.

4. As a power automate flow bot, I can update the SQL “Task Master” table with excel data.


# 2. Solution architecture    
![UNO Task upload](C:\Users\esathi\OneDrive - Capgemini\Desktop\Projects\UNO\UNO Task upload.png)

## 2.1 Components

> List out the components in the diagram above in a table, including purpose, technology, hosting, etc

| Component name | Technology     | Hosting | Purpose                                                     |
| -------------- | -------------- | ------- | ----------------------------------------------------------- |
| File Storage   | SharePoint     | SaaS    | To upload the task through excel file.                      |
| Data Storage   | SQL            | SaaS    | To store the task related data into Task Master SQL  table. |
| Integration    | Power Automate | SaaS    | To update the excel data into SQL server.                   |

# 3. User Instructions
1. Go to [SharePoint](https://bayergroup.sharepoint.com/sites/026703/) and download the excel template file in “[UNO Template](https://bayergroup.sharepoint.com/sites/026703/UNO%20Templates/Forms/AllItems.aspx)” document library.

2. Update the task in excel file and with additional information.
   
   ![image-20221222153532766](C:\Users\esathi\AppData\Roaming\Typora\typora-user-images\image-20221222153532766.png)
   
   - Pending topic & Pending action - Please select the given in dropdown
     - Goal setting
     - Development Dialogue
     - Midyear Check-In
     - Contribution Statement
   - User time zone - Please select from the given in dropdown.
     - For reference please view the time zone in excel (2nd sheet).
   - Pending description - Please select from the given in dropdown.
   - Action deadline - Task deadline to be completed and please follow the time stamp format (mm/dd/yyyy HH:mm)
     - Example: 12/22/1889 15:00
   - Next contact date - When do you want to get remainder notification regarding to task pending and please select future date (i.e., tomorrow date or future date)and follow the time stamp format (mm/dd/yyyy HH:mm)
     - Example: 12/22/1889 15:00
   - Reminder status - By default "New"
   - Last D1 update date - Please enter today date and follow the time stamp format (mm/dd/yyyy HH:mm)
   - Bayer email - Enter your Bayer email.
   - Enable Delegation - By default "false"
   - Last notified - Please enter today date and follow the time stamp format (mm/dd/yyyy)
   - Task Id - Unique task id which is not available in SQL DB.
   
3. Upload back to the SharePoint in “[Task Upload](https://bayergroup.sharepoint.com/sites/026703/Tasks%20upload/Forms/AllItems.aspx)” document library.

# 4. Reference

1. SharePoint site - https://bayergroup.sharepoint.com/sites/026703/
2. SharePoint permission - https://bayergroup.sharepoint.com/sites/026703/_layouts/15/user.aspx
3. Excel template - https://bayergroup.sharepoint.com/sites/026703/UNO%20Templates/Forms/AllItems.aspx
4. Task uploads - https://bayergroup.sharepoint.com/sites/026703/Tasks%20upload/Forms/AllItems.aspx
5. Time zone - https://learn.microsoft.com/en-us/previous-versions/windows/embedded/ms912391(v=winembedded.11)
