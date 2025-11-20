# Analyze event logs with NotebookLM

## Scenario
You're a junior security analyst, an entry-level professional responsible for monitoring networks and investigating security incidents. Your system has flagged some unusual activity. Your task is to review the following simplified log data to identify potential threats or policy violations.

You'll be using `NotebookLM`, an AI-powered tool, to help you with this investigation. It can assist you in sifting through data to find key patterns and anomalies, just like a modern analyst would.

## Goal
Analyze the log data below, identify any suspicious events, and use your findings to answer the questions.

## Instructions
1. `Copy the Log Data:` Copy all of the text in the code block below.

2. `Launch NotebookLM:` Navigate to https://notebooklm.google.com/

3. `Create a new Notebook:` Click on Create new notebook

4. `Create a new Document:` Paste the log data below into a new document in NotebookLM.

5. `Investigate with the AI:` Think like a detective. Ask NotebookLM questions to help you understand the data. Some good starting prompts might be:
a. "What do these logs tell me about user activity?"

b. "Can you identify any events that seem out of the ordinary?"

c. “Based on a security perspective, what are the most concerning log entries and why?"

 Log File: system_activity_log_2025-07-30.txt
 TIMESTAMP            | USER          | SOURCE_IP        | EVENT_TYPE         | DETAILS
---------------------|---------------|------------------|--------------------|--------------------------------------------
2025-07-30 08:00:15  | admin         | 192.168.1.1      | Login_Success      | User 'admin' logged in from internal network
2025-07-30 08:05:30  | John.Doe      | 192.168.1.5      | File_Access        | Opened: /documents/report_draft.docx
2025-07-30 08:10:45  | jane.smith    | 192.168.1.10     | Email_Sent         | To: allstaff@company.com, Subject: Important Update
2025-07-30 08:15:00  | guest         | 10.0.0.100       | Login_Failed       | User 'guest' attempted login from unknown IP (1 attempt)
2025-07-30 08:15:05  | guest         | 10.0.0.100       | Login_Failed       | User 'guest' attempted login (2 attempts)
2025-07-30 08:15:10  | guest         | 10.0.0.100       | Login_Failed       | User 'guest' attempted login (3 attempts)
2025-07-30 08:20:20  | John.Doe      | 192.168.1.5      | File_Access        | Copied: /finance/budget_2026_final.xlsx to /public_share
2025-07-30 08:25:35  | system        | N/A              | Service_Status     | Web server (Apache) is running.
2025-07-30 08:30:40  | admin         | 203.0.113.25     | Login_Success      | User 'admin' logged in from external IP (unusual location)
2025-07-30 08:35:50  | mary.jones    | 192.168.1.12     | File_Deletion      | Deleted: /personal/vacation_photos.jpg
2025-07-30 08:40:05  | system        | N/A              | Software_Update    | Antivirus

-----
1. According to my analysis with NotebookLM, `2025-07-30 08:20:20  | John.Doe      | 192.168.1.5      | File_Access        | Copied: /finance/budget_2026_final.xlsx to /public_share` log entry is the most suspicious and require immediate escalation.

2. These two separate log entries, `Successful Login by 'admin' from an Unusual External Location` and  `Copying a Financial File to a Public Share`, when combined, indicate a potential account compromise.

3.Based on NotebookLM analysis, all three Login_Failed attempts originated from the IP address `10.0.0.100`, by user: `guest`




