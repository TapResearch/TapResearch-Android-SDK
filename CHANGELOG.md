# Changelog
=============

(click on the version to see the repository artifacts, aar files, etc)

## <a href="https://artifactory.tools.tapresearch.io/artifactory/webapp/#/artifacts/browse/tree/General/tapresearch-android-sdk/com/tapresearch/tapsdk/3.3.1">v3.3.1</a>
- allow orca (remote platform) to be able set dim-able transparent background for interstitials and quick questions (not banners)
- additional 'optionalParentActivity' added to showContentForPlacement as optional parameter (non-protocol breaking)

## <a href="https://artifactory.tools.tapresearch.io/artifactory/webapp/#/artifacts/browse/tree/General/tapresearch-android-sdk/com/tapresearch/tapsdk/3.3.0">v3.3.0</a>
- Handle rare error conditions gracefully, such as the unforeseen inability to create new WebView object
- More logging to be able to diagnose and troubleshoot mentioned conditions
- Add stack trace and memory snapshot to remote logger
- Use 'default' WebView caching to improve orca loadUrl performance

## <a href="https://artifactory.tools.tapresearch.io/artifactory/webapp/#/artifacts/browse/tree/General/tapresearch-android-sdk/com/tapresearch/tapsdk/3.2.9">v3.2.9</a>
- Ability to detect if the app is a react native integration and it’s plugin version
- Ability to detect if underlying survey subsystem has encountered errors and recover and/or fail gracefully.
- Ability to remotely toggle showContentForPlacement ‘retry’ if encounter internal error.
- Added a screen-on listener so the SDK can preemptively determine its state and recover, if necessary.
- Log SDK error events in order to better diagnose issues and make future improvements.

## <a href="https://artifactory.tools.tapresearch.io/artifactory/webapp/#/artifacts/browse/tree/General/tapresearch-android-sdk/com/tapresearch/tapsdk/3.2.7">v3.2.7</a>
- Improved sdk ready callback logic

## <a href="https://artifactory.tools.tapresearch.io/artifactory/webapp/#/artifacts/browse/tree/General/tapresearch-android-sdk/com/tapresearch/tapsdk/3.2.6">v3.2.6</a>
- Added screen rotate button for phones. Tablet & stability improvements

## <a href="https://artifactory.tools.tapresearch.io/artifactory/webapp/#/artifacts/browse/tree/General/tapresearch-android-sdk/com/tapresearch/tapsdk/3.2.5">v3.2.5</a>
- Stability updates, improved error handling

## <a href="https://artifactory.tools.tapresearch.io/artifactory/webapp/#/artifacts/browse/tree/General/tapresearch-android-sdk/com/tapresearch/tapsdk/3.2.4">v3.2.4</a>
- Fraud-protection, stability updates, performance improvements

## v3.2.3
- Bug fixes, logging improvements
## v3.2.2
- Bug fixes, offer navigation improvements

## v3.2.1
- Add quick question capability, stability updates

## v3.1.1-beta6
- Bug Fixes

## v3.1.1-beta3
- Bug Fixes

## v3.1.1-beta1
- Bug Fixes

## v3.1.0-beta8
- Move content callbacks out of SDK init

## v3.1.0-beta7
- Update minSdk to api 24
- Fix compatiblity with Android api below 33

## v3.1.0-beta6
- Custom params optimizaiton

## v3.1.0-beta5
- Update headers for device id

## v3.1.0-beta4
- Fix bug with reward and error callbacks

## v3.1.0-beta3
- Update callbacks

## v3.1.0-beta2
- Update custom params
- Enable error callbacks from backend

## v3.1.0-beta1
- Add feature to send dedicated user attributes
- Bug fix for content callbacks
- Add sdk ready callbacks

## v3.0.0-beta6
- Fix potential memory leaks.
- Add mechanisms for code quality improvements and refinement.

## v3.0.0-beta5
- Bug fixes for Java interoperability

## v3.0.0-beta4
- Updates and fixes for java interoperability. 
- SDK rewritten for stability, simplicity, and performance.
- Added ability for some realtime feature updates and bug fixes.
- Partial screen interstitials and banners.
- Removed the need to store placement objects.
- Improved error reporting.

## v2.5.9
- Bug fixes for SurveyPresenter instantiation.

## v2.5.8
- Bug fix for SurveyWall Orientation lock

## v2.5.7
- Bug fixes for SurveyWall crashes

## v2.5+
- New Events Placement feature
- isEventAvailable method to check availability
- bug fix when passing null or non-null for customParameters and SurveyListener

## v2.2.0
- Networking improvements
- Response time optimization for in-app callback

## v2.0.15
- ANR Fix

## v2.0.14
- Clean up an empty network certificate warning 

## v2.0.13
- Added Remote error logging
- Google Play Services is now optional and will not be embededd but will use the on that is used in the app
- Performance enhancements 

## v2.0.12
- Fix: Failed to embed the support library

## v2.0.11
- Fix: remove obfuscation from custom paramerters objects

## v2.0.10
- Custom placement parameters
- Cleartext whitelist for SDK level 28 and above
- Handling native webview crashes
- Remove the webview zoom widget

## v2.0.9
- Fixes to support more surveys
- Undo the unsecure urls fix 

