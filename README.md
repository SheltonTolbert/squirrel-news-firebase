# Firebase Cloud Functions and Hosting functionality for Squirrel News

## Firebase (Functions)

We are using Firebase as our Application Cloud Backend. So far we are using 

* Firestore to persist curated articles
* Functions to provide an API for third-party-apps to publish curations

### Runtime Environment for Functions

To access firestore in the function environemnt, we need to configure

	"service_acc": {
	  "clientemail" :string
	  "projectid": string
	  "key": string (the private key)
	}

Firebase stores its environment on localhost in a .runtimeconfig.json which should not be versioned in git for safety and security reasons. Instead, if you want to start developing you will need to ask an admin for a private key to access firestore from the function or if you are the admin, generate a new private key using the firebase console and store them in the respective file. 

	firebase functions:config:get > .runtimeconfig.json


For more information visit: https://firebase.google.com/docs/functions/config-env
