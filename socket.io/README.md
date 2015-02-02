This directory describes all socket.io frames. They're splitted to modules (not all of them are on right place, but they're arranged so in our backend).
File name is frame name.

TIP: you can press `t` on github and search for frame name.

Almost all of frames use acks to get server response.

`ack` — callback function with signature `function(error, data)`. It follows javascript callbacks style.

Here is how you must read ack results: `error` value `null` means request completed successfully. Otherway `error` describes what's wrong.
