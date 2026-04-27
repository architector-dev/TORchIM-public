# TORchIM-public
TORchIM v0.1.2 — Pre-Alpha Release (only Windows 10\11)
TORchIM is a decentralized, anonymous, peer-to-peer messenger built on Tor hidden services. All communication is routed exclusively through the Tor network — no central servers, no accounts, no phone numbers.
Identity & Security

BIP-39 seed phrase identity (24 words) — deterministic Ed25519 keypair
PIN unlock with PBKDF2-HMAC-SHA256 (100,000 rounds) + AES-256-GCM session encryption
Seed phrase never stored on disk
5 wrong PIN attempts → session wipe

Network

Tor v3 hidden services — IP address never exposed
obfs4 bridge support — traffic obfuscation, resistant to DPI detection
Fully decentralized P2P — direct contact-to-contact communication

Features

Persistent encrypted contacts and message history (SQLite)
Message reply/quote, forward, copy, delete
Full message history dialog with search
Unread message indicators
Tor circuit info (Guard / Middle / Exit nodes)
Three UI themes




⚠️ Security Notice: Transport layer is protected by Tor encryption. However, message content is currently transmitted in plaintext at the P2P protocol level. End-to-end encryption (Double Ratchet / Signal Protocol) is planned for Phase 2. This build is intended for testing purposes only — do not use for sensitive communications.

