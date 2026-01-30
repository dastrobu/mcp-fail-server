# Migration from Zed Repository

This MCP server was extracted from the Zed repository to create a standalone, reusable testing tool.

## Original Location

- **Source**: `zed/crates/mcp_test_server/src/main.rs`
- **Purpose**: Testing tool use/result pairing in error scenarios

## Changes Made

1. **Repository Structure**
   - Created standalone Cargo project
   - Added comprehensive README
   - Added dual MIT/Apache-2.0 licensing
   - Added .gitignore and proper git setup

2. **Dependencies**
   - Updated to use rmcp 0.14 with proper features
   - Added serde_json dependency
   - Configured tokio with full features

3. **Code Updates**
   - Updated server name from "failing-mcp-server" to "mcp-fail-server"
   - Use `env!("CARGO_PKG_VERSION")` for version info
   - Enhanced documentation and comments
   - Streamlined for standalone use

4. **Documentation**
   - Added README with installation and usage instructions
   - Added example configurations for Zed and Claude Desktop
   - Created CHANGELOG
   - Added this migration notes file

## Testing

The server has been successfully built and verified:
- Compiles cleanly with `cargo build --release`
- Binary runs and displays startup info correctly
- Follows MCP protocol specification

## Usage in Zed

To use this in Zed, add to your settings:

```json
{
  "context_servers": {
    "mcp-fail-server": {
      "command": "mcp-fail-server"
    }
  }
}
```

## Differences from Original

- Standalone repository instead of Zed monorepo crate
- Proper versioning via Cargo.toml
- More comprehensive documentation
- Ready for distribution via `cargo install`
