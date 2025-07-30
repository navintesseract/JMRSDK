# Merging AndroidManifest

If a custom manifest is added to the project and is not willing to directly replace the existing AndroidManifest.xml, the following steps are to be done to merge them both.

1. Add following \<meta-data> tag in \<activity> tag

```xml
<meta-data android:name="unityplayer.UnityActivity" android:value="true" />
```

&#x20;   2\. Add / Replace existing JMRSDK AndroidManifest permissions with the following permissions. Your extra permissions should be added after this permission.

{% code overflow="wrap" %}
```xml
<uses-permission android:name="android.permission.RECORD_AUDIO" tools:node="remove" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" tools:node="remove"/>
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" tools:node="remove"/>
<uses-permission android:name="android.permission.READ_PHONE_STATE" tools:node="remove"/>
<uses-permission android:name="android.permission.READ_PRIVILEGED_PHONE_STATE" tools:node="remove"/>
<uses-permission android:name="android.permission.WAKE_LOCK"/>
```
{% endcode %}

3\. Uncomment permission from AndroidManifest or add the following permission for using the Camera.

```xml
<uses-permission android:name="android.permission.CAMERA"/>
```

4\. Ensure that the following **three** lines are present under the \<application> tag. Ensure that you follow the steps in the section [Adding Category Tag In AndroidManifest](../../getting-started/setting-up-a-jio-mixed-reality-project-in-unity.md#adding-category-tag-in-androidmanifest) to ensure that your application is reflected within the same category as it is uploaded on the developer console.

{% code overflow="wrap" %}
```xml
<meta-data android:name="com.jiotesseract.mr.category" android:value="1" />
<meta-data android:name="com.jiotesseract.platform" android:value="LITE" />
<activity android:name="com.jiotesseract.mr.sdk.JmrUnityActivity" android:label="@string/app_name" android:launchMode="singleTask" android:configChanges="orientation|keyboardHidden|screenSize|screenLayout">
```
{% endcode %}

5\. Make sure _"android:excludeFromRecents"_ attribute is not present in the activity/application tag.

```xml
<applicaition android:excludeFromRecents="*"/>
```

6\. The final **AndroidManifest** file should look like following

{% code overflow="wrap" %}
```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android" package="${applicationId}" xmlns:tools="http://schemas.android.com/tools" android:installLocation="preferExternal">
  <supports-screens android:smallScreens="true" android:normalScreens="true" android:largeScreens="true" android:xlargeScreens="true" android:anyDensity="true" />
  <application android:theme="@style/UnityThemeSelector" android:icon="@mipmap/app_icon" android:label="@string/app_name" android:requestLegacyExternalStorage="true" android:screenOrientation="landscape">
    <meta-data android:name="com.jiotesseract.mr.category" android:value="1" />
    <meta-data android:name="com.jiotesseract.platform" android:value="LITE" />
    <activity android:name="com.jiotesseract.mr.sdk.JmrUnityActivity" android:label="@string/app_name" android:launchMode="singleTask" android:configChanges="orientation|keyboardHidden|screenSize|screenLayout">
      <intent-filter>
        <action android:name="android.intent.action.MAIN" />
        <!--<category android:name="android.intent.category.LAUNCHER" />-->
        <category android:name="tesseract.intent.category.MR_LAUNCHER" />
      </intent-filter>
      <meta-data android:name="unityplayer.UnityActivity" android:value="true" />
    </activity>
  </application>
  <!--<uses-permission android:name="android.permission.CAMERA" />-->
  <!--uncomment permission  to use camera example -->
  <!--<uses-permission android:name="android.permission.RECORD_AUDIO" />-->
  <!-- permission is required to use Voice example -->
  <!--HARD STOPPED PERMISSIONS-->
  <uses-permission android:name="android.permission.RECORD_AUDIO" tools:node="remove" />
  <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" tools:node="remove" />
  <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" tools:node="remove" />
  <uses-permission android:name="android.permission.READ_PHONE_STATE" tools:node="remove" />
  <uses-permission android:name="android.permission.READ_PRIVILEGED_PHONE_STATE" tools:node="remove" />
  <uses-permission android:name="android.permission.WAKE_LOCK" />
</manifest>
```
{% endcode %}
