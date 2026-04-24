---
name: firebase
description: Use this skill when working with Firebase. Triggers when user mentions Firebase or imports from it.
---

# Firebase

## What this is
Firebase is a platform for building web and mobile applications. It provides a suite of tools for authentication, Realtime Database, Cloud Firestore, Cloud Storage, and more. With Firebase, developers can focus on building their applications without worrying about the underlying infrastructure.

## Installation
```bash
npm install firebase
```

## Key concepts
The most important APIs and patterns in Firebase include:
* Authentication: `firebase.auth()` - used to manage user authentication
* Realtime Database: `firebase.database()` - used to store and retrieve data in real-time
* Cloud Firestore: `firebase.firestore()` - used to store and retrieve data in a NoSQL database
* Cloud Storage: `firebase.storage()` - used to store and retrieve files

Example:
```javascript
import firebase from 'firebase/app';
import 'firebase/auth';
import 'firebase/database';

const auth = firebase.auth();
const database = firebase.database();
```

## Correct usage patterns
To use Firebase in an application, you need to initialize it with your project's configuration. You can then use the various Firebase services to build your application.
```javascript
import firebase from 'firebase/app';
import 'firebase/auth';

firebase.initializeApp({
  apiKey: '<API_KEY>',
  authDomain: '<AUTH_DOMAIN>',
  databaseURL: '<DATABASE_URL>',
  projectId: '<PROJECT_ID>',
  storageBucket: '<STORAGE_BUCKET>',
  messagingSenderId: '<MESSAGING_SENDER_ID>',
  appId: '<APP_ID>',
});

const auth = firebase.auth();

auth.createUserWithEmailAndPassword('user@example.com', 'password')
  .then((userCredential) => {
    console.log('User created:', userCredential.user);
  })
  .catch((error) => {
    console.error('Error creating user:', error);
  });
```

## Common mistakes to avoid
Common mistakes when using Firebase include:
* Not initializing Firebase before using its services
* Not handling errors properly
* Not using the correct Firebase service for the task at hand

## File and folder conventions
Firebase projects typically follow these conventions:
* The `firebase.json` file contains configuration for the Firebase project
* The `public` folder contains static assets for the application
* The `src` folder contains the application's source code
* The `functions` folder contains Cloud Functions for the application