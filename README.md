SCRIPTS
=======

In each case a tempory keyring that is deleted at the end of the invocation of the script is used, the current keyring is never affected.

## edit

Imports a full backup (secret keys included), drops to edit shell, exports modified keys to tmp files and prints paths to stdout, private followed by public

## edit no export

As above but no export. Useful for keytocard operations.
