# Android tools replace

If an app has `tools:replace` in `AndroidManifest.xml`, that indicates that the app is dependent on a .aar that already has these properties set in its `AndroidManifest.xml`. Using `tools:replace` overrides the values already set in the .aar dependency. This is necessary because if there are property conflicts between the app and its dependent .aars, the app will not compile.

For example, if the .aar dependency has `android:allowBackup` set to true, but the consuming application sets `android:allowBackup` to false, you either have to use `tools:replace="android:allowBackup"` or the app will not compile.

*source*: [stackoverflow: Bradford2000](https://stackoverflow.com/questions/51294469/tools-replace-in-androidmanifest)
