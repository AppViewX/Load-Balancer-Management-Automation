<h1>Modular Multi-Vendor Persona Based Virtual Server Creation</h1>
<h2>Description</h2>
<p>The Modular Persona Based Virtual Server Creation workflow is used to create a virtual server with profiles, monitors, pool, and pool members in F5 Big-IP LTM. The IP Address Management (IPAM) devices like Infoblox is integrated to this workflow, which allows the users to reserve a free IP address from the available address pools and create DNS binding for the new virtual server. Also, the workflow allows the users to create a change request tickets in IT Service Management (ITSM) tool called ServiceNow for approvals and tracking. The service request change ID is associated with the work order and is updated based on the implementation status.<span class="Apple-converted-space">&nbsp;</span></p>
<p><img src="https://github.com/AppViewX/Load-Balancers/blob/master/Modular%20Persona%20based%20F5%20BIG-IP%20Virtual%20Server%20Create/img/Modular%20Persona%20based%20VIP%20create%20flow%20diagram.png" alt="workflow" /></p>
<p>The workflow provides modularity to change the IPAM vendor from Infoblox to BlueCat, the ADC vendor from Citrix to F5, and vice versa by replacing the corresponding subflow in the workflow studio. The vendors can be integrated with this workflow by creating or importing a vendor specific subflow. The same workflow can be reused with minimal changes to avoid the vendor lock-in and it has the flexibility to build over your existing automation investments.<span class="Apple-converted-space">&nbsp;</span></p>
<p>A persona based approach enables the Application owner to capture the intent and provision a new application using the simple self-serviceable user form. The self-service user form abstracts the underlining network infrastructure level details from the end user and translates it to vendor specific configuration, which is then displayed to the admin user in the advanced user form.<span class="Apple-converted-space">&nbsp;</span></p>
<p>The admin user can perform the following using the advanced user-form:<span class="Apple-converted-space">&nbsp;</span></p>
<ul>
<li>Select the LTM or SLB device by checking the real-time performance metrics of the available LTM(s) or SLB(s).<span class="Apple-converted-space">&nbsp;</span></li>
<li>Update the auto-generated configurations such as load balancing method, add a new application server and so on.<span class="Apple-converted-space">&nbsp;</span></li>
</ul>
<p>The work order pre-validates the LTM or SLB device performance metrics (such as CPU and memory utilization) and confirms that the new virtual server and its associated objects are not available. On successful pre-validation, the configuration changes are reviewed through a two-level approval process: first by ServiceNow, then by AppViewX. After approval is received, the configuration changes are implemented on the device. A post-validation script ensures the virtual server and its associated objects are created successfully on the respective device.<span class="Apple-converted-space">&nbsp;</span></p>
<h2><strong>Prerequisites</strong></h2>
<div>
<p>To run this workflow in your environment, the following prerequisites must be met:<span class="Apple-converted-space">&nbsp;</span></p>
<ul>
<li>AppViewX version 12.3.0 has been downloaded and installed.<span class="Apple-converted-space">&nbsp;</span></li>
<li>The device corresponding to the vendor subflow must be added to the AppViewX inventory. The following devices have been added to the AppViewX inventory:<span class="Apple-converted-space">&nbsp;</span>
<ul>
<li>F5 LTM or Citrix SLB<span class="Apple-converted-space">&nbsp;</span></li>
<li>(Optional) Infloblox or BlueCat<span class="Apple-converted-space">&nbsp;</span></li>
</ul>
</li>
<li>Each device must be a managed entity in AppViewX.<span class="Apple-converted-space">&nbsp;</span></li>
<li>The Application user role and Network admin role are created and mapped with respective users.<span class="Apple-converted-space">&nbsp;</span></li>
<li>In the simple user-form palate settings, the Application owner has been assigned with 'submit' permissions and Network admin has been assigned with 'review' permissions.<span class="Apple-converted-space">&nbsp;</span></li>
<li>The subflows has been assigned with respective roles.<span class="Apple-converted-space">&nbsp;</span></li>
<li>(Optional) An ITSM tool, ServiceNow has been configured under the Change Management section of the AppViewX Settings module.<span class="Apple-converted-space">&nbsp;</span></li>
</ul>
</div>
<h2><br /><strong>Compatible Software Versions</strong></h2>
<div>
<div>
<p>This workflow has been validated for the following software versions:<span class="Apple-converted-space">&nbsp;</span></p>
<ul>
<li>AppViewX &ndash; v12.3.0<span class="Apple-converted-space">&nbsp;</span></li>
<li>F5 (LTM) &ndash; v11.x, v12.x, and v13.x<span class="Apple-converted-space">&nbsp;</span></li>
<li>Citrix &ndash; v11.x and v12.x<span class="Apple-converted-space">&nbsp;</span></li>
<li>Infoblox &ndash; v7.2.x<span class="Apple-converted-space">&nbsp;</span></li>
<li>BlueCat &ndash; v8.1.0<span class="Apple-converted-space">&nbsp;</span></li>
<li>ServiceNow &ndash; Geneva, Eureka, Istanbul, and Jakarta<span class="Apple-converted-space">&nbsp;</span></li>
</ul>
</div>
</div>
