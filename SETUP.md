# Cloud follow-up app: setup (about 15 minutes, free)

1. Go to https://console.firebase.google.com -> Add project -> name it -> turn OFF Google Analytics -> Create.
2. Build -> Authentication -> Get started -> Sign-in method -> Email/Password -> Enable -> Save.
3. Authentication -> Users -> Add user: your own email + a password. This is your TEACHER login.
   Copy the "User UID" shown in the list.
4. Build -> Firestore Database -> Create database -> pick a nearby location -> Start in PRODUCTION mode.
   a) Rules tab: delete everything, paste the content of firestore.rules, click Publish.
   b) Data tab -> Start collection -> Collection ID: teachers -> Document ID: paste your User UID
      -> add field  name  (string)  =  خادم  -> Save.
5. Project settings (gear icon) -> General -> Your apps -> Web icon </> -> register app (any name, no hosting)
   -> copy the values inside firebaseConfig and put them in www/config.js (edit the file on GitHub).
6. Upload everything to a NEW GitHub repo, add .github/workflows/build-apk.yml by hand, wait for the build,
   download the APK from Actions, install it on your phone and on the students' phones.
7. Open the app, log in with your email + password -> Students tab -> add names -> send each student
   his username and code. Students log in with them.
