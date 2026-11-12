# base-unit-trait-interceptor

The `Interceptor` unit trait: a unit type with it can attack aircraft.

A unit type with this trait may attack air units: in Civ1, a stack of air units only; in Civ2, bombers outside a city too.

For example: Civ1: Fighter. Civ2: flag 4 (Fighter, Stealth Fighter).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(Interceptor)`:

```ts
import Interceptor from '@civ-clone/base-unit-trait-interceptor/Interceptor';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, Interceptor));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
