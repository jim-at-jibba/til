# How to fix "Error obtaining UI heirarchy"

I have found a number of time, when trying to debug Android apps with `uiautomatorviewer` I get the following error:

`Error obtaining UI hierarchy Error while obtaining UI hierarchy XML file: com.android.ddmlib.SyncException: Remote object doesn't exist`

To fix it:

```bash
adb kill-server

adb start-server
```

[Source](https://stackoverflow.com/questions/40214342/error-obtaining-ui-hierarchy-error-while-obtaining-ui-hierarchy-xml-file-com-an)