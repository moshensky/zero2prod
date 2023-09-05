# README

```sh
cargo watch -x check

# Command chaining
cargo watch -x check -x test -x run | bunyan

# Measure test coverage
cargo tarpaulin --ignore-tests

# Lint
cargo clippy -- -D warnings

# Code format
cargo fmt

# For ci
cargo fmt -- --check

# Scan for security vulnerabilities
cargo audit

# Expands macros
 cargo expand

# Find unused dependencies
cargo +nightly udeps

# Enable logging during tests with pretty print
TEST_LOG=true cargo test health_check_works | bunyan

# Build
docker build --tag zero2prod --file Dockerfile .

# Prepare sqlx offline for building
cargo sqlx prepare -- --lib
```

## DB migrations

```sh
cargo install sqlx-cli --no-default-features --features rustls,postgres
```

## Prod build

```sh
docker build --tag zero2prod --file Dockerfile .
docker run -p 8000:8000 zero2prod

curl -v http://127.0.0.1:8000/health_check
```