# TORchIM-public
TORchIM — Anonymous Tor P2P Messenger using Tor Onion Services. End-to-end encrypted decentralized peer-to-peer messenger with BIP39 identity.

It uses Tor Onion Services for direct communication without central servers, provides end-to-end encryption, and derives identities from BIP39 mnemonic phrases.

Features

- Tor Onion Services
- P2P architecture
- End-to-End Encryption
- Anonymous identities
- No central server
- BIP39 recovery phrase
- Cross-platform

  
Status: Phase 1 — active development
License: AGPL v3 (core) · Commercial (services)
Language: Java 21
Platform: Desktop (Windows / Linux / macOS) · Headless node

🔦 TORchIM: Light in the Darkness of Control
"A free internet is an open ocean, not a network of supervised swimming pools."

The modern world is building digital walls. ISPs decide what you see, and corporations decide who you talk to. TORchIM brings back the pristine freedom of the early web. Here, communication depends only on two people, not on the ISP's permission.

Privacy is not a crime. It's a right.

🌊 Why TORchIM?
No Boundaries: Boundaries are a thing of the past. Uncensored communication.

True P2P: Communication that belongs only to two people. Not a corporation, but you.

Invisible: Become "invisible" to global monitoring systems.

🛠 Technical Core
TORchIM is a decentralized, anonymous, peer-to-peer messenger built on Tor hidden services. All communication is routed exclusively through the Tor network — no central servers, no accounts, no phone numbers.

🔐 Identity & Security
Seed-based Identity: BIP-39 seed phrase (24 words) generating a deterministic Ed25519 keypair.

Local Protection: PIN unlock with PBKDF2-HMAC-SHA256 (100,000 rounds) + AES-256-GCM session encryption.

Zero Storage: Your seed phrase is never stored on disk.

Self-Destruct: 5 wrong PIN attempts trigger an automatic session wipe.

🌐 Network Layer
Tor v3 Hidden Services: Your IP address is never exposed.

DPI Resistance: Native obfs4 bridge support to bypass traffic inspection and censorship.

Pure P2P: Direct contact-to-contact communication without middlemen.

📦 Features & UI
History: Persistent encrypted message history & contacts (SQLite).

UX: Message reply/quote, forward, copy, and delete.

Insights: Real-time Tor circuit info (Guard / Middle / Exit nodes).

Personalization: 12 UI themes (PC).

🚀 Getting Started
Current Version: v0.1.2 - Pre-Alpha Release
Target Platform: Desktop (Windows 10/11, Linux, macOS, Android) & Headless nodes.

[!IMPORTANT]
Security model. All traffic between two devices is end-to-end encrypted and authenticated by Tor's v3 onion-service protocol: each device runs its own hidden service, and the .onion address is the device's public key. No relay, rendezvous node, or server can read message content in transit — there is no server at all. This is the same transport-security model as Ricochet-Refresh.

Not yet implemented: an additional application-layer encryption ratchet (Signal-style Double Ratchet) on top of Tor, which would add forward secrecy and post-compromise security independent of the Tor layer. This is planned for Phase 2. Until then, in-transit confidentiality relies solely on Tor's onion encryption, and messages are stored locally without an extra at-rest layer beyond device storage.

This build is for testing purposes only — do not use for highly sensitive communications.

🛣Roadmap
[x] Phase 1: Core Tor P2P engine, Seed identity, UI implementation.

[ ] Phase 2: Integration of Double Ratchet (E2EE), File transfers.

[ ] Phase 3: Mobile clients (Android/iOS), Multi-device sync.

🛡 License
Core: AGPL v3

Services: Commercial

TORCHIM: Private. Encrypted. Essential. Bringing back the freedom of the early Web.




⚠️ Security Notice: Transport layer is protected by Tor encryption. Text messages now use experimental P2P session encryption based on X25519 + HKDF-SHA256 + ChaCha20-Poly1305 when a session handshake is established.

This is not yet Signal Protocol / Double Ratchet, has not been audited, and some metadata or fallback paths may remain unencrypted.

Offline message delivery is not implemented yet, so both clients should be online at the same time for reliable message delivery.

This build is for testing only — do not use for highly sensitive communications yet.

Releases, documentation, and feature information are currently being published, and the source code status will be determined later.
