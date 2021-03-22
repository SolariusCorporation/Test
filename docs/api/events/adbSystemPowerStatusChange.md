## Information

``adb:SystemPowerStatusChange`` is fired when the system power status is changed. System power, as in the devices state changing into Sleep Mode, or Hibernation.

!!! info
    ``adb:SystemPowerStatusChange`` does not get fired for shutting down, or powering on.

-----

## ADB Examples

### Ascript Request

Listener.ast:

```lua
local event = "system-software://api/v1.1/Events/adb/SystemPowerStatusChange"

event.OnEventInvoked:Connect()
```

ADB Command:

``adb --connect-device[auto] --fire-ast[~\Request.ast]``