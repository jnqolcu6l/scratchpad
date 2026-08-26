# API Design Checklist

Quick notes from today's whiteboard session.

- Use JSON:API or plain JSON? Pick one and document it.
- Version via URL path (`/v1/`) unless you have a strong reason not to.
- Keep error responses consistent:
  ```json
  { "error": { "code": "invalid_param", "message": "..." } }
  ```
- Paginate list endpoints with `page` and `per_page`, return `Link` header.
- Validate before touching the database.
- Deprecate with `Sunset` header, not just docs.

Todo:
- [ ] Write example responses for 400, 404, 422
- [ ] Decide on id format: UUID vs integer
