<!-- Start SDK Example Usage [usage] -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKeyAuth: process.env["NEST_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await nest.chapters.listChapters({
    country: "India",
    region: "Asia",
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->