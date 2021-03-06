# Simple Server
A glitch integrated webserver with continuous integration.

## Node
First install Node, https://nodejs.org/en/ which should come with npm that should be used to install with `npm i`

## Bot Hosting
This template is largely designed with free hosting over at [Glitch](https://glitch.com) in mind.
After making an account, make a new project, which one doesn't matter.

This next step is very important so be careful.

1. Open Dev tools with Right-click > Inspect and then go to the Network Tab
1. Click on the project name in the upper right and then 'Advanced Options'
1. Select Import from github, get access, and type in the username/repo as indicated
1. In Network there should be an entry after downloading the repo to glitch that says `githubImport?authori...`
1. Click on it and scroll to the Bottom where it says 'Query String Parameters' and copy them down
1. Create a private repo called 'api-keys' similar with a file with the name "glitch-config.json" and run `npm init` there
1. Next put the values into the file in the same format as the demo file in api-keys folder here, then commit and push
1. Add that new repo under the optional dependencies in package.json (replacing mine) for this project and reinstall with node

If everything worked you should be able to update to glitch automatically with `npm run update` (which also will git push for you).

## Api Security
This package also proposes a easy and fast way to keep track of API keys even if this is a public repo.

Added them the a private repo, in the same format as the template /api-keys folder and add the private repo under optionalDependencies in the package.json file.

This way there is no hassle while developing and they are still safe.

You can also add other people working on the project as a 'collaborator' in Github settings to allow them the update the bot.

## Uptime
The bot will likely go idle if webhooks are not used because glitch shutdowns bots after 5min of inactivity. Part of the bot script pings itself to prevent it from getting shut-down.

It is also recommended to have https://uptimerobot.com/ ping the site every 5min too.

Keep in mind the url for local is http://[name].gltich.me/, and the same for uptimerobot although you can use https.


## Running Server

Simply run the command `npm start`.  
