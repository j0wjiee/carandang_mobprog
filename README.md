Part 3: Laboratory Discussion

1. What challenges did you encounter while installing or configuring Flutter?
During project initialization and configuration, my main challenges involved project directory structure, naming conventions, and target device availability. When generating the project using the VS Code Command Palette, the default project name (`flutter_application_1`) was initially retained instead of the required `carandang_mobprog` naming format, and nested folders were created. Additionally, when attempting to execute `flutter run` for the first time, the terminal returned a `No supported devices connected` message because no Android emulator was actively booted and the initial empty template lacked web platform support.

2. Did you encounter any errors when running `flutter doctor`?
I didn't encounter any blocking errors when running `flutter doctor`. The Flutter SDK, Android toolchain, Chrome, and connected devices all passed with green checkmarks, with only a minor Visual Studio Windows 10 SDK warning.

3. How did you resolve installation, dependency, SDK, or device-related issues?
Visual Studio Windows SDK Warning - Since my intended development platforms for this activity are Android and Web (Chrome) rather than native Windows desktop applications, this warning did not block my workflow and was safely bypassed.
Project Naming & Directory Cleanup - Using the VS Code terminal, I navigated back to the root `carandang_mobprogAY2627` directory, removed the stray default project folders, and ran `flutter create --empty carandang_mobprog` to cleanly initialize the project with the exact required name and full platform support (including `android`, `ios`, and `web`).
Device Connection - Once the `web` platform folder was generated and an active target device was selected in the VS Code bottom-right status bar, `flutter run` compiled and launched the application without errors.

4. What did you learn about configuring a Flutter development environment?
I learned how `flutter doctor` diagnoses platform-specific toolchains independently, allowing developers to verify whether missing components affect their actual target platform before spending time on unnecessary installations. I also learned the difference between creating projects via the VS Code GUI wizard versus the `flutter create` CLI flags (such as `--empty`), as well as how Flutter maps platform folders (`android`, `ios`, `web`) to available connected devices. 

5. What practices will you follow to make future Flutter development easier?
- Always run `flutter doctor` after environment or SDK updates to verify toolchain health before starting a new project.
- Verify the active working directory in the terminal (`cd`) and double-check project naming conventions before executing `flutter create`.
- Ensure an Android Emulator or target browser is selected in the VS Code status bar prior to running or debugging (`F5`) an application.
- Keep `README.md` updated alongside project milestones so documentation and source code stay synchronized in GitHub.