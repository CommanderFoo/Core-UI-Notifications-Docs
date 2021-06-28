# Screen Positions

The system supports 9 screen positions, and along with setting offsets, you can get notifications to display exactly where you want with ease.

Below are all the screen positions that you can use to set the notification.

| Position |
| -------- |
| `TOP LEFT` |
| `TOP MIDDLE` |
| `TOP RIGHT` |
| `MIDDLE LEFT` |
| `MIDDLE MIDDLE` |
| `MIDDLE RIGHT` |
| `BOTTOM LEFT` |
| `BOTTOM MIDDLE` |
| `BOTTOM RIGHT` |

!!! info
	`MIDDLE MIDDLE` will fade in and out, while all other notifications will be tweened based on position.

```lua
Events.Broadcast("show_notification", "This is my notification.", {

	position = "TOP RIGHT"

})
```