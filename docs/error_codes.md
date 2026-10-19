# Error Codes

This document lists the stable error codes returned by the mux-account contract.

| Code | Variant | Description |
|------|---------|-------------|
| 1 | `Unauthorized` | The caller is not authorized to perform the requested action. |
| 2 | `SessionExpired` | The session key has expired and can no longer be used. |
| 3 | `SessionNotFound` | No session key record exists for the supplied key. |
| 4 | `InvalidPayload` | The payload could not be decoded or is malformed. |
| 5 | `ScopeNotAllowed` | The payload's target contract/method is not authorized by the session key's `scopes`. `execute_with_session` fails closed with this variant when the target is not explicitly listed in the session key's scopes (including when `scopes` is empty). |
