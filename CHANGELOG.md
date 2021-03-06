# Unreleased

- One more description for StaleChat error.

# 0.8.0

- Fixed `#reply_with`, now it sets `reply_to_message_id` as it's supposed to.
  Added `#respond_with` which works the same way, but doesn't set `reply_to_message_id`.
  Please, replace all occurrences of `reply_with` to `respond_with` to
  keep it working the old way.
- Fixes for Rails 5:
  - Controller callbacks
  - Middleware
  - Setup travis builds

# 0.7.4

- Rails 5 support by @dreyks (#4).

# 0.7.3

-  Fixed issues with poller in production (#3)

# 0.7.2

- Bot API 2.1
- Fixed possible crashes when payload type is not supported.
  Provides empty session when neither `from` nor `chat` is defined.

# 0.7.0

- New Bot API methods.
- Helpers for inline keyboards, support for callback_query (with contextual actions).
- Changed action methods signature
  - `#inline_query(payload) -> #inline_query(query, offset)`
  - `#chosen_inline_result(payload)` -> `#chosen_inline_result(result_id, query)`
- MessageContext doesn't use second #process call to run contextual action.
- Botan.io metrics.

# 0.6.0

- StaleChat error.
- Encode arrays as json in request body.

# 0.5.0

- MessageContext.
- Running controller action without update.
- Client.wrap supports symbols.
- Improved testing utils: ability to process multiple updates on same controller instance,
  stubbing all clients in application.
