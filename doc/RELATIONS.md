Relations and redactions

events that refer to another event will need support in the SyncWriter, Timeline and SendQueue I think.
SyncWriter will need to resolve the related remote id to a [fragmentId, eventIndex] and persist that on the event that relates to some other. Same for SendQueue? If unknown remote id, not much to do. However, once the remote id comes in, how do we handle it correctly? We might need a index on m.relates_to/event_id?

The timeline can take incoming events from both the SendQueue and SyncWriter, and see if their related to fragmentId/eventIndex is in view, and then update it?

alternatively, SyncWriter/SendQueue could have a section with updatedEntries apart from newEntries?