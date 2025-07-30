# Webcast

The webcasting feature enables users to share their screen views with others. This feature is handy for collaboration, remote demonstrations, and showcasing your gameplay and screen to others.&#x20;

## Setting up

To set up this capability on an Android platform using JMRSDK, follow these steps:

1. **Import the JMRSDK**: Ensure the JMRSDK is properly imported into your Android project.
2.  **Add WebRTC Package**: Include the WebRTC package required for webcasting by integrating it through the following Git URL:

    ```
    com.unity.webrtc@3.0.0-pre.6
    ```
3.  In Unity > JioMixedReality > Manifest > Show Asset > Check `Is Webcast Supported.`&#x20;

    <div align="left"><figure><img src="../.gitbook/assets/image.png" alt="" width="407"><figcaption></figcaption></figure></div>

## Testing webcast

### JioDive

To test the webcast functionality using JioDive, perform the following steps:

1. **Connect to Network**: Ensure the casting device and the webcast receiving device are connected to a stable and fast network to ensure seamless streaming.
2. **Initialize Webcast**: Launch the Companion app on your Android device and select Webcast.
3. Copy, share, and open the URL on another device where casting is to be seen.&#x20;
4. Start Webcast on the casting device.&#x20;
5. Put your phone in JioDive and select the desired app in MR Launcher.
6. **Verify Stream Quality**: Check the stream quality and adjust the settings to optimize performance.

### JioGlass

To test the webcast using JioGlass, follow these steps:

1. **Setup JioGlass**: Ensure that JioGlass is properly set up and connected.
2. Launch the Companion app on your device.
3. **Access Webcast Feature**: Open the relevant application that supports JioGlass and click webcast.
4. Copy, share, and open the URL on another device where casting is to be seen.&#x20;
5. Start Webcast on the casting device.&#x20;

## Troubleshooting Guide

Here's a list of common issues and solutions when using the casting function:

1. **Black Screen**
   * If the current network is restricted, consider switching to another one.
2. **Errors in Console**
   * Verify the Unity version you are using. Make sure it supports Webcast.
   * Reimport JMRSDK to resolve any compatibility/importing issues.
3. **There is no option to start Webcasting**
   * Check the version of the companion app. Ensure it is up to date.

