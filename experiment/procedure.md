<h4>Role-Based Access Control (RBAC)</h4>

<h5>Step 1 — Build Roles</h5>

<ul>
  <li>Read the instructions at the top and <strong>drag and drop</strong> the correct permissions into each role.<br>
    <img src="./images/step1-RBAC.png" alt="Build Roles" width="75%">
  </li>
  <li>Click <strong>Assign Permissions to Roles</strong> to validate your setup.<br>
    A green <strong>Assigned</strong> status indicates a successful configuration.
  </li>
  <li>Then click <strong>Next: Assign Roles to Users</strong> to continue.<br>
    <img src="./images/step2-RBAC.png" alt="Validate Roles" width="75%">
  </li>
</ul>

<h5>Step 2 — Assign Roles to Users</h5>

<ul>
  <li>Assign the available roles to users based on their <strong>positions and responsibilities</strong>.<br>
    <img src="./images/step3-RBAC.png" alt="Assign Roles to Users" width="75%">
  </li>
  <li>Click <strong>Verify User Roles</strong> to confirm your assignments, then select <strong>Next: Testing Phase</strong> to proceed.<br>
    <img src="./images/step4-RBAC.png" alt="Validate Assignments" width="75%">
  </li>
</ul>

<h5>Step 3 — Test & Verify Privileges</h5>

<ul>
  <li>In the Testing Phase, <strong>select a user</strong> from the left panel, choose an <strong>action</strong>, and test whether that user has access to perform it.<br>
    <img src="./images/step5-RBAC.png" alt="Test Access" width="75%">
  </li>
  <li>Click <strong>Test Access</strong> and observe the result:
    <ul>
      <li><strong>Access Granted</strong> — The user’s role includes the required permission.</li>
      <li><strong>Access Denied</strong> — The user’s role does not include the required permission.</li>
    </ul>
  </li>
  <li>Review the <strong>Access Log</strong> for details such as the user, assigned role, action, and timestamp.<br>
    <img src="./images/step6-RBAC.png" alt="Access Log / Result" width="75%">
  </li>
</ul>

<h4>Discretionary Access Control (DAC)</h4>

<h5>Step 1 — Grant Privileges</h5>

<ul>
  <li>Open the <strong>Grant Privileges</strong> tab.<br>
    <img src="./images/step1-DAC-grant.png" alt="Grant Privileges" width="75%">
  </li>
  <li>Select the <strong>Granter</strong> (user giving the privilege), typically <strong>Admin</strong>.</li>
  <li>Select the <strong>Grantee</strong> (user receiving the privilege).</li>
  <li>Choose the <strong>Object</strong> (table/resource such as <em>Customers</em> or <em>Orders</em>).</li>
  <li>Select the required <strong>Permission</strong> (<em>SELECT, INSERT, UPDATE, DELETE</em>).</li>
  <li>Enable <strong>WITH GRANT OPTION</strong> if the grantee is allowed to share the privilege.</li>
  <li>Click <strong>Grant</strong> to assign the privilege.<br>
    <img src="./images/step1.1-DAC-grant.png" alt="Grant Privilege Detail" width="75%">
  </li>
  <li>The privilege assignment is reflected in the <strong>Privilege Flow</strong>, and the <strong>Activity Log</strong> is updated.<br>
    <img src="./images/step2-DAC-privilege-flow.png" alt="Privilege Flow After Grant" width="75%">
  </li>
</ul>

<h5>Step 2 — Revoke Privileges</h5>

<ul>
  <li>Navigate to the <strong>Revoke Privileges</strong> tab.</li>
  <li>Select the <strong>User</strong> whose privilege needs to be removed.</li>
  <li>Choose the <strong>Object</strong> associated with the privilege.</li>
  <li>Select the <strong>Permission</strong> to revoke.</li>
  <li>Click <strong>Revoke (Cascade)</strong> to remove the privilege.<br>
    <img src="./images/step3-DAC-revoke.png" alt="Revoke Privileges" width="75%">
  </li>
  <li>The privilege is revoked from the user, dependent privileges are removed, and the <strong>Activity Log</strong> is updated.<br>
    <img src="./images/step4-DAC-revoked.png" alt="Privilege Flow After Revoke" width="75%">
  </li>
