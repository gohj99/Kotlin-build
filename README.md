# Kotlin-build

## Introduction
This repository contains GitHub Actions workflows for building and releasing Android applications written in Kotlin. The main workflow, defined in `app-build.yml`, automates the building, signing, and releasing of the application.

## Workflow: Android Build and Release

### Overview
The `Android Build and Release` workflow triggers on every push to the master branch. It performs the following main tasks:
- Sets up a Java and Android environment.
- Builds the release version of the Android application.
- Signs the APK.
- Publishes the APK as a GitHub release.

### Configuration
This workflow requires the following secrets to be set in the repository:
- `SIGNING_KEY`: Base64 encoded signing key for Android.
- `ALIAS`: Alias of the signing key.
- `KEY_STORE_PASSWORD`: Password for the key store.
- `KEY_PASSWORD`: Password for the key.

## Usage
To use this workflow:
1. Ensure all required secrets are configured in your GitHub repository.
2. Push changes to the master branch.
3. The workflow will run automatically, building, signing, and releaseing your application.
4. After the workflow completes, check the created release in your repository's "Releases" section.
5. Validate the generated APK and release informaion, make any necessary corrections manually.

## Files
### `app-build.yml`
This file contains the definition of the `Android Build and Release` workflow. It includes steps for checking out the code, setting up Java and Android SDK, building the APK, and handling the release process.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
