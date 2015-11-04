# Webhooks

Webhooks allow you to build or set up integrations which subscribe to certain events on GitBook.com. When one of those events is triggered, we’ll send a HTTP POST payload to the webhook’s configured URL. 

### Events

When configuring a webhook, you can choose which events you would like to receive payloads for. You can even opt-in to all current and future events. Only subscribing to the specific events you plan on handling is useful for limiting the number of HTTP requests to your server. You can change the list of subscribed events through the UI anytime.

By default, webhooks are only subscribed to all events. The available events are:

| Name | Description |
| ---- | ----------- |
| `all` | Any time any event is triggered (Wildcard Event). |
| `publish` | Content of the book has been updated. |