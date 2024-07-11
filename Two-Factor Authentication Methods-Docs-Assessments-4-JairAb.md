<!-- Documentation Pages
https://docs.osticket.com/en/latest/Features/Multifactor%20Authentication.html 
https://docs.osticket.com/en/latest/Plugins/Two%20Factor%20Authentication.html
I would use the page documentation page for both, because they are considered as a 2FA.-->
# Two-factor Authentication Documentation

## Introduction
<!--"Multifactor Authentication, sometimes referred to as Two Factor Authentication, adds an extra layer of authentication set up for Agents." 
This explanation is an ERROR, it is not a true statement.
Technical Explanation:
Two-factor Authentication (2FA):
2FA requires users to provide two forms of verification from different categories:
-Something you know: Typically, this is a password or PIN.
-Something you have: This could be a smartphone with an authentication app or a hardware token.
The combination of these two factors adds an extra layer of security beyond just a password, making it harder for unauthorized users to gain access.

Multi-factor Authentication (MFA):
MFA goes beyond 2FA by requiring users to provide more than two forms of verification.

In addition to "something you know" and "something you have," MFA may also include:

-Something you are: This involves biometric factors such as fingerprint scans or facial recognition.
-Somewhere you are: This factor verifies the user's location through GPS or IP address.
-Something you do: This might involve behavioral factors like typing patterns or mouse movements.-->
Two-factor authentication (2FA) adds an extra layer of security by requiring a second form of verification before granting access to an account or system.

## Steps to Enable Two-factor Authentication

1. **Navigate to Security Settings**
   - Log in to your oSticket account.
   - Click on your profile icon and select **Security Settings** from the dropdown menu.

   ![Step 1](https://docs.osticket.com/en/latest/_images/mfa1.png)

   
2. **Enable Multi-factor Authentication**
   - In the Security Settings page, locate the **Multi-factor Authentication** section by selecting
   **Admin Panel > Settings > Agents > Require agents to turn on 2FA**
   - Toggle the switch to enable 2FA for your account.

   ![Step 2](https://docs.osticket.com/en/latest/_images/mfa2.png)

3. **Choose Authentication Methods**
   - Select the authentication methods you wish to use. Consider that email is the Default Option. Options are SMS, Authenticator App or Email.

   ![Step 3.1](https://docs.osticket.com/en/latest/_images/mfa5.png)

   ![Step 3.2](https://docs.osticket.com/en/latest/_images/mfa6.png)

4. **Configure Each Method**
   - For each selected method, follow the on-screen instructions to configure and verify your identity. You will receive a verification code via email from the Support team to finish logging.

   ![Step 4](https://docs.osticket.com/en/latest/_images/mfa7.png)

5. **Complete Setup**
   - Once all selected methods are configured and verified, click **Save** to complete the setup.

6. **Edit Email Template for Administrators**
   - An administrator can edit the Email Template sent for the verification token by selecting:
   **Admin Panel > Settings > Agents > Templates > Two Factor Authentication Email**

   ![Step 6.1](https://docs.osticket.com/en/latest/_images/mfa16.png)

   ![Step 6.2](https://docs.osticket.com/en/latest/_images/mfa17.png)

   **Note:** The template variable that contains the token is %{otp}

   -In an event that an Agent becomes locked out of their account, an Administrator can reset their 2FA configuration by selecting:

   **Admin Panel > Agents > click Agent > Reset 2FA**

    ![Step 6.3](https://docs.osticket.com/en/latest/_images/mfa18.png)


## Watch the video for reference
![Password Policies Plugin](https://www.youtube.com/watch?v=JlOs7qdsHXA)

<!--Analysis and Explanation
This Markdown-formatted documentation follows best practices in technical writing and content organization. The headers clearly define the sections, with each step presented in a structured numerical list for easy comprehension.

Images are embedded after each step to visually guide users through the process, enhancing clarity and understanding. This approach maintains a professional and executive tone suitable for corporate environments, emphasizing security best practices and user-friendly guidance.

By using standardized guidelines, the documentation retains simplicity and readability, ensuring that users can follow the instructions smoothly while implementing robust security measures. -->
