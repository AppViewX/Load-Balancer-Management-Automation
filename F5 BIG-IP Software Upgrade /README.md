<h1><strong>F5 BIG-IP Software Upgrade&nbsp;</strong></h1>
<h2>Description</h2>
<p>The <em>F5 BIG-IP Software Upgrade </em>workflow upgrades the major and minor versions of BIG-IP. Also, the user will get a report with the object details before and after the upgrade.<span class="Apple-converted-space">&nbsp;</span></p>
<h2><strong>Prerequisites<span class="Apple-converted-space">&nbsp;</span></strong></h2>
<p>To run this workflow in your environment, the following prerequisites must be met:<span class="Apple-converted-space">&nbsp;</span></p>
<ul>
<li>Software image for the upgrade must either be available on the AppViewX server or in the SFTP server.<span class="Apple-converted-space">&nbsp;</span></li>
<li>The device must have bash access.<span class="Apple-converted-space">&nbsp;</span></li>
<li>Free AppViewX or AVX 12.3.0 has been downloaded and installed.<span class="Apple-converted-space">&nbsp;</span></li>
<li>An F5 LTM device has been added to AppViewX as a managed device.<span class="Apple-converted-space">&nbsp;</span></li>
</ul>
<h2><strong>Compatible Software Versions<span class="Apple-converted-space">&nbsp;</span></strong></h2>
<p>The application provisioning automation temples have been validated for the following software versions:<span class="Apple-converted-space">&nbsp;</span></p>
<ul>
<li>AppViewX &ndash; Free AppViewX and AVX 12.3.0<span class="Apple-converted-space">&nbsp;</span></li>
<li>ServiceNow &ndash; Eureka, Istanbul, and Jakarta<span class="Apple-converted-space">&nbsp;</span></li>
<li>F5 LTM &ndash; version 11, 12, and 13<span class="Apple-converted-space">&nbsp;</span></li>
</ul>
<p>&nbsp;</p>
<h2><strong>Limitations<span class="Apple-converted-space">&nbsp;</span></strong></h2>
<ul>
<li>This workfow will work for F5 BIG-IP software upgrades of minor or hotfix versions 11.x, 12.x, or 13.x.<span class="Apple-converted-space">&nbsp;</span></li>
<li>F5 BIG-IP versions from 11.1 to 11.4 may have issues based on complexity of the configurations.<span class="Apple-converted-space">&nbsp;</span></li>
<li>This workflow has been tested only for the LTM and GTM modules.<span class="Apple-converted-space">&nbsp;</span></li>
<li>F5 ASM and AFM module upgrade may work, but it was not tested</li>
<li>F5 BIG-IP known issues published for software upgrades apply here</li>
<li>The F5 BIG-IP target software version must be the same or later than the software version of the source.<span class="Apple-converted-space">&nbsp;</span></li>
</li>
</ul>
<p><strong>Note: </strong>If the checksum for the F5 BIG-IP image in source and destination after SCP (only for SFTP) is different, no action will be triggered. In such cases, image will not be displayed during the installation, which may lead to workflow failure.<span class="Apple-converted-space">&nbsp;</span></p>
