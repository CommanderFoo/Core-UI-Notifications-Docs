# How to Use

Using the system is really simple.  Once you have the `UI Notifications` template dropped into your hierarchy, all you need to do is broadcast to it to create your notifications.

Something to note that is important is the system comes with a queue built in for each screen position.  So for example if you call the API multiple times one after the other for the same screen position, then the system will queue up the notifications and display them in order they were received.

Here is an example of creating 2 notifications that make use of the queuing system.  By default this will be `INFO` notifications and display `TOP LEFT`.

```lua
Events.Broadcast("show_notification", "Notification 1.")
Events.Broadcast("show_notification", "Notification 2.")
```

Creating notifications is that simple.  Broadcast to the event `show_notification` and as the second parameter send your message.  The third parameter is a table with a list of options you can override if needed.

```lua
Events.Broadcast("show_notification", "This is my notification.", {

	type = "WARNING",
	position = "TOP MIDDLE",
	offset = Vector2.New(50, 100),
	ease_in = "outElastic",
	ease_out = "inElastic",
	in_duration = 1,
	out_duration = 1,
	stay_duration = 2,
	on_start = function(queue_item, notification, tween)
		print("Start")
	end,
	on_complete = function()
		print("Complete")
	end

})
```