# wrapper-coil-extension

`wrapper-coil-extension` is a wrapper around Coil's Web Monetization browser extension that allows it to be used from node.js.

---

# Install

```bash
npm install --save wrapper-coil-extension
```

---

# Usage

```javascript
const { login, logout, monetize } = require("wrapper-coil-extension");

// To Login with your Coil Account

login();

// To Logout

logout();

// To start Monetization

monetize(monetizationPackages[,timeout]);
```

---

### timeout

timout defines how much time is spent on monetizing one package in queue
timeout<20000 defaults to 20000

---

### monetizationPackages

monetizationPackages is an object of the type which is passed by `monetize-npm-cli`

```javascript
// monetizationPackages

{
    packages:[
        {
          name: "",
          version: "",
          webMonetization: {
              wallet:""
          },
          state: "",
          monetizationpending: [],
          monetizationstart: [],
          monetizationstop: [],
          monetizationprogress: [],
        }
    ],
    invokeListener(i,listener){
        // i is the index of package
        // listener is the name of listeners to invoke
        // monetizationpending || monetizationstart || monetizationstop || monetizationprogress
    }
}

```

---
