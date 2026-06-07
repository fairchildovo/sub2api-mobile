# Project Agent Instructions

- This is an Expo / React Native app with an npm lockfile; use `npm ci` in CI.
- Native folders are generated output and ignored by Git. Use `npx expo prebuild --platform ios --non-interactive` when CI needs an iOS project.
- Unsigned iOS IPA builds should run on macOS/Xcode, disable signing in `xcodebuild`, package `Payload/*.app`, and upload the `.ipa` as a workflow artifact.
- The existing EAS workflow is for Expo cloud builds. Do not use it for unsigned IPA output.
