<!-- Start SDK Example Usage [usage] -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.chapters.listChapters({
    country: "India",
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->