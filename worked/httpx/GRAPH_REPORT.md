# Graph Report - raw  (2026-08-08)

## Corpus Check
- cluster-only mode — file stats not available

## Summary
- 193 nodes · 456 edges · 6 communities
- Extraction: 76% EXTRACTED · 24% INFERRED · 0% AMBIGUOUS · INFERRED: 110 edges (avg confidence: 0.5)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Request
- Response
- exceptions.py
- client.py
- BaseTransport
- utils.py

## God Nodes (most connected - your core abstractions)
1. `Response` - 55 edges
2. `Request` - 43 edges
3. `Client` - 27 edges
4. `AsyncClient` - 26 edges
5. `BaseTransport` - 20 edges
6. `HTTPTransport` - 20 edges
7. `BaseClient` - 19 edges
8. `Cookies` - 19 edges
9. `AsyncHTTPTransport` - 18 edges
10. `TransportError` - 16 edges

## Surprising Connections (you probably didn't know these)
- `Auth` --uses--> `Response`  [INFERRED]
  auth.py → models.py
- `AsyncClient` --uses--> `Auth`  [INFERRED]
  client.py → auth.py
- `BaseClient` --uses--> `Auth`  [INFERRED]
  client.py → auth.py
- `Client` --uses--> `Auth`  [INFERRED]
  client.py → auth.py
- `Limits` --uses--> `Auth`  [INFERRED]
  client.py → auth.py

## Import Cycles
- None detected.

## Communities (6 total, 0 thin omitted)

### Community 0 - "Request"
Cohesion: 0.09
Nodes (17): Auth, BasicAuth, BearerAuth, DigestAuth, NetRCAuth, Authentication handlers. Auth objects are callables that modify a request…, Load credentials from ~/.netrc based on the request host., Base class for all authentication handlers. (+9 more)

### Community 1 - "Response"
Cohesion: 0.11
Nodes (4): AsyncClient, Client, Synchronous HTTP client., Response

### Community 2 - "exceptions.py"
Cohesion: 0.07
Nodes (31): Exception, CloseError, ConnectTimeout, CookieConflict, DecodingError, HTTPError, HTTPStatusError, PoolTimeout (+23 more)

### Community 3 - "client.py"
Cohesion: 0.10
Nodes (11): BaseClient, Limits, The main Client and AsyncClient classes. BaseClient holds all shared logic.…, Shared implementation for Client and AsyncClient. Handles auth, redirects,…, Timeout, InvalidURL, URL is improperly formed or cannot be parsed., Cookies (+3 more)

### Community 4 - "BaseTransport"
Cohesion: 0.12
Nodes (19): ConnectError, NetworkError, An error occurred at the transport layer., A network error occurred., Failed to establish a connection., TimeoutException, TransportError, AsyncBaseTransport (+11 more)

### Community 5 - "utils.py"
Cohesion: 0.12
Nodes (17): build_url_with_params(), flatten_queryparams(), is_known_encoding(), normalize_header_key(), obfuscate_sensitive_headers(), parse_content_type(), primitive_value_to_str(), Utility functions shared across the library. Small helpers that don't belong in… (+9 more)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Response` connect `Response` to `Request`, `exceptions.py`, `client.py`, `BaseTransport`?**
  _High betweenness centrality (0.247) - this node is a cross-community bridge._
- **Why does `Request` connect `Request` to `Response`, `exceptions.py`, `client.py`, `BaseTransport`?**
  _High betweenness centrality (0.177) - this node is a cross-community bridge._
- **Why does `Cookies` connect `client.py` to `Response`, `exceptions.py`, `utils.py`?**
  _High betweenness centrality (0.092) - this node is a cross-community bridge._
- **Are the 18 inferred relationships involving `Response` (e.g. with `Auth` and `BasicAuth`) actually correct?**
  _`Response` has 18 INFERRED edges - model-reasoned connections that need verification._
- **Are the 18 inferred relationships involving `Request` (e.g. with `Auth` and `BasicAuth`) actually correct?**
  _`Request` has 18 INFERRED edges - model-reasoned connections that need verification._
- **Are the 12 inferred relationships involving `Client` (e.g. with `Auth` and `BasicAuth`) actually correct?**
  _`Client` has 12 INFERRED edges - model-reasoned connections that need verification._
- **Are the 12 inferred relationships involving `AsyncClient` (e.g. with `Auth` and `BasicAuth`) actually correct?**
  _`AsyncClient` has 12 INFERRED edges - model-reasoned connections that need verification._