_When using a command with parameters, do not include the triangle <> brackets. e.g. if you wanted to add your account to the leaderboard, you would do_ `/add username` _rather than_ `/add <username>`

See the [quick start](https://github.com/kevinjycui/Practice-Bot/wiki/Quick-Start) to get started.

See the [moderation guide](https://github.com/kevinjycui/Practice-Bot/wiki/Moderation) for server admins and moderators -->

# General commands
- `/help` Sends you a list of available commands

## Account

-  `/add <leetcode_username> <include_url>` Adds your LeetCode account onto the corresponding server's leaderboard. 
>    - `leetcode_username`: Your permanent LeetCode username.
>    - `include_url` _(optional)_: 'yes' or 'no' if you want leaderboards in the corresponding server to include a hyperlink to your LeetCode profile or not. Default is 'yes'.
>    - `name` _(optional)_: Your preferred name to be displayed on the leaderboards in the corresponding server.
- `/update <include_url> <name>` Updates your account preferences for the corresponding server.
>    - `include_url` _(optional)_: 'yes' or 'no' if you want leaderboards in the corresponding server to include a hyperlink to your LeetCode profile or not. Default is 'yes'.
>    - `name` _(optional)_: Your preferred name to be displayed on the leaderboards in the corresponding server.
- `/remove` Removes your LeetCode account from the corresponding server.

## Leaderboard

- `/leaderboard [timeframe] <page>` Displays the leaderboard of your server. A page number can be specified but if none is provided, it will initially display the first page

There are currently 3 timeframe subcommands:

> `daily` Returns today's leaderboard stats which resets at midnight (UTC)

> `weekly` Returns the week's leaderboard stats which resets on Sunday at midnight (UTC)

> `alltime` Returns the all-time leaderboard stats

Note: stats for `daily` and `weekly` will only be calculated after an account is created. Any previous questions done that day or that week will not be calculated.

## Statistics

- `/stats <leetcode_username>` Returns the statistics of your or someone else's LeetCode account.
>    - `leetcode_username` _(optional)_: A LeetCode username. Default is your connected LeetCode account.

## Questions

- `/daily` Returns the LeetCode daily question
- `/question <difficulty>` Returns a random question of your specified difficulty level. 
>    - `difficulty` _(optional)_: A difficulty level ('easy', 'medium' or 'hard'). Default is a 'random' difficulty level.
- `/rating <question_id_or_title>` Returns the Zerotrac rating of the given question.
>    - `question_id_or_title`: The LeetCode question ID or the question's name/title.

# Admin commands
These commands are only available to administrators of the corresponding server.
## Settings

- `/settings timezone <timezone>` Change the timezone of the server.
>    - `timezone`: A timezone (case sensitive) from the following list of timezones: https://gist.github.com/heyalexej/8bf688fd67d7199be4a1682b3eec7568 .

## Notifications

- `/notifychannel enable <channel>` Set what notifications the channel receives.
>    - `channel` _(optional)_: The channel (e.g. "#home-channel"). Default is the channel where the command was run.
- `/notifychannel disable <channel>` Stop channel from receiving selected notifications.
>    - `channel` _(optional)_: The channel (e.g. "#home-channel"). Default is the channel where the command was run.

Note: please press the 'save' button twice