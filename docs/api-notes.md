# API Design Scratch Notes

- Prefer explicit `status` fields over HTTP codes for domain errors.
- Use `problem+json` for error responses.
- Never break existing clients; add new versions instead.
- Document rate limits in headers: `X-RateLimit-Limit`, `X-RateLimit-Remaining`.
- Validate input early, fail fast, log context.

_Updated 2026-08-13_