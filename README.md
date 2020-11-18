# Firebase Cloud Functions and Hostng functionality for Squirrel News

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

you can generate our config using

    firebase functions:config:get > .runtimeconfig.json