# Device State

To get the currently active device, use the below function.

```csharp
int deviceID = JMRRigManager.Instance.getDeviceID();
// or cast into device type enum
JMRRigManager.DeviceType deviceType = (JMRRigManager.DeviceType) deviceID;
```

This returns an int which tells the device you are currently running on. It is mapped in an enum as follows.

<table data-full-width="false"><thead><tr><th>DeviceType</th><th>Value</th><th>Device Name</th></tr></thead><tbody><tr><td>Editor</td><td>0</td><td>Unity Editor</td></tr><tr><td>JioHoloboard</td><td>1</td><td>JioPrism</td></tr><tr><td>JioGlass</td><td>2</td><td>JioGlass</td></tr><tr><td>JioCardboard</td><td>3</td><td>JioDive</td></tr></tbody></table>

## JioDive Methods

| Method                                    | Description                    |
| ----------------------------------------- | ------------------------------ |
| [DiveGyroStatus](jiodive-device-state.md) | Checks if device is being used |

## JioGlass Methods

| Method                                                                   | Description                                |
| ------------------------------------------------------------------------ | ------------------------------------------ |
| [Power State Change](jioglass-device-state.md#jioglass-proximity-sensor) | Called when device proximity value changes |

## Controller Methods

| Controller & Gamepad Method                                                    | Description                        |
| ------------------------------------------------------------------------------ | ---------------------------------- |
| [OnConnected](controller-device-state.md#controller-connected-disconnected)    | Called when device is connected    |
| [OnDisconnected](controller-device-state.md#controller-connected-disconnected) | Called when device is disconnected |

| Controller Method                                                       | Description                              |
| ----------------------------------------------------------------------- | ---------------------------------------- |
| [OnBatteryUpdate](controller-device-state.md#battery-percentage-update) | Called when battery percentage updated   |
| [GetBatteryPercentage](controller-device-state.md#battery-percentage)   | Returns battery percentage of controller |
