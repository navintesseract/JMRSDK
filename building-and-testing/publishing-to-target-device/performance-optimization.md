# Performance Optimization

### IL2CPP Scripting Backend Support

All JMRSDK APIs are now compatible with IL2CPP Backend. With this type of compilation, in which Unity compiles code specifically for a target platform when it builds the native binary, is called ahead-of-time (AOT) compilation. The Mono compiles code at runtime, with a technique called just-in-time compilation (JIT).\
\
Also, with IL2CPP you will also be able to latest arm64 architecture for the best performance of your application.\
\
You can apply this configuration in the Project Setting section of your Unity Editor.

<figure><img src="../../.gitbook/assets/Scripting-Backend-Configration.png" alt=""><figcaption><p>Recommended Settings for Scripting Backend Configration</p></figcaption></figure>

{% hint style="info" %}
IL2CPP increases build times by 2X-5X. You can use Mono for faster development and IL2CPP for final optimized releases.
{% endhint %}

### OpenGLES3 Support

OpenGLES3 Graphics API is supported and should be placed above OpenGLES2 for preference.

<figure><img src="../../.gitbook/assets/Graphics-API-Settings.png" alt=""><figcaption><p>Reccomended Settings for Grapics APIs Settings</p></figcaption></figure>

### Multithreading Support

JMRSDK APIs are now threadsafe and compatible with Unity Multi-threading Rendering Settings **(Except Camera and Mediaplayer)**

<figure><img src="../../.gitbook/assets/Multithreading-Settings.png" alt=""><figcaption><p>Recommended Settings</p></figcaption></figure>

{% hint style="danger" %}
Apps using **Camera and Mediaplayer** provided in JMRSDK need to disable multithreading rendering settings.
{% endhint %}
