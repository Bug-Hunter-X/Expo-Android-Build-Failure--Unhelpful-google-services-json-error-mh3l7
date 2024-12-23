# Expo Android Build Failure: Unhelpful google-services.json Error

This repository demonstrates a common yet frustrating issue when building Android APKs using Expo CLI. The error message, related to `google-services.json`, lacks specificity, making debugging difficult.  The solution focuses on verifying the `google-services.json` file's correctness and proper integration within the Expo project.

## Reproducing the Bug

1. Clone this repository.
2. Attempt to build an Android APK using `expo build:android`. 
3. Observe the error related to `google-services.json` processing.

## Solution

The solution involves several steps to ensure the `google-services.json` file is correctly configured and integrated:

1. **Verify `google-services.json` Contents:**  Ensure your `google-services.json` file contains the correct information for your Firebase project.  Common mistakes include typos or incorrect project IDs.
2. **Correct File Placement:**  Make sure that `google-services.json` is placed correctly in the `android/app` directory of your Expo project. 
3. **Clean and Rebuild:** Sometimes, cached build files can cause issues. Try cleaning the project (`expo prebuild --clean`) before rebuilding.
4. **Check for Conflicting Dependencies:** Look for any conflicting dependencies that may interfere with the Google services integration.
5. **Review Firebase Setup:** Double-check your Firebase project setup and make sure it's correctly linked to your Android application. 

This repository provides examples of both the problematic setup and the corrected setup, allowing you to compare and learn how to avoid this error in your own projects.