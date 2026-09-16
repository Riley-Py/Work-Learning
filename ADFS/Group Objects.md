- Used to manage user accounts that request the same level of access
- Diagram of this:
	- ![[Pasted image 20260916155406.png]]
- Two types of groups
	- *Security* - assign permission to various resources; security-enabled
	- *Distribution* - aren't security enabled

## Scopes
- *Local* - assign abilities/permissions on local resources only; members can be anywhere in ADDS forest; used for standalone servers/workstations
- *Domain-local* - exist on domain controllers in ADDS domain; assign abilities/permissions only in local domain; manage access to resources/assign management rights
- *Global* - consolidate users with similar characteristics (geographic location/department); can assign abilities/permissions anywhere in forest; can only be from local domain only
- *Universal* - multidomain networks; combines domain-local and global group properties; can assign abilities/permissions anywhere in forest like global groups