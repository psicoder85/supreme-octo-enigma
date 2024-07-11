<!-- Documentation page
https://docs.osticket.com/en/latest/Plugins/Password%20Management%20Policies.html-->
# Password Management Policies

The Password Management Policies plugin allows helpdesk Administrators to enforce custom password requirements for Agents and Users.


## Installation Steps

1. **Download and Upload**:
   - Download the plugin from [osTicket website](https://osticket.com/).
   - Select the appropriate version of osTikcket before the plugin selection.
   - Upload the plugin to your server and place it in the `include/plugins/` folder.
   - Ensure the plugin has appropriate file permissions and ownership.

2. **Install the Plugin**:
   - Log in to your helpdesk.
   - Navigate to **Admin Panel > Manage > Plugins**.
   - Click **Add New Plugin** and click **Install** next to the desired plugin.

   ![Plugins_add_new](https://docs.osticket.com/en/latest/_images/plugins_add_new.png)

   ![pwmgt_plugin_install](https://docs.osticket.com/en/latest/_images/pwmgt_plugin_install.png)

3. **Enable the Plugin**:
   - Click on the plugin name in the list of installed plugins.
   - Set **Status** to **Active**.
   - Click **Save Changes**.

   ![pwmgt_plugin_enable](https://docs.osticket.com/en/latest/_images/pwmgt_plugin_enable.png)

## Configuration

1. **Navigate to Configuration**:
   - Go to **Admin Panel > Manage > Plugins > Password Management Policies > Instances**.
   - Click **Add New Instance**.
   - Name the instance, set **Status** to **Active**, and configure settings under the **Config** tab.

![pwmgt1](https://docs.osticket.com/en/latest/_images/pwmgt1.png)

![pwmgt_plugin_new_instance](https://docs.osticket.com/en/latest/_images/pwmgt_plugin_new_instance.png)

![pwmgt_plugin_instance](https://docs.osticket.com/en/latest/_images/pwmgt_plugin_instance.png)

![pwmgt2](https://docs.osticket.com/en/latest/_images/pwmgt2.png)


2. **Password Settings**:
<!--This section was really unorganized and lack of format related with the other sections-->
   - **Minimum Length**: Specify the minimum number of characters required. 
   <!--I investigated but I didnt find what's the least amount of characters.-->
   - **Character Classes Required**: Set the number of different character classes required: uppercase, lowercase, numbers, special characters.
   - **Password Strength**: Choose the required password strength: Disable, Weak, Good, Strong, Awesome.
   <!--I excluded the Wikipedia reference. References must be with official websites, and referring to Wikipedia could lead to misunderstanding and not correct information.-->
   - **Enforce on Login**: Prompt Agents and Users to update passwords at login if they don't meet requirements.
   - **Password Reuse**: Decide whether to allow or prevent password reuse. Administrators can configurate it in a higher level.
   - **Password Expiration**: Set the frequency for password changes: 30 days, 60 days, 90 days, 180 days, 365 days, Never expires.

## Setting the Password Policy

1. **For Agents**:
   - Navigate to **Admin Panel > Settings > Agents > Password Policy**.
   - Select **Password Management Plugin**.

   ![pwmgt6](https://docs.osticket.com/en/latest/_images/pwmgt6.png)

2. **For Users**:
   - Navigate to **Admin Panel > Settings > Users > Password Policy**.
   - Select **Password Management Plugin**.

   ![pwmgt7](https://docs.osticket.com/en/latest/_images/pwmgt7.png)

## Notes
- **Default Basic Policy**: Refers to the legacy policy prior to the current version of osTicket. If none was set, passwords will not expire.

For detailed steps and additional information, refer to the full [Password Management Policies Guide](https://docs.osticket.com/en/latest/Plugins/Password%20Management%20Policies.html).

## Watch the video for reference
![Password Policies Plugin](https://www.youtube.com/watch?v=JlOs7qdsHXA)
<!-- Analysis
Steps to Follow: The original content lacked clear, sequential steps and adherence to documentation standards.
Verb Usage: Each step starts with a verb (e.g., Install, Download, Add, Select, Save, etc), ensuring clarity and avoiding redundancy.
Clarity and Professionalism: This format enhances clarity and professionalism by providing a structured and easy-to-follow guide for users.
Example: 
This step processes lacks of consistency and following the standardized guidelines:
1- Admin Panel > Manage > Plugins. Click Add New Plugin and click Install next to the desired plugin.
2- Admin Panel | Manage | Plugins | Password Management Policies | Instances
3- For Agents: Admin Panel | Settings | Agents | Password Policy | Password Management Plugin
4- For users: Admin Panel | Settings | Users | Password Policy | Password Management Plugin
This is definitely not a best industry practice and must be re organized.-->