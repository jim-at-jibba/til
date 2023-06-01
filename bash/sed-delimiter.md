# SED delimiter

- I have a script where I need to replace some text with a url. My initial script looked like this

```bash
#!/bin/sh

INPUT=$(gum input --placeholder "Name of task")
TASK_NUMBER=$(gum input --placeholder "Task number")
TASK_URL=$(gum input --placeholder "Task URL")

sed "s/\[Task Name\]/$INPUT/g; s/\[Ticket\]/[$TASK_NUMBER]/g; s/()/($TASK_URL)/g" /Users/jamesbest/code/other/wiki/Templates/Task.md > /Users/jamesbest/code/other/wiki/breedr/tasks/${INPUT}.md
```

- This caused issues as the url contained `/` characters which broke my SED code.
- Its possible for the delimiter to be any character. So by replacing the `/` with `,` this script was fixed

```bash
#!/bin/sh

INPUT=$(gum input --placeholder "Name of task")
TASK_NUMBER=$(gum input --placeholder "Task number")
TASK_URL=$(gum input --placeholder "Task URL")

sed "s,\[Task Name\],$INPUT,g; s,\[Ticket\],[$TASK_NUMBER],g; s,(),($TASK_URL),g" /Users/jamesbest/code/other/wiki/Templates/Task.md > /Users/jamesbest/code/other/wiki/breedr/tasks/${INPUT}.md

```
