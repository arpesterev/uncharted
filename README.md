# Uncharted

Uncharted is a React/TypeScript visualization library built around configurable views and resizable grid layouts. Its published entry point exports `View`, `ViewGrid`, visualization types and related TypeScript interfaces.

This is a component package, not a generic Create React App starter.

## Main pieces

- [`src/index.ts`](src/index.ts): public exports.
- [View component](src/): view rendering and related implementations.
- [ViewGrid component](src/): grid layout.
- [`src/api/`](src/api/): API types and generated client code.
- [`openapi/`](openapi/): API description used for code generation.

The code uses React, TypeScript, `react-grid-layout`, `amCharts 5` and Axios. Some component files are under a directory whose first character is a Cyrillic `с` (`src/сomponents`); keep that exact path when navigating imports.

## Local development

With Node.js and npm installed:

```sh
npm ci
npm start
```

Additional scripts defined in `package.json`:

- `npm run build`: builds the React app.
- `npm run rollup`: creates the library bundle using Rollup.
- `npm run openapi`: regenerates API client code from `openapi/paths/used_api.yaml`.
- `npm test`: starts the configured test command.

Package publishing is configured for a separate npm registry. Do not assume the package is available from the public npm registry.

**Status:** commands and exports are taken from checked-in source and package metadata; execution and publication have not been verified here.
