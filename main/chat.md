# chat
The chat object. Controls the sending and receiving of messages.
### blur()
De-focuses the chat and places it in the background.
### clear()
Removes every message in chat.
### hide()
Removes chatlog from view.
### receive(msg)
Sends a custom message to the client only. Used for the mentioning feature. `msg` is an object, with its values explained below.
 - **a** : Message
 - **p** : Optional parameters
	 - **name** : Name of the fake user
	 - **color** : Hex value of the text color
- **m** : Message type. If `"dm"`, the message acts as a direct message and makes use of `msg.sender` and `msg.recipient`.

**Example**
```js
MPP.chat.receive({
	a: 'Hello, world!',
	p: {
		name: 'User',
		id: 'a4d979b59687e390796eb0ce',
		_id: 'a4d979b59687e390796eb0ce',
		color: '#0D1117'
	}
})
```
### scrollToBottom()
Scrolls the chatlog to the most recent messages, if user has scrolled up.
### send(message)
Sends a message.
### show()
Makes chatlog visible again, if not already.