<!--
---
layout: post
title: 小组信息
---


<div class="message">
  The improvement of the OnSchooler project was completed by Liangge Deng.
</div>

## Tools and Technical Approaches

> NuGet package

> Microsoft SQL Server Management Studio

> Google+ API


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

-->
