# Setting up a Jio Mixed Reality Project in Unity

This section will help you set up a Project so that you can start developing applications using **JMRSDK**. You will need Unity Game Engine (any version above 2019.4.3f1) and the latest version of the JMRSDK package.

### Importing the SDK

* Download any supported version of **Unity**. During the install, ensure that you have **Android Build Support** selected as your target platform.
* Open **Unity** and create a new Project.
* Use the latest version of **Jio Mixed Reality SDK** (JMRSDK).
* Navigate to **Assets -> Import-Package -> Custom Package** as shown below.

<div align="center"><img src="../.gitbook/assets/0.png" alt="Import-Package"></div>

* Navigate to the folder where you have stored the SDK package and select the file named **JMRSDKv4.1.0.unitypackage** where(for example:) **4.1.0** is the **version** number.
* Once the **Import Unity Package** dialog opens, select **All** at the bottom of the dialog and then select **Import**.

![Package Contents](../.gitbook/assets/1.png)

* After the import process is complete, a new folder will be created under **Assets** named **JMRSDK**.

### Setting up your Jio Mixed Reality Scene

* If you are creating a new scene, ensure that no Camera component is present in the scene. **Remove the Main Camera (if any) from your scene.**
* After you have imported JMRSDK, you will see a new **JioMixedReality** menu on the top menu bar. Click on it and then click on Configure scene for **JioMixedReality** as shown below.

![Configure Scene](../.gitbook/assets/2.png)

* You should now see a **JMRMixedReality** object in your scene as shown in the image below.

![Elements Added](../.gitbook/assets/3.png)

* Your scene is now ready to be used with **JMRSDK**. To test this, let’s add a cube to the scene.
  1. Go to **GameObject -> 3D Object -> Cube**
  2. Set the position of this **Cube** to **(0, 0, 5)**.

![Add Cube to the scene](../.gitbook/assets/4.png)

* You can now follow the instructions provided in the **Publishing** section to build your first application to your **Target Device**.
* Once you run the application on **JioGlass**, you will notice the **Cube** floating somewhere around you. (You might have to look around to find it! OR you can **long-press** the **Home Button** to **Recenter** the screen which will bring the **Cube** in front of you). Have a look at the controller interactions below to get an idea of how to use the JioGlass controller.

### Setting up System UI configuration

{% hint style="info" %}
**Mandatory**: Configure System UI in all applications before building your app.
{% endhint %}

From Menu, select

JioMixedReality > SystemUI > UpdateSortingLayer

![](<../.gitbook/assets/image (17).png>)
