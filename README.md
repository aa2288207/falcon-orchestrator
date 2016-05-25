![Logo](https://cloud.githubusercontent.com/assets/15896631/15528891/62e1f582-2216-11e6-85cd-b34ea9755c87.png)
<p align="center">
Falcon Orchestrator is a monolithic windows stack application that provides workflow automation, case management and security response functionality.  The tool leverages the highly extensible APIs contained within the Falcon Connect program.
</p>

# Development

Being a Windows based application, the tool was developed with the use of .NET 4.5, C#, ASP.NET MVC 4, Entity Framework and PowerShell.  If forking or cloning the repository, please note the code was written with Visual Studio 2015. Compatibility with earlier Visual Studio versions can be problematic.

# Third Party Libraries

The following external libraries are used within the project.  These are not provided via the GitHub repository, if building from source you will need to right click on the solution file in Visual Studio and select _Restore NuGet Packages_.

* HighCharts - Javascript charting library
* HighCharts.NET - .NET wrapper for HighCharts
* DotNetZip
* JSON.NET
* AutoMapper
* Log4Net
* WIX


# Project Structure

The solution is composed of 7 projects/modules, each providing specific functionality to the overall application. Each project is prepended with the project name _FalconOrchestrator_.

 Name     | Type | Description
 ---------|------|-----------
Client    | Windows Service | This is an ETL service that is responsible for connecting to the Falcon Host Streaming API, consuming detection events and executing the configured workflow logic against those events.
DAL       | Class Library | Centralized library using Entity Framework for common database access related tasks
Installer | Setup Project | WIX project used to build full application into an MSI installer for simplified deployment.
LDAP      | Class Library | Centralized library for performing activity related to Active Directory integration.
Forensics | Class Library | Centralized library that manages PowerShell's Remoting calls to execute pre-defined actions.
IOC       | Class Library | Library managing calls to and from the Falcon Host Management API for indicators.
Web       | ASP.NET Web Application | MVC based web application to provide user interface for interacting with the system.


# Support

As an open source project this software is not officially supported by CrowdStrike.  As such we ask that you please refrain from sending inquiries to the CrowdStrike support team.  The project maintainers will be working with active community contributors to address bugs and supply new features.
If you have identified a bug please submit an issue through GitHub by following the contribution guidelines.  You can also post questions or start conversations on the project through our [community forums](http://community.crowdstrike.com) page.

# Contribution

Contribution is key to the successs of any open source project.  As such we highly recommend you get involved and help us to make the tool better for everyone!  For guidelines on contributing refer to [CONTRIBUTING.md](https://github.com/CrowdStrike/falcon-orchestrator/blob/master/CONTRIBUTING.md) 


# License

All code in this repository (unless otherwise specified in the source file) is licensed under the Affero GPLv3 license.

Refer to [LICENSE.md](https://github.com/CrowdStrike/falcon-orchestrator/blob/master/LICENSE.txt) for more information.
