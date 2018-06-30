<h1>Zero-Touch Provisioning of F5 BIG-IP Virtual Edition on KVM</h1>
<h2>Description</h2>
<div class="Item-BodyWrap">
<div class="Item-Body">
<div class="Message userContent">
<div>The <em>ZTP of BIG-IP VE on KVM</em> workflow is used to perform the following:<br /><br /></div>
<div>1) Instantiate F5 BIG-IP Virtual Edition (VE) on a KVM hypervisor.</div>
<div>2) License using either a BIG-IQ or Bring Your Own License (BYOL) key.</div>
<div>3) Integrate the workflow with an ITSM tool &ndash; ServiceNow for approvals and tracking.</div>
<div>4) Do basic provisioning on the new BIG-IP and add it to the AppViewX inventory.</div>
<div>5) Send email notifications regarding the implementation status and the new BIG-IP details.<br /><br />
<h2><strong>Prerequisites</strong></h2>
<div>&nbsp;</div>
<div>To run the&nbsp;<em>ZTP of BIG-IP VE on KVM</em>&nbsp;workflow in your environment, ensure that the following pre-requisites are met:<br /><br />1) Free AppViewX or AppViewX version 12.3.0 has been downloaded and installed.</div>
<div>2) The following devices have been added to the AppViewX inventory - KVM Hypervisor,&nbsp; BIG-IQ, DNS Name server, NTP server, SNMP server, LDAP server, Infoblox</div>
<div>3) A storage pool (/opt/vm/) is available in KVM within which the guest VMs will be created.</div>
<div>4) An image (.qcow2 format) of BIG-IP version 12.1 is available in the KVM home directory.</div>
<div>5) KVM has at least 2 bridges to the external network. One will be used for device management and the other for the VLAN connection.</div>
<div>6) The subnet of an additional interface is managed by the Infoblox IPAM.</div>
<div>7) The management interface given to the VM has a proper DHCP in order to assign an IP address that will be used to access it.</div>
<div>8) The following packages are available in KVM -&nbsp;nmap, routes,&nbsp;brctl,&nbsp;virsh</div>
<div>9) An ITSM device (ServiceNow) has been configured under the Change Management section of the AppViewX Settings module.</div>
<div>10) If the user prefers not to use BIG-IQ, then they have their own registration key.</div>
<div>11) The BIG-IQ has a registration key pool with free licenses activated in it.</div>
<div>12) The time zone of the BIG-IQ and the new BIG-IP VE must be maintained. A device will be added whenever the time difference between the new VE and the BIG-IQ is more than 300 seconds.</div>
<div>13) An SMTP server has been configured under <strong>System</strong> settings in order to receive email notifications.&nbsp;<br /><br /></div>
<h2><strong>Compatible Software Versions</strong></h2>
<div>&nbsp;</div>
<div>The workflow has been tested and validated on the following software versions:</div>
<div>1) AppViewX &ndash; Free AppViewX and AVX 12.3.0</div>
<div>2) ServiceNow &ndash; Geneva, Eureka, Jakarta, and Istanbul<br />3) Infoblox &ndash; Version 7.2.X</div>
<div>4) F5 (both LTM and DNS) &ndash; Version 10.x, 11.x, or 12.x</div>
</div>
</div>
</div>
</div>
