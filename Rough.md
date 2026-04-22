# Rough Notes

> Reference:
> https://github.com/KQLMSPress/definitive-guide-kql

> List all log sources:
> https://github.com/rod-trent/SentinelKQL/blob/master/WorkspacesAndTables.txt


- ### What is KQL

KQL stands for Kusto Query Language. Exploring your data and discovering patterns, identifying anomalies and outliers is what is does best. The data is stored in different tables. In these tables, there are columns where the data actually resides. This is very similar to SQL. KQL was also designed and developed to take advantage of cloud computing through custering and scaling compute. You can process enormous amounts of data very quickly. This is accomplished through read-only queries, which are case-sensitive, including table names, table column names, operators, and functions. You can turn this data into actionable insights by filtering, analyzing, and preparing data.













- ### Microsoft Entra ID supports the following log categories:

  - **AuditLogs:** These Entra ID audit logs contain changes to the object state in the directory. Examples of this would be a new license applied to a user object, registering for Self Service Password Reset, or an updated attribute on the user object. This category also includes changes to applications and groups.
  
  - **SignInLogs:** The interactive sign-ins performed by a user, such as logging in with a password and responding to multifactor authentication challenges through the Microsoft Authenticator app or other phone-based methods.
  
  - **NonInteractiveUserSignInLogs:** These logs are sign-ins done on behalf of the user. A client application or an operating system component performs these. For example, Outlook will continue to request a fresh access token (silently in the background) to maintain access to Exchange online. Note that this log source can be extremely large.
  
  - **ServicePrincipalSignInLogs:** These log sources are sign-ins by a nonuser account, such as an application or service principal. These sign-ins have their own credentials, such as a certificate or an application secret to access resources.
  
  - **ManagedIdentitySignInLogs:** These log sources are for Managed Identities, a special type of service principal. Their secrets are managed by Azure, simplifying credential management for the developer.
  
  - **ProvisioningLogs:** These log sources are from provisioning and deprovisioning users and groups to other applications leveraging the SCIM protocol.
  
  - **ADFSSignInLogs:** These log sources are if the environment is federated with Active Directory Federation Services (AD FS) and if Azure AD Connect Health is installed, this will allow you to easily see the entire login flow in one view.
  
  - **RiskyUsers:** This log source is from Microsoft Entra Identtiy Protection, including users with low, medium, and high risk scores.
  
  - **UserRiskEvents:** This log source is from Microsoft Entra Identity Protection. This includes risk detections, such as impossible travel, leaked credentials, and sign-ins from IPs associated with malware.
  
  - **NetworkAccessTrafficLogs:** This log source is for all network traffic, which includes Microsoft 365, Microsoft Entra Internet Access and Private Access. This will include information on the connection and sessions to resources and what action occurred.
  
  - **RiskyServicePrincipals:** This log source is from Microsoft Entra Identity Protection. This provides the service principal or workload identities with low, medium, or high risk scores.
  
  - **ServicePrincipalRiskEvents:** This log source is from Microsoft Entra Identity Protection. This includes the risk detections for service principal or workload identities such as suspicious sign-ins, leaked credentials, and anomalous behavior patterns like suspicious changes to the directory.
  
  - **EnrichedOffice365OfficeLogs:** This log source provides information about Microsoft 365 workloads so you can review network diagnostic data, performance data, and security events related to Microsoft 365 apps.
  
  - **MicrosoftGraphActivityLogs:** This log source is the activity of graph calls made against Microsoft Graph, including Microsoft applications such as Outlook, Microsoft Teams, your line-of-business applications, API clients, and SDKs. This includes data such as when the request was received, when the token was generated, and the roles and scopes in the claim. Note that this log source can be large.
