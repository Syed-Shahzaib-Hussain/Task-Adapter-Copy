---
layout: docs
title: Installation
permalink: /docs/installation/
---

<p>First, <a href="/download">download Task Adapter application</a>.</p>
<p>Unfortunately, recent Google Chrome versions started marking the distributive as "uncommon" because of 2 start scripts we include in it (one for Windows and one for Linux/MacOS). Oh sweet sweet Google... If your browser complains about the distributive, click the arrow on the right and use "Keep" menu item:</p>
<p><a href="http://www.taskadapter.com/wp-content/uploads/2012/05/chrome_warning.png"><img class="alignnone size-full wp-image-776" src="http://www.taskadapter.com/wp-content/uploads/2012/05/chrome_warning.png" alt="chrome_warning" width="544" height="129" /></a></p>
<p>Feel free to explore the start scripts in "bin" folder before launching them: they simply check if minimum Java version is present on your computer and then launch the app.</p>
<p>Unpack the distributive into any folder (any modern operating system can open ZIP files).</p>
<p><a href="http://www.taskadapter.com/wp-content/uploads/2012/05/install.png"><img class="alignnone size-full wp-image-444" title="install" src="http://www.taskadapter.com/wp-content/uploads/2012/05/install.png" alt="install task adapter" width="607" height="131" /></a></p>
<p>Open the folder where you unpacked the application to, then open "bin" sub-folder and run "launcher.bat" (for Windows) or "launcher" (for Linux and Mac OS).</p>
<p><a href="http://www.taskadapter.com/user-guide/installation/launcher/" rel="attachment wp-att-565"><img class="alignnone size-full wp-image-565" src="http://www.taskadapter.com/wp-content/uploads/2012/05/launcher.png" alt="launcher" width="384" height="148" /><br />
</a><br />
A default Internet browser will be automatically started and opened with "<strong>http://localhost:10842/ta</strong>" &nbsp;URL.</p>
<p>Note that the <strong>default port</strong> for Task Adapter web application is <strong>10842</strong>.</p>
<h3>Changing port number.</h3><br />
The port number Task Adapter will use for embedded HTTP server can be provided in command line parameters:</p>
<div style="padding-left: 30px;"><em>launcher --port=9977<b><br />
</b></em></div><br />
Or set it in "launcher.bat" &nbsp;(Windows) and "launcher" files (Linux and Mac OS):</p>
<p style="padding-left: 30px;"><em>&nbsp;@rem Execute launcher</em></p></p>
<div style="padding-left: 30px;">
<div style="padding-left: 30px;"><em>"%JAVA_EXE%" %DEFAULT_JVM_OPTS% %JAVA_OPTS% %LAUNCHER_OPTS% &nbsp;-classpath "%CLASSPATH%" com.taskadapter.launcher.<wbr />TALauncher %CMD_LINE_ARGS% --<wbr />openTaskAdapterPageInWebBrowse<wbr />r <strong>--port=9977</strong></em></div><br />
</div><br />
The default account name is "<strong>admin</strong>" and password is "<strong>admin</strong>".</p>
<p>Use "<strong>Configure</strong>" link in the page header to change system-wide settings.<img class="alignnone size-full wp-image-446" title="settings" src="http://www.taskadapter.com/wp-content/uploads/2012/05/settings.png" alt="" width="514" height="344" /></p>
<p>Set<strong> "Local / server" mode</strong> setting to "LOCAL" if you are running Task Adapter on your local machine. "Server" mode is used for a shared installation when multiple users will need to connect to this Task Adapter. "Server" mode will require you to UPLOAD your Microsoft Project files to Task Adapter server before it can load them and then save to a system like Jira, Redmine or Github.</p>
<p>"admin" user can add/delete other users accounts and reset their passwords. Users can only access Microsoft project files uploaded or created by them.</p>
<p>User data is stored in <user home>/taskadapter folder. Sample value for Windows OS: c:\users\myusername\taskadapter\...</p>
