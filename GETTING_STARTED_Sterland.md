## Project Onboarding Checklist 

- [ ] O365
- [ ] 1Password
- [ ] Github Repository
- [ ] Shortcut
- [ ] Timely


# Sterland Setup Guide

## Initial Set-up

- Clone Git Repository : `https://github.com/Soda-Digital/sterland-trade-portal.git`

## Dependencies

* Version
	
	- [.NET Framework 3.1 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/3.1)

	- [node.js 16.x LTS](https://nodejs.dev/download)
		
* Credentials
		
## Installation

1.  Browse to the `/trade-portal` directory.

2.  If customizing the build for a client:

    -   Open `public/manifest.webmanifest` to reflect the desired properties of the client:

        -   `name`
        -   `short_name`
        -   `description`
        -   `background_color`
        -   `theme_color`

    -   Open `public/theme/theme.css` and update any required theme properties.

    -   Update any desired imagery (matching image resolution and naming scheme) in:
        -   `/public/icons`
        -   `/public/splash`
        -   `/public/theme`
        -   

3. Navigate to `<Sterland Folder location>/trade-portal` directory and run `npm install` 

***Building the Application :***

After following the setup steps above, to create a production build run:

`npm run build`

	
***Running the Application :***

After following the setup steps above, to start a local dev build run:

`npm run dev`

## Directory Overview

```
/trade-portal
  /dist - output of the build, will be created from `npm run build`
  /public - public assets that will be copied with the build
  /src  - source code of the project
```
