  Visitor Management System (VMS)

A web-based Visitor Management System built with ASP.NET Web Forms and C#. It enables organizations to register visitors, manage check-ins/check-outs, and monitor visits. Administrators and receptionists can log in to approve visitors, scan QR-coded badges, track visit logs, and view analytics, while visitors can register their details and receive a QR code badge.

Key Features

Visitor Registration: Visitors can enter personal and visit details (name, contact, purpose, etc.) through a registration form.

Admin Approval: Administrators review pending visitor requests and approve or reject them.

QR Code Badges: Upon approval, the system generates a QR code badge for the visitor (using the QRCoder library).

Check-In/Check-Out: Reception staff can scan the visitor’s badge (or enter the badge ID) to log check-in and check-out times.

Visit Analytics: Dashboard displays statistics (e.g. total visitors, daily/monthly trends) for administrators and receptionists.

Contact Messages: Visitors can submit contact inquiries, which admins can view in a messaging panel.

Role-Based Access: Separate interfaces for Admin and Reception users, with login authentication.

Technology Stack

ASP.NET Web Forms (C#, .NET): Uses Microsoft’s ASP.NET Web Forms framework (included with Visual Studio)
learn.microsoft.com
 on the .NET Framework. This event-driven model simplifies dynamic page development
learn.microsoft.com
learn.microsoft.com
.

.NET Framework 4.8: The project targets .NET Framework 4.8 (C#)
learn.microsoft.com
.

Frontend: HTML5, CSS for styling, and the QRCoder library for generating QR codes for visitor badges.

Database: Microsoft SQL Server (Express). A local SQL database stores tables for users, visitors, check-in logs, etc.

Folder Structure

The repository is organized as follows:

VMS/                   # Solution root
├─ .vs/                # Visual Studio settings folder (local files)
├─ packages/           # NuGet package cache (compiler and framework tools)
├─ VMS/                # ASP.NET Web Forms project directory
│   ├─ Admin.aspx, Login.aspx, Register.aspx, etc.   # WebForms pages
│   ├─ GenerateQR.ashx                                 # HTTP handler for QR code images
│   ├─ Styles/ (CSS files for styling)
│   ├─ QR/ (sample QR code images)
│   ├─ Uploads/ (uploaded profile images)
│   ├─ bin/ (compiled DLLs, including QRCoder.dll)
│   ├─ obj/ (build artifacts)
│   ├─ Web.config, Global.asax, VMS.csproj            # Config and project files
├─ VMS.sln            # Visual Studio solution file
└─ 29_07_2025_sql.sql # SQL script to create the “Reg” database and tables

Prerequisites

Visual Studio 2019 or later with the ASP.NET and web development workload installed
learn.microsoft.com
.

.NET Framework 4.8 (the project is built targeting .NET 4.8).

Microsoft SQL Server or SQL Server Express for the database. (The connection string uses .\SQLEXPRESS by default.)

Git (to clone the repository) and any tool (e.g. SSMS or Visual Studio) to run the SQL script.

Setup Instructions

Clone the repository:

git clone https://github.com/YourUsername/VMS.git
cd VMS


Open the solution: Launch Visual Studio and open VMS.sln. Visual Studio will restore NuGet packages (see packages/ folder).

Configure the database:

Open SQL Server (or SQL Server Management Studio) and create a new database named Reg.

Execute the SQL script 29_07_2025_sql.sql (located in the repository root) against this database. This will create the required tables (Users, Book, CheckInLog, ContactMessages, Details, etc.).

Ensure the connection string in VMS/Web.config matches your SQL Server instance. By default it is:

Data Source=.\SQLEXPRESS;Initial Catalog=Reg;Integrated Security=True;


Modify Data Source or Initial Catalog if needed for your environment.

Build the project: In Visual Studio, clean and rebuild the solution (Build > Rebuild Solution).

Run the application: Start the web app in debug mode. In Visual Studio select the IIS Express button or press F5 to launch the site locally
learn.microsoft.com
. A browser window should open at the home page.

Building and Running Locally

With the prerequisites installed and the database configured, you can run the app locally using Visual Studio:

In Visual Studio’s toolbar, click the IIS Express (or Play) button to start debugging
learn.microsoft.com
.

Alternatively, press F5 (start debugging) or Ctrl+F5 (start without debugging) to build and launch the application.

The site will open in your web browser. Navigate through pages like Login, Register, and the Admin/Reception dashboards to verify functionality.

Contributing

This is currently a solo project. However, contributions and suggestions are welcome! Feel free to fork the repository and submit pull requests. When contributing, please ensure code follows the existing style and is thoroughly tested.

License

This project is licensed under the MIT License. (See the LICENSE file or the official MIT License for details.)

Sources: Project code and structure analyzed from the provided ASP.NET Web Forms application; technology references from Microsoft documentation
