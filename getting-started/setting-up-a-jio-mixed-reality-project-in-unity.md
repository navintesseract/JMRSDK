# Setting Up A Jio Mixed Reality Project in Unity

This section will help you set up a Project so that you can start developing applications using **JMRSDK**. You will need Unity Game Engine (any version above 2019.4.3f1) and the latest version of the JMRSDK package.

### Importing the SDK

* Download any supported version of **Unity**. During the installation, ensure that you have **Android Build Support** selected as your target platform.
* Open **Unity** and create a new Project.
* Use the latest version of **Jio Mixed Reality SDK** (JMRSDK).
* Navigate to **Assets -> Import-Package -> Custom Package** as shown below.

<div align="center"><img src="../.gitbook/assets/0.png" alt="Import-Package"></div>

* Navigate to the folder where you have stored the SDK package and select the JMRSDK-Core package.
* Once the **Import Unity Package** dialogue opens, select **All** at the bottom of the dialogue and then select **Import**.

![Package Contents](../.gitbook/assets/1.png)

* After the import process is complete, a new folder will be created under **Assets** named **JMRSDK**.

### Configuring your Project for JioGlass Lite

* Navigate JioMixedReality -> Manifest -> Configure for LITE as shown below

<figure><img src="https://lh3.googleusercontent.com/d8abPKNu6pd_dk6-DfaCelhZfY0souvEE9af7ZAyTQcixHjq8gnHCy-limYnZPdSoz_YcIPtYHIsm6sgM1D5pcKAKMg5WAhu80M6iznD8lQKaiTS0WSSequnD4dnAKzqKc00AluUwgaSNug4z7i2lzYvzSDOry6-AtUbmJVaJDIaSjBvwa4yxzbG7_nx1ijcLPXkJw" alt=""><figcaption><p>Configuring your project for JioGlass Lite</p></figcaption></figure>

* Ignore any debug errors if present. You will get a debug log saying Manifest status as completed when the process completes successfully.

<figure><img src="https://lh3.googleusercontent.com/ihh63CN1T7K8v_Ji5u-cYRpsg4GjHqWH-gcW-RNlqzLlrVUgAJWd13a3zjk_FibebvGbf9FONr_D3aM_34yVCpet6G2P5IHSpcIi6btR9dWS9aqxD9RJaDaMofZ56sYkQPcPhkLHg3PMDJKRG3UuKIr1xGGwYTIiJya3xuHPHAODNxEsDmqscyruKemd2I37bC34Bg" alt=""><figcaption><p>Manifest Setup Complete</p></figcaption></figure>

* Your project is now set up to build Applications for JioGlass Lite Ecosystem.

### Adding Category Tag In AndroidManifest

* Find the value corresponding to your application category from the table below -&#x20;

| Category            | Value |
| ------------------- | ----- |
| Entertainment       | 0     |
| Gaming              | 1     |
| Learning            | 2     |
| Productivity        | 3     |
| Utilities           | 4     |
| Health and Wellness | 5     |
| Shopping            | 6     |
| Miscellaneous       | 7     |

* Edit the "android:value" parameter in the following line in your AndroidManifest to reflect your JioGlass Lite Application in the right category. Ensure that you use the same category as used in Developer Console while creating your application listing

```csharp
<meta-data android:name="com.jiotesseract.mr.category" android:value="1" />
```

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

* You can now follow the instructions provided in the **Publishing** section to build your first application for your **Target Device**.
* Once you run the application on **JioGlass**, you will notice the **Cube** floating somewhere around you. (You might have to look around to find it! OR you can **long-press** the **Home Button** to **Recenter** the screen which will bring the **Cube** in front of you). Have a look at the controller interactions below to get an idea of how to use the JioGlass controller.

### Setting up System UI configuration

{% hint style="info" %}
**Mandatory**: Configure System UI in all applications before building your app.
{% endhint %}

From Menu, select

JioMixedReality > SystemUI > UpdateSortingLayer

![](<../.gitbook/assets/image (24).png>)
