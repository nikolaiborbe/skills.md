# Human assistance
I wont be home, so you will have to figure out everything yourself. I have given you all permissions, but if you get stuck somewhere and really do need my help you have to think of something else.

# Contacting Nikolai via Apple Notes (iCloud sync)
You can send messages to Nikolai's phone using Apple Notes via osascript. Notes sync instantly via iCloud.

## Creating a new note
```bash
osascript -e 'tell application "Notes"
    make new note at folder "Notes" with properties {name:"Title", body:"<h1>Title</h1><br>Body text here"}
end tell'
```

## Updating an existing note
- Notes uses the first line / `<h1>` tag as its display name
- To find a note, search by name content: `first note whose name contains "keyword"`
- Use HTML for formatting: `<h1>`, `<br>`, `<b>`, etc.
```bash
osascript -e 'tell application "Notes"
    set theNote to first note whose name contains "keyword"
    set body of theNote to "<h1>Title</h1><br>Updated content"
end tell'
```

## CC Status note
There is a persistent "CC Status" note (search for name contains "CC Status"). Use this to update Nikolai on progress during long tasks. Update it with current status when starting and finishing work.