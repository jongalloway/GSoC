*Example project idea format - include once per project idea** 
## Succinct data structure implementations to replace glib dependencies
**Complexity:** Medium

Bitmask-driven data structures allow for SIMD operations on the data structure’s top-level structure schema. They’re space-efficient, cache-efficient, and they’re easy to debug after a crash because the bitmask and the data structure have a minimal number of pointers.

Offering succinct arrays (no nulls) and other data structures as drop-in replacements might be ways to significantly reduce memory footprint for some specific use cases.

Benchmarking is necessary to find those use-cases.

Deliverables:
 * Implement full replacement for GArray and ensure passes GLib GArray tests.
 * Benchmark high-allocation places and see if the succinct replacement helps
 * (Optional) Implement replacement for ghashtable which supports bare minimum of operations, using CTries
 * (Optional) Use CTries in high-contention environments or high-allocation environments and benchmark uses that have savings

**Mentors**: Alexander Kyte
