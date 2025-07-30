# iOS Deep linking

1. Deep linking is necessary to access applications from the JioVerse Store within the JioImmerse iOS application.
2. After providing the deep link, the application becomes accessible from the JioVerse Store within the JioImmerse application.
3. Once the user installs the application from the JioVerse Store, it will appear in the list of installed applications within the JioImmerse application.
4. The user can then access the installed application from within the JioImmerse application.

## Generating Deep Link

1. Open your Xcode project.
2. Goto Info > URL types > Item 0 > URL Schemas > Item 0
3. Copy this value which resembles your application name

{% hint style="warning" %}
Make sure **NOT** to include any special characters or white spaces; if present, remove them.
{% endhint %}

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

4. In Developer Console go to your iOS app > Upload Build&#x20;
5. In the Deep link section insert value copied in step 3. Append it with `://`

Example

> From Step 3 you copied `ApplicationName`
>
> then in Deep link enter `ApplicationName://`

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### Checking Your Deeplink Functionality

To check if your deep link is working properly. Then enter your application deep link in your browser.&#x20;

#### Check 1 -

When your application is not installed. The browser should be redirected to the app store.&#x20;

#### Check 2 -

When your application is installed with your application containing associated domains capability. The browser should open the application.&#x20;
