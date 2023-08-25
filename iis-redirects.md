# Create Redirects in IIS

Use the URL Rewrite module in IIS to point users from the old plugin paths to the new. The module is not installed by default, so if it has not yet been installed, download it from the official Microsoft website and install it on the server.

To create the redirect, follow these  steps:

1. **Open the IIS Manager.**
   - This can be done by typing 'inetmgr' in the Run dialog (Windows Key + R)

2. **Navigation is done to the appropriate site.**
   - The server name in the Connections pane is expanded, followed by Sites, and then the site that needs to be configured is clicked.

3. **In the site's Home pane, URL Rewrite is double-clicked.**

4. **In the Actions pane, Add Rule(s)... is clicked.**

5. **In the Add Rules dialog box, under Inbound rules, Blank Rule is clicked and then OK is clicked.**

6. **In the Edit Inbound Rule dialog box, a friendly name for the rule is entered in the Name box.**
   - For example, the name could be 'Redirect Rule for dacdbplus.zip'

7. **In the Match URL section:**
   - In the Requested URL dropdown, 'Matches the Pattern' is selected
   - In the Using dropdown, 'Regular Expressions' is selected
   - In the Pattern field, `^wordpress/dacdbplus\.zip$` is entered

8. **In the Conditions section:**
   - 'Add...' is clicked to open the Add Condition dialog box
   - In the Condition input field, `{HTTP_HOST}` is entered
   - In the Check if input string dropdown, 'Matches the Pattern' is selected
   - In the Pattern field, `^www\.dacdb\.com$` is entered
   - OK is clicked to close the dialog box

9. **In the Action section:**
   - In the Action type dropdown, 'Redirect' is selected
   - In the Redirect URL field, `https://wordpress.dacdb.com/plugins/dacdbplus/dacdbplus.zip` is entered
   - The box for 'Append query string' is checked
   - In the Redirect type dropdown, 'Permanent (301)' is selected

10. **Apply is clicked in the Actions pane.**

This rule tells IIS to redirect any requests that match the URL pattern `https://www.dacdb.com/wordpress/dacdbplus.zip` to `https://wordpress.dacdb.com/plugins/dacdbplus/dacdbplus.zip` permanently. It is recommended that this rule be thoroughly tested before being deployed in a live environment.