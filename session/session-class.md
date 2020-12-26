---
description: The root of any interaction with EcoleDirecte.
---

# The Session class

```javascript
import { Session } from "ecoledirecte.js"
```

The `Session` class is quite simple to use. It's actually just a stack of properties, nothing much, and it's mostly used to generate an extension of the [`Account`](../accounts/account-class.md) class, depending on the account type of your session.

```javascript
const session = new Session("username", "password")
```

## Properties

### `login()`

* no arguments
* returns an extension of `Account`

### `credentials`

* can only `get`
* returns the credentials given during the class init

### `token`

* last token given by EcoleDirecte

### `loginRes`

* complete login response got during the `login()` call



