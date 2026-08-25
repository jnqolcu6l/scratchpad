# API Design Scratchpad

Quick notes for designing resource-oriented APIs.

## Naming
- Use plural nouns for resources: `/users`, `/orders`
- Prefer concrete names over generic
- Keep nesting shallow: `/users/:id/orders` ok, avoid deep

## Actions
- Use HTTP methods for CRUD
- For custom actions, use subresource or `POST /resource/:id/action`
- Keep verbs out of URLs

## Responses
- Return consistent JSON envelope for errors
- Include a request id in error responses
- Use RFC 7807 problem details for errors

## Versioning
- Start with `/v1`
- Only break backwards compatibility in major versions

## Ruby notes
- Use dry-struct for response schemas
- Roda or Sinatra for small APIs
- Document with OpenAPI 3.1
