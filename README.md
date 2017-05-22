# Node Js Library

This project serves as a template for any library compiled to be published in npm and consumed in a node js environment.

The repository includes:
- Transpiling and bundling of the core library's code written in Typescript.
- Transpiling and running of tests also written in Typescript.
- The definition of tasks written in Typescript.
- Linting of all contains sourcecode.
- The publishing of the library to the npm registry.
- Typescript definition files for the library's interface.

## Scripts

All tasks are defined in as npm scripts:

- Building the library: `npm run build:lib`
- Building the library in watch mode: `npm run build:lib:watch`
- Building the tests: `npm run build:test`
- Building the tests in watch mode: `npm run build:test:watch`
- Running the tests: `npm test`
- Running the tests in watch mode: `npm run test:watch`
- Running the code linter: `npm run lint`
- Running the code linter in watch mode: `npm run lint:watch`

## Creating a new library

Follow these instructions to create a new forked library repository:
1. Fork this repository on github.
2. Setup the repository locally.
3. Add a remote by entering `git remote add base git@github.com:Player1os/node-js-library.git`
or `git remote add base https://github.com/Player1os/node-js-library.git`.

## Updating the new library with changes from the base

Follow these instructions to update the new library:
1. Fetch the base repository's branches `git fetch base`.
2. Make sure you are in the library's master branch `git checkout master`.
3. Rebase the library's master branch to the base repository's master `git rebase upstream/master`.

## Developement

It is is recommended to run the following scripts in seperate windows during development:
1. `npm run build:lib:watch`
2. `npm run build:test:watch`
3. `npm run lint:watch`
4. `npm run test:watch`

## Publishing a new version

Follow these instructions, when a new version is ready to be published:
1. Commit and push the final changes to the topic branch of the git repository.
2. Run the `npm version` script choosing the `patch`, `minor` or `major` depending on the significance of the changes to be applied.
3. Run the `npm publish` script to publish the package to the npm registry.

## TODO

- Add NYC code coverage.
- Correctly setup the vscode launch configuration.