This Repository hosts of two Websites:

[Tamex Website](https://tamex.com.au)

[Tamex Portal](https://portal.tamex.com.au/)



# Initial Set-up

- Clone Git Repository : 'https://github.com/Soda-Digital/Tamex.git'


# [Tamex Website](https://tamex.com.au)

## Dependencies

	* Version 

		- [.NET Framework 3.1 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/3.1)

		- [node.js 16.x LTS](https://nodejs.dev/download)

## Installation 

	* Building the application :
	'''
		npm install
		npm run webpack
		dotnet build
	'''
		
	* Running the Application :
	'''
		dotnet dev-certs https --trust
		dotnet run
	'''

# [Tamex Portal](https://tamex.com.au)

## Dependencies

	
	* Version
	
		- [.NET Framework 3.1 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/3.1)

		- [node.js 16.x LTS](https://nodejs.dev/download)
		
		- LocalDB 
		
			- Windows Platform
				- Visual Studio 
				- [Standalone Install]( https://docs.microsoft.com/en-us/sql/database-engine/configure-windows/sql-server-express-localdb?view=sql-server-ver15#installation-media )
			
			- [Linux Platform](https://docs.microsoft.com/en-us/sql/linux/sql-server-linux-setup?view=sql-server-ver15#:~:text=1%20Supported%20platforms.%20SQL%20Server%20is%20supported%20on,command%20line.%20%20...%20You%20can...%20More%20)
		 
			- [MacOS Platform](https://www.quackit.com/sql_server/mac/install_sql_server_on_a_mac.cfm#:~:text=Microsoft%20has%20made%20SQL%20Server%20available%20for%20macOS,on%20a%20Mac%20prior%20to%20SQL%20Server%202017%29.)

	* Secrets Management
	
	Refer to 'Tamex Auth0 Client Secret' entry in 1Password 
	
		**Important Note :**
		
## Installation

	* Building the Application :
	'''
	npm install
	npm run webpack
	dotnet build
	'''
	
	* Running the Application
	'''
	dotnet dev-certs https --trust
	dotnet 
	'''
