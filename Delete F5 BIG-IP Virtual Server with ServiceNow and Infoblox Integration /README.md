<h1>Delete F5 Virtual Server with ITSM and IPAM Integration</h1>
<h2>Description</h2>
<div class="Item-BodyWrap">
<div class="Item-Body">
<div class="Message userContent">Multiple virtual servers and the associated objects like profiles and monitors can be deleted using the <em>Delete F5 Virtual Server with ITSM and IPAM Integration </em>automation workflow. <br /><br />This workflow filters available F5 ADC devices based on a user&rsquo;s access permissions, defined by Role Based Access Control (RBAC), and displays the list of virtual servers available on the selected ADC device. It provides an option to release the virtual server IP address and delete the DNS records in an IP address management (IPAM) system, such as Infoblox. <br /><br />The workflow can also integrate with ITSM systems such as ServiceNow for approvals and governance. When the form is submitted, a change request is created and the service request change ID is associated with the work order. This is updated based on the implementation status.<br /><br />The first step in the work order is a pre-validation check to see if the virtual server exists. If the server does exist, the configurations needed to delete the virtual server and its associated profiles and monitors are reviewed through a two-level approval process: first by ServiceNow and then by AppViewX. After approval is granted, the virtual server and its unused dependent objects, like profiles and monitors, are deleted. A series of post-validation scripts ensure that the virtual server is deleted and any orphan objects are removed.<br /><br />
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
<h2><br /><strong>Compatible Software Versions</strong></h2>
<div>&nbsp;</div>
<div>
<div>The application provisioning automation workflow have been validated for the following software versions:</div>
<div>1) AppViewX &ndash; Free AppViewX version and AVX 12.3</div>
<div>2) ServiceNow &ndash;&nbsp;Geneva, Eureka, Istanbul and&nbsp;Jakarta</div>
<div>3) Infoblox &ndash; Version 7.2.X</div>
<div>4) F5 LTM &ndash; Version 10.X, 11.X, or 12.X</div>
</div>
</div>
</div>
</div>
