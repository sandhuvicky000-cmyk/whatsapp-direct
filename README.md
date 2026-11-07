# SANDHU CLIENT CONNECT — Android project

## Included
- Modern blue/gold branded interface and launcher icon
- Punjabi/English interface toggle
- Customer name + mobile number form
- Local SQLite customer database (persists on the device)
- Save contact to Android phonebook after `WRITE_CONTACTS` permission
- Search, edit, and delete customers in the app
- Normal phone call via Android dialer (`ACTION_DIAL`)
- WhatsApp chat with `Hi` pre-filled (`https://wa.me/...`)

## Important WhatsApp limitation
The app cannot silently send a WhatsApp message or reliably launch a direct WhatsApp voice/video call to a particular contact through the public Android API. WhatsApp opens the chat with `Hi` filled in; the user must press Send. For a voice call, open the WhatsApp chat and tap its call icon.

## Build APK using Android Studio
1. Install Android Studio (current stable) and Android SDK Platform 35.
2. Extract this ZIP.
3. In Android Studio choose **Open** and select the `SandhuClientConnect` folder (the folder containing `settings.gradle`).
4. Allow Gradle sync and install any requested Android SDK components.
5. Choose **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
6. Android Studio will show the generated APK location, normally `app/build/outputs/apk/debug/app-debug.apk`.
7. Install the APK on your Android phone. On first save, grant Contacts permission to write customers into the phonebook.

## Technical
- Package: `com.sandhu.clientconnect`
- Min Android: Android 6.0 (API 23)
- Target/compile SDK: 35
- No backend or paid API required; customer data stays in the app's local SQLite database.
