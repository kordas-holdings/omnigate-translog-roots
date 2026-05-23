# omnigate-translog-roots

Daily-published Merkle roots of the OmniGate transparency log. Each entry is a JSON file `YYYY-MM-DD.json` with:

```json
{
  "date": "YYYY-MM-DD",
  "kid": "translog-2026-qN",
  "last_seq": 1234,
  "root_hash": "deadbeef...",
  "ts": "2026-05-24T00:00:00Z",
  "signature_hex": "..."
}
```

The `signature_hex` is `sk_translog` Ed25519 signature over the raw `root_hash` bytes.

External observers can detect log tampering by comparing local witnesses to this public timeline (Certificate Transparency monitor pattern).
