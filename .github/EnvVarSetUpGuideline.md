# Environment Variables Setup Guidelines

This document provides a step-by-step guide to setting up the required `.env` files for both the frontend and backend. These variables are essential for the application to function properly.

---

1. **`VITE_PUBLICATION_KEY`**

   - **Description:** The public Stripe key for client-side payment processing.
   - **How to Obtain:**

     1. Log in to the [Stripe dashboard](https://dashboard.stripe.com/).
     2. Navigate to the Developers section.
     3. Click on API Keys.
     4. Copy the Publishable Key (starts with pk*test* for test environments).
     5. Set the VITE_PUBLICATION_KEY variable in your env file with the copied key.

     `VITE_PUBLICATION_KEY=your_stripe_publishable_key`

2. **`VITE_JAAS_APP_ID`**

   - **Description:** The key for integrating Jitsi Meet video conferencing.
   - **How to Obtain:**

     1. Go to the [Jitsi developer portal](https://jaas.8x8.vc/).
     2. Sign up or log in to your account.
     3. Navigate to the API section.
     4. Create a new application if you don't have one.
     5. Copy the App ID provided.
     6. Set the VITE_JAAS_APP_ID variable in your env file with the copied App ID.

     `VITE_JAAS_APP_ID=your_jaas_app_id`

3. **`VITE_API_KEY`**

   - **Description:** The API key for Chat-Bot
   - **How to Obtain:**
     1. Go to the [Google AI Studio](https://aistudio.google.com/app/apikey).
     2. Sign in with your Google account.
     3. Once logged in, you should see an interface for managing projects and API keys (If prompted, create a new project or select an existing one).
     4. Now In the API Key section, look for an option to Generate API Key & click on it to create a new API key
     5. Once the key is generated, it will be displayed on the screen.
     6. Copy the API key.
     7. Open your `.env` file in frontend folder.
     8. Replacing `your_api_key` with the key you copied:
        `VITE_API_KEY = your_API_key`

4. **`VITE_FIREBASE_CONFIG`**

   - **Description:** These credentials allow the frontend to interact with Firebase services, such as authentication and Firestore.

   - **How to Obtain:**

     1. **Go to Firebase Console:**

        - Visit [Firebase Console](https://console.firebase.google.com/).
        - Select your project.

     2. **Add a Web App (if not added already):**

        - In the **Project Overview**, click on the **</> Web** icon to add a new web app.
        - Follow the setup instructions provided by Firebase to configure your web app.
        - **Do not select Firebase Hosting** during the setup process.

     3. **Find Firebase Configurations:**

        - After setting up the web app, click on the **Project Overview Settings** (⚙️) icon in the left sidebar.
        - Scroll down to the **Your Apps** section under "General".
        - Click on your web app (or create one if not already added).

     4. **Copy the Firebase Configuration Object:**

        - Locate the **Firebase SDK snippet** and copy the `firebaseConfig` object values.

     5. **Set Environment Variables:**
        - Add each value from the `firebaseConfig` one at a time to your `.env` file in the following format:
        - **Note:** The entire `firebaseConfig` object should be wrapped as a string under the variable `VITE_FIREBASE_CONFIG` in your `.env` file.

     ```
     VITE_FIREBASE_API_KEY=your-api-key
     VITE_FIREBASE_AUTH_DOMAIN=your-auth-domain
     VITE_FIREBASE_PROJECT_ID=your-project-id
     VITE_FIREBASE_STORAGE_BUCKET=your-storage-bucket
     VITE_FIREBASE_MESSAGING_SENDER_ID=your-messaging-sender-id
     VITE_FIREBASE_APP_ID=your-app-id
     VITE_FIREBASE_MEASUREMENT_ID=your-measurement-id
     ```

     6. **Enabling Authentication**
        - On your project console, left side bar click on `Authetication` & enable with google (email/password)
        - Give your project name(your choice) & support email, then click save.

---

### **Important Notes**

- Always keep `.env` files private and do not expose them in version control systems like GitHub.
- Use environment variable management tools like `dotenv` in development or configure the deployment environment with these variables.
- Ensure secure storage and limited access to keys, passwords, and tokens.

---
