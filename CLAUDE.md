# Go + Chi Project

This is a Go API using the Chi router.

## Commands

- `go run .` - Start dev server on port 8080
- `go test ./...` - Run tests
- `go build -o server .` - Build binary
- `golangci-lint run` - Lint code

## Architecture

- **Handlers** in `internal/api/` handle HTTP requests
- **Models** in `internal/models/` are data structures
- **Services** in `internal/services/` contain business logic
- **Migrations** in `migrations/` are SQL files

## Conventions

- Use Chi middleware for cross-cutting concerns
- Keep handlers thin - delegate to services
- Use context for request-scoped values
- Return JSON responses with consistent structure
- Use structured logging (slog)

## Error Handling

- Return errors from functions, handle at top level
- Use custom error types for different categories
- Respond with appropriate HTTP status codes
- Log errors with context

## Database

- PostgreSQL via sqlx
- Use sqlx.DB for connection pooling
- Write raw SQL - avoid heavy ORMs
- Migrations managed with golang-migrate
