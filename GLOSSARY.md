# TypeCore Glossary

Core concepts of the TypeCore operating system.

---

## Objects

| Term | Definition |
|------|-----------|
| **Object** | The fundamental unit in TypeCore. Everything — files, processes, devices, permissions — is represented as an object with identity, type, state, and capabilities. |
| **Object ID** | 64-bit random identifier, unique per device, never reused. Unpredictable by design. |
| **Object Type** | A classification that defines methods and accepted messages. Many objects share a type — code exists once. |
| **Method** | An operation defined by an object's type, invoked via message passing. |
| **Composition** | A group of objects co-located for fast internal communication and shared lifecycle. If the composition is destroyed, all members are destroyed. |

## Security

| Term | Definition |
|------|-----------|
| **Capability** | An unforgeable token granting specific access to a specific object. Cannot be forged, escalated, or copied. |
| **Keyring** | An object that holds capabilities. The only way to access other objects. You either hold the key or you don't. |

## Communication

| Term | Definition |
|------|-----------|
| **Message Passing** | Sending a structured message from one object to another. The primary communication mechanism in TypeCore. |
| **IPC** | Interprocess Communication. In TypeCore, the kernel provides synchronous message passing. The capability is checked on every send. |

## Kernel

| Term | Definition |
|------|-----------|
| **Microkernel** | A kernel that keeps only essential services in kernel space, moving everything else to user space. |
| **Object Runtime** | User-space system service that manages types, method dispatch, and policy enforcement. |

## Hardware Platforms

| Term | Definition |
|------|-----------|
| **MCU** | Microcontroller. No MMU, flat memory. The "$5 chip." |
| **AP** | Application Processor. Full MMU, virtual memory, multiple cores. |

## Real-Time

| Term | Definition |
|------|-----------|
| **Hard Real-Time** | A scheduling guarantee where deadline miss = failure. In TypeCore, hard RT is a property of objects holding reservation capabilities — not a system mode. |
| **Soft Real-Time** | A scheduling preference where deadline miss = degraded quality but not failure. Audio, video, UI responsiveness. |