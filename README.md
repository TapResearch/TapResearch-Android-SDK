# TapResearch-Android-SDK
TapResearch Android SDK v1.2.7

For additional information, please see the [TapResearch Android SDK integration guide](https://www.tapresearch.com/docs/android-integration-guide).

## v1.2.7
- Added two additional survey listener callbacks. 
  - onSurveyAvailable()
  - onSurveyNotAvailable()

## v1.2.6
- Bug fixes.
- Please update the TRSurveyActivity definition to enable hardware acceleration.
  - `<activity android:name="com.tapr.internal.c.TRSurveyActivity" android:hardwareAccelerated="true" android:configChanges="orientation|keyboardHidden|screenSize" android:theme="@android:style/Theme.Holo.Light" />`

## v1.2.5
- The SDK is now compatible with Amazon devices.

## v1.2.4
- Bug fixes.

## v1.2.3
- The orientation for TRSurveyActivity is now set to `SCREEN_ORIENTATION_SENSOR`. This allows users to take surveys in either portrait or landscape mode. 

## v1.2.2
- Bug fixes
- **Important** Please update the TRSurveyActivity definition in your AndroidManifest.xml file.
  - Old: `<activity android:name="com.tapr.internal.c.TRSurveyActivity" android:theme="@android:style/Theme.Holo.Light" />`
  - New: `<activity android:name="com.tapr.internal.c.TRSurveyActivity" android:configChanges="orientation|keyboardHidden|screenSize" android:theme="@android:style/Theme.Holo.Light" />`

## v1.2.1
- TRSurveyActivity no longer inherits from AppCompatActivity. Remember to update your AndroidManifest.xml file to use the new activity definition found in the integration guide.

## v1.2.0
- In-app webviews! Your users will stay inside the app as they complete TapResearch surveys.
- Multi-language support
- Bug fixes
- **Important changes**:
  - TapResearchShowSurveyListener has been renamed to TapResearchSurveyListener
    - OnSurveyDialogDismissed(boolean cancelled) has been removed.
    - Added OnSurveyModalOpened()
    - Added OnSurveyModalClosed()
  - showSurvey() now starts a new activity -- remember to update your AndroidManifest.xml file. See the integration guide for further instructions.

Other platforms:

[TapResearch iOS SDK](https://github.com/TapResearch/TapResearch-iOS-SDK)  
[TapResearch iOS SDK integration guide](https://www.tapresearch.com/docs/ios-integration-guide)

[TapResearch Unity SDK integration guide](https://www.tapresearch.com/docs/unity-integration-guide)

[TapResearch JavaScript SDK integration guide](https://www.tapresearch.com/docs/javascript-integration-guide)  
