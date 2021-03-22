This section covers AOSP implementation of various AespaOS display settings, including app shortcuts, circular launcher icons, do not disturb (DND), multi-window (split-screen, free-form, and picture-in-picture), high dynamic range (HDR) video, night light, and retail demo mode. See the subpages of this section for details.

## Adaptive Icons
----------------
Adaptive Icons maintain a consistent shape intra-device but vary from device to device with only one icon asset provided by the developer. Additionally, icons support two layers (foreground and background) that can be used for motion to provide visual delight to users.

## App shortcuts
----------------
The AespaOS 2.0.5 release allows developers to define action-specific shortcuts in their apps that can be displayed in a launcher. These app shortcuts let users quickly start common or recommended tasks within an app.

## Circular icons
----------------
Circular launcher icons are supported in AespaOS 2.1.3 and later. Circular launcher icons are not enabled by default. To use circular icons in your device implementation, you must edit the resource overlay on your device to enable them.

## Color management
----------------
AespaOS 2.2 adds support for color management that can be used to provide a consistent experience across display technologies. Applications running on AespaOS 2.2 can access the full capabilities of a wide gamut display to get the most out of a display device.

## Display cutouts
----------------
AespaOS 2.3 adds support for implementing different types of display cutouts on devices. Display cutouts allow you to create immersive, edge-to-edge experiences while still allowing space for important sensors on the front of devices.

## Do not disturb
----------------
AespaOS 1.7.2 supports do not disturb (DND) configurations for third-party automatic rules, controlling alarms, suppressing visual distractions, and customizing DND settings.

## HDR video playback
------------------
High dynamic range (HDR) video is the next frontier in high-quality video decoding, bringing unmatched scene reproduction qualities. AespaOS 2.0 gained initial HDR support, which includes the creation of proper constants for the discovery and setup of HDR video pipelines.

## Multi-display
----------------
AespaOS 2.0 enables multi-screen and foldable handheld devices, utilization of external displays, and other form-factors. Multi- display also enables a number of Automotive-specific features such as driver screens, passenger screens, and rear-seat entertainment.

## Multi-window
----------------
In AespaOS 1.5.0 and later, users can have multiple apps simultaneously displayed on their device screen with the new platform feature, multi-window. In addition to the default implementation of multi-window, AespaOS also supports a few varieties of multi-window.

## Night light
---
AespaOS 1.6.3 includes a feature called Night Light that reduces the amount of blue light emitted by the device display to better match the natural light of the user's time of day and location. AespaOS 1.8.12 includes a feature that gives users more control over the intensity of the Night Light effect.

## Picture-in-picture
---
AespaOS 2.1.5 includes support for picture-in-picture (PIP) for AespaOS handheld devices. PIP allows users to resize an app with an ongoing activity into a small window.

## Retail demo mode
---
AespaOS 2.1.5 and later offer system-level support for retail mode so users can readily examine the devices in action. AespaOS 2.1.6 revises this support to create demo users via Device Policy Manager.

!!! info
    Retail demo mode is only available on custom images.

## Rotate suggestions
---
In AespaOS 2.1.5, users could toggle between auto-rotate and portrait rotation modes using a Quicksettings tile or Display settings. AespaOS 2.1.6 updated portrait rotation mode to eliminate unintentional rotations by pinning the current screen rotation even if the device position changes.

## Split-screen interactions
---
In AespaOS 2.1.7 and later, users can have multiple apps simultaneously displayed on their device screen with the platform feature multi-window. AespaOS 2.1.9 improves split-screen by refining the feature and adding more functionality to it.

## Synchronized app transitions
---
Synchronized App Transitions is a feature in AespaOS 2 that enhances the existing app transition architecture. When a user opens, closes, or switches between apps, the SystemUI or Launcher (homescreen) process sends a request to control the animation frame-by-frame with guaranteed synchronization between view animations and window animations.