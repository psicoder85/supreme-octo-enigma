<!--Page 
https://docs.osticket.com/en/latest/Plugins/Two%20Factor%20Authentication.html
-->

# Two-factor Authentication Documentation

## Introduction
Two-factor authentication (2FA) adds an extra layer of security by requiring users to provide two forms of verification before accessing their oSticket account.

## Prerequisites

Before configuring the plugin, ensure you have the following authentication app downloaded on your mobile device.
   - Download the Google Authenthicator App for Apple from [Google Apple](https://apps.apple.com/us/app/google-authenticator/id388497605).
   - Download the Google Authenthicator App for Android from [Google Android](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&pli=1).
   - Download the Microsoft Authenthicator App for Apple from [Microsoft Apple](https://apps.apple.com/us/app/microsoft-authenticator/id983156458).
   - Download the Microsoft Authenthicator App for Android from [Microsoft Android](https://play.google.com/store/apps/details?id=com.azure.authenticator&referrer=%20adjust_reftag%3Dc6f1p4ErudH2C%26utm_source%3DLanding%2BPage%2BOrganic%2B-%2Bapp%2Bstore%2Bbadges%26utm_campaign%3Dappstore_android).

## Steps to Enable Two-factor Authentication

1. **Access Plugin Installation**
   - Log in to your oSticket admin panel.
   - Navigate to the **Admin Panel > Manage > Plugins** section.
   - Select **Add New Plugin > Install**.
   - To enable the plugin, Select **Status > Active > Save Changes**.
   
   ![Step 1.1](https://docs.osticket.com/en/latest/_images/plugins_add_new.png)

   ![Step 1.2](https://docs.osticket.com/en/latest/_images/2fa_plugin_install.png)

   ![Step 1.3](https://docs.osticket.com/en/latest/_images/2fa_plugin_enable.png)

2. **Locate Two-factor Authentication Plugin**
   - Search or scroll through the available plugins list to find the **Two-factor Authentication** plugin.
   - Select **Admin Panel > Manage > Plugins > Two Factor Authenticator > Instances**.

   ![Step 2.1](https://docs.osticket.com/en/latest/_images/2fa3.png)

   ![Step 2.2](https://docs.osticket.com/en/latest/_images/2fa_plugin_new_instance.png)

3. **Add and Configurate a New Instance**
   - Select **Add New Instance** .
   - Give a **Name**.
   - Set the **Status** to **Active** and select **Config** to configure.
   
   ![Step 3.1](https://docs.osticket.com/en/latest/_images/2fa_plugin_instance.png)

   ![Step 3.2](https://docs.osticket.com/en/latest/_images/g2fa4.png)

4. **Configure and Enable Authentication App as a Default Two-factor Authentication**
   - After activation, navigate to the plugin settings.
   - Choose an authentication method (e.g., Google Authenticator, Microsoft Authenticator SMS, Email).
   - Configure the chosen method by following the on-screen instructions.
   - Select **Authenticator** as the default 2FA method. 
   - Scan the QR code shown with your mobile authenticator app device.
   - Enter the code displayed in the app and verify its accuracy.
   
   ![Step 4.1](https://docs.osticket.com/en/latest/_images/2fa4.png)

   ![Step 4.2](https://docs.osticket.com/en/latest/_images/2fa5.png)
   
   ![Step 4.3](https://docs.osticket.com/en/latest/_images/2fa6.png)

   ![Step 4.4](https://docs.osticket.com/en/latest/_images/2fa7.png)

   ![Step 4.5](https://docs.osticket.com/en/latest/_images/2fa12.png)

   ![Step 4.6](https://docs.osticket.com/en/latest/_images/2fa11.png)
   
<!--Analysis and Explanation
The documentation was rewritten and organized to enhance clarity, improve the user experience, and ensure alignment with best industry practices for technical documentation. The restructuring was guided by the following principles:

Clarity and Readability: The steps are presented in a clear and concise manner, using a numerical list to ensure users can easily follow the sequence of actions required to enable Two-factor Authentication. This reduces the likelihood of errors and misunderstandings.

Content Hierarchy: The documentation is structured with a clear hierarchy, starting with an introduction that explains the purpose and benefits of 2FA, followed by a step-by-step guide. This logical flow helps users understand the context before diving into the technical steps.

Visual Aids: Images are included after each step to provide visual guidance, making it easier for users to follow along and verify that they are on the right track. This is particularly important in technical documentation, where visual confirmation can aid in comprehension.

Standardized Methods: By adhering to standardized methods for technical writing, such as using consistent terminology and formatting, the documentation ensures that users can quickly grasp the instructions and apply them correctly.

Corporate and Executive Standards: The documentation reflects a professional tone and structure suitable for a corporate environment. Clear instructions, coupled with a logical progression of steps, ensure that users can implement security measures efficiently and effectively, thereby enhancing the overall security posture of the organization.

Rewriting and organizing the documentation in this manner ensures that it is user-friendly, reduces the potential for errors, and aligns with the high standards expected in corporate technical documentation.-->