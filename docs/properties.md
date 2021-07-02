# Properties

While you can create a notification without adjusting any properties, you may soon come to realise that you may wish to modify the height, width etc of the notification you want to show to the player.

Below are all the properties you can set when making a call to the API.

| Property Name | Description |
| ------------- | ----------- |
| `type` | The type of notification.  Possible types are `INFO`, `WARNING`, `SUCCESS`, `ERROR`, `GENERAL`. |
| `position` | There are 9 screen positions you can use.  `TOP LEFT`, `TOP MIDDLE`, `TOP RIGHT`, `MIDDLE LEFT`, `MIDDLE MIDDLE`, `MIDDLE RIGHT`, `BOTTOM LEFT`, `BOTTOM MIDDLE`, `BOTTOM RIGHT`. |
| `rotation` | The rotation of the notification. |
| `width` | The width of the notification. |
| `height` | The height of the notification. |
| `offset` | A Vector2 that use used to set the notification offset. |
| `add_width` | A useful property if you need to add an aditional width to the notification. |
| `add_height` | A useful property if you need to add an aditional height to the notification. |
| `template` | A custom template to use instead of the default ones that come with the system.  See the template section for info. |
| `ease_in` | The easing method to use for when the notification is eased in. See easing section. |
| `ease_out` | The easing method to use for when the notification is eased out. See easing section. |
| `delay_duration` | The duration to delay this notification from showing. |
| `stay_duration` | THe duration of how long this notification will stay out for. |
| `in_duration` | The duration of the in animation. |
| `out_duration` | The duration of the out animation. |
| `sound` | The sound to be played when this notification is displayed. |
| `on_complete` | The function to call when the notification is completed (i.e removed). |
| `on_start` | The function to call when the notification is created. |
| `dynamic` | If true, and using a `GENERAL` type of notification, the system will attempt to dynamically set the height. |
| `text_color` | Changed the color of the text. |
| `background_color` | Change the color of the background, this should be used on the `GENERAL` type, or custom templates, otherwise icons will look out of place. |

Below is an example of using some of these properties.

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