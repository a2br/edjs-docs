---
description: The root of any interaction with EcoleDirecte.
---

# La classe Session

```javascript
import { Session } from "ecoledirecte.js"
```

La classe `Session` est assez facile à utiliser. C'est en fait juste un tas de propriétés, rien de plus, et elle est particulièrement utilisée pour générer une extension de la classe [`Account`](../accounts/account-class.md), en fonction du type de compte de votre session.

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



