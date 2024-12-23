# Expo DocumentPicker Android Bug: Null URI

This repository demonstrates a bug in the Expo DocumentPicker API on Android.  After selecting a file, the promise sometimes resolves with a null `uri`, even if a file was successfully chosen. This behavior is inconsistent and can cause unexpected app crashes or errors.

## Reproduction

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app on an Android device or emulator.
4. Attempt to select a file using the DocumentPicker. You may encounter the error intermittently.

## Expected Behavior

The `uri` property of the returned object should contain a valid URI of the selected file, even on Android.

## Actual Behavior

The `uri` property is sometimes null, making it impossible to access the selected file.