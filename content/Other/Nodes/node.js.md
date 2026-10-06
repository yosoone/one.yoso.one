---
publish: true
permalink: /Other/Nodes/node.js.md
created: 2026-05-29
modified: 2026-10-06T05:52:34.399Z
published: 2026-05-29
---

mac 2018 v10.16.3

---

You're all set! Node.js 26.2.0 is installed and set as your default.

You can verify anytime with:

bash

```bash
node --version   # v26.2.0
npm --version
```

And if you ever need to switch versions:

bash

```bash
nvm use 10.16.3   # switch back to old version
nvm use 26.2.0    # switch back to v26
```





---

/Users/yoso/.nvm/versions/node/v26.2.0/bin/npx

11:20

Perfect. Here's your exact config to paste into `claude_desktop_config.json`:

json

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "/Users/yoso/.nvm/versions/node/v26.2.0/bin/npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/Users/yoso/Library/Mobile Documents/iCloud~md~obsidian/Documents/Yoso Synch"
      ]
    }
  }
}
```

In Claude Desktop: **Settings → Developer → Edit Config**, replace everything with the above, save, then fully quit (Cmd+Q) and reopen.

Then test it by asking: _"List my Daily Notes folder."_

---

DEFAULT DESKTOP CONFIG PRE CHANGES

{
"coworkUserFilesPath": "/Users/yoso/Claude",
"preferences": {
"coworkScheduledTasksEnabled": false,
"ccdScheduledTasksEnabled": true,
"bypassPermissionsGateByAccount": {
"809aee04-3fc4-4e38-bfb0-3cd96998378c": false
},
"coworkWebSearchEnabled": true,
"remoteToolsDeviceName": "mac-mini-local",
"epitaxyPrefs": {
"starred-local-code-sessions": \[],
"starred-cowork-spaces": \[],
"starred-session-groups": \[],
"dframe-local-slice": {
"pinnedOrder": \[],
"customGroupAssignments": {},
"customGroupOrder": {}
}
},
"sidebarMode": "chat"
}
}

---

merged

{
"coworkUserFilesPath": "/Users/yoso/Claude",
"preferences": {
"coworkScheduledTasksEnabled": false,
"ccdScheduledTasksEnabled": true,
"bypassPermissionsGateByAccount": {
"809aee04-3fc4-4e38-bfb0-3cd96998378c": false
},
"coworkWebSearchEnabled": true,
"remoteToolsDeviceName": "mac-mini-local",
"epitaxyPrefs": {
"starred-local-code-sessions": \[],
"starred-cowork-spaces": \[],
"starred-session-groups": \[],
"dframe-local-slice": {
"pinnedOrder": \[],
"customGroupAssignments": {},
"customGroupOrder": {}
}
},
"sidebarMode": "chat"
},
"mcpServers": {
"filesystem": {
"command": "/Users/yoso/.nvm/versions/node/v26.2.0/bin/npx",
"args": \[
"-y",
"@modelcontextprotocol/server-filesystem",
"/Users/yoso/Library/Mobile Documents/iCloud~md~obsidian/Documents/Yoso Synch"
]
}
}
}
