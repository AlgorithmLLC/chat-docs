Almost all of socket.io frames use acks to get server response.

`ack` — callback function with signature `function(error, data)`. It follows node.js/io.js callbacks style.

Here is how you must read ack results: `error` value `null` means request completed successfully. Otherway `error` describes what's wrong.
