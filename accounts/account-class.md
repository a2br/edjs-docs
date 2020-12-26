# The Account Class

`Account` est une classe que vous ne devriez jamais avoir à utiliser directement. Ce que vous utiliserez sera des variantes, comme `Student`, `Family`, `Teacher`, `Staff`... Ces variantes vont vous permettre d'utiliser des méthodes qui sont spécifiques à certains types de comptes. Ici, seules les propriétés propres à tous les types de comptes sont listées.

```javascript
import { Session } from "ecoledirecte.js"

const session = new Session("username", "password")
const account = await session.login() 
// Woosh! A wild variant of Account appeared!
// Now, we should check which type of class 
// has been generated, with account.type.
switch (account.type) {
    case 'student':
        console.log("It's a student!")
        break;
    case 'teacher':
        console.log("It's a teacher!")
        break;
    case 'staff':
        console.log("Oh, it's a staff member!")
        break;
    case 'family'
        console.log("No, it's a whole family!!")
    default:
        console.log("If you read that, ed.js is " + 
            "outdated... It means that the type isn't " +
            "recognized.")
}
```

## Properties

### `_raw`

* represents the account extracted from the raw login response from EcoleDirecte, without any change.

### `token`

* can be `set` and `get`
* will directly change the `token` prop of the parent `Session` 



