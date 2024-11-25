# Eventos

Na pasta apps

```bash
npx create-next-app@latest frontend
```

Para usar o code runner
criar uma pasta .vscode e o aruqivo settings.json

```bash
{
    "code-runner.executorMap": {
        "typescript": "npx tsx",
    }
}
```

Configuração do next.config para não dar problema com as imagens vindas da url externa:

```bash
import type { NextConfig } from "next";

const nextConfig: NextConfig = {
  images: {
    remotePatterns: [
      {
        protocol: "https",
        hostname: "**",
      },
    ],
  },
};

export default nextConfig;

```
