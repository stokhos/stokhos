# Stokhos

<p align="center">
  <code>explicit state</code> · <code>terminal-first tools</code> · <code>observable failure</code> · <code>measured tails</code>
</p>

## `./hello`

```text
explore      👀  low-level cool stuff
build        🛠️  focused systems understood end to end
diagnose     🔎  clear cause, clear cost
collaborate  💞️  on low-level cool stuff
believe      ✨  the lone wolf survives, but the pack dies
```

🧪 My other GitHub: [@DrunkenRandomWalker](https://github.com/DrunkenRandomWalker)  
📫 [Open an issue here](https://github.com/stokhos/stokhos/issues) 
## `./featured-work`

### `./adjacent-study`

Bid/ask binary-search tree rendered in plain text:

```text
            ------   /
           |21, 32| /
           |21, 21|<
           |  20  | \
            ------   \
  --------   /
 | 20, 20 | /
 |14.1, 21|<
 |  None  | \
  --------   \
                      ----------   /
                     | 19.3, 21 | /
                     |19.3, 19.3|<
                     |    19    | \
                      ----------   \
            ----------   /
           | 19, 121  | /
           |14.1, 19.3|<
           |    20    | \
            ----------   \
                      ----------   /
                     |14.1, 199 | /
                     |14.1, 14.1|<
                     |    19    | \
                      ----------   \
ASK: min 14.1  max 21
BID: max 13    min 10
            ------   /
           |13, 10| /
           |13, 13|<
           |  12  | \
            ------   \
  ------   /
 |12, 10| /
 |10, 13|<
 | None | \
  ------   \
            ------   /
           |10, 21| /
           |10, 10|<
           |  12  | \
            ------   \
```

This is a separate BST-backed visualization study. The featured engine uses price-indexed FIFO levels plus an occupancy bitset.

### `./in-the-lab`

#### [`order-matching-engine`](https://github.com/stokhos/Projects/tree/main/match_engine)

A deterministic, in-memory matching engine for studying order-book design, failure boundaries, and the operator surface around a hot path.

[Implementation and usage](https://github.com/stokhos/Projects/blob/main/match_engine/README.md) · [Design and trade-offs](https://github.com/stokhos/Projects/blob/main/match_engine/docs/design-and-performance.md)

## `./working-principles`

```text
question -> build -> measure -> explain
```

- Separate machine output from human diagnostics.
- Reconstruct every transition from stable inputs, IDs, and reason codes.
- Measure tails, saturation, drops, and instrumentation overhead.
- Keep terminal views keyboard-first, stable, and readable without color.

## `./modeling-workbench`

**JAX / PyTorch** for modeling. **Ray** for parallel execution. **Gym** for environment contracts. Deterministic runs. Comparable measurements.

## `./upstream`

All merged upstream:

- [`ndarray` #978](https://github.com/rust-ndarray/ndarray/pull/978) — API ergonomics around shape metadata
- [`Alacritty` #4923](https://github.com/alacritty/alacritty/pull/4923) — underline thickness for double-width terminal cells
- [`Sapling` #50](https://github.com/kneasle/sapling/pull/50) — integration testing for DAG behavior
