# AespaOS Developer CLI Update Log
## [2.0.0] - March 20 2021
### Added
- Added ADB (Aespa Debug Bridge) to configure and tweak devices remotely.
- **Methods**
    - ``getSystemInfo([query]);`` Returns a table of system information.
    - ``setSystemInfo([key], [value], [root_password]);`` Sets system settings to passed value.
    - ``getConnectedDevices();`` Returns a table of connected devices.
- **Events**
    - ``adb:SystemConnected``
    - ``adb:SystemPowerStatusChange``
    - ``adb:SystemConfigurationChange``
    - ``adb:DeviceExternalDeviceStatusChange``
    - ``adb:SecurityPromptShown``

### Changed
- Nothing.

### Fixed
- Fixed file quarantine.