# Building to Target Device

In this section, we will look at the steps to build your application for **JioGlass**.

### Setting up Unity for Target Device

* Go to **File -> Build Settings** to open the **Build Settings** dialogue box.

![](../.gitbook/assets/36.png)

* In Platform under Build Settings, Choose **Android** and click on **Switch Platform** if not done already as the destination platform.

![](../.gitbook/assets/37.png)

* Ensure your scene(s) are added to the **Scenes in the Build** section. If not, then open your current scene(s) in the unity editor and click on Add Open Scenes under build settings. You can also drag and drop your scene into the build settings window.

![](../.gitbook/assets/38.png)

* Click on **Player Settings** to configure the player settings for your target device.

![](../.gitbook/assets/39.png)

### Player Settings

Ensure that your Target Device and the Development System are configured to build for Android.

#### Configure the Player Settings as shown below for Android Device

* Under the **Resolution and Presentation** tab, set the **Default Orientation** to **Landscape Left**.

![](../.gitbook/assets/40.png)

* Under the **Other Settings** tab, set the **Graphics APIs** to **OpenGLES2**, and remove all others.

![](../.gitbook/assets/41.png)

* Under the **Other Settings** tab, deselect the **Multithreaded Rendering**.

![](../.gitbook/assets/42.png)

* Under the **Other Settings** tab, set the **Minimum API Level** to **Android 8.0 (API Level 26)** or above and **Target API Level** to **anything above Android 8.0**.

![](../.gitbook/assets/43.png)

* Plugin your Target Android device into your Development System.

![](../.gitbook/assets/44.png)

* Build the Application.

![](../.gitbook/assets/45.png)

#### Running the Application

* Run the build on your Android Device.
* Insert your phone into the **Holoboard** such that the phone’s top side is facing the left side while the screen is facing away from you.

![](../.gitbook/assets/46.jpeg)

* Enjoy.
