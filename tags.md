## Tags

Tags structure logs making them more searchable, usable and performant. Blitzlog provides multiple ways to add tags to your logs.

### Log tags

Add tags to specific logs using `log.With()` method.

### Global tags

Attach global tags using `log.Global()` method. All logs from this instance will have these tags. This is a handy way to assigning service specific tags.

### API key tags

You may associate tags with the API key. Any logs that are send using this API key will have these tags. This is a handy way of assigning environment specific tags.
