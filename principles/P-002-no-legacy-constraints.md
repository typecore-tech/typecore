# P-002: No Legacy Constraints

| Field      | Value    |
|------------|----------|
| **ID**     | P-002    |
| **Status** | accepted |

## Statement

> TypeCore assumes no backward compatibility with existing software, formats, or paradigms. It is a clean-slate design.

## Rationale

The "we've always done it this way" argument is the weakest reason to constrain a new system. Users care about what apps do, not what kernel they run on. The 50 years of Unix tooling is not a constraint; it's someone else's history.

## Implications

- No POSIX compatibility layer required
- No file descriptor emulation
- Design choices are evaluated on merit, not familiarity
- Application-layer compatibility is a solvable problem (translation layers), not a design constraint