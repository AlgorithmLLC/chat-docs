When client app authenticated and got user object using `who am i` request, you should check if user must proceed with startup wizard.

Possible wizard steps:
### Rename yourself
If user's `first_name` or `second_name` are empty.
See [Profile/rename yourself].

### Change password
If user's `is_planned_password_change` is `true`.
See [Profile/change password].

### Create/import key
If users's `PublicKeys` array has no key with `is_default === true`.
Or if there is such key, but client app has no private key for that public key.
See [Keys manager].

### Change avatar (optional)
If users's `avatar` is null.
See [Profile/change avatar].
