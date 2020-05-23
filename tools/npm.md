# NPM

## Philosophy

A package manager for node.

## Commands

- `npm install npm@latest` to install latest npm. 
- ``npm init`` to create a new package.
- `npm init --scope=@company` to create a new package with scope.
- ``npm install express`` to add a package.
- ``npm install babel-cli --save-dev`` to add package for development. Won't be included in the production package.
- ``npm install express -g` to add a new package globally.
- `npm install eslint@5.2.0` to install a package with specific version.
- `npm uninstall package` to remove a package.

## Version

- `^` - all minor and patches OK.
- `~` - all patches only.

## Package lock

- Pins the library version so that the install is determinstic.

## Admin Commands

- `npm outdated -g` to check for outdated packages.
- `npm update eslint` to update the package.

# Auditing

High or critical warnings should be fixed immediately.
Watch for semver - this will break the package.

- `npm audit` - to generate a security report.
- `npm audit fix` - to fix all issues.

For those packages that aren't able to be fixed:

- Look if patch is available and `npm i` that package if it exists.

## Manage Cache

npm states in their manual that sometimes their cache gets confused.

- Cache is located in ~/.npm/_cacache
- `npm cache verify` - verifies cache via a report.
- `npm cache clean --force` - forces cache clean.

## Global Packages

- `/usr/local/lib/node_modules` OR `/usr/local/lib/node`

## Scripts

- For custom script commands, use `npm run <script command>`
- See [this overview](https://docs.npmjs.com/misc/scripts)

## npx

Temporary install packages.

- `npx -p @angular/cli ng new myapp`

## Scoped Packages

- Unique, descriptive, and meets npm policies. (example: @angular/cli)

## NPM Publishing / Dist-tag

- Human-readable description added to a published package.
    - `npm publish --tag bugfix` `npm dist-tag add test-npm@1.0.0 [stable]`
- Scoped packages are private by default and require a paid account to publish.
    - `npm public --access public`
- Tokens are used for CI to publish and update packages in npm.

## Resources

1. [NPM Enterprise Settings](https://docs.npmjs.com/configuring-your-registry-settings-as-an-npm-enterprise-user)
1. [Node Version Manager](https://github.com/nvm-sh/nvm)
1. [npm common errors](https://docs.npmjs.com/common-errors)
