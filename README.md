AeroNyx
The encrypted coordination layer for autonomous agents.
AeroNyx is an open protocol for private routing, encrypted memory, and
agent-native coordination. It is designed around a simple invariant:
Infrastructure can coordinate work, but it must not read user content or own
user context.

This repository describes the AeroNyx protocol direction: a blind privacy
fabric where humans, applications, and autonomous agents can route encrypted
payloads, preserve private context, and request services without exposing the
middle of the flow.
Why AeroNyx Exists
AI agents are becoming participants in everyday work: they read context, call
tools, coordinate tasks, and act across services. That creates a new
infrastructure question:
Who sees the private data, memory, and routing context that agents depend on?

AeroNyx is building the version where the answer is: nobody in the middle.
The protocol treats privacy as a coordination primitive, not as a UI toggle or
a closed subscription feature.
Protocol Goals
Private routing
Move encrypted traffic through protocol nodes without revealing payloads,
destinations, or user-level activity to infrastructure.

Encrypted memory
Preserve durable personal and agent context as encrypted, versioned records
that can be synced without storage nodes reading the memory they hold.

Blind coordination
Allow nodes and services to route, meter, recover, and report aggregate health
while remaining blind to content.

Agent-native services
Provide a coordination surface that autonomous agents can use directly:
routing, encrypted messaging, private memory handoff, and scoped service
requests.

Public verifiability
Expose protocol health and relay evidence as aggregate, privacy-safe signals
rather than user-level telemetry.

Core Invariant
Every AeroNyx layer should only see the minimum information required to do its
job.
Client / user device
  - local plaintext before encryption
  - private keys and user intent
  - memory and context before sealing

Protocol nodes
  - ciphertext
  - TTL and signed routing metadata
  - aggregate relay and health evidence

Public status
  - aggregate protocol health
  - readiness and relay evidence
  - no user payloads, domains, destinations, or social graph
Protocol Components
Blind Privacy Fabric
AeroNyx nodes exchange signed peer summaries, route encrypted payloads, and
report aggregate health. Nodes move data without reading user content.
The fabric is designed for:
encrypted payload routing
blind relay boundaries
signed node identity
peer discovery and lifecycle recovery
privacy-safe aggregate observability
future multi-hop private routing
Privacy Network
The AeroNyx Privacy Network is a more private, open protocol layer for global
use. It is intended to move encrypted coordination traffic for humans, apps, and
agents without turning public network health into user surveillance.
MemChain
MemChain is the encrypted memory layer for humans and agents.
It preserves durable context as encrypted, versioned records. Storage and relay
nodes can help synchronize state, but they should not be able to read the memory
they hold.
MemChain is designed for:
node-blind encrypted memory
local-first recall
signed memory records
portable agent context
encrypted conversation and coordination history
Encrypted Coordination Services
Humans, applications, and agents use the same private service surface to:
route encrypted traffic
exchange encrypted messages
preserve private context
request work through blind services
coordinate without exposing payloads to infrastructure
What AeroNyx Is Not
AeroNyx is not a traditional centralized VPN service, a single messenger, or a
closed AI memory silo.
It is a protocol effort for private coordination:
not "trust the provider"
not user-level telemetry as public proof
not plaintext memory inside infrastructure
not agent context locked inside one vendor
Security And Privacy Boundary
AeroNyx protocol infrastructure should not see:
message plaintext
private memory plaintext
wallet secrets or seed phrases
social graph contents
destination domains or URLs
full user-level traffic history
raw per-user operational telemetry
Network and product observability should remain aggregate, privacy-safe, and
bounded to protocol health.
Roadmap Direction
2026: The Fabric Hardens
blind relay foundation moves from proof to product
verified peer views
restart recovery
aggregate public health as the observable surface
multi-hop private routing path
2028: Memory Becomes Portable
encrypted personal context follows the user between AI tools
identity-derived keys become the memory root
agent frameworks can read and write user-owned state through scoped access
sync works without nodes seeing raw content
2030: Agent-Native Coordination
agents route traffic and exchange encrypted payloads through blind services
private memory and relay services compose at the protocol layer
humans set intent; agents coordinate within it
Public Links
Website: aeronyx.network
Documentation: docs.aeronyx.network
Repository: github.com/AeroNyxNetwork/AeroNyx
Status
AeroNyx is under active development. Protocol surfaces, terminology, and
compatibility boundaries may change across early releases.
License
License information should be finalized before broad external contribution
intake or production protocol distribution.
