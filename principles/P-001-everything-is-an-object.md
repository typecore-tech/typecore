# P-001: Everything Is an Object

| Field | Value |
|-------|-------|
| **ID** | P-001 |
| **Status** | accepted |

## Statement

> Every system resource — processes, memory, files, devices, permissions — is an object with identity, type, and defined interfaces.

## Rationale

The core premise of TypeCore. Objects provide uniform abstraction: everything is managed the same way, secured the same way, and communicated with the same way. This eliminates special cases and makes the system predictable.

## Implications

- The kernel provides an object table as the foundational data structure
- Security is object-level, not file-level
- Interoperability is about object interfaces, not byte streams