# NPM

## Philosophy

A package manager for node.

## Commands

- `npm install npm@latest` to install latest npm. 
- ``npm init`` to create a new package.
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

## Manage Cache

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
