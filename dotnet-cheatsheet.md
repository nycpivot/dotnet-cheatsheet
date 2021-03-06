# .NET CHEATSHEET

The purpose of this document is to enable solutions engineers, platform architects, developers, operators, and security and infrastructure SMEs gain a high-level overview of the most popular Microsoft offerings. For more in-depth use cases that are VMware/Pivotal specific, consult the [.NET Cookbook](https://dotnet-cookbook.cfapps.io/intro/). This is to provide a quick knowledge check with a customer introducing these products.

## PRE .NET (COM, COM+)

### Classic ASP (Active Server Pages)

- Released in 1998.
- Minimal production usage (seen at an EY POC mid 2018).
- Files end with .asp extension.
- Based on VBScript (or Javascript).
- Code is interpreted at runtime.
- Object creation requires COM & Windows Registry (DLL Hell).


## .NET FRAMEWORK (4.8 final version)

### ASP.NET WebForms

- Officially released in 2002.
- Continued support through .NET Framework 4.8.
- Wide and broad production usage.
- Introduction of C# (supports VB and C#).
- Drag-and-drop designer (like Windows Forms, aka, WinForms).
- Files end with .aspx extension.
- Precompiled, code-behind modules.
- Underlying concepts of raw HTTP verbs are abstracted.
- HTML abstracted by server controls (runat=server) mixed with HTML elements.
- ViewState dictionary maintains form and control state with server.
- Web.Config externalizes common settings and configurations.
- Windows and Forms-based authentication.
- Rapid Application Development (RAD).

### ASP.NET Web Services

- Officially released in 2002.
- Continued support through .NET Framework 4.8.
- Production usage uncertain.
- Support of XML SOAP Web Services.
- Easily expose and consume XML data over HTTP.
- Files end with .asmx extension.
- Wizards create proxies in consuming applications.
- Web.Config externalizes common settings and configurations.
- Windows and Forms-based authentication.
- Rapid Application Development (RAD).

### WCF (Windows Communication Foundation)

- Officially released in 2006.
- Introduced with .NET Framework 3.0.
- Continued support through .NET Framework 4.8.
- Wide production usage.
- More powerful than asmx at the cost of complexity.
- Bindings for TCP, Named Pipes, MSMQ.
- Three hosting options 1) IIS, 2) Windows Service, or 3) Self-hosted.
- Complex configuration.

### WPF (Windows Presentation Foundation)

- Officially released in 2006.
- Evolution of desktop applications.
- Very rich and advanced GUI development.
- Frequently employed in financial trading.

	*DESKTOP ONLY! NOT A CANDIDATE FOR CONTAINERIZATION. HERE FOR REFERENCE ONLY.*


## .NET FRAMEWORK & CORE

### ASP.NET MVC

- Officially released in 2007.
- Continued support through .NET Framework 4.8.
- Wide production usage.
- Better separation of concerns (in comparison to WebForms).
- More flexibility at the HTTP and HTML levels (less abstraction).
- Controller methods align closer to HTTP verbs.

### ASP.NET WebAPI

- Officially released in 2012.
- Might see remnants of WCF API.
- Continued support through .NET Framework 4.8.
- Wide production usage.
- Adoption of HTTP RESTful principles.
- Core HTTP constructs (verbs, response status codes, etc).
- An alternative to complex WCF abstractions and configurations.

### Windows Services

- A background process, much like a Linux daemon.
- Project specific template, configuration, deployments.
- Tightly integrated into the core Windows administrative services.
- Scheduling, security, system event logs.

### Console

- Text-based command line.
- Simpler alternative to Windows services.
- Usually launched from Task Scheduler.


## IDE

### Visual Studio

- Powerful code editor (C#, VB, F#, C++).
- Project templates (MVC, API, Console).
- Most popular tool for the vast majority of .NET developers.
- Too heavy for some tasks.

### Visual Studio Code

- Lightweight code editor.
- Great for scripting.
- Command terminal.
- Large library of plugin components.
- Cross platform.


## SOURCE CONTROL

### Visual Source Safe

- The first Microsoft source code control.
- Production usage unknown.
- Internal network only.
- Discontinued.

### Azure DevOps

- First known as Visual Studio Team Services (VSTS), then Team Foundation Server (TFS).
- Complete application lifecycle management.


## DATABASES

### MS Access

- Popular database pre .NET.
- Minimal production usage (seen at an EY POC mid 2018).

### SQL Server

- Enterprise RDBMS.
- Wide production usage.
- Windows Authentication.
- SQL Server Authentication.

### Entity Framework

- Object Relational Mapper (ORM).
- Wide production usage.
- Database First support.
- Code First support.
- Builtin automatic migrations (app runs migrations when executed).


## OPERATING SYSTEMS & SERVICES

### Windows

- Windows Server Desktop Experience (GUI), Server Core (command line), Nano.
- Long-Term Service Channels (LTSC) are initial releases (2016, 2019).
- Semi-Annual Channels (SAC) are bi-annual releases from an initial release.
- Active Directory (AD), Active Directory Domain Services (AD DS).
- Windows Authentication.

### IIS (Internet Information Server)

- Windows only.
- Website hosting.
- Windows authentication integration.
- Wide variety of features and integrations with Windows.


## AZURE

### App Services

- Publish (Push) from Visual Studio.
- Configuration Management.
- Authentication/Authorization.
- Deployment Slots (Blue/Green).


## PIVOTAL

### Buildpacks

- dotnet_core_buildpack, .NET Core onLinux only.
- binary_buildpack, .NET Core on Windows only.
- hwc_buildpack, .NET Framework on Windows only, IIS dependent apps.
