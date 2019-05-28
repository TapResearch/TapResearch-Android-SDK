# TapResearch-Android-SDK
TapResearch Android SDK v2.0.7

For additional information, please see the [TapResearch Android SDK integration guide](https://www.tapresearch.com/docs/android_integration_guide).

## Setup

Create an [app](/supplier_dashboard/dashboard/apps/new) and grab your API Token.

#### Download:

Add the following to the repositories closure of the app's module `build.gradle` file


  ```groovy
  repositories {
      maven { url "https://artifactory.tools.tapresearch.io/artifactory/tapresearch-android-sdk/" }
      ...
    }
  ```
  Next, add the following to the dependencies closure

  ```groovy
    dependencies {
      compile 'com.tapr:tapresearch:2.0.7'
      ...
     }
  ```

  And synchronize the project with the gradle files

  #### Manual:

  Download the latest version of the [TapResearch Android SDK](https://github.com/TapResearch/TapResearch-Android-SDK) and drop **tapresearch.aar** to the lib folder

## Other platforms:

[TapResearch iOS SDK integration guide](https://www.tapresearch.com/docs/ios-integration-guide)

[TapResearch React Native SDK integration guide](https://www.tapresearch.com/docs/react-native-integration-guide)

[TapResearch Unity SDK integration guide](https://www.tapresearch.com/docs/unity-integration-guide)

[TapResearch JavaScript SDK integration guide](https://www.tapresearch.com/docs/javascript_integration_guide)  
