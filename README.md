# eslint-prettier-husky-boilerplate
This is a boilerplate that leverages Prettier, ESLint, and Husky for use with NodeJS and React projects.

## Background:
Cleaner, more uniform code is easier to read and maintain, and facilitates a standard across development teams of all sizes. Using these tools, it's possible to stop poorly formated and unlinted code from entering source control.

## Requirements:
- It is presumed that you're already familiar with ESLint and Prettier and their application to NodeJS/React
- It is presumed that you are savvy enough to Google instructions on how to configure ESLint and Prettier using their config files in this project

## How this boilerplate is intended to work:
1. When you try to commit code, Husky will first check that your staged .js files are properly formatted using Prettier
2. Husky will then check if your code is properly linted with ESLint using the options set in .eslintrc.js
3. If either of these steps fail, Husky will stop you from committing the 'bad' code

## Default behavior/trying it out:
- This boilerplate recursively formats and lints all **staged** .js files
- If cloning this project, remove the .git directory and run `git init`
- `npm install` or `yarn`, depending on which package manager you use, to install all dependencies
- `npm run sample1` and `npm run sample2` are sample scenarios in which someone tries to commit unformatted/unlinted code

## How to run the pre-commit hook:
- If cloning this project, remove the .git directory and run `git init`
- `npm install` or `yarn`, depending on which package manager you use, to install all dependencies
- Do a `git add` and `git commit` as you normally would
- `git commit` automatically triggers lint-staged

## How to fix your code if Husky stops you from committing:
- `npm run lint` looks at **all** files for ESLint-related violations, and shows these violations in the command line
- `npm run lint-fix` looks at **all** unignored .js files for ESLint-related violations, shows them in the command line, and fixes the issues that it can
- `npm run format` looks at **all** unignored .js files and formats them 
- `npm run format-test` looks at *all** unignored .js files and tests if they are properly formatted
- All of these behaviors can be easily modified in the package.json file 

## Changes you will probably make:
- The script section in package.json. You may want to, for example, lint/format the src folder
- .prettierrc to modify how Prettier will format your project
- .eslintrc.js to add, implement, and configure extensions and rules for ESLint
- Use the .prettierignore and .eslintignore files to ignore specific files and/or directories

### Additional resources:
- https://prettier.io/docs/en/options.html the rules for Prettier
- https://eslint.org/docs/2.0.0/rules/ list of available ESLint rules
- https://github.com/typicode/husky/blob/master/DOCS.md more information on Husky