---
icon: circle-exclamation
---

# Error management

### Effect.catchTag

```typescript
import { Effect } from "effect"
import { program } from "./error-tracking"
 
const recovered = program.pipe(
  Effect.catchTag("HttpError", (_HttpError) =>
    Effect.succeed("Recovering from HttpError")
  )
)
```
