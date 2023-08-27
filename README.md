# monorepo-config
A preconfigured monorepo setup for full stack web app development.

# Tools
## Version Management
.gitignore has been configured for recommended Node standards.
## Package Manager and Workspace Provider
npm has been configured as the package manager and workspace provider. To add an additional package use ```npm init -y --scope {scope} -w {path to workspace}```
@TODO: Add scripts to make using npm workspaces easier.
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
## Test Tools
Cypress is used for e2e testing and Jest is used for component testing.
## CI/CD Integration and Pipeline
Turborepo + CircleCI
