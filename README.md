# Cors Middleware for ntex framework

## Documentation & community resources

* [API Documentation](https://docs.rs/ntex-cors/)
* Cargo package: [ntex-cors](https://crates.io/crates/ntex-cors)
* Minimum supported Rust version: 1.42 or later

## A loose config example

```rust
.wrap(
    Cors::new()
        .allowed_methods(vec![
            "GET", "HEAD", "POST", "OPTIONS", "PUT", "PATCH", "DELETE",
        ])
        .send_wildcard()
        .finish(),
)
```

Will produce CORS headers for every request:

```http
vary: Origin
access-control-allow-origin: *
```
