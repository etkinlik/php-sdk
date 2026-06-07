## 2.0.6

- Regenerated from OpenAPI 2.0.6.
- Event resource: added `start_r001` and `end_r001` (UTC instants, ISO8601) and `timezone` (IANA, always present).
- `end_r001` is nullable when the event has no scheduled end time.
- Legacy fields `start` and `end` are unchanged for existing integrations (local wall-clock with offset). `end` remains always present; when `end_r001` is null, `end` is local `start` plus 2 hours.
- New integrations should use `start_r001`, `end_r001`, and `timezone` for time handling.

## 2.0.5

- Initial release of the Etkinlik.io V2 API PHP client (Guzzle). Packagist: `etkinlik/php-sdk`. Regenerated from OpenAPI 2.0.5.
- Requires PHP ^8.1.
