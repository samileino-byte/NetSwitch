NEW MODULES (88 new tests):

1. Protocol Extensions (15 tests) --proto-ext-only
- DNS resolution: A/AAAA via getaddrinfo(), CNAME/MX/NS/TXT/SRV/SOA/PTR
- HTTP/2: binary framing per RFC 7540, HPACK compression, server push, flow control, priority
- QUIC: RFC 9000 handshake, 0-RTT early data, connection migration over UDP, multiplexed streams, NewReno congestion control

2. Traffic Analyzer (15 tests) --traffic-only
- Rule engine: priority-sorted, first-match-wins evaluation chain
- Filter actions: ALLOW, DENY, LOG, REDIRECT, RATE_LIMIT
- Pattern matching on payloads, IP prefix, port ranges
- Token bucket rate limiting
- Protocol identification (TCP/UDP/ICMP)
- Thread-safe concurrent evaluation

3. Load Balancer (15 tests) --lb-only
- 6 algorithms: Round Robin, Least Connections, Weighted, Random, IP Hash (FNV-1a), Least Response Time
- Health checking with failure threshold
- Automatic failover to healthy backends
- Sticky sessions, drain mode
- Dynamic backend add/remove

4. Config Profiles (10 tests) --config-only
- Save/load configuration profiles
- Key=value serialization with section headers
- 3 templates: network, security, tunnel
- Version tracking, profile diffing

5. Multi-Hop Tunnel Chaining (15 tests) --chain-only
- IKEv2 -> SSH -> SOCKS5 -> endpoint chaining
- Sequential hop establishment through previous hop
- Latency accumulation, encryption verification
- Reverse-order teardown, failover detection
- Max 10 hops depth

6. Auth Extensions (18 tests) --auth-ext-only
- SAML SSO: AuthnRequest building, assertion validation, time-based checks, bindings
- mTLS: DER cert parsing, expiry/hostname/chain/revocation verification
- API tokens: HMAC signing, lifecycle, rate limiting, scope validation
- REST endpoint registry with auth requirements

All tests passing:
- Desktop: 395/395
- Phone: 392/392
- Tablet: 395/395
- Total: 1182 tests across all form factors

New files: 6 headers + 6 source files (12 new files total)
Version bumped to 1.5.0
