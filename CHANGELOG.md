## 2.0.11

- Regenerated from OpenAPI 2.0.11.
- Event resource: added `modified_at` (UTC ISO8601). `GET /events` supports `sort_by=updated`.

## 2.0.10

- Regenerated from OpenAPI 2.0.10.
- OpenAPI schemas: `required` arrays added for response models (Event, Venue, pagination, errors, etc.). Nullable optional fields marked explicitly. Wire format unchanged.

## 2.0.9

- Regenerated from OpenAPI 2.0.9.
- Event resource: `start`, `end`, and `venue` marked **deprecated** in the API contract. Fields remain in JSON responses for backward compatibility.
- New integrations: use `start_r001`, `end_r001`, `timezone`, and `venue_type` / `venue_data` instead.

## 2.0.8

- Regenerated from OpenAPI 2.0.8. API surface unchanged from 2.0.7.
- New release tag; same immutable-version policy as 2.0.6 → 2.0.7.

## 2.0.7

- Regenerated from OpenAPI 2.0.7. API surface unchanged from 2.0.6; use v2.0.7 on Packagist (v2.0.6 could not be re-tagged after publish).
- See 2.0.6 release notes below for event time field changes.

## 2.0.6

- Regenerated from OpenAPI 2.0.6.
- Event resource: added `start_r001` and `end_r001` (UTC instants, ISO8601) and `timezone` (IANA, always present).
- `end_r001` is nullable when the event has no scheduled end time.
- Legacy fields `start` and `end` are unchanged for existing integrations (local wall-clock with offset). `end` remains always present; when `end_r001` is null, `end` is local `start` plus 2 hours.
- New integrations should use `start_r001`, `end_r001`, and `timezone` for time handling.

## 2.0.5

- Initial release of the Etkinlik.io V2 API PHP client (Guzzle). Packagist: `etkinlik/php-sdk`. Regenerated from OpenAPI 2.0.5.
- Requires PHP ^8.1.
