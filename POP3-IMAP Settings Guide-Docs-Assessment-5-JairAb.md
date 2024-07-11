<!--Documentation page
https://docs.osticket.com/en/latest/Getting%20Started/POP3-IMAP%20Settings.html
-->

# POP3/IMAP Settings Documentation

## Introduction
POP3 (Post Office Protocol 3) and IMAP (Internet Message Access Protocol) are protocols used by email clients to retrieve messages from a mail server. This guide will help you configure POP3/IMAP settings in oSticket to manage email fetching.

## Prerequisites
Before configuring POP3/IMAP settings, ensure you have the following:
- Access to the oSticket admin panel
- Email server details (hostname, port, and credentials)
- SSL/TLS configuration details (if applicable)

## Steps to Configure POP3/IMAP Settings

1. **Access Email Settings**
   - Log in to your oSticket admin panel.
   - Navigate to **Admin Panel** > **Emails** > **Email Settings**.
   <!-- " Enable mail fetch in Admin Panel => Settings => Email Settings "- This format is not the same like the other documentation. So, it is not allowed and need to be remediated.-->


2. **Add a New Email**
   - Click on the **Add New Email** button to configure a new email account.
   - Enter the email address and other required information.


3. **Configure Mail Account**
   - In the email configuration page, enter the following details:
     - **Email Address**: The email address you want to configure.
     - **Protocol**: Select either **POP3** or **IMAP**.
     - **Hostname**: The mail server hostname (e.g., `mail.example.com`).
     - **Port**: The port number (e.g., 110 for POP3, 143 for IMAP, 993 for IMAP over SSL).
     - **Username**: The email account username.
     - **Password**: The email account password.


4. **Set Fetch Frequency**
   - Under the **Mail Account** settings, set the fetch frequency to determine how often oSticket checks for new emails.
   - Recommended: 5 minutes.

   
5. **Enable SSL/TLS (if applicable)**
   - If your email server requires a secure connection, enable **SSL/TLS**.
   - Ensure you use the correct port for SSL/TLS (e.g., 995 for POP3 over SSL, 993 for IMAP over SSL).


6. **Test Email Fetching**
   - Click on the **Fetch Now** button to test the email fetching configuration.
   - Verify that emails are being fetched correctly.

   
## Schedule Polling

Polling must be scheduled for repeated execution. Depending on your hosting environment, choose one of the methods below:

### Recurring Tasks Scheduler (Cron Job)

  -For Unix systems, add an entry to the crontab file:
      ```shell
       */5 * * * * nobody /path/to/php /path/to/api/cron.php

 -For Windows, add a scheduled task:
     ```shell
        "c:\php\bin\php.exe c:\website\osticket\api\cron.php"

### Host's Custom Task Scheduler

  - Schedule the task using your web host’s scheduling interface to run the cron.php script. -Ensure to set up API keys and rules for secure access.

### External Triggering Using WGET

   - Set up a cron job to run wget:
     ```shell
     */5 * * * * nobody wget -q -O /dev/null --user-agent=<API key here> http://<host & path goes here>/api/cron.php

### Auto Cron

    - Enable in **Admin Panel > Emails > Settings** and ensure Email Fetching Fetch on auto-cron is enabled. Note: Emails are fetched based on staff activity.
    - Note: Emails are fetched based on staff activity.

<!--Analysis and Explanation
The documentation was reorganized to enhance clarity, improve user experience, and ensure alignment with best industry practices for technical documentation. The restructuring was guided by the following principles:

Clarity and Readability: Each step is presented in a clear and concise manner, using a numerical list to ensure users can easily follow the sequence of actions required to configure POP3/IMAP settings. This reduces the likelihood of errors and misunderstandings.

Content Hierarchy: The documentation is structured with a clear hierarchy, starting with an introduction that explains the purpose and benefits of POP3/IMAP, followed by prerequisites, and then a step-by-step guide. This logical flow helps users understand the context before diving into the technical steps.

Standardized Methods: By adhering to standardized methods for technical writing, such as using consistent terminology and formatting, the documentation ensures that users can quickly grasp the instructions and apply them correctly.

Corporate and Executive Standards: The documentation reflects a professional tone and structure suitable for a corporate environment. Clear instructions, coupled with a logical progression of steps, ensure that users can implement email fetching configurations efficiently and effectively, thereby enhancing the overall functionality of the oSticket system.

Rewriting and organizing the documentation in this manner ensures that it is user-friendly, reduces the potential for errors, and aligns with the high standards expected in corporate technical documentation.-->