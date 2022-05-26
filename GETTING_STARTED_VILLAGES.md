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
	- [Admin Pack for SQL Server]
      > After installing Azure Data Studio, install Admin Pack for SQL Server from Extensions:Marketplace
      > 
	- Docker Desktop
      - [Install Docker Desktop on Linux](https://docs.docker.com/desktop/linux/install/)
      - [Install Docker Desktop on Mac](https://docs.docker.com/desktop/mac/install/)
      - [Install Docker Desktop on Windows](https://docs.docker.com/desktop/windows/install/)

  
## Initial Set-up

1.  Clone Git Repository : https://github.com/Soda-Digital/villages-directory
2.  Pull up a terminal and navigate to the root directory of the Villages-Directory repository
3.  Run `docker compose up` 
    > This may take a few minutes, please wait 
4.  Open **Azure Data Studio** 
5.  ![image](https://user-images.githubusercontent.com/100733950/170425995-65ab7eb2-5187-4ed6-808f-5366a182eb8b.png)



## Building and Running the Application

1. 
2. Launch Windows Terminal and navigate to `<RepoLocation>\villages-directory\Directory.Admin` folder

2. Run the following commands :
  ```
  npm install
  
  ```
3. **Open** browser and navigate to https://localhost:50551/Identity/Account/Login
    > This should display a login page along with the default Admin credentials

