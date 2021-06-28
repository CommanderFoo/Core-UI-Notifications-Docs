# Easings

Below is a list of all the support easing types that you can use for notifications.  See the below link for a good visual on which easing would best suit your notification.

[Easings.net](https://easings.net/)

| Easing Type |
| ----------- |
| `linear` |
| `inQuad` |
| `outQuad` |
| `inOutQuad` |
| `outInQuad` |
| `inCubic` |
| `outCubic` |
| `inOutCubic` |
| `outInCubic` |
| `inQuart` |
| `outQuart` |
| `inOutQuart` |
| `outInQuart` |
| `inQuint` |
| `outQuint` |
| `inOutQuint` |
| `outInQuint` |
| `inSine` |
| `outSine` |
| `inOutSine` |
| `outInSine` |
| `inExpo` |
| `outExpo` |
| `inOutExpo` |
| `outInExpo` |
| `inCirc` |
| `outCirc` |
| `inOutCirc` |
| `outInCirc` |
| `inElastic` |
| `outElastic` |
| `inOutElastic` |
| `outInElastic` |
| `inBack` |
| `outBack` |
| `inOutBack` |
| `outInBack` |
| `inBounce` |
| `outBounce` |
| `inOutBounce` |
| `outInBounce` |

```lua
Events.Broadcast("show_notification", "This a notification.", {

	ease_in = "inBounce",
	ease_out = "outBounce"

})
```