## Project Onboarding Checklist 

- [ ] O365
- [ ] 1Password
- [ ] Github Repository
- [ ] Shortcut
- [ ] Timely


# Bravure

## Initial Set-up

- Clone Git Repository : `https://github.com/Soda-Digital/Bravure.git`

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
		
## Installation

***Pre-Installation :***

 Go to `...\Bravure\src\Bravure` and edit `Program.cs` file, then uncomment out

```
                //db.Database.Migrate();
                //var seeder = scope.ServiceProvider.GetRequiredService<SampleDataSeeder>();
                //await seeder.SeedDataBase(true);		
```
Update `appsettings.json` with correct connection string

```
"ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=Bravure;Trusted_Connection=True;MultipleActiveResultSets=true"
  }
```

***Building the Application :***
```
npm install
npm run webpack
dotnet build
```
	
***Running the Application :***
```
dotnet dev-certs https --trust
dotnet run
```
