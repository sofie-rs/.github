<img src="logo.png" alt="" width="96" height="96">

# Sofie

A Rust web framework built around a fixed app structure. Every file has a known
place and role, so the framework reads the whole app at build time and derives
the wiring, endpoints, screens, permissions, telemetry, documentation and checks
from it. An app writes only its own logic.

- Secure by default: CSRF, sessions, egress allowlists and masked telemetry are
  on without configuration.
- The database is the only infrastructure an app needs: Postgres (or SQLite)
  holds its events, jobs, schedules and caches; Redis and Meilisearch are
  optional.
- Checked at build time: `sofie check` holds every app to the structure, so a
  finding fails `cargo build`.

> **Status: proof of concept.** APIs change without notice. Do not build on it
> for production yet.

## Get started

```sh
cargo install --git https://github.com/sofie-rs/sofie sofie-cli
sofie new app shop
```

The [documentation](https://sofie-rs.github.io/sofie.rs/) has the full steps
and the reference; the [repository](https://github.com/sofie-rs/sofie) has the
examples and the design documents.

Licensed under MIT or Apache-2.0, at your option.
