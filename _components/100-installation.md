---
layout: docs
title: Installation
permalink: /docs/task-adapter-installation/
---

## Task Adapter installation

First, [download Task Adapter application](/download).

Recent Google Chrome versions started marking the distributive as "uncommon" because of 2 start scripts we include in it
(one for Windows and one for Linux/MacOS). If your browser complains about the distributive,
click the arrow on the right and use "Keep" menu item:

<a href="/images/uploads/chrome_warning.png"><img src="/images/uploads/chrome_warning.png" alt="chrome_warning"/></a>

Feel free to explore the start scripts in "bin" folder before launching them:
they check if minimum Java version is present on your computer and then launch the app.

Unpack the distributive into any folder (any modern operating system can open ZIP files).
<a href="/images/uploads/install.png"><img class="alignnone size-full wp-image-444" title="install" src="/images/uploads/install.png" alt="install task adapter" width="607" height="131" /></a>

Open the folder where you unpacked the application to, then open "bin" sub-folder and run "launcher.bat" (for Windows) or "launcher" (for Linux and Mac OS).

![Task Adapter Launcher](/images/uploads/launcher.png)

A default Internet browser will be automatically opened with **http://localhost:10842/ta** URL.
Note that the **default port** for Task Adapter web application is **10842**.

### Changing port number.

The port number Task Adapter will use for embedded HTTP server can be provided in command line parameters:

{% highlight sh %}
    launcher --port=9977
{% endhighlight %}

Or set it in "launcher.bat" (Windows) and "launcher" files (Linux and Mac OS):

{% highlight sh %}
    @rem Execute launcher
    "%JAVA_EXE%" %DEFAULT_JVM_OPTS% %JAVA_OPTS% %LAUNCHER_OPTS% -classpath "%CLASSPATH%" com.taskadapter.launcher.TALauncher %CMD_LINE_ARGS% --openTaskAdapterPageInWebBrowser --port=9977
{% endhighlight %}

The default account name is "**admin**" and password is "**admin**".

Use "**Configure**" link in the page header to change system-wide settings.
<img class="alignnone size-full wp-image-446" title="settings" src="/images/uploads/settings.png"  width="514" height="344" />

Set **"Local / server" mode** setting to "LOCAL" if you are running Task Adapter on your local machine.
"Server" mode is used for a shared installation when multiple users will need to connect to this Task Adapter.
"Server" mode will require you to UPLOAD your Microsoft Project files to Task Adapter server before it can load them
 and then save to a system like JIRA, Redmine or Github.

"admin" user can add/delete other users accounts and reset their passwords.
Users can only access Microsoft project files uploaded or created by them.

User data is stored in <user home>/taskadapter folder. Sample value for Windows OS: c:\users\myusername\taskadapter