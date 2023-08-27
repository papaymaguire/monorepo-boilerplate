# monorepo-boilerplate
A preconfigured monorepo setup for full stack web app development.

# Tools
## Version Management
.gitignore has been configured for recommended Node standards.
## Package Manager and Workspace Provider
npm has been configured as the package manager and workspace provider. To add an additional package use ```npm init -y --scope {scope} -w {path to workspace}```
@TODO: Add scripts to make using npm workspaces easier in root package.json
@TODO: Add scripts to do boilerplate code
## Type Checking
Typescript is used for type checking. Every additional package needs a tsconfig.json. The recommended format is:
```javascript
{
  "extends": ["@papaymaguire/typescript-config/tsconfig.json", "most relevant tsconfig.json from https://github.com/tsconfig/bases"],
  "compilerOptions": {
    "outDir": "./dist",
    "rootDir": ".",
  },
  "include": [
    "**/*.ts"
  ]
}
```
## Code Linting
@TODO: ESLINT CONFIG NEEDS WORK
A shared ESLint Config is packaged. Every additional package needs a .eslintrc.json. The recommended format is:
```javascript
{
  "extends": ["other configs", "...", "@papaymaguire/eslint-config"] //must be last so all conflicting prettier settings are turned off
}

```
## Code Formatting
Prettier is included using its default configuration. 
## Editor
A recommended set of extensions for VSCode includes the following:
1. https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint
2. https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode
3. https://marketplace.visualstudio.com/items?itemName=rvest.vs-code-prettier-eslint
4. https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens
The settings for VSCode have already been configured for these four to work well, a restart may be needed after installation.
## Test Tools
Cypress is used for e2e testing and Jest is used for component testing.
## CI/CD Integration and Pipeline
Turborepo + CircleCI
