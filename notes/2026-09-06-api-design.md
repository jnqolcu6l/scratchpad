# API Design Notes

- Prefer explicit `keyword` arguments over positional options in public methods.
- Keep response envelopes flat unless versioning requires nesting.
- `created_at`/`updated_at` should always be ISO 8601 with UTC.
- Error payloads: `{ "error": { "code": "...", "message": "..." } }`.
- Use `ApplicationRecord` for shared model concerns, not modules with too many hooks.
