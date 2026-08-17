# Stokhos

<p align="center">
  <code>explicit state</code> · <code>terminal-first tools</code> · <code>observable failure</code> · <code>measured tails</code>
</p>

This is my public engineering workbench: small systems pushed far enough to expose their invariants, failure modes, operator surfaces, and measurement costs. I want failures to reveal what changed, why, how long it took, and what observing it cost.

## `./hello`

✨ I think the lone wolf survives but the pack dies  
👀 I’m interested in low level cool stuff  
💞️ I’m looking to collaborate on low level cool stuff
🧪 My other GitHub: [@DrunkenRandomWalker](https://github.com/DrunkenRandomWalker)  
📫 [Open an issue here](https://github.com/stokhos/stokhos/issues) · [LinkedIn](https://www.linkedin.com/in/peiyun-jin-3938362b9/)

## `./featured-work`

### `./adjacent-study`

Bid/ask BST:

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

### `./in-the-lab`

#### [`order-matching-engine`](https://github.com/stokhos/Projects/tree/main/match_engine)

`C++` · `single writer` · `price-time priority` · `direct cancellation`

A deterministic, in-memory matching engine for studying order-book design, failure boundaries, and the operator surface around a hot path.

[Implementation and usage](https://github.com/stokhos/Projects/blob/main/match_engine/README.md) · [Design and trade-offs](https://github.com/stokhos/Projects/blob/main/match_engine/docs/design-and-performance.md)

## `./working-principles`

```text
question -> model -> build -> instrument -> test -> benchmark -> explain
```

- Keep machine output stable and human diagnostics on a separate, pipeable channel.
- Make transitions reconstructible from stable inputs, identifiers, and reason codes.
- Measure distributions, saturation, drops, and instrumentation overhead—not only averages.
- Design terminal views for keyboard use, stable geometry, stale-state visibility, and color-independent meaning.

### Questions on the bench

- What is the smallest event schema that can reconstruct an order lifecycle?
- Which signals justify their hot-path cost, and which belong off-path?
- How should a terminal view expose backpressure, dropped events, and stale state?

## `./modeling-workbench`

I use **JAX** and **PyTorch** for comparable modeling loops, **Ray** for parallel trials and rollouts, and **Gym** for explicit environment contracts. The interesting questions are determinism, compilation boundaries, steady-state throughput, orchestration overhead, and whether implementations measure the same thing.

## `./upstream`

All merged upstream:

- [`ndarray` #978](https://github.com/rust-ndarray/ndarray/pull/978) — API ergonomics around shape metadata
- [`Alacritty` #4923](https://github.com/alacritty/alacritty/pull/4923) — underline thickness for double-width terminal cells
- [`Sapling` #50](https://github.com/kneasle/sapling/pull/50) — integration testing for DAG behavior
