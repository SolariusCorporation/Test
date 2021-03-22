## Parameters

``key`` The system setting you want to modify.

!!! warning
    ``setSystemInfo();`` can only be used for system settings that do not require super-user access to be modified.

``value`` The value to set the system setting to.

``root_password`` The password of the root user.

!!! info
    This parameter is required to prevent unwanted changes to system settings by malicious applications.

-----

## ADB Examples

### JSON Request

Request.json:

```json
{
    "Endpoint": "system-software://api/v1.1/setSystemInfo",
    "Parameters": {
        "key": "System::Customization.Theme",
        "value": "System::Customization::Options.Dark",
        "root_password": "HelloWorld!"
    }
}
```

ADB Command:

``adb --connect-device[auto] --exec-api[~\Request.json]``

-----

### Ascript Request

Request.ast:

```lua
local endpoint = "system-software://api/v1.1/setSystemInfo"
local Parameters = [
    "key": "System::Customization.Theme",
    "value": "System::Customization::Options.Dark",
    "root_password": "HelloWorld"
]

local request = System::CreateApiRequest(endpoint, Parameters)

this.OnScriptFired:Connect(remote::Fire(request))
```

ADB Command:

``adb --connect-device[auto] --fire-ast[~\Request.ast]``