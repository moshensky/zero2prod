# README


```sh
cargo watch -x check

# Command chaining
cargo watch -x check -x test -x run

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
```