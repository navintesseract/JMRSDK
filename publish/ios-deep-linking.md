# iOS Deep linking

1. Deep linking is necessary to access applications from the JioVerse Store within the JioImmerse iOS application.
2. After providing the deep link, the application becomes accessible from the JioVerse Store within the JioImmerse application.
3. Once the user installs the application from the JioVerse Store, it will appear in the list of installed applications within the JioImmerse application.
4. The user can then access the installed application from within the JioImmerse application.

## Generating Deep Link

Prerequisite: Publish the application on Appstore / Test Flight

{% hint style="warning" %}
Step Xcode I and Xcode II need to be done with every build.
{% endhint %}

### Firebase I

Goto [console.firebase.google.com](https://console.firebase.google.com/)

Add a project

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.17.57 PM.png" alt=""><figcaption></figcaption></figure>

Enter application name

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.18.11 PM.png" alt=""><figcaption></figcaption></figure>

Create Project

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.18.24 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.19.10 PM.png" alt=""><figcaption></figcaption></figure>

Goto iOS

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.20.06 PM.png" alt=""><figcaption></figcaption></figure>

Create your application

Enter Apple bundle ID, App name, and App store ID (Mandatory to enter all fields)

{% hint style="info" %}
Get the App Store ID by going into your application, when uploaded on Test Flight in App Store Connect > App information > Apple ID
{% endhint %}

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.22.36 PM.png" alt=""><figcaption></figcaption></figure>

Get the Team ID for Generating GoogleService-info.plist in next step

<figure><img src="../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

Download the GoogleService-Info.plist

<figure><img src="../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

### Xcode I

Add the above downloaded GoogleService-Info.plist in Unity-iPhone root folder

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.23.36 PM.png" alt=""><figcaption></figcaption></figure>

Select add framework button to add the firebase sdk

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.27.11 PM.png" alt=""><figcaption></figcaption></figure>

Click on "Add Other.." dropdown

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.27.45 PM.png" alt=""><figcaption></figcaption></figure>

Select "Add Package Dependency.."

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.28.01 PM.png" alt=""><figcaption></figcaption></figure>

When prompted, add the Firebase Apple platforms SDK repository:

```
  https://github.com/firebase/firebase-ios-sdk
```

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.28.45 PM.png" alt=""><figcaption></figcaption></figure>

Choose the Firebase library > FirebaseDynamicLinks

<figure><img src="../.gitbook/assets/MicrosoftTeams-image (5) (1).png" alt=""><figcaption></figcaption></figure>

### Firebase II

Goto Engage > Dynamic Links

Create a dynamic link page with the URL ending with _<mark style="color:yellow;">page.link</mark>_

{% hint style="success" %}
Keep your dynamic link page handy. It will be required in step Xcode II.
{% endhint %}

Create a new Dynamic Link

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.39.02 PM.png" alt=""><figcaption></figcaption></figure>

In **Deep Link URL**; enter your application URL&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.41.52 PM.png" alt=""><figcaption></figcaption></figure>

Define the link behavior for Apple to Open the deep link in your Apple app.

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.42.47 PM.png" alt=""><figcaption></figcaption></figure>

Select your application in the dropdown

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 7.42.53 PM.png" alt=""><figcaption></figcaption></figure>

Create the deep link.

Now you need to associate your generated page to Xcode as sown in Xcode II.

### Xcode II

Unity iPhone > Signing & Capabilities > All > +Add Capacity > Associated Domains:

1. webcredentials:_<mark style="color:yellow;">pagelink</mark>_
2. applinks:_<mark style="color:yellow;">pagelink</mark>_
3. activitycontinuation:_<mark style="color:yellow;">pagelink</mark>_

{% hint style="info" %}
In the above Associated Domains replace _<mark style="color:yellow;">pagelink</mark>_ with dynamic link page generated in step Firebase II.
{% endhint %}

Goto Unity-iPhone > Info > URL Types > URL Schemes and clear it.

<figure><img src="../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

Now create another build of your application and publish it to the App Store

Your deep link is the URL that you get in Firebase. It should be in this format. `https://appname.page.link/page`

### Checking Your Deeplink Functionality

To check if your deep link is working properly. Then enter your application deep link in your browser.&#x20;

#### Check 1 -

When your application is not installed. The browser should be redirected to the app store.&#x20;

#### Check 2 -

When your application is installed with your application containing associated domains capability. The browser should open the application.&#x20;
