SCRIPTS
=======

In each case a tempory keyring that is deleted at the end of the invocation of the script is used, the current keyring is never affected.

## expire

Expects an openpgp backup that looks like the following

$folder
├── public.asc
├── secret.asc
└── secret-subs.asc

Only `secret.asc` needs to exist. Passing `$folder` as the only argument to `expire` will import the key to a temporary keyring and prompt for keys to adjust and the adjustment to be applied. The adjustment is in the same format as expected when using the expire command from `--edit-key` i.e. 0 to remove an expiry date and 1y to move the expiration date to be one year from today. It them prompts if the adjustments should be written back to folder. If so the secret keys, secret subkeys and public key will be written back to the folder.

## edit

Imports a full backup (secret keys included), drops to edit shell, exports modified keys to tmp files and prints paths to stdout, private followed by public. Needs work.

## edit no export

As above but no export. Useful for keytocard operations. Needs work.
