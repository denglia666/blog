---
layout: post
title: All workflows
---


<div class="message">
  The improvement of the OnSchooler project was completed by Liangge Deng.
</div>

## Tools and Technical Approaches

> NuGet package

What needs to be confirmed in advance is that this project is based on the ASP.NET platform to build Web applications and services. NuGet package is a tool that cannot be bypassed, and it will even accompany the entire development process. When a developer tries to generate a solution for this project in Microsoft Visual Studio, a bunch of errors and warnings are bound to be generated. The reason is that the NuGet package is not installed. Make sure that the following NuGet packages are installed and correspond to the same version. It is worth noting that the NuGet package should not be updated to the latest version. Because the previous team used the old version.
	- EntityFramework v5.0.0
	- Microsoft.AspNet.Mvc v4.0.20710
	- Microsoft.AspNet.Web.Optimization v1.1.3
	- Microsoft.AspNet.WebApi v4.0.20710
	- Microsoft.AspNet.WebPages v2.0.20710
	- Microsoft.Web.Infrastructure v1.0.0

> Microsoft SQL Server Management Studio

In order to connect to the database and log in the user, the developer needs to obtain the BACPAC file from the project partner. Developers need to install sqlserver2019 and SQL Server Management Studio (SSMS). Use SSMS import database. The last step is to open Microsoft Visual Studio and find the connection database in the toolbar.

> Google+ API

Using Google sign in is a sign-in method other than connecting to the database and logging in directly. Due to a version issue that was not available before, it has now been fixed by our team. Migrating from the old Google+ API to the new Google API. This user login method is more suitable for developers who use macOS. Because downloading SQL Server 2019 Developer and SQL Server Management Studio directly is not feasible for developers using macOS, you must download docker, which brings a lot of trouble.

The above are the main tools used by our team. As phase 2 of a project, these tools are necessary and have nothing to do with our satisfaction or dissatisfaction. If this project is started by us from phase 1, maybe we need to evaluate how some tools can be more helpful. The main work of our term is to modify the codebase according to the needs of the project partner. We use black box testing to directly test whether bugs have been fixed or UI/UX improved.

### Pseudo-code

Modifications have been made to the menu bar to improve the user's guidance experience.

{% highlight js %}
SqlException: Cannot open server'dxke0yxj7h' requested by the login. Client with IP address '183.167.6.41' is not allowed to access the server. To enable access, use the Windows Azure Management Portal or run sp_set_firewall_rule on the master database to create a firewall rule for this IP address or address range. It may take up to five minutes for this change to take effect.
Modify the connection string of web.config (ICP.WEB) and APP.config (ICP.DATAACESS) to
<add name="CurriculumEntities"
            connectionString="metadata=
                res://*/ICP.csdl|res://*/ICP.ssdl|res://*/ICP.msl;<!--Add metadata, no need to change-->
                provider=System.Data.SqlClient;
                provider connection string=&quot;data source=FZX;initial catalog=StudentCopy;persist security info=True;user id=sa;password=12345;MultipleActiveResultSets=True;App=EntityFramework&quot;"<!--Database address, database name and username and Password needs to be changed -->
            providerName="System.Data.EntityClient" />
Modify the cshtml file of ICP.WEB/Areas/Site/VIew/shared, comment out the two li
Modify ICP.WEB/Views/shared/_SiteDashboardHeader.cshtml to add
<li><a href="@Url.Action("Index", "CreditAccount", new {area = "Site" })"8>Credit Account</a></li>
{% endhighlight %}





-----


