# Appraisal Process Automation

RPA bot built on **AutomationEdge** to automate the employee appraisal workflow for HR. Deployed on the AutomationEdge T3 server and run automatically through the Scheduler.

## What it does
- Downloads appraisal forms submitted by employees
- Validates each form and flags errors
- Checks who has and hasn't submitted
- Sends reminder emails to employees with pending forms
- Sends error notification emails when something fails
- Generates manager-wise and weekly reports and emails them to managers

## Tools & Technologies
- AutomationEdge (Process Studio)
- AutomationEdge Server (T3) and Scheduler
- Java
- [Excel / Outlook or SMTP / other tools you used]

## Project Structure
| Folder / File | Purpose |
|---|---|
| `PR_HR_Apprasial.psp` | Main appraisal process |
| `PR_HR_Remainder.psp` | Reminder process |
| `WF_FormValidation.psw` | Validates appraisal forms |
| `WF_Check_Submission.psw` | Checks submission status |
| `WF_Emp_Reminder.psw` | Sends reminders to employees |
| `WF_Remainder_ErrorHandling.psw` | Handles errors in the reminder flow |
| `WF_Manager_Wised_Report.psw`, `WF_ManagerWiseReportSend.psw` | Builds and sends manager-wise reports |
| `WF_ReportsToManager.psw` | Sends reports to managers |
| `WF_WeeklyReport.psw` | Generates the weekly report |
| `WF_Mail.psw`, `WF_ErrorMail.psw` | Email and error notifications |
| `WF_SuccesProcess.psw` | Success handling |
| `Screenshots/` | Workflow and output screenshots |

## How to Run
1. Open AutomationEdge Process Studio and import this project (File > Import).
2. Update the email settings and file paths for your environment.
3. Set `PR_HR_Apprasial.psp` as the main process and run it.
4. In production, the process runs automatically through the AutomationEdge Scheduler.

## Deployment & Scheduling
- Published to the **AutomationEdge T3 server** and running there
- Configured with the AutomationEdge **Scheduler**, so no manual trigger is needed

| Process | Schedule |
|---|---|
| Appraisal form download & validation (`PR_HR_Apprasial`) | [e.g., daily at 10:00 AM] |
| Employee reminders (`PR_HR_Remainder`) | [e.g., every Monday at 9:00 AM] |
| Weekly report to managers (`WF_WeeklyReport`) | [e.g., every Friday at 5:00 PM] |

## Results
- Reduced manual effort by [X hours / X%] per appraisal cycle
- [Number of employees or managers covered]

## Note
All sample data is dummy data. No real employee information, server details, or credentials are included.

## Author
**Alok Godhankar**
RPA Developer | UiPath | Power Automate | Python | Java
