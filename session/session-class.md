---
description: The root of any interaction with EcoleDirecte.
---

# The Session class

```javascript
import { Session } from "ecoledirecte.js"
```

The `Session` class is quite simple to use. It's actually just a stack of properties, nothing much, and it's mostly used to generate an extension of the [`Account`](../accounts/student-class.md) class, depending on the account type of your session.

```javascript
const session = new Session("username", "password")
```

