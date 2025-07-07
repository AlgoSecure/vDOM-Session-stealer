# vDOM-Session-stealer
Small javascript script to search all DOM for a value and return it.

## Usage:

Copy paste the "exploit" function in your browser developper tools console on a React or Vue.js (or other) where you did not find the session token in the cookies nor in the browser storage.
Then run it with the known session ID or with a Regex matching the app session ID format.

Direct value:
`let results = exploit(this, "304d8cb0-6e83-4677-858a-9e1b044ddfed")`

Regex (UUIDv4):
`let results = exploit(this, /[0-9a-fA-F]{8}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{12}/)`

Regex (JwT):
`let results = exploit(this, /e[yw][A-Za-z0-9-_]+\.(?:e[yw][A-Za-z0-9-_]+)?\.[A-Za-z0-9-_]{2,}(?:(?:\.[A-Za-z0-9-_]{2,}){2})?/)`
