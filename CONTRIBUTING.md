# Contributing to BotMyst
BotMyst is built using <a href="www.microsoft.com/net/core">.NET Core</a> with the <a href="https://github.com/RogueException/Discord.Net">Discord.NET</a> wrapper for the Discord API.

The current recommened version of .NET Core for this project is 2.0.

Please submit pull request from the development branch.

## Configuration file
For the bot to be able to connect to your app and work, it needs to have a BotMystConfig.json file in the same directory as the BotMyst.cs file.

How the BotMystConfig.json should look:
```json
{
  "token": "<your-token-here>"
}
```

**WARNING** Please don't publish the BotMystConfig file anywhere as it contains sensitive information that can compromise your bot. This file is already in the .gitignore, but make sure it is also in yours. We're not responsible for any damage done to you or your bot.

## Issues
In the <a href="https://github.com/LeonLaci/BotMyst/issues">Issues</a> section you can submit a bug, a new feature you want implemented or request documentation improvements / additions.

### Issue labels
* ![#f03c15](https://placehold.it/15/B91315/000000?text=+) **Bug** Obviously for bugs.
* ![#f03c15](https://placehold.it/15/2176D9/000000?text=+) **Documentation** When the documentation needs to be improved.
* ![#f03c15](https://placehold.it/15/673BB5/000000?text=+) **Feature** Request a new feature to be implemented.
* ![#f03c15](https://placehold.it/15/5F7C8A/000000?text=+) **Question** You can ask various questions about the bot or development.
* ![#f03c15](https://placehold.it/15/4AAE52/000000?text=+) **Easy** The issue should be easy to complete. Stands for bug, documentation, feature and question. Same for other difficulty labels.
* ![#f03c15](https://placehold.it/15/FEEA41/000000?text=+) **Medium** The issue is more difficult.
* ![#f03c15](https://placehold.it/15/E55006/000000?text=+) **Hard** The issues is hard to complete. Requires a deep understanding of programming and the bot itself.

## Building / running
Building or running the bot should be very simple and straightforward. Depending on the IDE you use, you can simply build or run the project using the IDE's integrated tools.

If you aren't using an IDE or using the CLI the command for building the project is:
```
dotnet build
```
And for running:
```
dotnet run
```

## Join our development Discord server
If you are planning on contributing to the project you should join the BotMyst development Discord server here: https://discord.gg/rNQBq9

## Comprehensive guide on contributing
Before you even begin working on fixes or features you have to fork the repository as you cannot directly work on this one.

#### Forking a repository
Forking a repository is very simple. All you have to do is go to the official BotMyst github repository and click the fork button.
![Forking a repository](https://i.imgur.com/AUnzsEu.png)

#### Adding new features / bug fixing
You should branch off from the dev branch:

```sh
$ git checkout -b myFeature dev
# Create a new branch "myFeature" that branches off from the dev branch, and switch to it.
```

Then you should do all the new work in that branch (myFeature). Then merge that branch back into the dev branch.
After you merged the branch back into the dev branch you should do a pull request on the dev branch in THIS repository. After that we will review it and merge it with our dev branch or master branch.

How to do it in CLI:
```sh
$ git checkout dev
# Switch to the dev branch
$ git merge --no-ff myFeature
# (Summary of changes)
$ git branch -d myFeature
# Delete the myFeature branch
$ git push origin dev
# Push to your forked dev branch
```
And after that do a simple pull request against our dev branch.
