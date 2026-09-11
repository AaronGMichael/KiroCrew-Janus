---
name: Bug report
about: Something broken in the extension
title: ''
labels: bug
assignees: ''
---

**What happened**

A clear description of the problem.

**Expected behavior**

What you expected instead.

**Environment**

- Extension version (Extensions panel → KiroCrew Janus):
- VSCode version (`Help → About`):
- OS / architecture:
- Remote-SSH? (yes/no):
- KiroCrew gateway version (`kirocrew --version`):

**KiroCrew output channel log**

View → Output → pick "KiroCrew" from the dropdown. Paste the relevant window below.
For auth/Forbidden issues, set `"kirocrew.logLevel": "debug"` and `"kirocrew.debugAuthTracing": true` in Settings, reproduce, and include the log — it never contains tokens or cookie values, only names and fingerprints.

```
<log here>
```
