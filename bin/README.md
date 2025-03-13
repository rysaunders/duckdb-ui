# Pre-built DuckDB UI Extension

This directory contains pre-built versions of the DuckDB UI extension.

## Files

- `ui.duckdb_extension`: The DuckDB UI extension with HTTP proxy support

## Usage

To use the pre-built extension:

1. Download the `ui.duckdb_extension` file
2. Load it in DuckDB using:
   ```sql
   LOAD 'path/to/ui.duckdb_extension';
   ```
3. Start the UI:
   ```sql
   CALL start_ui();
   ```

## HTTP Proxy Support

This version includes support for HTTP proxies. To use a proxy:

```sql
-- Set proxy server
SET http_proxy='http://proxy.example.com:8080';

-- Optional: Set proxy authentication
SET http_proxy_username='username';
SET http_proxy_password='password';

-- Start the UI
CALL start_ui();
```

The UI extension will use the configured proxy for all outbound HTTP and HTTPS connections. 