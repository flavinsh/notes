---
tags:
  - Tech
  - Android
---
The **Android Open Source Project** (AOSP) is the repository of source code that is responsible for the core of the [[Android]] operating system. Using code from AOSP, anyone can download and create their own operating system based on Android. 
> [!tldr] TLDR: AOSP is the open source portion of Android. 

> [!links]- 
> - [TechTarget](https://www.techtarget.com/searchmobilecomputing/definition/Android-Open-Source-Project-AOSP)
## What's included ?
The AOSP code contains the things needed to make a basic OS and some core apps. It includes: 
- the [[kernel]]
- the hardware abstraction layer
- the Android runtime
- some core apps

## What's not included ?
It does not include all the pieces needed to make a functioning smartphone though. A device manufacturer will need to add other portions that are not open source, such as device drivers and Google apps:
- The majority of Android-based smartphones have licensed Google apps that come preinstalled.
- Some device manufacturers will only use the open-source components of AOSP and not the Google proprietary fonctions. For example, Amazon Fire OS is AOSP-based but does not come with Google services (so device owners must use the Amazon app store).

> [!cite] To help illustrate the AOSP, it is like the plans to make a car engine and its controls. The manufacturer will need to add the wheels, body, interior and styling. 

Third-party ROM makers can freely produce and distribute replacement operating systems based on AOSP for old devices but cannot include Google services in the code.

## Is AOSP the same as Android ?
Not exactly. Since AOSP doesn't provide everything needed to compile a complete OS, it isn't stock or plain Android. Google would also say that the non-open source Google apps are needed to complete the Android experience. 

Android-based systems that stick close to AOSP without making many changes or replacing the launcher are often easier to run and more consistent though.