## v2.0.8
- Fix: Protect from unsecure survey urls

## v2.0.7
- Fix: Check rewards when SDK initialized
- Fix: Crash on 4.+ devices
- Support Local Storage

## v2.0.6
- Fix offer wall load crash
- In app rewards race condition 

## v2.0.5
- Support more survey providers
- Better exception reporting and handling
- Bug fixes

## v2.0.4
- Fix a typo in the SDK
- Supporting Pure Spectrum surveys

## v2.0.3
- Send a placement response when the SDK isn't ready
- Bug fixes

## v2.0.2
- Adding `hasHotSurvey` method to `TRPlacement`
- Fixing the `triggered_at` attribute
- Crash fixes

## v2.0.1
- Crash fix - The SDK may crash when pulling a new placement

## v2.0.0

**Version v2.0.0 isn't backwards compatible and will require code changes from previous versions**

- Introducing TRPlacement to evaluate availability and to display the survey wall
- Introducing TRReward to handle in app rewards
- Bug fixes

### The following methods and interfaces were removed

~~~java

public abstract boolean isSurveyAvailable();
public abstract boolean isSurveyAvailable(String offerIdentifier);
public abstract void showSurvey();
public abstract void showSurvey(String offerIdentifier);
public abstract void setOnRewardListener(TapResearchOnRewardListener listener);
public abstract void setSurveyListener(TapResearchSurveyListener listener);
public abstract void setPlacementsListener(TapResearchPlacementsListener listener);

public interface TapResearchOnRewardListener
public interface TapResearchPlacementsListener
public interface TapResearchSurveyListener

~~~

## v1.4.2
- Crash when parsing an offer with an identifier
- Passing offer identifier with AppSession 

## v1.4.1
- Fix is for `isSurveyAvailable(String identifier)`

## v1.4.0
- Introduce the `TapResearchPlacementsListener`. The interface passes a placement identitifer with the survey events
- New methods to skin the survey wall `setActionBarColor(int color)`, `setActionBarTextColor(int color)`, `setActionBarText(String text)`

## v1.3.9
- Fix passing an empty offer identifier

## v1.3.8
- Fix offer check availability

## v1.3.7
- Reward redeemed fix

## v1.3.6
- Refresh button in the survey wall
- Bug fixes

## v1.3.5
- Fix the requests concurrency bug

## v1.3.4
- Android v5 ANR fix

## v1.3.3
- Include offer identifier in the receive reward callback - TapResearchOnRewardListener#onDidReceiveReward signature was changed
``
void onDidReceiveReward(int rewardAmount, String transactionIdentifier, String currencyName, @PayoutOptions int payoutEvent, String offerIdentifier);
``
- Init the SDK using an Activity
- Performance improvements
- Bug fixes

## v1.3.2
- Fixing the survey wall exit
- Saving the state failed in certain cases

## v1.3.1
---------
- Bug fixes


## v1.3.0
---------
- Gradle integration
- Multi currency support - please note that TapResearchOnRewardListener#onDidReceiveReward signature was changed
``
void onDidReceiveReward(int rewardAmount, String transactionIdentifier, String currencyName, @PayoutOptions int payoutEvent);
``
- Multi offers
- Bug fixes


## v1.2.7
---------
- Added two additional survey listener callbacks.
  - onSurveyAvailable()
  - onSurveyNotAvailable()

## v1.2.6
---------
- Bug fixes.
- Please update the TRSurveyActivity definition to enable hardware acceleration.
  - `<activity android:name="com.tapr.internal.c.TRSurveyActivity" android:hardwareAccelerated="true" android:configChanges="orientation|keyboardHidden|screenSize" android:theme="@android:style/Theme.Holo.Light" />`

## v1.2.5
---------
- The SDK is now compatible with Amazon devices.

## v1.2.4
---------
- Bug fixes.

## v1.2.3
---------
- The orientation for TRSurveyActivity is now set to `SCREEN_ORIENTATION_SENSOR`. This allows users to take surveys in either portrait or landscape mode.

## v1.2.2
---------
- Bug fixes
- **Important** Please update the TRSurveyActivity definition in your AndroidManifest.xml file.
  - Old: `<activity android:name="com.tapr.internal.c.TRSurveyActivity" android:theme="@android:style/Theme.Holo.Light" />`
  - New: `<activity android:name="com.tapr.internal.c.TRSurveyActivity" android:configChanges="orientation|keyboardHidden|screenSize" android:theme="@android:style/Theme.Holo.Light" />`

## v1.2.1
---------
- TRSurveyActivity no longer inherits from AppCompatActivity. Remember to update your AndroidManifest.xml file to use the new activity definition found in the integration guide.

## v1.2.0
---------
- In-app webviews! Your users will stay inside the app as they complete TapResearch surveys.
- Multi-language support
- Bug fixes
- **Important changes**:
  - TapResearchShowSurveyListener has been renamed to TapResearchSurveyListener
    - OnSurveyDialogDismissed(boolean cancelled) has been removed.
    - Added OnSurveyModalOpened()
    - Added OnSurveyModalClosed()
  - showSurvey() now starts a new activity -- remember to update your AndroidManifest.xml file. See the integration guide for further instructions.
