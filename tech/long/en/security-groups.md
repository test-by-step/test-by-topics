# Security Groups

Security Groups gathers subjects such as users, accounts, and devices into groups that can be managed together to specify policies, privileges, and permissions for all members or entities assigned to the group.

Security Groups are used primarily to manage access to shared resources on the system or network through permissions.

Common security polices can be changed and deployed quickly as a standard set for all users of a given group.

Security Groups can be used to segment users and accounts access to resources only required for their group, such as shared folders, or even services on the network. As an example, separate security groups can be made for Accounting and Sales and each will have access to their own shared cloud folder, but not each others.

Security Groups function similarly to Role Based Access Control (RBAC) where access to resources is defined by a role, and users are assigned the role in order to gain access to the resources.

Security Groups will often act in tandem with Network Access Control, approving or denying network access for a device or placing the device in a particular VLAN based on Security Group policy.

## Resources

[1] https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/manage/understand-security-groups
[2] https://cloud.google.com/identity/docs/how-to/update-group-to-security-group