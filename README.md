# Discord Activity Monitor
<!--summary-->
A discord bot to assign/remove a role from users in your guild based on whether or not they have been active lately
<!--/summary-->

## Features
<!--features-->
- Remove an 'active' role from a user who has not been active for a number of days
- Optionally assign an 'inactive' role to a user when they lose the 'active' role
- Optionally re-assign the 'active' role when a user who becomes active again
- Configure specific users or roles to be exempt from monitoring
- Configure threshold for inactivity
<!--/features-->

## Use cases
- You want to keep active members at the top of the members sidebar
- You want to reward active members for participating in the community
- You want to recognise how many inactive members your server has

## Examples
- Active users can easily see which other active users are online, without the sidebar being full of lurkers
- After a period of time inactive users could lose read/write permissions until re-enabled by a moderator

## Getting started
### Invite
- By using this bot you agree to the terms laid out in the [Privacy & Terms](./docs/privacy-and-terms) document
- If you agree, use my [public invite]() (coming soon!) to invite the bot to your server

### Setup
**Admin only**
Setup requires administrator permission in the Discord server
1. Create a role (or choose an existing one) to use to mark active users
2. Make your chosen role *mentionable* (only needed until setup is complete)
3. Put the bot's role *higher* in the list than your chosen role
4. Run `@Activity Monitor setup` in a channel the bot can *read* and *write* in
	- If you've nicknamed the bot, substitute `@Activity Monitor` for it's nickname
5. Respond with the information the bot asks you for, until setup is complete

- You can view your guild settings with `@Activity Monitor view-config`

Example:  
![example image](http://i.imgur.com/3W8jN4I.png)

### Permissions

The bot requires certain permissions, which you are prompted for on the invite screen.
Each permission has a reason for being required, explained below.

| Permission     | Reason                                                                |
|----------------|-----------------------------------------------------------------------|
| Read messsages | Detect when people are active                                         |
| Send messages  | Used to ask setup questions (can be disabled after setup is complete) |
| Manage roles   | Assign and remove the active role from users                          |
| Embed links    | Responses to 'help' requests use message embeds for nice formatting   |

## Self hosting
1. Clone the repository, or download and extract the zip file (preferrably from the release page)
2. Make sure you have *npm* and *git* installed
3. Run `npm install`
4. Run `npm run build`
5. Add a file named *token* in the root folder with your token string in
6. Run `npm start`

**Note for git users**  
If you cloned the repository with git, make sure you `git reset --hard vX.Y` to a specific version, as latest master isn't always production ready!

## Need help?

I am available for contact via my [support Discord server](https://discordapp.com/invite/SSkbwSJ). I will always do my best to respond, however I am often busy so can't always be available right away, and as this is a free service I may not always be able to resolve your query.

## Built With
- [discord.js](https://github.com/discordjs/discord.js) - *Discord library*
- [disharmony](https://github.com/benji7425/disharmony) - *Bot framework*

## Versioning
[SemVer](http://semver.org/) is used for versioning; view available versions on the [tags page](https://github.com/your/project/tags)

## License
This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details