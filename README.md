# Chat client using Firebase

## Create a Firebase project and Set up your project

### Create project

In the <a href="https://console.firebase.google.com">Firebase console </a> click on Add Project and create a project. This project will be assigned a unique ID in the form {name}-1234 which is what is ultimately used to identify your project.

The application that we are going to build uses the whole set of Firebase products available on the web:
* **Firebase Authentication** to easily let your users sign-in your app.
* The **Firebase Realtime Database** to save structured data on the Cloud and get instant notification when the data is updated.
* **Cloud Storage** for Firebase to save files in the cloud.
* **Firebase Hosting** to host and serve your static assets.
* **Firebase Cloud Messaging** to send push notifications and display browser popup notifications.
Some of these products need special configuration or need to be enabled using the Firebase console:


## Enable Google Auth

To let users sign-in the app we'll use Google auth which needs to be enabled.
In the Firebase Console open the **Develop** section > **Authentication** > **SIGN IN METHOD** tab (or click here to go there) you need to enable the **Google** Sign-in Provider and click **SAVE**. This will allow users to sign-in the Web app with their Google accounts. You could also set a public facing name of your app

## Enable The Realtime Database

The app uses the Firebase Realtime database to save the chat messages and receive new chat messages. To enable The Realtime Database on your Firebase project visit the **Database** section and click the **Create database** button in the **Realtime Database** box

Then select the **Start in test mode** option and click **Enable** when you receive the disclaimer about the security rules. This will ensure that we can freely write to the database. We'll make this more secure later on.

![Security Rules](https://codelabs.developers.google.com/codelabs/firebase-web/img/48cd87a25c56a1aa.png)


## Enable Cloud Storage
The app uses Cloud Storage to upload pics. To enable Cloud Storage on your Firebase project visit the **Storage** section and click the **Get Started** button.

Then click **Got It** when you receive the disclaimer about the security rules. With the default security rules, any authenticated users can write to anything to Cloud Storage. We'll make this more secure later on.

![Security Rules](https://codelabs.developers.google.com/codelabs/firebase-web/img/328ca996218b2e41.png)


## Firebase Command Line Interface

The Firebase Command Line Interface (CLI) will allow you to serve your web apps locally and deploy your web app to Firebase hosting.

To install the CLI run the following npm command:

`npm -g install firebase-tools`

To verify that the CLI has been installed correctly open a console and run:

`firebase --version`


**Initialize your site**

From the root of your project directory, run the following command:

`firebase init`

The firebase init command creates a firebase.json configuration file in the root of your project directory. This file is required to deploy your site using the CLI. You can customize your Hosting configuration in the firebase.json file.


Authorize the Firebase CLI by running:

`firebase login`


Once authorized, go back to the console and make sure you are in the web-start directory. Then set up the Firebase CLI to use your Firebase Project:

`firebase use --add`

You will be prompted to select your Project ID. Follow the instructions.


**Deploy your site**

To deploy your site, run the following command from your project's root directory:

`firebase deploy`


## Run the starter app

`firebase serve`



