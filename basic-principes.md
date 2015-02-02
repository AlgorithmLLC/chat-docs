## How it works
![default](https://cloud.githubusercontent.com/assets/312855/6000541/c503928e-ab2a-11e4-8573-16f965af551e.png)

Picture description:
  1. Client app connects to socket.io server
  2. App requests frame `doThat` with `data` and `ack`
  3. Server processes request and puts/gets data to/from `REST/DB` server.
     When all work done, server calls `ack` with `error` and `result` 
  4. App processes result and does other things

## Client authentication
We support two authentication methods. First is for fresh launched app, when user not gave credentials.
Second is for reconnect because of network troubles or app relaunch.

Fresh authentication process (no token present):
  1. Connect to socket.io server
  2. [`auth by credentials`](/socket.io/auth/auth by credentials.md)
  3. If success, forget username/password and store token for future use

Warmed up authentication process (token is present):
  1. Reconnect to socket.io server
  2. [`auth by token`](/socket.io/auth/auth by token.md)
  3. If success, store token for future use

If any of two methods failed, app must request user to provide `username` and `password` credentials.

## Data gathering
On any method of authentication suceed, app should do following data gather (in any order):
  - get server config (TODO split to ack request, now just `storage urls` emited)
  - get self info — [`who am i`](/socket.io/auth/who am i.md)
  - get self public keys (TODO split out from `who am i`)

After that, you should do [Wizard](/wizard.md) checks. If they succeed, do following (in any order):
  - get public keys for contacts — [`give me keys`](/socket.io/key/give me keys.md)
  - get contacts — [`give me users`](/socket.io/user/give me users.md)
  - get groups — [`give me groups`](/socket.io/group/give me groups.md)
  - get dialogs — [`give me dialogs`](/socket.io/dialog/give me dialogs.md)

At this step app is full of user contacts and data and ready for use. 
