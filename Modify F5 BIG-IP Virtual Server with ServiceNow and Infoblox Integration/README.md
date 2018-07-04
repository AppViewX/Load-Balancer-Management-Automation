<h1>Modify F5 BIG-IP Virtual Server with ITSM and IPAM Integration</h1>
<h2>Description</h2>
<p>The <em>Modify F5 BIG-IP Virtual Server with ITSM and IPAM Integration </em>automation workflow can add or delete iRules, profiles, monitors, and pool members on an existing virtual server. <br /><br />This workflow filters F5 ADC devices based on the user&rsquo;s access permissions, defined by Role Based Access Control (RBAC), and displays the list of virtual servers available on the selected ADC device. When a virtual server is selected, object details like iRules, profiles, monitors, and pool members are displayed in the form fields. <br /><br />The workflow also provides an option to modify the association of these virtual server objects and allows users to create change request tickets in ITSM systems like ServiceNow for approvals and tracking. The service request change ID is associated with a work order and is updated based on the implementation status.<br /><br />The work order that is generated confirms the existence of the virtual server and its associated objects before any changes are made. On successful pre-validation, the configuration changes are reviewed through a two-level approval process: first by ServiceNow, then by AppViewX. After approval is received, the configuration changes are implemented on the ADC device. A post-validation script ensures the virtual server and the associated objects are modified successfully.<br /><br /></p>
<h2><strong>Prerequisites</strong></h2>
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
<div>The automation workflow has been validated for the following software versions:</div>
<div>1) AppViewX &ndash; Free AppViewX version and AVX 12.3</div>
<div>2) ServiceNow &ndash;&nbsp;Geneva, Eureka, Istanbul and&nbsp;Jakarta</div>
<div>3) Infoblox &ndash; Version 7.2.X</div>
<div>4) F5 LTM &ndash; Version 10.X, 11.X, or 12.X</div>
</div>
