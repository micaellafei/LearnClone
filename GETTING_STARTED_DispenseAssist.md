## Project Onboarding Checklist 
  * Check access to the following 
- [ ] O365
- [ ] 1Password
- [ ] Github Repository
- [ ] Shortcut
- [ ] Timely


# Dispense Assist

## Dependencies

* Version
	
	- [.NET Framework 3.1 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/3.1)

	- [node.js 16.x LTS](https://nodejs.dev/download)
		
	- LocalDB :
		
		<details><summary>Windows Platform</summary>
		<p>

		##### [Standalone Install]( https://docs.microsoft.com/en-us/sql/database-engine/configure-windows/sql-server-express-localdb?view=sql-server-ver15#installation-media)

		##### Using Visual Studio 

		> Alternatively, you can install LocalDB through the Visual Studio Installer, as part of the Data Storage and Processing workload, the ASP.NET and web development workload, or as an individual component.

		</p>
		</details>

		<details><summary>Linux Platform</summary>
		<p>

		> You may refer to this Microsoft documentation for more information on install SQL Server on Linux Platforms : [SQL Server on Linux](https://docs.microsoft.com/en-us/sql/linux/sql-server-linux-setup?view=sql-server-ver15#:~:text=1%20Supported%20platforms.%20SQL%20Server%20is%20supported%20on,command%20line.%20%20...%20You%20can...%20More%20)

		</p></details>

		<details><summary>MacOS Platform</summary>
		<p>

		> You may refer to this article for steps in installing SQL server for MacOS Platforms :
		[Install SQL Server on a Mac](https://www.quackit.com/sql_server/mac/install_sql_server_on_a_mac.cfm#:~:text=Microsoft%20has%20made%20SQL%20Server%20available%20for%20macOS,on%20a%20Mac%20prior%20to%20SQL%20Server%202017%29.)

		##### ***Note :***
		> The steps above will not work on Apple M1 chips.

		</p>
		</details>
    
 * Secrets Management
  1. Navigate to `<RepoLocation>\src\DispenseAssist.Platform\` and open `Appsettings.json`
  2. Update file with Secrets from **1Password** under `Dispense Assist - Dev Secrets`
  
## Initial Set-up

1.  Clone Git Repository : https://github.com/Soda-Digital/DispenseAssist.git
2.  **Open** the `DispenseAssist.sln` file in the root directory using either Visual Studio or VS Code.
3.  **Build** the solution.

## Building and Running the Application

1. Launch Windows Terminal and navigate to `<RepoLocation>\DispenseAssist\src\DispenseAssist.Platform` folder

2. Run the following commands :
  ```
  npm install
  dotnet run watch
  ```
3. **Open** browser and navigate to https://localhost:50551/Identity/Account/Login
    > This should display a login page along with the default Admin credentials


