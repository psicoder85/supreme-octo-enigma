<!--  Documentation of this page:
https://docs.osticket.com/en/latest/Getting%20Started/Installation.html
Here’s a detailed explanation of why the documentation was arranged in this order, aligning with content guidelines, best industry practices for content priority, hierarchy, and different content structures:
-The content was highly disorganized and lacked clarity from the outset. There was no clear structure or guideline to effectively divide and explain the information, leading to confusion and inefficiency. A more methodical approach with a well-defined hierarchy and focused content is essential for providing a professional and coherent user experience.

1. **Prerequisites**:
   - **Content Priority**: Establishing system requirements is essential before proceeding. It ensures the user can actually run the software.
   - **Content Structure**: Lists the necessary server specifications and database details clearly and concisely.

2. **Getting Started**:
   - **Content Priority**: The first actionable steps involve preparing the files and ensuring the environment is ready for installation.
   - **Content Structure**: Provides a step-by-step guide to downloading, uncompressing, and uploading files, followed by permission settings.

3. **Using Installation Script**:
   - **Content Priority**: Running the installation script is the core of the setup process.
   - **Content Structure**: A sequential guide through the installation script, from accessing the URL to completing the configuration, ensures clarity.

4. **Installing osTicket Using Fantastico in CPanel**:
   - **Content Priority**: Offering an alternative installation method for users with CPanel provides flexibility and caters to a wider audience.
   - **Content Structure**: Separate section for an alternative method keeps the primary guide clear and dedicated to the standard installation process.

5. **Finishing Up**:
   - **Content Priority**: Post-installation steps are crucial for securing the setup and ensuring it runs correctly.
   - **Content Structure**: Clearly defined steps to modify permissions, delete setup files, and enable the system.

6. **Self-Help Troubleshooting**:
   - **Content Priority**: Providing troubleshooting tips at the end helps users resolve common issues without interrupting the main flow of the installation guide.
   - **Content Structure**: Placed at the end to ensure users first complete the installation before addressing potential problems.

By following these content guidelines and best practices, the documentation ensures users can efficiently navigate through the installation process, addressing each critical step in a logical and user-friendly manner. -->
# osTicket Installation Guide
osTicket comes with its own web-based installer to help guide you through the installation process without the frustration. While the installer provides step by step guide during the installation process, it's important and helpful to have general knowledge about Web servers, PHP and MySQL.

## Prerequisites
- Apache/LiteSpeed/IIS with URL Rewrite
- PHP 8.1-8.2: Download link [https://windows.php.net/download/]
- MySQL 5.0 or better : Download link[https://dev.mysql.com/downloads/installer/]
- MariaDB 10.11 for Windows Server: Download link [https://mariadb.org/download/?t=mariadb&p=mariadb&r=11.4.2&os=windows&cpu=x86_64&pkg=msi&mirror=archive]
- MySQL database details (user with FULL privileges, password, hostname): Download link []

## Getting Started
<!-- At this point you should have downloaded latest version of osTicket.
I excluded and re organized all this content, it lacks of profesionalism and not a technical approach of the task-->
1. Download and uncompress the latest version of osTicket.
2. Upload files from the `upload` folder to a server directory (e.g., `/osticket/`, `/helpdesk/`, or `/support/`).
3. Ensure `ost-config.php` in the include directory is writable.

## Using Installation Script
1. Access the osTicket URL in your browser to start the installer (e.g., `http://www.yourdomain.com/support/setup/`).
2. Follow the installer steps to detect paths, permissions, and correct any errors.
3. Complete the form with required information and submit to configure the database and create the configuration file.

## Installing osTicket Using Fantastico in CPanel
1. From CPanel, use Fantastico to install osTicket.
2. Change the default email address from `support@system.com` immediately after installation.
3. Verify if the Fantastico package is up-to-date with the osTicket.com version.

## Finishing Up
<!--I excluded a paragraph that lacked precision and contained redundant information, which detracted from the documentation's focus and seriousness. The excluded paragraph read:

"If the setup script has finished running with no errors, then [congratulations]? osTicket is now installed. You can now log in with the username and password you created during the install process. After verifying that the installation completed correctly - your next step should be to fully configure your new support ticket system for use. But before you get to it please take a second to cleanup."

This content was not essential for guiding the user through the technical installation process and detracted from the document's clarity and professionalism. -->
1. Change permission of `include/ost-config.php` to remove write access.
2. Delete the setup directory.
3. Enable the system.
<!-- It is important to have right punctuation in the documentation, following the rules of technical writing and best industry practices-->

## Self-Help Troubleshooting
<!--It is obvious that if you are trouble shooting it is because you are having problems finding a solution, so I excluded all the redundancy in the paragraphs and focus on the tasks. Documentation is focused on follow the steps and avoid phrases that confuses the end user. -->
- Enable “Show Errors” in `/bootstrap.php` to display errors for troubleshooting. Use `/main.inc.php` in older versions.
- Check osTicket Dashboard and mail server logs for additional issues.
Example:
``# Don't Display Errors
ini_set('display_errors',0);
ini_set('display_startup_errors',0); ``

Change this to:
``ini_set('display_errors',1);
ini_set('display_startup_errors',1); ``

Errors are displayed in your web browser or your server `error.log` file.

For detailed steps and additional information, refer to the full [osTicket Installation Guide](https://docs.osticket.com/en/latest/Getting%20Started/Installation.html).
<!-- Analysis
Prerequisites: Remains a bullet list to succinctly list system requirements.
Getting Started: Uses a numerical list for clear, sequential setup steps.
Using Installation Script: Continues the numerical list format for step-by-step guidance through the primary installation method.
Installing osTicket Using Fantastico in CPanel: Uses a numerical list to maintain consistency and clarity for the alternative installation method.
Finishing Up: Uses a numerical list for the final steps to ensure security and completion.
Self-Help Troubleshooting: Uses a bullet list for quick, easy-to-follow troubleshooting tips.
This structure ensures clarity and consistency throughout the documentation.-->
