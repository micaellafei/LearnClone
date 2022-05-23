## Project Onboarding Checklist 

- [ ] O365
- [ ] 1Password
- [ ] Github Repository
- [ ] Shortcut
- [ ] Timely


# Jennchem

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

* Credentials

	<details><summary> DEV </summary>
  
 	 <p> 
	  
  	 	Username : dev@example.com
  		Password : Admin!@1
    
   
	 > Contains all roles
 	 </p>
	</details>
  
	<details><summary> Admin </summary>
  	<p>
    
		Username : admin@bravure.com.au
		Password : Admin!@1
		
  	</p>
	</details>
  
  	<details><summary> Admin with 2FA </summary>
  	<p>
    
		Username : admin2FA@bravure.com.au
		Password : Admin!@1
		
    > Admin Account with Two Factor Authentication enabled.
  	</p>
	</details>
  
  	<details><summary> Bravure Account </summary>
  	<p>
    
		Username : bravure@bravure.com.au
		Password : Admin!@1
		
  	</p>
	</details>
  
  	<details><summary> Buyer Account </summary>
  	<p>
    
		Username : buyer@example.com
		Password : Admin!@1
		
  	</p>
	</details>
  
  	<details><summary> Seller Account </summary>
  	<p>
    
		Username : seller@example.com
		Password : Admin!@1
		
  	</p>
	</details>
		
## Initial Set-up

1.  Clone Git Repository : `https://github.com/Soda-Digital/Bravure.git`
2.  **Open** the “Jennchem.sln” file in the root directory using either Visual Studio or VS Code
3.  **Build** the solution

#### Setting Up Certificates and Node JS Packages:

  1. **Open** Windows Terminal and navigate to the root Jennchem folder.

  2. **Run** “.\\setup.ps1”
      * Dotnet, npm and node should display a &#9745; indicating they are successfully installed
      * The remaining output should only display warnings
  3. **Run** “.\\generate-certs”
      * If successful, this should display messages containing “valid HTTPS certificate” and “writing RSA key”


## Installation

***Pre-Installation :***

 Go to `...\Jennchem\src\Jennchem.API\Migrations` and edit `20220113022522_seed_inventory.cs` file, then uncomment out

```
            //migrationBuilder.Sql(@"  INSERT INTO [Inventory] 
            //([CreatedAt] ,[PartCode] ,[Description] ,[Unit] ,[InventoryCategoryId] ,[Active] ,[MakeOrBuy])
            //VALUES 
            //(GETDATE(),  'LABOURCREWSUPER',  'Labour - Crew Supervisor',  0,  6,  1,  1),
            //(GETDATE(),  'LABOUROOSCS',  'Any Crew Supervisor labour requested by the minesite outside of the normal roster',  0,  6,  1,  1),
            //(GETDATE(),  'LABOURPHCS',  'Any Crew Supervisor labour requested by the minesite during a public holiday',  0,  6,  1,  1)"
            //);	
```

***Building and Running Frontend :***

1. Launch Windows Terminal and navigate to the root of the Backoffice2 folder
    * \\<RepoLocation\>\\src\\Jennchem.Backoffice2\\
2. Run the following commands :
```
npm install
npm run build
nom run dev
```
3. After a brief delay, the terminal window should display “&#9745; service worker”
4. **Open** a browser and navigate to <https://localhost:3000/>
    * This should display a login page
    * **Click** the <superadmin@superadmin.com> button under the login box
    
  Note: Check if WSL run on correct instance (eg. Ubuntu)




# Soda Digital Jennchem Setup Guide 

*Note: Links and versions accurate at the time of writing 18/11/2020*

*See individual readme documents for more detail*

## Clone & Setup the Jennchem repository

1. **Clone** <https://github.com/Soda-Digital/jennchem.git> using your preferred GIT client

2. **Open** the “Jennchem.sln” file in the root directory using either Visual Studio or VS Code

3. **Build** the solution

## Setup Certificates and NodeJS Packages



## Running the Backend (Jennchem.API)

1. **Open** the Solution in Visual Studio or VSCode and start without debugging (Ctrl-F5).
    * This should bring up a terminal window ending with the message “Application Started”
2. **Open** a browser and navigate to <https://localhost:5000/>
    * A json response with status 404 indicates the backend is running.

## Running the Frontend (Jennchem.Backoffice2)

1. Open Windows Terminal and navigate to the root of the Backoffice2 folder
    * \\<RepoLocation\>\\src\\Jennchem.Backoffice2\\
2. **Run** the command “npm run build”
3. **Run** the command “npm run dev”
4. After a brief delay, the terminal window should display “&#9745; service worker”
5. **Open** a browser and navigate to <https://localhost:3000/>
    * This should display a login page
    * **Click** the <superadmin@superadmin.com> button under the login box
    
  Note: Check if WSL run on correct instance (eg. Ubuntu)
