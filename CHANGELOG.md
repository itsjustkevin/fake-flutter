In general, our philosophy is to update the `stable` channel on a quarterly basis with feature updates. In the intervening period, occasionally we may decide a bug or regression warrants a hotfix. We tend to be extremely conservative with these hotfixes, since there's always a risk that fixing one bug introduces a new one, and we want the `stable` channel to always represent our most tested builds.

We intend to announce hotfixes to the [flutter-announce](https://groups.google.com/forum/#!forum/flutter-announce) group, and we recommend that you subscribe to that list if you publish an application using Flutter.

Note that we only hotfix the latest version -- if you see bugs on older versions of the `stable` channel, please consider moving to the latest `stable` channel version.

To ensure that you have the latest stable version with the hotfixes listed below, use the flutter tool at the command line as follows:

```
$ flutter channel stable
$ flutter upgrade
```

<!--
INTERNAL NOTE: PLEASE DON'T JUST PASTE ISSUE TITLES!

Make sure that the text here helps customers understand
whether they are likely to be affected by the issue,
without them needing to read each issue individually.
Our goal is to make the list easy for them to scan.

More information and tips:
docs/releases/Hotfix-Documentation-Best-Practices.md

INTERNAL NOTE
-->

## Flutter 3.27 Changes

### [3.27.1](https://github.com/flutter/flutter/releases/tag/3.27.1)

- [flutter/160041](https://github.com/flutter/flutter/issues/160041) - [Impeller][Android] Disables Impeller on older Android devices.
- [flutter/160206](https://github.com/flutter/flutter/issues/160206) - [Impeller][Android] Disables Android HardwareBuffer based swapchains on all devices.
- [flutter/160208](https://github.com/flutter/flutter/issues/160208) - [iOS] Fixes an issue on iOS preventing the ability to tap web view links in some plugins.

### [3.27.0](https://github.com/flutter/flutter/releases/tag/3.27.0)
Initial stable release.

## Flutter 3.24 Changes

### [3.24.5](https://github.com/flutter/flutter/releases/tag/3.24.5)
- [flutter/158125](https://github.com/flutter/flutter/pull/158125) - [iOS] Fixed a tool issue causing failures when `flutter build ios-framework --xcframework` copies Flutter debug symbols.
- [flutter/56301](https://github.com/flutter/engine/pull/56301) - [Android] Fixes a crash on Android devices when the surface is released unexpectedly when using PlatformView's.

### [3.24.4](https://github.com/flutter/flutter/releases/tag/3.24.4)
- [dart 3.5.4 changelog](https://github.com/dart-lang/sdk/blob/stable/CHANGELOG.md#354---2024-10-17)
- [flutter/154915](https://github.com/flutter/engine/pull/55366) - [macOS] Comply with the new Apple privacy manifest policy for the macOS Flutter engine framework and prevent the "Missing privacy manifest" warning when submitting a macOS app to the App Store.
- [flutter/153471](https://github.com/flutter/flutter/issues/153471) - [Tool] Fixes RPCError crash when setting up log filtering for Android devices.

### [3.24.3](https://github.com/flutter/flutter/releases/tag/3.24.3)
- [dart 3.5.3 changelog](https://github.com/dart-lang/sdk/blob/stable/CHANGELOG.md#353---2024-09-11)
- [flutter/154275](https://github.com/flutter/flutter/issues/154275) - [Android] Fixes performance issues on Android caused by engine threads not matching the core count.
- [flutter/154276](https://github.com/flutter/flutter/issues/154276) - [Impeller] Fixes an issue on iOS preventing mesh gradients from rendering correctly.
- [flutter/154349](https://github.com/flutter/flutter/issues/154349) - [Wasm] Fixes an issue on web causing Platform Views to break when compiled to Wasm.
- [flutter/154564](https://github.com/flutter/flutter/issues/154564) - [Impeller][iOS] Fixes an issue when using Impeller on iOS when using backdrop filters on older iPads, causing the GPU to hang.
- [flutter/154712](https://github.com/flutter/flutter/issues/154712) - [iOS] Fixes an issue on iOS causing video playback to flicker.
- [flutter/154892](https://github.com/flutter/flutter/issues/154892) - [Impeller][iOS] Fixes an issue when using Impeller on iOS causing a memory leak when using Platform Views.
- [flutter/154536](https://github.com/flutter/flutter/issues/154536) - [Tool] Fixes a CLI crash that occurs when shutting down after running a Flutter app on a browser.
- [flutter/154720](https://github.com/flutter/flutter/pull/154720) - Fixes an issue with the `Drawer` widget, causing it to open or close incorrectly.
- [flutter/154944](https://github.com/flutter/flutter/pull/154944) - [Tool] Fixes a Flutter tool crash that occurs when building Flutter modules for Android when using AGP 8.0+.

### [3.24.2](https://github.com/flutter/flutter/releases/tag/3.24.2)
- [Dart 3.5.2 Changelog](https://github.com/dart-lang/sdk/blob/stable/CHANGELOG.md#352---2024-08-28)
- [flutter/153949](https://github.com/flutter/flutter/issues/153949) - Fixes a crash on Android when deleting `EditableText` inside `CupertinoPageRoute`, with a CJK (chinese, japanese, korean) keyboard.
- [flutter/153939](https://github.com/flutter/flutter/issues/153939) - Fixes an issue on iOS where Flutter `TextField`s may stop accepting input.
- [flutter/152420](https://github.com/flutter/flutter/issues/152420) - Fixes scrolling jank on Android and iOS when a `SelectionArea`/`SelectableRegion` is used as a child of a Scrollable like `ListView` or `PageView`.
- [flutter/154199](https://github.com/flutter/flutter/pull/154199) - Removes excessive logging when building a freshly created template app for Android.
- [flutter/153967](https://github.com/flutter/flutter/pull/153967) - Fixes a host build failure on macOS when the `native assets` experiment is enabled, and there are no native asset frameworks to codesign.
- [flutter/153769](https://github.com/flutter/flutter/pull/153769) - When running a Flutter app, display a concise error message when connection to the device is lost.
- [flutter/154270](https://github.com/flutter/flutter/pull/154270) - Prevent preemptive gradle crash for android builds that would fail to build anyway but with a confusing error message.
- [flutter/54735](https://github.com/flutter/engine/pull/54735) - Fixes an error on Flutter Web where `onTap` is called twice on various widgets (`GestureDetector`, `InkWell`) when semantics are enabled.

### [3.24.1](https://github.com/flutter/flutter/releases/tag/3.24.1)

- [dart/56464](https://github.com/dart-lang/sdk/issues/56464) - Fixes resolving `include:` in `analysis_options.yaml` file in a nested folder in the workspace.
- [dart/56423](https://github.com/dart-lang/sdk/issues/56423) - Fixes source maps generated by `dart compile wasm` when optimizations are enabled.
- [dart/56374](https://github.com/dart-lang/sdk/issues/56374) - Fixes a bug in the `dart2wasm` compiler in unsound `-O3` / `-O4` modes where a implicit setter for a field of generic type will store null instead of the field value.
- [dart/56440](https://github.com/dart-lang/sdk/issues/56440) - Fixes a bug in the `dart2wasm` compiler that can trigger in certain situations when using partial instantiations of generic tear-offs (constructors or static methods) in constant expressions.
- [dart/56457](https://github.com/dart-lang/sdk/issues/56457) - The algorithm for computing the standard upper bound of two types, also known as UP, is provided the missing implementation for `StructuralParameterType` objects. In some corner cases the lacking implementation resulted in a crash of the compiler.
- [flutter/152047](https://github.com/flutter/flutter/issues/152047) - [Web] Fixes an issue in Flutter Web apps where when semantics are enabled, tapping on the label of a checkbox in a mobile browser won't togle the checkbox.
- [flutter/153308](https://github.com/flutter/flutter/issues/153308) - [Web] Adds source map support in `flutter run` / `flutter build` for `dart2wasm` for debugging in Chrome DevTools.
- [flutter/54446](https://github.com/flutter/engine/pull/54446) - [Web] Fixes an issue in Flutter Web apps where the app may crash if CanvasKit is loaded from the network instead of a cache.
- [flutter/152955](https://github.com/flutter/flutter/issues/152955) - [Impeller] Fixes an issue where when using unbound `saveLayers` rendering issues would occur.
- [flutter/153037](https://github.com/flutter/flutter/issues/153037) - [Impeller] Fixes an issue where RTL glyphs would render incorrectly.
- [flutter/153038](https://github.com/flutter/flutter/issues/153038) - [Impeller] Fixes an issue where padding would be applied incorrectly in `Canvas.drawVerticies` when using texture coordinates.
- [flutter/153041](https://github.com/flutter/flutter/issues/153041) - [Impeller] Fixes an rare issue causing applications to crash when using platform views on older iPhones.
- [flutter/153188](https://github.com/flutter/flutter/issues/153188) - [Impeller] Fixes a rendering issue on iOS devices using Impeller where clips do not appear around entities drawn with certain advanced blend modes.
- [flutter/54513](https://github.com/flutter/engine/pull/54513) - [iOS/MacOS] Fixes an issue preventing iOS Apps Store validation from failing for Flutter apps using Xcode versions before Xcode 16.
- [flutter/54518](https://github.com/flutter/engine/pull/54518) - Fixes an issue on OpenGL ES devices where a black screen would appear instead of the Flutter app output.
- [flutter/153117](https://github.com/flutter/flutter/pull/153117) [iOS/MacOS] Fixes an issue where compilation errors are not displayed in the output of `flutter run` when using Xcode 16.
- [flutter/153321](https://github.com/flutter/flutter/issues/153321) - [Desktop] Fixes an issue where older Windows devices could not run Flutter apps built using Flutter  3.21 or later.
- [flutter/153294](https://github.com/flutter/flutter/pull/153294) [Tool] Fixes an issue in the Flutter tool streamlining the crash message that occurs when running `flutter run -d chrome` and Chrome is closed before Flutter tries to close it.
- [flutter/153579](https://github.com/flutter/flutter/pull/153579) [Tool] Fixes an issue where users would experience large crash messages when `flutter run` or `flutter debug-adapter` are unable to connect to the Flutter web app.

### [3.24.0](https://github.com/flutter/flutter/releases/tag/3.24.0)
Initial stable release.

## Flutter 3.22 Changes

### [3.22.3](https://github.com/flutter/flutter/releases/tag/3.22.3) (July 17, 2024)

- [dart/55979](https://github.com/dart-lang/sdk/issues/55979) - Fixes an issue where `const bool.fromEnvironment('dart.library.ffi')` is true and conditional import condition `dart.library.ffi` is true in dart2wasm.
- [dart/55943](https://github.com/dart-lang/sdk/issues/55943) - Fixes an issue where FFI calls with variadic arguments on MacOS Arm64 would mangle the arguments.
- [flutter/149700](https://github.com/flutter/flutter/issues/149700) - [Impeller] Fixes rendering corruption when running on Intel mac simulators.
- [flutter/149701](https://github.com/flutter/flutter/issues/149701) - [Impeller] Fixes an issue on iOS that causese paths to render incorrectly.
- [flutter/149702](https://github.com/flutter/flutter/issues/149702) - [Impeller] Corrects and issue on iOs where coverage computation results in distored pixels in Impeller targets.
- [flutter/149704](https://github.com/flutter/flutter/issues/149704) - [Impeller] Fixes and issue on iOS where flickering may be occur when translating a blurred rounded rectangle.
- [flutter/149745](https://github.com/flutter/flutter/issues/149745) - [Impeller] Fixes a segfault on iOS when tessellating empty convex polygons.
- [flutter/149771](https://github.com/flutter/flutter/issues/149771) - [Impeller] Fixes a rendering error on iOS when advanced blend is double scaled.
- [flutter/53183](https://github.com/flutter/engine/pull/53183) - Fixes an issue where Linux apps show visual corruption on some frames
- [flutter/149856](https://github.com/flutter/flutter/issues/149856) - Clarifies Flutter Fix log on how to update Kotlin Gradle Plugin that was introduced in Flutter 3.19.
- [flutter/150617](https://github.com/flutter/flutter/pull/150617) - Fixes a bug in `flutter test` where `--flavor` wasn't considered when validating cached assets, causing the flavor-conditional asset bundling feature to not work as expected.
- [flutter/150724](https://github.com/flutter/flutter/issues/150724) - Fixes an issue on Web+Linux that prevents users from inputting data using the numpad.
- [flutter/150787](https://github.com/flutter/flutter/pull/150787) - Fixes and issue on Windows when running certain commands, such as `flutter run` or `flutter build`, users get a lengthy crash message including the full contents of a FileSystemException.
