 Evaluating Logical Controls, Default Systems, and Data Integrity

Overview

This practical lab focuses on evaluating logical security controls, local user accounts, authentication mechanisms, security event logs, and file system permissions in a Windows environment.

The main purpose of this lab is to identify security weaknesses that may exist because of default system configurations, unmanaged user accounts, weak authentication settings, unauthorized sessions, or excessive file permissions. The lab also demonstrates how security controls can be reviewed and how excessive privileges can be identified and remediated.

Objectives

The major objectives of this practical are:

- Identify security vulnerabilities caused by unmanaged default accounts and open access parameters.
- Review local Windows user accounts and their properties.
- Examine authentication policies and Security Event Logs.
- Monitor active user sessions and login activity.
- Inspect file and folder permissions using Access Control Lists (ACLs).
- Compare permissions between protected system locations and a test directory.
- Identify and remove excessive user privileges.
- Understand the principles of Least Privilege and logical access management.
- Prepare an objective IS Audit Findings Report based on the observations.

Practical Tasks

1. Account Enumeration and Session Audit

The first task focuses on identifying local accounts configured on the Windows system.

The "net user" command is used to enumerate registered local accounts. Detailed information about important accounts such as Administrator and Guest can then be inspected using:

net user Administrator
net user Guest

The "query user" command is used to examine active user sessions. It helps identify interactive or remote sessions, session IDs, states, and logon times.

This task helps an auditor determine whether unnecessary accounts, unexpected sessions, or potentially unmanaged access exist on the workstation.

2. Authentication Policy and Security Event Log Inspection

The second task evaluates local account policies and authentication activity.

The "net accounts" command is used to review authentication-related settings such as password aging, minimum password requirements, and lockout parameters.

Security Event Logs are also examined for successful and failed login attempts. Event ID 4624 represents successful logon activity, while Event ID 4625 represents failed logon activity.

Reviewing these events provides an audit trail that can help identify authentication activity and verify whether security logging is functioning as expected.

3. ACL and Privilege Audit

The third task focuses on file system permissions and privilege management.

A test directory named "C:\SystemData" is created, and permissions are intentionally configured to provide the Users group with Full Control. The "icacls" command is then used to inspect the permissions applied to the directory.

The permissions of the protected Windows configuration directory and the test directory are compared to understand the difference between restricted and excessive access.

Finally, the excessive permission assigned to the Users group is removed and the ACL is checked again to verify that the remediation was successful.

Security Concepts Covered

Logical Access Control

Logical access control refers to mechanisms used to control who can access systems, accounts, files, and other digital resources.

Least Privilege

The Least Privilege principle means that users should receive only the permissions required to perform their legitimate tasks. Excessive permissions can increase the impact of unauthorized or accidental actions.

Authentication and Audit Trails

Authentication controls verify user access, while security logs provide records of authentication activity. Successful and failed logon events can therefore be useful during security auditing.

Access Control Lists (ACLs)

ACLs define which users or groups can access a resource and what actions they are allowed to perform. Reviewing ACLs helps identify excessive or inappropriate permissions.

Governance and Security Frameworks

The practical relates its activities to several recognized security frameworks and controls, including:

- ISO/IEC 27001:2022 — A.5.15 and A.5.18: Logical access management, identity-related controls, and privilege reviews.
- COBIT 2019 — DSS05.04: Management of logical access privileges.
- NIST SP 800-53 — AC-2 and AC-6: Account management and enforcement of least privilege.

Audit Findings

The practical requires observations from the three major tasks to be documented in an Audit Findings Matrix.

Typical findings include:

- Review of active and dormant user accounts.
- Evaluation of password and account lockout settings.
- Review of successful and failed authentication events.
- Identification of excessive file permissions.
- Verification that excessive privileges were successfully revoked.

Each finding is evaluated against the relevant security objective and assigned an appropriate risk level based on the observed system state.

Conclusion

This practical provides hands-on experience in Windows logical access auditing and data integrity protection. It demonstrates how security administrators and auditors can review user accounts, authentication policies, event logs, active sessions, and file permissions to identify potential security weaknesses.

The practical also emphasizes that access should be properly controlled and excessive privileges should be removed according to the Least Privilege principle. Through account enumeration, log analysis, ACL comparison, and privilege remediation, the lab provides a practical understanding of how logical security controls can be evaluated in a real Windows environment.Ye version GitHub README ke liye professional hai aur lab ke actual content ko follow karta hai. Agar chaho to main isi ke neeche “Tools/Commands Used” + “Learning Outcomes” + “GitHub README ka complete final format” bhi bana sakta hoon.