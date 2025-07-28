# AndroidManifest update

If custom manifest is added to the project and not willing to directly replace the existing AndroidManifest.xml, following steps to be done.

1. Add following \<meta-data> tag in \<activity> tag

```
<meta-data android:name="unityplayer.UnityActivity" android:value="true" />
```

&#x20;   2\. Add / Replace existing JMRSDK AndroidManifest permissions with        following permissions. Your extra permissions should be added after these permission.

```
<uses-permission android:name="android.permission.RECORD_AUDIO" tools:node="remove" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" tools:node="remove"/>
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" tools:node="remove"/>
<uses-permission android:name="android.permission.READ_PHONE_STATE" tools:node="remove"/>
<uses-permission android:name="android.permission.READ_PRIVILEGED_PHONE_STATE" tools:node="remove"/>
<uses-permission android:name="android.permission.WAKE_LOCK"/>
```

3\. Uncomment permission from AndroidManifest or add following permission for using Camera.

```
<uses-permission android:name="android.permission.CAMERA"/>
```

Final **AndroidManifest** file should look like following

```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android" package="${applicationId}" xmlns:tools="http://schemas.android.com/tools" android:installLocation="preferExternal">
  <supports-screens android:smallScreens="true" android:normalScreens="true" android:largeScreens="true" android:xlargeScreens="true" android:anyDensity="true" />
  <application android:theme="@style/UnityThemeSelector" android:icon="@mipmap/app_icon" android:label="@string/app_name" android:requestLegacyExternalStorage="true" android:screenOrientation="landscape">
    <activity android:name="com.jiotesseract.mr.sdk.JmrUnityActivity"
			  android:label="@string/app_name"
        android:launchMode="singleTask"
			  android:configChanges="orientation|keyboardHidden|screenSize|screenLayout">
      <intent-filter>
        <action android:name="android.intent.action.MAIN" />
        <category android:name="android.intent.category.LAUNCHER" />
        <category android:name="tesseract.intent.category.MR_LAUNCHER"/> 
      </intent-filter>
      <meta-data android:name="unityplayer.UnityActivity" android:value="true" />
    </activity>
  </application>

  <!--<uses-permission android:name="android.permission.CAMERA"/>--> <!--uncomment permission  to use camera example -->
  <!--<uses-permission android:name="android.permission.RECORD_AUDIO"/>--> <!-- permission is required to use Voice example -->
 
  <!--HARD STOPPED PERMISSIONS-->
  <uses-permission android:name="android.permission.RECORD_AUDIO" tools:node="remove" />
  <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" tools:node="remove"/>
  <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" tools:node="remove"/>
  <uses-permission android:name="android.permission.READ_PHONE_STATE" tools:node="remove"/>
  <uses-permission android:name="android.permission.READ_PRIVILEGED_PHONE_STATE" tools:node="remove"/>
	
  <uses-permission android:name="android.permission.WAKE_LOCK"/>
 
</manifest>

```
