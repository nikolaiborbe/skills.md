# Contact Nikolai via Apple Notes

Send messages to Nikolai's phone through Apple Notes. Notes sync instantly via iCloud.

## Create a new note

```bash
osascript -e 'tell application "Notes"
    make new note at folder "Notes" with properties {name:"Title", body:"<h1>Title</h1><br>Body text here"}
end tell'
```

## Update an existing note

Find notes by name with `first note whose name contains "keyword"`. Format content with HTML tags: `<h1>`, `<br>`, `<b>`, etc.

```bash
osascript -e 'tell application "Notes"
    set theNote to first note whose name contains "keyword"
    set body of theNote to "<h1>Title</h1><br>Updated content"
end tell'
```

## Update the CC Status note

At the start and end of long tasks, update the "CC Status" note with your current progress:

```bash
osascript -e 'tell application "Notes"
    set theNote to first note whose name contains "CC Status"
    set body of theNote to "<h1>CC Status</h1><br>Status update here"
end tell'
```
