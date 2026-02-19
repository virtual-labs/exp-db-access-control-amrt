
#### **Access Control in Databases**


Access control in databases refers to the mechanisms that regulate which users are allowed to view, modify, or manage data. Its primary purpose is to ensure that data is accessed securely and only by authorized individuals, following predefined rules and security policies. Effective access control protects data integrity, confidentiality, and proper usage within a database system.

The three primary access control models used in database environments are **Role-Based Access Control (RBAC)**, **Discretionary Access Control (DAC)**, and **Mandatory Access Control (MAC)**. Each model implements access restrictions through a different approach and is suitable for different security requirements.


#### **1. Role-Based Access Control (RBAC)**

Role-Based Access Control (RBAC) manages access by assigning permissions to roles, which are then assigned to users. A role represents a job function, and each role carries a predefined set of permissions.

##### **Key Concepts**

* Permissions are grouped into roles rather than being assigned individually.
* Users inherit permissions based on the roles they are assigned.
* Enforces the **principle of least privilege**, ensuring users only receive the access necessary for their tasks.
* Improves scalability and simplifies management, especially in large systems.

RBAC reduces administrative complexity by allowing administrators to modify role permissions instead of adjusting permissions for each user individually.



#### **2. Discretionary Access Control (DAC)**

Discretionary Access Control (DAC) allows the data owner to determine who can access or modify the data. Permissions are typically managed using SQL commands such as `GRANT` and `REVOKE`.

##### **Key Concepts**

* Users can be granted specific privileges such as `SELECT`, `INSERT`, or `UPDATE`.
* The **WITH GRANT OPTION** allows a user to pass their privileges to others.
* Offers flexible control but can be less secure due to cascading privilege assignments.
* Commonly used in environments where fine-grained data sharing is required.

DAC must be carefully administered to prevent unauthorized privilege propagation.



#### **3. Mandatory Access Control (MAC)**

Mandatory Access Control (MAC) is a strict, policy-driven model where access decisions are enforced based on security classifications assigned to data and clearance levels assigned to users.

##### **Key Concepts**

* Data objects are labeled with classifications such as *Confidential*, *Secret*, or *Top Secret*.
* Users are assigned clearance levels corresponding to these classifications.
* Enforces mandatory rules such as:

  * **No Read Up:** Users cannot read data above their clearance level.
  * **No Write Down:** Users cannot write data to a lower classification level.
* Typically used in environments requiring robust security, such as defense or government systems.

MAC provides strong protection by ensuring that users cannot alter or override system-defined security policies.

