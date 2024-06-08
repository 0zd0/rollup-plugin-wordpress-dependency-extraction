# rollup-plugin-wordpress-dependency-extraction

## Installation

Install the plugin

```bash
bun install rollup-plugin-wordpress-dependency-extraction --save-dev
```

## Vite

```ts
export default defineConfig(({ mode }) => {
    return {
        plugins: [
            react(),
            wpDependencyExtraction(),
        ],
        build: {
            manifest: true,
            rollupOptions: {
                output: {
                    format: 'iife',
                },
            },
        },
        esbuild: {
            minifyIdentifiers: false,
        },
    }
})
```