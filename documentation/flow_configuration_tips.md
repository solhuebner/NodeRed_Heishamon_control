## Tips and tricks

### 1 - Create a [WP Personal] tab
If you make personal changes inside the downloaded flow, you risk loosing them during an update.<br>
_Example: on [WP Input] tab insert your source node for sensors_<br>
<br>
Better do this:
- Create a new tab (aka flow)
- Call it [WP Personal]
- Put your source sensors in THAT tab
- Add a `link out` node there
- Direct the link out node to the correct link in node on [WP Input]

***
