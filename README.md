# TapResearch-Android-SDK
TapResearch Android SDK v1.2.0

For additional information, please see the [TapResearch Android SDK integration guide](https://www.tapresearch.com/docs/android-integration-guide).

## v1.2.0
- In-app webviews! Your users will stay inside the app as they complete TapResearch surveys.
- Multi-language support
- Bug fixes
- Breaking changes:
  - TapResearchShowSurveyListener has been renamed to TapResearchSurveyListener
    - OnSurveyDialogDismissed(boolean cancelled) has been removed.
    - Added OnSurveyModalOpened()
    - Added OnSurveyModalClosed()
  - showSurvey() now starts a new activity. Remember to update the AndroidManifest.xml. See the integration guide for further instructions.

Other platforms:

[TapResearch iOS SDK](https://github.com/TapResearch/TapResearch-iOS-SDK)  
[TapResearch iOS SDK integration guide](https://www.tapresearch.com/docs/ios-integration-guide)

[TapResearch Unity SDK integration guide](https://www.tapresearch.com/docs/unity-integration-guide)

[TapResearch JavaScript SDK integration guide](https://www.tapresearch.com/docs/javascript-integration-guide)  
