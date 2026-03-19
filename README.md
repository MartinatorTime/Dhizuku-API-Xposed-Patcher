# Dhizuku-API-Xposed-Patcher

> **DISCLAIMER:** This project is intended **strictly for developer purposes, research, and testing only**. It is provided as-is, without any guarantees of stability, security, or functionality. By using this tool, you acknowledge that you are responsible for any potential issues, data loss, or system instability that may occur. Use at your own risk.

## Overview
Dhizuku-API-Xposed-Patcher is an experimental automation tool designed to streamline the integration of the Dhizuku API into Android applications using the LSpatch framework. 

This repository automates the patching process based on configurations defined in `build-apps.yml`. It is designed for developers who need to quickly iterate on patched builds to test compatibility between Dhizuku and various Android applications.

## Known Limitations & Behavior
* **Instability**: As an experimental tool, crashes are to be expected. It is not intended for production environments.
* **Initialization**: The patched application may crash on the first launch. This is common during the initial hook injection process.
* **Permission Handshake**: After installing and performing the initial setup, you must **Force Stop** the app to trigger the Dhizuku API permission dialog. Alternatively, attempting to initiate an app installation within the patched app may force the prompt to appear.

## Features
* **Developer-Focused**: Easy to fork and adapt for specific testing environments or custom module integration.
* **Automated Patching**: Uses a CI/CD-style approach to fetch upstream releases and apply patching logic automatically.
* **Release Artifacts**: Pre-patched builds are generated for testing purposes and are available on the [releases page](https://github.com/MartinatorTime/Dhizuku-API-Xposed-Patcher/releases/tag/Dhizuku-API-patched).

## Usage
1. Fork this repository.
2. Update `build-apps.yml` with your target applications and module requirements.
3. Use the provided automation scripts to generate patched APKs in your testing environment.

## Acknowledgements
This project leverages code and research from the following contributors and projects:

* **Patcher Frameworks**: [LSPatch](https://github.com/LSPosed/LSPatch) / [LSPatch](https://github.com/JingMatrix/LSPatch)
* **Xposed Module**: [Dhizuku-API-Xposed](https://github.com/iamr0s/Dhizuku-API-Xposed)
* **Targeted Apps**: [Obtainium](https://github.com/ImranR98/Obtainium), [Droid-ify](https://github.com/Droid-ify/client), [Neo-Store](https://github.com/NeoApplications/Neo-Store)
* **Code/Automation**: [MartinatorTime](https://github.com/MartinatorTime/auto-lspatch) and [dsys1100](https://github.com/dsys1100/tg-autolspatch)