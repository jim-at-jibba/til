# Create global shortcuts

There are times when your software will need global shortcuts.

```javascript
app.on("ready", () => {
  createMainWindow()

  // Global shortcuts
  globalShortcut.register("CmdOrCtrl+R", () => mainWindow.reload())
  globalShortcut.register(isMac ? "Command+Alt+I" : "Ctrl+Shift+I", () =>
    mainWindow.toggleDevTools(),
  )

  // bit of garbage collection
  mainWindow.on("closed", () => (mainWindow = null))
})

```
