# Vitabu 📚

Android application for reading storybooks.

![device-2020-12-14-173528](https://user-images.githubusercontent.com/15718174/102108186-4796f480-3e3b-11eb-9375-4dcc53b60d7e.png)

<img width="320" alt="device-2020-06-10-152302" src="https://user-images.githubusercontent.com/15718174/84238987-6e900900-ab2e-11ea-82d5-c41a510473dd.png">

## Installation

Note: This app depends on the [elimu.ai Content Provider](https://github.com/elimu-ai/content-provider) to be installed.

## Development 👩🏽‍💻

Compile APK:

```
./gradlew clean build
```

Install APK:

```
adb install app/build/outputs/apk/debug/ai.elimu.vitabu-<versionCode>-debug.apk
```
## Build signed APK using Github actions
Convert Your Signing Keystore to a base64 text:
```
openssl base64 < your_signing_keystore.jks | tr -d '\n' | tee your_signing_keystore_base64_encoded.txt
```
### Steps
1. Add a new GitHub Secret called `KEYSTORE`. copy the content from the your_signing_keystore_base64_encoded.txt file and paste it into the value field.
2. Create a secret that is called `SIGNING_STORE_PASSWORD` and contains your KeyStore password.
3. Create one that is called `SIGNING_KEY_PASSWORD` and contains your key alias password.
4. The last secret we need to add is called `SIGNING_KEY_ALIAS` and should contain the alias of your app.

---

## About the elimu.ai Community

![elimu ai-tagline](https://user-images.githubusercontent.com/15718174/54360503-e8e88980-465c-11e9-9792-32b513105cf3.png)

 * For a high-level description of the project, see https://github.com/elimu-ai/wiki#readme.
 * For project milestones, see https://github.com/elimu-ai/wiki/projects.
