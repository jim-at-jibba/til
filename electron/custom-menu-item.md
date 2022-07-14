# Add custom menu item

To create custom menu items, you need to create a menu template and then feed that into the `Menu.buildFromTemplate`

```javascript
app.on("ready", () => {
  createMainWindow()

  const mainMenu = Menu.buildFromTemplate(menu)
  Menu.setApplicationMenu(mainMenu)

  // bit of garbage collection
  mainWindow.on("closed", () => (mainWindow = null))
})

// create menum template
const menu = [
  ...(isMac ? [{role: "appMenu"}] : []), // this readds the correct menu under app name for mac
  {
    label: "File",
    submenu: [
      {
        label: "Quit",
        accelerator: "CmdOrCtrl+W",
        click: () => app.quit(),
      },
    ],
  },
]

```
