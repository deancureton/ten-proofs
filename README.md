# ten-proofs, faster

A fork of OpenAI's [ten-proofs](https://github.com/openai/ten-proofs), with faster builds. Final theorem statements are unchanged.

Full build is 40% faster: `17:29` down to `10:27`, measured after `lake exe cache get`.

## Build times

Below per-module times were measured with `lake build <module>` with a warm mathlib cache.

| # | Module | Before | After | Δ |
|---|--------|-------:|------:|--:|
| 1 | `SpherePacking` | 5:43 | 4:22 | −24% |
| 2 | `MetricCodes` | 11:26 | 5:49 | −49% |
| 3 | `NonSoficGroup` | 4:09 | 3:22 | −19% |
| 4 | `ConnesRigidity` | 10:44 | 8:05 | −25% |
| 5 | `Permanent` | 5:15 | 3:59 | −24% |
| 6 | `QuantumParallelRepetition` | 13:54 | 6:56 | −50% |
| 7 | `GapCVP` | 9:21 | 6:26 | −31% |
| 8 | `EhrhartVolumeInequality` | 5:04 | 4:01 | −21% |
| 9 | `MulticolorTriangleRamsey` | 0:39 | 0:23 | −41% |
| 10 | `CompactnessAndDegeneracy` | 3:29 | 2:17 | −34% |
| | **Full build (wall)** | **17:29** | **10:27** | **−40%** |

## Building

Same as upstream:

```sh
lake exe cache get
lake build All
```
