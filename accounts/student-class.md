---
description: Extends Account
---

# The Student Class

```javascript
account.type === 'student'
```

## Properties

### `getHomework()`

* read the name
* takes as argument an array or only 1 of the following:
  * `Date`
  * `string` \(that represents a date\)
  * `number` \(that represents a date\)
* if no argument, it will automatically select all the dates with future homework
* some `contenuDeSeance` values are not displayed on the ED UI
* it will always return an array of assignments
* for each assignment, `_raw` gives the original document

```javascript
const homework = await student.getHomework(["2021-01-14", 
new Date("01/15/2021"), new Date("2021-01-15").getTime()];
```

### `getMessages()`

* again, read the name
* gets all sent and received messages
* the content of the message needs another request, but `getContent()` is here to help

```javascript
const messages = await student.getMessages()
const message = messages[0]
const content = await message.getContent()
console.log(content.text)
```



