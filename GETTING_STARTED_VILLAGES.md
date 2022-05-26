## Project Onboarding Checklist 
  * Check access to the following 
- [ ] O365
- [ ] 1Password
- [ ] Github Repository
- [ ] Shortcut
- [ ] Timely


# Villages Directory Set-up Guide

## Dependencies
	
* Version
	
	- [.NET Framework 6.0 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-6.0.300-windows-x64-installer)
	- [node.js 16.x LTS](https://nodejs.dev/download)
	- [Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver16)
	   > Azure Data Studio supports Windows, Linux and macOS, except systems with the ARM architecture.
	- Admin Pack for SQL Server
     		 > After installing Azure Data Studio, install **Admin Pack for SQL Server** from Extensions:Marketplace
     		  ![image](https://user-images.githubusercontent.com/100733950/170428089-dd23b861-0753-4732-a87c-c1b5430e763f.png)

	- Docker Desktop
      - [Install Docker Desktop on Linux](https://docs.docker.com/desktop/linux/install/)
      - [Install Docker Desktop on Mac](https://docs.docker.com/desktop/mac/install/)
      - [Install Docker Desktop on Windows](https://docs.docker.com/desktop/windows/install/)

  
## Initial Set-up

1.  Clone Git Repository : https://github.com/Soda-Digital/villages-directory
2.  Pull up a terminal and navigate to the root directory of the Villages-Directory repository
3.  Run `docker compose up` 
    > This may take a few minutes when runniong it the first time. Wait for this process to finish before proceeding to the next step.
4.  Open **Azure Data Studio**, go to **Connections** or `Ctrl+Shift+D`
5.  Create a New Connection. Mulitple options to do this, see image below for reference :
	 ![image](https://user-images.githubusercontent.com/100733950/170425995-65ab7eb2-5187-4ed6-808f-5366a182eb8b.png)
6. Fill in all required data and click **Connect** as shown in the image below 
	![image](https://user-images.githubusercontent.com/100733950/170431935-6bbf9573-e3cd-4e8a-8f78-585732105f76.png)

	<details><summary> SQL Credentials </summary>
 	 <p> 
	  
  	 	Username : sa
  		Password : yourStrong(!)Password
    
 	 </p>
	</details>
	> Make sure that Docker Desktop is running successfully to avoid unexpected errors.
7. Once Successfully connected to the database, proceed with importing **.bacpac** file.
	- Click **Server** > Right-click **Databases** > **Data-Tier Application Wizard**. See details and next steps in images below
		1. ![image](https://user-images.githubusercontent.com/100733950/170432784-44691578-c1fd-40bc-acf3-bd425155e72b.png)
		2. ![image](https://user-images.githubusercontent.com/100733950/170433184-e0c1f6dc-6b33-475f-8c13-136503361467.png)
		3. ![image](https://user-images.githubusercontent.com/100733950/170433219-23d5722c-5b3c-48ea-a5b3-49fab15d4c5c.png)
		4. ![image](https://user-images.githubusercontent.com/100733950/170433241-f5ea6557-cd20-4c10-9cc2-2d4dcbafc907.png)

		> NOTES:
		> 
		> **.bacpac** file Location `<RepoLocation>\villages-directory\Concierge.Integration\support\villages-directory.bacpac`
		> Make sure to change **Target Database** name from `villages-directory` to **Villages.Directory** 

## Building and Running the Application
- Refer to each sites for detailed steps 

#### Directory.Admin

- Secrets Management
	- Go to <RepoLocation>\villages-directory\Directory.Admin\ and update `appsettings.Development.json`
	- Use notes found in **1Password** under **(Dev) Villages Directory Admin Auth0**
	
- Setting up Directory Admin Site
	
1. Launch Windows Terminal and navigate to `<RepoLocation>\villages-directory\Directory.Admin` folder
2. Run the following commands :
  ```
 npm install
 npm run dev
  ```
3. **Open** the **"Concierge.sln”** file in the root directory using either Visual Studio or VS Code.
4. **Build** the solution

	
#### Directory.API
#### Concierge.Web
