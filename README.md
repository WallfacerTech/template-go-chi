# Go + Chi Template

Lightweight Go API with Chi router.

## Stack

- **Go 1.22+**
- **Chi** router
- **sqlx** for database access
- **PostgreSQL** database
- **Go standard testing**

## Getting Started

```bash
# Install dependencies
go mod download

# Copy environment file
cp .env.example .env

# Start development server
go run .

# Open http://localhost:8080
```

## Development

```bash
# Run tests
go test ./...

# Run with race detection
go test -race ./...

# Build binary
go build -o server .

# Run linting (install golangci-lint first)
golangci-lint run
```

## Project Structure

```
├── cmd/
│   └── migrate/        # Migration tool
├── internal/
│   ├── api/            # HTTP handlers
│   ├── models/         # Data models
│   └── services/       # Business logic
├── migrations/         # SQL migrations
├── main.go             # Application entry point
└── go.mod              # Go module file
```

## Building for Production

```bash
# Build optimized binary
go build -ldflags="-s -w" -o server .

# Run the binary
./server
```
