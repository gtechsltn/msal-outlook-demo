# MSAL Outlook Demo

MSAL Overview

https://learn.microsoft.com/en-us/entra/identity-platform/msal-overview

Example of using MSAL in Outlook Native.

See https://github.com/AzureAD/microsoft-authentication-library-for-js/issues/1072 .

https://eirikb.github.io/msal-outlook-demo/

https://gist.github.com/gtechsltn/ae05c255ba45c2fc470c612bc4078d7d

https://gist.github.com/gtechsltn/1fc91ee03bc20c7047a35be20bfba1ed

PKCE

https://devblogs.microsoft.com/identity/migrate-to-auth-code-flow/

SPAs

https://learn.microsoft.com/en-us/entra/identity-platform/reference-third-party-cookies-spas

## Test 

I've deployed this add-in to GitHub for testing purposes.  
Add this manifest:

https://eirikb.github.io/msal-outlook-demo/manifest.xml


## Run locally

Run like this:
  * Open manifest.xml and replace "eirikb.github.io" with your desirable host. 
  * Create a file called `.env` with `CLIENTID=...` with Client ID of your AAD app
  * `npm i`
  * `npm start`
  * Add custom Add-in by file
  
  
What makes this demo special:
Overrides [`openPopup` of MSAL](https://github.com/AzureAD/microsoft-authentication-library-for-js/blob/e3f4081/lib/msal-core/src/UserAgentApplication.ts#L738-L770) with [custom hack](https://github.com/eirikb/msal-outlook-demo/blob/2a034bc/app.js#L62-L77) using [Outlook Office API Dialog](https://docs.microsoft.com/en-us/javascript/api/office/office.dialogoptions).  
