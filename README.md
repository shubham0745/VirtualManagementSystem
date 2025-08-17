🚀 Visitor Management System (VMS)

A web-based Visitor Management System built with ASP.NET Web Forms and C#.
It enables organizations to register visitors, manage check-ins/check-outs, and monitor visits.

👥 Roles Supported:

Visitors – Register details and receive a QR badge.

Receptionists – Handle check-ins and check-outs.

Administrators – Approve visitors, manage logs, and view analytics.

✨ Key Features

📝 Visitor Registration – Fill in name, contact, and visit details.

✅ Admin Approval – Approve or reject visitor requests.

🎟 QR Code Badges – Auto-generated with the QRCoder library.

⏱ Check-In/Check-Out – Log entries using badge scanning or ID.

📊 Visit Analytics – Dashboard with daily/monthly visitor stats.

📩 Contact Messages – Visitors can send inquiries to admins.

🔑 Role-Based Access – Separate dashboards for Admin & Reception.

🛠 Technology Stack

ASP.NET Web Forms (C#, .NET Framework 4.8) – Event-driven web development framework.

Frontend: HTML5, CSS, Bootstrap.

QR Code Generation: QRCoder Library.

Database: Microsoft SQL Server (Express).

📂 Folder Structure
VMS/                   # Solution root
├─ .vs/                # Visual Studio settings
├─ packages/           # NuGet packages
├─ VMS/                # Main project folder
│   ├─ *.aspx          # WebForms pages (Admin, Login, Register, etc.)
│   ├─ GenerateQR.ashx # HTTP handler for QR code generation
│   ├─ Styles/         # CSS files
│   ├─ QR/             # QR code images
│   ├─ Uploads/        # Profile uploads
│   ├─ bin/            # Compiled DLLs (incl. QRCoder.dll)
│   ├─ obj/            # Build artifacts
│   ├─ Web.config      # App configuration
│   └─ VMS.csproj      # Project file
├─ VMS.sln             # Solution file
└─ 29_07_2025_sql.sql  # SQL script for database setup

⚡ Prerequisites

Visual Studio 2019+ (with ASP.NET and web development workload)

.NET Framework 4.8

Microsoft SQL Server / SQL Server Express

Git

🏗 Setup Instructions

Clone the repository

git clone https://github.com/YourUsername/VMS.git
cd VMS


Open the solution
Open VMS.sln in Visual Studio.

Configure the database

Create a database named Reg.

Run 29_07_2025_sql.sql to create tables (Users, Book, CheckInLog, etc.).

Update the connection string in Web.config if needed:

Data Source=.\SQLEXPRESS;Initial Catalog=Reg;Integrated Security=True;


Build the project
In Visual Studio: Build > Rebuild Solution.

Run the app

Click IIS Express or press F5.

The web app will open in your browser.

🖥 Running Locally

▶️ Start the project with F5 (debug mode) or Ctrl+F5 (without debug).

Access pages like Login, Register, Admin Dashboard, Reception Dashboard.

🤝 Contributing

This is a solo project right now.
But contributions are welcome! 🎉

Fork the repo

Make your changes

Submit a Pull Request

📜 License

Licensed under the MIT License.
See LICENSE for details.
