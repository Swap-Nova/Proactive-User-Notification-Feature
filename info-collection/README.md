## The project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).
- The goal of this project was to build a framework that will be able to accepts the user credentials.
- Specifically the web-app accepts the user's LinkedIn credentials.
- In order to receive an mail from the backend server regarding the user's unread notifications and messages,
credentials are taken to factor in for auth and moreover to retrieve the user's data.
- Moreover, the admin will not be able to view the user's password which is an great solution to tackle 
the security hotspot.

## Retrieving the user's password:
- In order to maintain the security and the credibility of the application we are using an npm module *crypto-js*
- To install the node module:
```bash
npm install axios
```
- CryptoJS is a growing collection of standard and secure cryptographic algorithms implemented in JavaScript using best practices and patterns. They are fast, and they have a consistent and simple interface.

## Where is the data being stored?
- The data is stored in google spreadsheets through the usage of axios.
- Axios is an another node module that is a promised-based HTTP client for JavaScript. It has the ability to make HTTP requests from the browser and handle the transformation of request and response data.
- To install the said node-module:
```bash
npm install axios
```
- In order to use it in api form, we are using an platform that is <a href="https://sheet.best/">Best Sheets</a> that turns spreadsheets into REST APIs. We can connect a google spreadsheet or a csv to anything. 
- Once the data is stored we can clearly view that the password is encrypted and can be decrypted only by assuming we have the encrypted password stored in a variable called encryptedPassword.
- Implementation:
```javascript
const decryptedBytes = CryptoJS.AES.decrypt(encryptedPassword, 'your-encryption-key');
const decryptedPassword = decryptedBytes.toString(CryptoJS.enc.Utf8);
```

## Data Collection:
- The data is collected in the spreadsheet and moreover, the password is encrypted:
<img width="1273" alt="Screenshot 2023-06-21 at 7 09 02 PM" src="https://github.com/Swap-Nova/Proactive-User-Notification-Feature/assets/92979885/cdad6b6b-93e6-4943-806a-b49cf5ec5f15">