</ul>

<h5>Step 3 — Test & Verify Access</h5>

<ul>
  <li>Open the <strong>Test Access</strong> tab.</li>
  <li>Select a <strong>User</strong> to test.</li>
  <li>Choose an <strong>Action</strong> (<em>SELECT, INSERT, UPDATE, DELETE</em>).</li>
  <li>Select the <strong>Object</strong> on which the action is tested.</li>
  <li>Click <strong>Test Access</strong>.<br>
    <img src="./images/step5-DAC-test-access.png" alt="Test Access" width="75%">
  </li>
  <li>Observe the result:
    <ul>
      <li><strong>Access Granted</strong> — The user has the required privilege.</li>
      <li><strong>Access Denied</strong> — The user does not have the required privilege.</li>
    </ul>
  </li>
  <li>The access result is recorded in the <strong>Activity Log</strong>.<br>
    <img src="./images/step6-DAC-access-result.png" alt="Access Result" width="75%">
  </li>
</ul>

<h4>Mandatory Access Control (MAC)</h4>

<h5>Step 1 — Assign Security Levels</h5>

<ul>
  <li>Read the instructions displayed at the top of the interface.</li>
  <li>Drag a <strong>Security Level</strong> from the center panel and drop it onto a <strong>User (Subject)</strong> to assign clearance.</li>
  <li>Drag a <strong>Security Level</strong> and drop it onto a <strong>Data Object</strong> to assign classification.</li>
  <li>Ensure each user and data object has an assigned security level.</li>
  <li>Click <strong>Next: Test Access</strong> to proceed.<br>
    <img src="./images/step1-MAC-assign-levels.png" alt="Assign Security Levels" width="75%">
  </li>
</ul>

<h5>Step 2 — Verify Assigned Clearances and Classifications</h5>

<ul>
  <li>Review the assigned <strong>clearance levels</strong> for all users.</li>
  <li>Review the assigned <strong>classification levels</strong> for all data objects.</li>
  <li>Confirm that the visual indicators reflect the correct security hierarchy.</li>
  <li>The <strong>Activity Log</strong> is updated to record each assignment.<br>
    <img src="./images/step2-MAC-assigned-levels.png" alt="Assigned Clearances and Classifications" width="75%">
  </li>
</ul>

<h5>Step 3 — Test & Verify Access</h5>

<ul>
  <li>Select a <strong>User</strong> from the <em>Select User (clearance)</em> panel.</li>
  <li>Select a <strong>Data Object</strong> from the <em>Select Object (classification)</em> panel.</li>
  <li>Choose an <strong>Action Mode</strong>:
    <ul>
      <li><strong>READ</strong> (No Read Up)</li>
      <li><strong>WRITE</strong> (No Write Down)</li>
      <li><strong>COMBINED</strong></li>
    </ul>
  </li>
  <li>Click <strong>Test Access</strong> to evaluate the access request.<br>
    <img src="./images/step3-MAC-test-access.png" alt="Test Access" width="75%">
  </li>
</ul>

<h5>Step 4 — View Access Decision</h5>

<ul>
  <li>Observe the <strong>Security Ladder Visualization</strong> showing the relative positions of the user and data object.</li>
  <li>The system displays one of the following results:
    <ul>
      <li><strong>Access Granted</strong> — The request satisfies MAC rules.</li>
      <li><strong>Access Denied</strong> — The request violates MAC rules.</li>
    </ul>
  </li>
  <li>The access decision is recorded in the <strong>Activity Log</strong>.<br>
    <img src="./images/step4-MAC-access-result.png" alt="MAC Access Result" width="75%">
  </li>
</ul>