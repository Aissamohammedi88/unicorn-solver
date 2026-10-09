# Changelog

All notable changes to Unicorn Solver.

## [1.0.0] - 2026

### Added
- Five independent solutions to the Facebook Graph Search problem:
  - solve_inverse_index — O(R × fanin)
  - solve_bitmap — compressed RLE bitmaps
  - solve_hll — HyperLogLog cardinality approximation
  - solve_lattice — bucket-based ordering
  - solve_hybrid — HLL pre-filter + bitmap verify + lattice sort
- Synthetic graph generator (`generer_graphe`) with scale parameter
- Full benchmark harness with side-by-side comparison
- Theoretical explainer (`expliquer`) printed on run
- Zero external dependencies (pure stdlib)
- Python 3.8+ compatibility
- a-Shell iOS compatibility

### Benchmark results (iPhone 14, a-Shell)
- inverse_index: 234 ms
- bitmap_rle: 87 ms
- hyperloglog: 41 ms
- lattice: 19 ms
- hybrid: 63 ms
- All five solutions return identical result counts
