# Changelog
=============
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
