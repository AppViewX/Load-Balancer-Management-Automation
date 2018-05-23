{\rtf1\ansi\ansicpg1252\cocoartf1561\cocoasubrtf400
{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 <h1>Modular Persona Based Citrix NetScaler Virtual Server Create</h1>\
<h2>Description</h2>\
<p>This workflow will create a virtual server with profiles, monitors, pool, and pool members on Citrix NetScaler ADC. It provides an option to integrate with Infoblox to reserve a free IP address from the available address pools and create DNS binding for the new virtual server. The workflow also provides an option to create a change request ticket in IT Service Management (ITSM) tool called ServiceNow for approvals and tracking. The service request change ID is associated with the work order and is updated based on the implementation status.</p>\
<p><img src="Load-Balancers/Modular Persona based Citrix NetScaler Virtual Server Create/img/Modular Persona based VIP create flow diagram.png" alt="Modular Virtual Server Create Flow diagram " /></p>\
<p>This workflow illustrates the persona based approach which enables self-servicing of service request without losing the control.&nbsp;The Application owners can provision a new application using simple self-serviceable user-form, which gathers the users intent. The workflow translates the intent to ADC object configurations and presents the advanced technical user-form to an admin user for submitting the request. The admin user can update the auto-generated configurations using this advanced user-form. The admin user can select the SLB by checking the real-time performance metrics of the available SLBs using the advanced user-form. The advanced user-form access is restricted to application owner, abstracting the underlining infrastructure level details to the requestor.</p>\
<p>The workflow provides the modularity to change the IPMA vendor from Infoblox to BlueCat and ADC vendor from Citrix to F5 by simply replacing the corresponding sub-workflow in the visual workflow studio. New vendor integration can be added to this workflow by creating or importing vendor specific sub-workflow. With minimal changes the same workflow can be reused, avoiding vendor lock-in. The modular workflow provides the flexibility to build over your existing automation investments.</p>\
<p class="p1">The workflow pre-validates the ADC device performance metrics (such as CPU and memory utilization) and confirms that the new virtual server and associated objects are not present. On successful pre-validation, the configuration changes are reviewed through a two-level approval process: first by ServiceNow, then by AppViewX. After approval is received, the configuration changes are implemented on the ADC device. A post-validation script ensures the virtual server and the associated objects are created successfully on the SLB.</p>\
<h2 class="p1"><strong>Prerequisites </strong></h2>\
<p class="p2">To run this workflow in your environment, the following prerequisites must be met:</p>\
<ul>\
<li class="p3">AppViewX version 12.3.0 has been downloaded and installed.</li>\
<li class="p2">The following devices have been added to the AppViewX inventory:\
<ul>\
<li class="p2">Citrix NetScaler SLB</li>\
<li class="p2">(Optional) Infoblox</li>\
</ul>\
</li>\
<li class="p2">If the default vendor integrations are changed by replacing the sub workflows, corresponding devices should be added to the AppViewX inventory.</li>\
<li class="p3">Each device must be a managed entity in AppViewX.</li>\
<li class="p3">The Application owner role and Network Admin role are created and mapped with respective users.</li>\
<li class="p3">The Application owner role has 'submit' permissions and Network Admin role has 'review' permissions assigned in simple user-forms pallet settings.&nbsp;</li>\
<li class="p2">(Optional) An ITSM tool, ServiceNow has been configured under the Change Management section of the AppViewX Settings module.</li>\
</ul>\
<p class="p5">&nbsp;</p>\
<h2 class="p1"><strong>Compatible Software Versions </strong></h2>\
<p class="p2">The workflow and sub-workflows have been validated for the following software versions:</p>\
<ul>\
<li class="p3">AppViewX v12.3.0</li>\
<li class="p3">Citrix v11.x and v12.x</li>\
<li class="p3">Infoblox v7.2.x</li>\
<li>F5 (LTM) v11.x, v12.x, and v13.x</li>\
<li class="p2">BlueCat v8.1.0</li>\
</ul>\
<p class="p1">&nbsp;</p>}