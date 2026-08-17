# Stokhos

C++/Rust systems engineer interested in trading infrastructure, market
microstructure, performance engineering, and high-performance data structures.

- 👋 Hi, I’m @stokhos
- ✨ I think the lone wolf survives but the pack dies
- 👀 I’m interested in low level cool stuff
- 🌱 I’m currently learning Jax, Pytorch, GYM
- 💞️ I’m looking to collaborate on low level cool stuff
- 📫 How to reach me: [Open an issue here](https://github.com/stokhos/stokhos/issues)

## Featured project

### [C++ Order Matching Engine](https://github.com/stokhos/Projects/tree/main/match_engine)

A C++26 price-time-priority matching engine with direct cancellation,
defensive input handling, 90 automated tests, and documented design tradeoffs.

- [Implementation and usage](https://github.com/stokhos/Projects/blob/main/match_engine/README.md)
- [Design and performance analysis](https://github.com/stokhos/Projects/blob/main/match_engine/docs/design-and-performance.md)

## Open-source contributions

- [ndarray #978](https://github.com/rust-ndarray/ndarray/pull/978)
- [Alacritty #4923](https://github.com/alacritty/alacritty/pull/4923)
- [Sapling #50](https://github.com/kneasle/sapling/pull/50)

## Binary Search Tree Structure

An example bid/ask order-book structure using price-level trees:

```
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

## Current focus

- Benchmarking matching-engine throughput, latency, and cache behavior
- Exploring efficient order-book data structures
- Writing modern C++ and Rust
