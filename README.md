# 🌌 Viz-Atlas: The Decentralized Cosmic Atlas 🚀

> An advanced, production-ready interactive 3D Cosmic Atlas built on top of live scientific APIs (NASA, SIMBAD TAP) and integrated with local blockchain networks (Polygon Mainnet) to store verified astronomical discoveries.

**Live Application**: [vizatlas.space](https://vizatlas.space)  
**Main Target**: Democratize access to scientific space data, representing stellar structures in highly-performant GLSL viewport and recording immutable space ownership markers in Web3 ledger boards.

---

## ⚡ High-Level Architecture Overview
┌──────────────────────────────┐
                    │   ASTRONOMICAL DATA INGESTION│
                    │   (NASA Exoplanets / SIMBAD) │
                    └──────────────┬───────────────┘
                                   │ Real-time API
                                   ▼
                 ┌───────────────────┐
                 │ Express JS Server │
                 └─────────┬─────────┘
                           │ JSON Stream
                           ▼
    ┌─────────────────────────────────────────────────────────────┐
    │                  VIZ-ATLAS FRONTEND ENGINE                  │
    │                                                             │
    │   ┌─────────────────────┐       ┌───────────────────────┐   │
    │   │  3D Render Sphere   │       │ Custom GLSL Shaders   │   │
    │   │  (Three.js / Fiber) │       │ Solar Atmosphere Maps │   │
    │   └─────────────────────┘       └───────────────────────┘   │
    └──────────────┬──────────────────────────────┬───────────────┘
                   │                              │
                   ▼ Secure Signatures            ▼ On-chain Registry
     ┌───────────────────────────┐   ┌────────────────────────────┐
     │ Firestore State & DB Cache│   │ Polygon (ERC-721 Contract) │
     └───────────────────────────┘   └────────────────────────────┘
     ---

## 🛠️ Complete Technical Stack

| Layer | Technologies & Ecosystem | Key Features |
|---|---|---|
| **Client Core** | React 18, Vite, TypeScript, TailwindCSS, Motion/React | Optimized, modern layout with high rendering efficiency. |
| **3D Rendering** | Three.js, `@react-three/fiber`, `@react-three/drei` | Multi-body system simulation with realistic orbits on React tree. |
| **Shaders (GPU)**| GLSL custom shaders, noise generators | Real-time procedural rendering of stellar atmospheres, solar flares, and surface heat. |
| **Database Core**| Firebase Firestore & Firebase Auth | Secure object registry, persistent player profiles, and synchronization logs. |
| **API Ingestion** | NASA planetary catalogs, SIMBAD Astronomical TAP | Complex Astronomical Data Query (ADQL) integrations with custom coordinate calculations. |
| **Web3 Layer** | Ethers.js, MetaMask Wallet Connector, IPFS (Pinata) | Decentralized minting of registered cosmic objects on-chain. |

---

## 🪐 Mathematical Formulation: Orbits and Distances

To represent astronomical structures accurately in localized 3D viewports, we utilize custom normalization constants for distances, celestial masses, and orbits.

### Stellar Coordinate Transforms (from Right Ascension / Declination):
$$\alpha = \text{Right Ascension}, \quad \delta = \text{Declination}, \quad d = \text{Distance in Parsecs}$$
$$x = d \cos(\delta) \cos(\alpha)$$
$$y = d \cos(\delta) \sin(\alpha)$$
$$z = d \sin(\delta)$$

The Three.js camera uses log-depth buffer systems to guarantee smooth scaling transitions—from local star planetary orbits up to deep galactic scales.

---

## ⛓️ Smart Contract Specification

The decentralized registry is anchored using an immutable **Solidity Scrypt Registry Smart Contract**:
- **Standard**: Secure extension of Polygon Standard Register.
- **Auditable Functions**: Permanent tracking of object IDs corresponding to Simbad catalog designations, prevents double claim coordinates.

*To view the official solidity contract, check `/contracts/VizAtlasRegistry.sol` inside this repository.*

---

## 👥 Contributors & Leadership
* **Dmytro Pavliuk** (Lead Visionary & System Software Architect)
* **Liubomyr Pavliuk** (Co-Founder & Lead Astronomy Data Researcher)

---
© 2026 Viz-Atlas. Created in Ukraine 🇺🇦. Protected under MIT License.
