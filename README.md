# Open in Obsidian

A one-file page that turns a web link into an Obsidian link, so apps that only accept `https://` links (Telegram buttons, for one) can still open a note.

```
https://your-name.github.io/open/#v=your-vault-name&f=Folder/Note
```

The vault and note names sit after the `#`. Browsers never send that part to the server, so the host sees only that the page was loaded, never which note. The page itself holds no data: it reads the fragment, opens `obsidian://open?vault=…&file=…`, and shows an "Open in Obsidian" button in case the automatic hand-off is blocked.
