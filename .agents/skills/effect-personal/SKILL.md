# Effect v4 Personal Practices

Use this skill when writing, reviewing, or refactoring Effect v4 code and the user asks to apply my personal Effect practices.

## Relationship To Existing Setup

Do not replace or bypass the repo's Effect instructions.
Before writing Effect code:

1. Follow the repository `AGENTS.md` Effect setup.
2. Run `effect-solutions list`.
3. Run `effect-solutions show <relevant-topic>`.
4. Search `~/.local/share/effect-solutions/effect` when docs are insufficient.
5. Then apply the personal practices in this skill.

## Personal Practices

- Build services instead of functions where possible
- Store services in /src/services
- Prefer make and type inference in services using this format:

```ts
import { Context, Effect, Layer } from "effect";

class Logger extends Context.Service<Logger>()("Logger", {
  make: Effect.gen(function* () {
    const config = yield* Config;
    return { log: (msg: string) => Effect.log(`[${config.prefix}] ${msg}`) };
  }),
}) {
  // Build the layer yourself from the make effect
  static readonly layer = Layer.effect(this, this.make).pipe(Layer.provide(Config.layer));
}
```
