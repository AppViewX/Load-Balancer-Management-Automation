<h1>Create F5 Virtual Server with ITSM and IPAM Integration</h1>
<h2>Description</h2>
<p>The <em>Create F5 Virtual Server with ITSM and IPAM Integration </em>workflow creates a virtual server and associates it with profiles, monitors, pool, and pool members in F5 LTM using Infoblox and ServiceNow integration. <br /><br />It uses a simple, self-service based approach to gather application-provisioning requirements and generate vendor-specific configurations or REST APIs. This self-service workflow filters F5 ADC devices based on the user&rsquo;s access permissions, defined by Role Based Access Control (RBAC). The platform integrates with IPAM systems like Infoblox, which allows users to reserve a free IP address from the available address pools and create DNS binding for the new virtual server in Infoblox. <br /><br />The workflow also includes an option to create or bind existing profiles and monitors to the virtual server and allows users to create change request tickets in ITSM systems like ServiceNow for approvals and tracking. The service request change ID is associated with the work order and is updated based on the implementation status.<br /><br />The work order pre-validates ADC device performance metrics (CPU and memory utilization) and confirms that the new virtual server and associated objects are not present. On successful pre-validation, the configuration changes are reviewed through a two-level approval process: first by ServiceNow, then by AppViewX. After approval is received, the configuration changes are implemented on the ADC device. A post-validation script ensures the virtual server and the associated objects are created successfully.<br /><br /></p>
<h2><strong>Prerequisites</strong></h2>
<div>&nbsp;</div>
<div>To run this workflow in your environment, the following prerequisites must be met:<br />
<div>&nbsp;</div>
<div>1) Free AppViewX or AVX 12.3 is downloaded and installed.&nbsp;</div>
<div>2) An F5 LTM device is added to AppViewX as a managed device.&nbsp;</div>
<div>3) (Optional) An Infoblox device is added to AppViewX.&nbsp;</div>
<div>4) (Optional) ServiceNow is registered to AppViewX.&nbsp;</div>
<div>5) Multiple server nodes are running the application.</div>
</div>
<h2><strong><br />Compatible Software Versions</strong></h2>
<div>&nbsp;</div>
<div>
<div>The automation workflow has been validated for the following software versions:</div>
<div>1) AppViewX &ndash; Free AppViewX version and AVX 12.3</div>
<div>2) ServiceNow &ndash; Geneva, Eureka, Istanbul and&nbsp;Jakarta</div>
<div>3) Infoblox &ndash; Version 7.2.X</div>
<div>4) F5 LTM &ndash; Version 10.X, 11.X, or 12.X</div>
</div>
