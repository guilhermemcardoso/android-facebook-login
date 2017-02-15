# facebook-login

This is a simple app that uses the FacebookSDK to login/validate a user.

### How to use this project:

  1. Open the downloaded/cloned project in your [Android Studio] (https://developer.android.com/studio/index.html)
  2. Create a new application in your [Facebook Developer Account] (https://developers.facebook.com)
  3. Add a new platform in your facebook app
    1. In the 'Package Name' field, copy the package name from your AndroidManifest.xml
    2. In the 'Class Name' field, put your Package Name + ".MainActivity" (or another activity that you prefer to use to login in your app)
    3. In the 'Hash Key' field, you need to put a new hash key. And to generate a new hash key:
      1. Download the [OpenSSL] (https://code.google.com/p/openssl-for-windows/downloads/list)
      2. Open a new Command Prompt Window (WinKey + R --> type "cmd" --> Press Enter)
      3. Use the command "cd" to natigate to java/bin folder
      4. Copy this command changing all the variables that you need:
      
      ```
      keytool -exportcert -alias androiddebugkey -keystore "yourpath\debug.keystore" | "openssl_path" sha1 -binary | "openssl_path" base64
      ```
      
      - debug.keystore: the file that you will save your hash keys
      - openssl_path: the path to access your OpenSSL/bin/openssl.exe file
      
      - **This is a Windows command !! If you are using a Unix machine, you will need to use a similar command.**
      
      5. Press 'Enter'
      6. Copy the generated hash key in the 'Hash Key' field
      7. Check the 'Unique Login' option
      
    4. Save your changes and confirm
    
  4. In your Android Studio project, open the strings.xml file
  5. Replace the facebook_app_id content with your facebook app id 
  6. Replace the facebook_app_secret content with your facebook app secret
  7. Come back to your facebook app page, look at the side menu and click on 'App Review'
  8. Check the 'Make this app public' option (or something like that) and confirm
  
  9. Run your project in Android Studio
