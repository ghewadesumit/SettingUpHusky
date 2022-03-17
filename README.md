# SettingUpHusky
Readme on how to set up Husky

This is for you React application is up and running

## Setting up Husky in project
1) Install Husky is Dev environment

` npm install husky --save-dev`

2) Enable the Husky's Git Hooks

`npx Husky install`

3) In order to get Husky ready for everyone else on team prepare a script

`// package.json
{
  "scripts": {
    "prepare": "husky install"
  }
}`

if you don't want to type the above code simply run the following command

`npm set-script prepare "husky install"`

## Create a Git Hook in Husky

To add a command to a hook or create a new one, use `npx husky add <file> [cmd]` (don't forget to run husky install before).

Example: `npx husky add .husky/pre-commit "npm test"`

Note: 1) the above command is used if you want to run test before a commit is made.
2) You can add more actions using the above command that you want to execute before making a commit.

## How to Bypass the Husky

If you want to bypass the Husky check (which is not a good idea) then you much use `--no-verify` after your commit message.

Example: `git commit -m "some meaningful message" --no-verfiy`

This should skip the Husky pre-commit checks.

## How to Make Husky check only the staged files (lint-staging)




