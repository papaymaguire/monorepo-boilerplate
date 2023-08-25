# monorepo-config
A preconfigured monorepo setup for full stack web app development.

# Tools
## Version Management
.gitignore has been configured for recommended Node standards.
## Package Manager and Workspace Provider
yarn has been configured as the package manager and workspace provider. Every additional package added needs its own package.json. To do this, create a new directory and use yarn init
## Type Checking
Typescript is used for type checking. Every additional package needs a tsconfig.json. The recommended format is:
```javascript
{
  "extends": [<path to root tsconfig.json>, <most relevant tsconfig.json from https://github.com/tsconfig/bases>],
  "compilerOptions": {
    "outDir": "dist",
    "rootDir": ".",
  },
  "include": [
    "**/*.ts"
  ]
}
```
## Code Linting
## Code Formatting
## Editor
## Build Tool
## Test Tool
## CI/CD Integration and Pipeline
