# Elite JavaScript

**Zero-dependency browser experiments. WebAssembly edge. Service Worker mastery.**

JavaScript that treats the browser as a systems platform. No bundlers, no frameworks, just vanilla JS + Web APIs pushing WebAssembly, SharedArrayBuffer, and OffscreenCanvas to their limits.

## Featured

| Experiment | Bundle Size | Key Technique |
|------------|-------------|---------------|
| **No-Alloc Parser** | 2.1KB | `TextDecoder` → AST, zero GC pressure |
| **Lock-Free Queue** | 1.8KB | `SharedArrayBuffer` + Atomics |
| **WASM SIMD** | 3.4KB | WebAssembly SIMD + `postMessage` zero-copy |
| **Terminal Renderer** | 4.2KB | `OffscreenCanvas` + 60fps block graphics |

## Characteristics

- **No bundlers:** Single `index.html` files, `<script>` tags only
- **No frameworks:** Vanilla JS + Web APIs exclusively
- **Bundle ≤ 5KB:** Gzip targets for instant loading
- **Service Workers:** Offline-first, cache-first architecture
- **Complete demos:** Open `index.html` → works immediately

## Philosophy

JavaScript's strength is **WebAssembly integration**. These experiments show how to:

Build WASM allocators without Emscripten  
60fps terminals via OffscreenCanvas  
Lock-free data structures with Atomics  
Zero-copy pipelines via ReadableStream

## Usage

```bash
git clone https://github.com/pithycyborg/elite-javascript
cd experiment-name
open index.html  # or double-click
```

## Benchmarks

| Experiment | Input Size | JS (Vanilla) | Rust (WASM) | Python |
|------------|------------|--------------|-------------|--------|
| JSON Parser | 1MB | 4.2ms | 2.1ms | 187ms |
| Queue (1M ops) | - | 28μs | 14μs | 2.7ms |

**Newsletter** for JS deep-dives + weekly prompts: [PithyCyborg.com](https://PithyCyborg.com)

**X:** [@mrcomputersci](https://x.com/mrcomputersci) | [@pithycyborg](https://x.com/pithycyborg)

MIT License
