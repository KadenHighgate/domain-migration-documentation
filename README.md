# domain-migration-documentation
Documentation for transferring a domain from GoDaddy to Firebase and GCP

## Domain Migration

Reference: [Firebase custom GoDaddy Domain](https://www.pawangaria.com/post/map-custom-domain-with-godaddy-firebase/)

**Prerequisites** 
- Setup a Google Firebase Account
- Install firebase cli
  - `npm install -g firebase-tools`
- Initialize a project and Deploy it
  - Sign into Google
  `firebase login`
  - Initialize your project
  `firebase init`
- Deploy to Firebase
  `firebase deploy`

**Steps**
1. Navigate to the firebase dashboard
2. Select Hosting from the side Panel
3. Select Add Custom Domain
4. Add domain name
5. Get the google site verification ID; we'll add it to our  **TXT** record in DNS provider
6. Login to GoDaddy and navigate to the Domain menu
7. Find the Manage DNS Link
8. Add a Record **Type:** TXT  **Host:** @ **TXT Value:** <google-site-verification-ID> 
9. In Firebase verify the domain following the next steps of the screen
10. Once verified you will be given Ip adresses. Add those records to your GoDaddy **Type:** A  **Host:** @ **TXT Value:** <IP>
11. In Firebase console connect to the site
  
At this point you should be able to access your newly hosted web application. You may have to set up a redirection in GoDaddy for the www.
  
## Setup Hosting on Firebase
  
  Now that you have a project you can access that project in Firebase. Navigate to the firebase console in your browser for the next steps.
  
  **Steps**
  1. Goto Hosting and selectget started
  2.
  


