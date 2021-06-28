# Types

There are 5 types of notifications this system supports.

| Type | Description |
| ------------- | ----------- |
| `INFO` | A notification to display some information to the player. |
| `SUCCESS` | A notification to show that something was successful for the player. |
| `WARNING` | A notification to show a warning to the player (i.e "Inventory is nearly full."). |
| `ERROR` | A notification to show an error to the player. |
| `GENERAL` | This is a special type of notification that can be used for just general things. |

```lua
Events.Broadcast("show_notification", "An error has occurred.", {

	type = "ERROR"

})
```