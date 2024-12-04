## Requirements
- Rust
- Docker
- docker-compose
- docker postgres image

## Usage
```bash
# Copy example .env file
cp .env.example .env

# Run postgres
docker-compose up -d postgres

# Install diesel
cargo install diesel_cli --no-default-features --features postgres

# Run db migrations
DATABASE_URL=postgres://actix:actix@localhost:5432/actix diesel migration run

# Run unit tests
cargo test

# Run integration tests
cargo test --features "integration"

# Run the server (Add --release for an optimized build)
cargo run 
```
```bash
curl -s http://localhost:8080/
```
