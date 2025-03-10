# EntraAudit
Due to Azure Entra ID being used for the management of a significant application, we will need to review the need for administrative access, enforcement of secure passwords, and the enforcement of MFA. Therefore, we would like to receive the items listed below. Microsoft links are provided for easy access, including the setting of custom managed views to gather non-default attributes that are relevant in performing the IT audit work of your Entra tenant.

## Users Export

```
Using Microsoft Entra Admin Center (GUI)
1.	Sign in to Microsoft Entra Admin Center.
2.	Navigate to Identity > Users > All users.
3.	Click Download users at the top.
4.	Choose the file format (CSV) and click Download to export the list.
```
Link to skip to step 3:
```
https://entra.microsoft.com/#view/Microsoft_AAD_UsersAndTenants/UserManagementMenuBlade/~/AllUsers
```

## Privileged Identity Management Export

```
Using Microsoft Entra Admin Center (GUI)
1.	Sign in to Microsoft Entra Admin Center.
2.	Go to Identity > Identity Governance > Privileged Identity Management.
3.	In the Privileged Identity Management section, navigate to  Microsoft Entra roles.
4.	Under  Microsoft Entra Roles, go to the Assignments tab.
5.	Here, you can see the list of role assignments, which includes:
- Active: Users currently assigned roles.
- Eligible: Users eligible to activate roles.
- Expiring soon: Roles with upcoming expiry dates.
6.	Export role assignments:
- Click the Download button (top-right corner) to export the list as a CSV file.
```
Link to skip to step 6:
```
https://entra.microsoft.com/#view/Microsoft_Azure_PIMCommon/ResourceMenuBlade/~/members/resourceId//resourceType/tenant/provider/aadroles
```

## Role Assignments Export
```
Using Microsoft Entra Admin Center (GUI)
1.	Sign in to Microsoft Entra Admin Center.
2.	Navigate to Identity > Roles & Administrators.
3.	Click Roles & administrators to see assigned roles.
4.	Click Roles & administrators then click the "Download assignments" button at the top of the table.
5.	Click Download or Export to CSV to save the role assignments.
6.	This file is exported with the naming convention "AzureExportRoleAssignments_All_{YYYY-MM-dd}.csv"
```
Link to skip to step 4:
```
https://entra.microsoft.com/#view/Microsoft_AAD_IAM/RolesManagementMenuBlade/~/AllRoles
```

## Screenshots of the configurations within the “Manage>Users and groups” tab under the significant application(s) found under
```
Using Microsoft Entra Admin Center (GUI)
1. Sign in to Microsoft Entra Admin Center.
2. Navigate to Identity > Applications > Enterprise applications.
3. Click on the Enterprise application(s) in scope
4. Navigate to Manage>Users and groups (on the left pane). Take a screenshot of this screen
```
Link to skip to step 3:
```
https://entra.microsoft.com/#view/Microsoft_AAD_IAM/StartboardApplicationsMenuBlade/~/AppAppsPreview
```

## Screenshots of the configurations within the “Security>Conditional Access” tab under the significant application(s) found under:
```
Using Microsoft Entra Admin Center (GUI)
1. Sign in to Microsoft Entra Admin Center.
2. Navigate to Identity > Applications > Enterprise applications.
3. Click on the Enterprise application in scope
4. Navigate to Security>Conditional Access (on the left pane). Take a screenshot of this screen
```
Link to skip to step 3:
```
https://entra.microsoft.com/#view/Microsoft_AAD_IAM/StartboardApplicationsMenuBlade/~/AppAppsPreview
```

## Screenshots of the Configurations of Conditional Access Policies

Screenshots are only needed for Conditional Access Policies that enforce MFA for remote access, administrators, and users with access to the significant systems (determined by the `Enterprise Applications>users & groups` view from above)

1. That are used to enforce MFA for the following scenarios:
- Administrative Entra access (and AD if applicable)
- Remote access
- Significant system access
2.	Please include screenshots for the following categories:
- Users (Unless “All users” is visible)
- Include and exclude tabs
- Target resources
- Include and exclude tabs
- Network
- Conditions
- Grant

```
Using Microsoft Entra Admin Center (GUI)
1. Sign in to Microsoft Entra Admin Center.
2. Navigate to Identity > Protection > Conditional Access.
3. Under Policies, you'll see a list of all Conditional Access policies configured in your tenant.
4. Click on a policy to view its settings, including:
5. Assignments (Users, Groups, Roles, Cloud Apps)
6. Conditions (Device Platforms, Locations, Client Apps, Risk Levels)
7. Access Controls (Grant or Block Access, MFA Requirements)
8. Click Download (top-right corner) to export the policies in JSON format.
```
Link to skip to step 4:
```
https://entra.microsoft.com/#view/Microsoft_AAD_ConditionalAccess/ConditionalAccessBlade/~/Policies/menuId//fromNav/Identity
```

## Screenshot of the password protection screen to show lockout threshold, lockout duration, and banned password configurations
```
Using Microsoft Entra Admin Center (GUI)
1. Sign in to Microsoft Entra Admin Center.
2. Navigate to Identity > Protection > Authentication Methods.
3. Click on Password Protection (left menu).
```
Link to skip steps above:
```
https://entra.microsoft.com/#view/Microsoft_AAD_IAM/AuthenticationMethodsMenuBlade/~/PasswordProtection/fromNav/Identity
```

## The Entra Connect (formerly known as Azure AD Connect) configuration export in JSON format.
```
To get this export, you may follow these steps on the device that manages your organization’s Entra Connect instance.
1. Open Entra Connect.
2. Click on the Configure tab.
3. Click on the View or export current configuration link.
4. Click on the Export Settings button.
5. Save the JSON file to a location on your computer.
```
