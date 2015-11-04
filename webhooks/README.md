# Webhooks

Webhooks allow you to build or set up integrations which subscribe to certain events on GitBook.com. When one of those events is triggered, we’ll send a HTTP POST payload to the webhook’s configured URL. 

### Events

| Name | Description |
| ---- | ----------- |
| `all` | Any time any event is triggered (Wildcard Event). |
| `publish` | Content of the book has been updated. |