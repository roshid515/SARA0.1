# SARA0.1 Android Starter

This is an early source-code prototype for the SARA0.1 personal assistant.

## Included
- Native Android app shell
- Basic chat-like interface
- Android speech input intent (uses an installed speech-recognition service)
- Spoken replies using Android Text-to-Speech
- Local notes saved with SharedPreferences
- Provider-independent architecture goal (AI provider is not connected yet)

## Not included yet
- Online AI API integration
- Offline language model
- "Hey Sara" wake-word detection/background service
- Advanced Android actions
- Secure owner authentication

## Build options
This is an Android Studio/Gradle project. Since this project is intended to be operated from a phone only, a compatible cloud build service or an Android development environment is needed to compile it into an APK. Do not paste an API key into source code or share it publicly; later we should use a secure configuration.

## Build from a compatible Gradle environment
Run:
`gradle assembleDebug`

The debug APK is normally created at:
`app/build/outputs/apk/debug/app-debug.apk`

This source is a starting prototype and must be built and tested before use.
## Phone-only cloud build (GitHub Actions)
1. Create a GitHub repository and upload the contents of this project ZIP (including the hidden `.github` folder).
2. Open the repository's **Actions** tab.
3. Choose **Build SARA0.1 APK** and tap **Run workflow** (or push to the `main` branch).
4. When the run completes successfully, open the run and download the `SARA0.1-debug-apk` artifact.
5. Extract the downloaded artifact ZIP on your phone, then tap `app-debug.apk` to install. Android may ask you to allow installs from the browser or file manager you used.

This workflow builds a debug APK. It does not sign a release APK for Play Store distribution. The app is an early prototype and does not yet include an AI provider, offline model, or "Hey Sara" wake-word service.
