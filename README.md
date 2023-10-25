# TapResearch-Android-SDK

For additional information, please see the [TapResearch Android SDK integration guide](https://supply-docs.tapresearch.com/docs/android-integration).

## Setup

Create an [app](https://www.tapresearch.com/supplier_dashboard/overview) and grab your API Token.

#### Download:

Add the following to the repositories closure of the app's module `build.gradle` file:


  ```groovy
  repositories {
      maven { url "https://artifactory.tools.tapresearch.io/artifactory/tapresearch-android-sdk/" }
      ...
    }
  ```
  Next, add the following to the dependencies closure:

  ```groovy
    dependencies {
      implementation("com.tapresearch:tapsdk:3.1.0-beta8")
      ...
     }
  ```

  And synchronize the project with the gradle files.

  #### Manual:

  Download the latest version of the [TapResearch Android SDK](https://github.com/TapResearch/TapResearch-Android-SDK) and drop **tapsdk.aar** to the lib folder

## Other platforms:

[TapResearch iOS SDK integration guide](https://supply-docs.tapresearch.com/docs/ios-integration)

[TapResearch React Native SDK integration guide](https://supply-docs.tapresearch.com/docs/react-integration)

[TapResearch Unity SDK integration guide](https://supply-docs.tapresearch.com/docs/unity-integration)
  
