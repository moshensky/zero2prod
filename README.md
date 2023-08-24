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
```

## DB migrations

```sh
cargo install sqlx-cli --no-default-features --features rustls,postgres
```
