# NextJS Sample App

This demo includes all of the files necessary to get started with a basic, hello world app. This app was built using NextJS, BigDesign, Typescript, and React.

## App Installation

To get the app running locally, follow these instructions:

1. [Use Node 10+ and NPM 7+](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm#checking-your-version-of-npm-and-node-js)
2. Install npm packages
    - `npm install`
3. Use Localtunnel to expose your localhost server to the internet.
    - Go to package.json and find the `"lt"` script. Change the subdomain to something that matches your project. Not that you may not get that url if it is in use by someone else so try to come up with a unique name.
    - `npm run lt`
    - Note of the url
4. [Register a draft app.](https://developer.bigcommerce.com/api-docs/apps/quick-start#register-a-draft-app)
     - For steps 5-7, enter callbacks as `'{localtunnel-url}/api/{auth||load||uninstall}'`. 
     - `localtunnel-url` is the url you noted in step 3 above.
     - e.g. auth callback: `https://12345.loca.lt/api/auth`
5. Copy .env-sample to `.env`.
6. [Replace client_id and client_secret in .env](https://devtools.bigcommerce.com/my/apps) (from `View Client ID` in the dev portal).
7. Update AUTH_CALLBACK in `.env` with the `localtunnel-url` from step 3.
8. Enter a jwt secret in `.env`.
    - JWT key should be at least 32 random characters (256 bits) for HS256
9. Specify DB_TYPE in `.env`
    - If using Firebase, enter your firebase config keys. See [Firebase quickstart](https://firebase.google.com/docs/firestore/quickstart)
10. Start your dev environment in a **separate** terminal from `localtunnel`. If `localtunnel` restarts, update callbacks in steps 4 and 7 with the new localtunnel url (if it has changed).
    - `npm run dev`
11. [Install the app and launch.](https://developer.bigcommerce.com/api-docs/apps/quick-start#install-the-app)
