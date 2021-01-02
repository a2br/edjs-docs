---
description: Browse EcoleDirecte's private API with the module of your dreams.
---

# edjs-docs

{% hint style="warning" %}
These docs may be incomplete.
{% endhint %}

`ecoledirecte.js` is a neat node module that lets you interact with the EcoleDirecte private API in a snap. Its goal is not only to make API calls easier but also to take the mess of the ED API and simplify it before giving it to you. The raw data is still always available.

It is built with TypeScript, and all the EcoleDirecte API responses are hard-typed, so everything you do is covered by your IntelliSense and the power of TypeScript.

Each feature takes time to be implemented in the module. But we prefer to offer a minimum of awesomeness when it comes to serving data, we don't want to just give you the API responses.

```javascript
import { Session } from "ecoledirecte.js"

async function main() {
    const session = new Session("EDELEVE", "0")
    const account = await session.login()
    if (account.type !== "student") return;
    
    const someHomework = await account.getHomework("2021-01-14")
    console.log("Hi,", someHomework[0].prof)
};

main()
```

