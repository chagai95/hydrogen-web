# Minimal thing to get working

 - DONE: finish summary store
 - DONE: move "sdk" bits over to "matrix" directory
 - DONE: add eventemitter
 - DONE: make sync work
 - DONE: store summaries
 - DONE: setup editorconfig
 - DONE: setup linting (also in editor)
 - DONE: store timeline
 - DONE: store state
 - DONE: make summary work better (name and joined/inviteCount doesn't seem to work well)
 - DONE: timeline doesn't seem to recover it's key well upon loading, the query in load seems to never yield an event in the persister
 - map DOMException to something better
 	- it's pretty opaque now when something idb related fails. DOMException has these fields:
 		code: 0
		message: "Key already exists in the object store."
		name: "ConstraintError"
 - DONE: emit events so we can start showing something on the screen maybe?
 - DONE: move session._rooms over to Map, so we can iterate over it, ...
 - DONE: build a very basic interface with
 	- DONE: a start/stop sync button
 	- DONE: a room list sorted alphabetically
 - do some preprocessing on sync response which can then be used by persister, summary, timeline
 - support timeline
 	- clicking on a room list, you see messages (userId -> body)
 - send messages
 - fill gaps with call to /messages
 - create sync filter
 - lazy loading members
 - decide denormalized data in summary vs reading from multiple stores PER room on load
 - allow Room/Summary class to be subclassed and store additional data?
 - store account data, support read markers