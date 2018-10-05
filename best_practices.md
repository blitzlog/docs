# Best Practices

- Use tags. Tags are a powerful feature that make logs more searchable, usable and performant.
```
log.I("account: %s added member: %s", accountID, memberID)

// with tags
log.With(log.Tags{
	"account_id": accountID,
	"member_id":  memberID,
).I("added member")
```

- Use global tags to improve tracability of your logs. All logs from this instance are tagged by these global tags.
```
log.Global(log.Tags{"env": "development", "service": "api"})
```

WIP
