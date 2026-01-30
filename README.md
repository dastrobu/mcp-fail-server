# MCP Fail Server

A simple Model Context Protocol (MCP) server that provides a single tool which always fails. Useful for testing error handling in MCP clients.

## Features

- Single tool `fail` that always returns an error
- Built with the official [MCP Rust SDK](https://github.com/modelcontextprotocol/rust-sdk)
- Communicates over stdio for easy integration
- Minimal dependencies

## Installation

```bash
cargo install --git https://github.com/dastrobu/mcp-fail-server
```

Or build from source:

```bash
git clone https://github.com/dastrobu/mcp-fail-server
cd mcp-fail-server
cargo build --release
```

## Usage

Run the server:

```bash
mcp-fail-server
```

The server communicates via stdio and follows the [Model Context Protocol](https://modelcontextprotocol.io/) specification.

### Available Tools

- **fail**: Always returns an error with the message "This tool always fails intentionally for testing purposes"

## License

Licensed under either of

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
- MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

