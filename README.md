# Kotlin-build

## Introduction
This repository contains GitHub Actions workflows for building and releasing Android applications written in Kotlin. The main workflow, defined in `app-build.yml`, automates the building, signing, and releasing of the application.

## Workflow: Android Build and Release

### Overview
The `Android Build and Release` workflow triggers on every push to the master branch. It performs the following main tasks:
- Sets up a Java and Android environment.
- Builds the release version of the Android application.
- Signs the APK.
- Publishes the APK as a release.

### Configuration
This workflow requires you to provide the following secrets in the repository settings:
- `SIGNING_KEY`: Base64 encoded content of the Android signing key store file (*.jks).
- `ALIAS`: Alias of the key within the key store.
- `KEY_STORE_PASSWORD`: The password for the key store file.
- `KEY_PASSWORD`: The password for the key.

## Usage
To use this workflow:
1. Place the `app-build.yml` file in the `.github/workflows` directory of your repository.
2. Ensure all required secrets are configured in your GitHub repository.
3. Push changes to the master branch.
4. The workflow will run automatically, building, signing, and releaseing your application.
5. After the workflow completes, check the created release in your repository's "Releases" section.
6. Validate the generated APK and release informaion, make any necessary corrections manually.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
