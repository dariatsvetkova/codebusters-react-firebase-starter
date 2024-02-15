<!-- prettier-ignore-start -->
# React & Firebase Starter

![react-firebase-starter](https://user-images.githubusercontent.com/68360696/129435412-11320287-3afd-4e9d-8595-7194bc358c47.png)

> This is a copy of the original open-source project from the now-defunct [CodeBusters](https://github.com/codebusters-ca/react-firebase-starter) org

## Tech Stack

* [Firebase](https://firebase.google.com/) - Firestore database, auth, cloud functions, local emulators
* [React](https://reactjs.org/)
* [Webpack](https://webpack.js.org/)
* [Tailwind CSS](https://tailwindcss.com/)
* [React Router](https://reactrouter.com/web)
* [react-firebase-hooks](https://github.com/CSFrequency/react-firebase-hooks/)
* [React Helmet](https://www.npmjs.com/package/react-helmet) - SEO
* [Mocha](https://mochajs.org/) - testing for Firebase
* [ESLint](https://eslint.org/) - based on AirBnB config

### Prerequisites

You will need the following to use this starter: 

* [Node](https://nodejs.org/en/)
* [Java DK](https://docs.oracle.com/en/java/javase/16/install/overview-jdk-installation.html#GUID-8677A77F-231A-40F7-98B9-1FD0B48C346A)
* A Firebase project created in [Firebase Console](https://console.firebase.google.com)
* Install Firebase CLI tools: ```npm install -g firebase-tools```

## Setup Guide

In [Firebase Console](https://console.firebase.google.com),click Add project, then enable Firestore Database and Authentication via Google.

Clone this repo:
```git clone https://github.com/codebusters-ca/react-firebase-starter.git```

Go to the Firebase project directory and Install the dependencies and setup Firebase:
```cd .\react-firebase-starter\ && npm run setup```

Once all dependencies installed it will prompt you to log in via the browser and authenticate the firebase tool

After login , the terminal will prompt with the firebase initialization process.
**When asked if you'd like to overwrite `firestore.rules`, choose 'No'.**

This project is set up to use Firestore, Functions, and Emulators. Make sure you choose these options when prompted by Firebase CLI. Similarly, when asked about which emulators you want to use, choose Auth, Firestore, and Functions.

Now that we've initialized the local Firebase directory, let's connect it to your project.

Run `firebase projects:list` and copy the ID of the project you want to use.

Then tell Firebase CLI to use that project:
```firebase use <your project ID>```

Head over to `/src/firebase.clientApp.js` and add your config object (found in Firebase Console under Project Settings).

Finally, run Emulators in another terminal with `npm run emulators`. Head over to the browser ([localhost:3000](http://localhost:3000/)) and see `Hello from Firestore Emulator` appear there.

Congratulations! The setup process is now complete.

## Usage

### Build

```npm start```

### Test

```npm run emulators```
In another terminal: `npm test`

You should see a list of 3 tests that all pass. 

### Deploy

```npm run build```

## Contribute

We ❤️ feedback and help from fellow devs! Check out [open issues](https://github.com/codebusters-ca/react-firebase-starter/issues), create a [new one](https://github.com/codebusters-ca/react-firebase-starter/issues/new?labels=bug), or send us a [pull request](https://github.com/codebusters-ca/react-firebase-starter/compare).

## Licence

This project is licensed under the [MIT license](https://github.com/codebusters-ca/react-firebase-starter/blob/main/LICENSE).
<!-- prettier-ignore-end -->
