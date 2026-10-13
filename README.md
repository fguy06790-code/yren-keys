# Yren key list

`keys.json` is the list of keys the Yren macro accepts. Yren reads it from
https://raw.githubusercontent.com/fguy06790-code/yren-keys/main/keys.json when it starts, when a key is typed in,
and every 10 minutes while it runs.

Each entry holds:

- `id`: a SHA-256 fingerprint of the key text (not the key)
- `name`: the name typed when the key was made
- `tier`: `free`, `premium` or `owner`
- `made`, `expires`: unix seconds (`expires` is 0 for a key that never ends)
- `pc`: optional, the one PC the key works on (blank for any PC)

The keys themselves are never stored here. They are kept on the PC that made them. Removing an entry stops its key
working in Yren, even while Yren is open.
