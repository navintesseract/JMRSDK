# Capturing Screenshot/Videos using scrcpy

* **Download scrcpy from:**
  * Windows: [link](https://github.com/Genymobile/scrcpy/releases/download/v1.16/scrcpy-win64-v1.16.zip)
  * For Linux: `$ sudo apt-get install scrcpy`&#x20;
  * For macOS: `brew install scrcpy` (Available in Homebrew)

&#x20;                                                                                           \---------

* **Run using Wireless Connection**
  * Open CMD/Terminal and go to ADB path
  * Connect your android device
  * Run `adb devices` to check the device is connected
  * Now run the following command: `adb tcpip 5555` _(The port 5555 is used here. You can use any port number you want)_
  * After the above command is executed, run `adb connect IP_ADDR:5555` (Replace IP\_ADDR with the IP Address of your device.)
  * Once done, disconnect the device and run scrcpy. It will start displaying your device’s screen wirelessly.
* **Run using USB Connection**
  * Connect your android device and simply click on the scrcpy.exe file present in the folder downloaded
  * Once the file is opened, it will start displaying the device’s screen.
* **Get Display ID**
  * JioGlass: Get DipsplayId by running the following command&#x20;
    * `adb shell dumpsys display | grep "HDMI"`
  * Holoboard: Not required.
*   **Recording videos using scrcpy**

    * Holoboard: To record the video, simply run the command `scrcpy --record myrecording.mp4` in scrcpy terminal opened already
    * JioGlass: To record the video, simply run the command `scrcpy --display <DisplayId> --record myrecording.mp4` in scrcpy terminal opened already



    **Note:** Currently, there is no option to stop the recording in scrcpy but the workaround for the same can be found here: [Github](https://github.com/Genymobile/scrcpy/issues/1032)

Scrcpy can do a lot more other things. Check other features of scrcpy, visit [**HERE**](https://github.com/Genymobile/scrcpy#features).

