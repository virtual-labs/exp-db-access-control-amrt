#### Access Control in Databases

Access control in databases refers to mechanisms that regulate which users are permitted to view, modify, or manage data within a database system. Its purpose is to ensure that data is accessed securely and only by authorized users according to predefined security policies.

The three primary access control models used in database environments are **Role-Based Access Control (RBAC)**, **Discretionary Access Control (DAC)**, and **Mandatory Access Control (MAC)**. Each model enforces access restrictions using a different approach and is applied based on specific security requirements.



##### 1. Role-Based Access Control (RBAC)

Role-Based Access Control (RBAC) manages access by assigning permissions to roles rather than directly to users. A role represents a specific job function or responsibility within an organization, and each role contains a predefined set of permissions.

###### Key Concepts

- Permissions are grouped into roles.
- Users are assigned roles instead of individual permissions.
- Users inherit permissions based on their assigned roles.
- Enforces the **principle of least privilege**, ensuring users receive only the minimum permissions required to perform their tasks.
- Simplifies administration and improves scalability in large systems.

RBAC reduces administrative complexity because administrators manage permissions at the role level instead of configuring privileges separately for each user. This model is widely used in enterprise database systems due to its efficiency and structured approach.



##### 2. Discretionary Access Control (DAC)

Discretionary Access Control (DAC) allows the owner of a database object (such as a table or view) to control access to that object. Permissions are typically granted or revoked using SQL commands such as `GRANT` and `REVOKE`.

###### Key Concepts

- Specific privileges such as `SELECT`, `INSERT`, `UPDATE`, or `DELETE` can be granted to individual users.
- The `WITH GRANT OPTION` allows a user to grant their assigned privileges to other users.
- Provides flexible and fine-grained access control.
- Privileges can be revoked at any time using the `REVOKE` command.

Although DAC offers flexibility, it can introduce security risks due to cascading privilege assignments when `WITH GRANT OPTION` is used. If not carefully managed, privileges may propagate beyond the intended scope.


##### 3. Mandatory Access Control (MAC)

Mandatory Access Control (MAC) is a strict, policy-driven access control model where access decisions are enforced based on system-defined security classifications and user clearance levels. Unlike DAC, users cannot alter access permissions.

###### Key Concepts

- Data objects are assigned classification labels, and users are assigned clearance levels. In this simulation, the hierarchy of levels is (from highest to lowest):
  - Top Secret
  - Secret
  - Confidential
  - Public
- Access decisions are enforced by the system based on security policy.
- Users cannot override or delegate permissions.

While MAC often follows strict frameworks like the **Bell-LaPadula security model** (which enforces "No Read Up" and "No Write Down" rules), this simulation implements a **General Mandatory Access Control** model with a unified dominance rule. In this simulation:

- **Access Rule** – A subject may perform any access operation (Read or Write) **only if** their clearance dominates (is greater than or equal to) the object's classification.

MAC provides strong security enforcement and is typically used in high-security environments such as military, government, and defense systems.


