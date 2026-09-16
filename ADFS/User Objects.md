- Users can authenticate to ADDS domain and access network resources with user account
- User account includes
	- Username
	- User password
	- Group memberships
- Example of setting up user
	- ![[Pasted image 20260916153935.png]]
- Can use the following to create one
	- AD Admin Center
	- AD Users and Computers
	- Windows Admin Center
	- PowerShell
	- ``dsadd`` command tool

## Managed Service Accounts (MSA)
- To start up and authenticate a service - apps running in background and not requiring user interaction - use service account
- Can be local to computer, or be domain-based
- Managed service account enables
	- Password management 
	- Service principal name (SPN) management (tells what service client is trying to authenticate to)

## Group Managed Service Accounts (gMSA)
- Extends to multiple servers in domain
- Must create KDS (Key Distribution Service) root key
	- Use this command: ``Add-KdsRootKey EffectiveImmediately``
- To create gMSA, use command: ``New-ADServiceAccount -Name LondonSQLFarm -PrincipalsAllowedToRetrieveManagedPassword SEA-SQL1, SEA-SQL2, SEA-SQL3``
- Managed by AD to run service on multiple servers
## Delegated Managed Service Accounts (dMSA)
- Windows Server 2025 exclusive feature
- Transition from service -> machine accounts have randomized keys; disables service account passwords
- Prevents credential harvesting with a compromised account associated with MSA
- Managed by admin to run service on specific server