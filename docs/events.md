# Events

Each notification has 2 support events that you can register a callback too.

| Event | Description
| -------- | --------- |
| `on_start` | Called when the notification start animation is started. |
| `on_complete` | Called when the notification complete animation has finished. |

There are also a few parameters that may be of use which are passed to the callback for you to access.

| Parameter | Description
| -------- | --------- |
| Parameter 1 | This is the item popped from the queue that will contain all the options. |
| Parameter 2 | This is the notification object (template instance). |
| Parameter 3 | This is the tween instance used for this notification. |

```lua
Events.Broadcast("show_notification", "This is my notification.", {

	on_start = function(queue_item, notification, tween)
		print("Start")
	end,

	on_complete = function(queue_item, notification, tween)
		print("Complete")
	end

})
```