# SimpleTasks
SimpleTasks is exactly what it sounds like: a simple task/notes system for your Twitch chat!

## Features:
- Add, edit, and delete tasks with a single command
- Easily complete or undo tasks
- View all tasks in a handy togglable stream overlay

## Requirements
- [Firebot v5.66.7](https://firebot.app) or later
- A Twitch account able to stream
- A Discord server that *you* own

## Setup

### 1. Basics

1. Download SimpleTasks.firebotsetup from the main repository.
2. Go to Firebot > Firebot Setups > Import Setup, and select the setup you just downloaded.
3. All of the necessary components should be set up.

### 2. The Text File

This program relies on using a plain text file to store the data. Firebot setups do not support including a plain text file, however, so you will need to create one manually:
1. Create a blank plain text file (.txt) to use as the tasks list; and make sure it's saved in a place you'll remember it.
2. Copy the filepath to your plain text file, *making sure the file name is at the end of it.*
3. Turn on Firebot.
4. Run the command `!tasks filepath <path>`, putting your filepath at the end of the command.
5. If you've done it successfully, it will post a message in chat comfirming this. If not, make sure that you've copied the filepath correctly.

### 3. Discord Integration
If you haven't set it up already, you'll need to create an integration to Discord so it can export the tasks list at the end of stream. (If you already have a Discord integration set up, skip to the next section.)
1. In Discord, navigate to the channel you want the bot to post to, then go to Edit Channel > Integrations > Webhooks > New Webhook.
2. Customize the webhook name and image, if you want, and copy the URL.
3. In Firebot, navigate to Settings > Integrations > Discord, and hit "Configure."
4. Under the Channel Setup section, add a new channel. Name it whatever you desire.
5. In the URL section, paste the URL that you've just copied, and hit save. You now have Firebot connected to Discord!

Now that you have Twitch connected, you'll need to set up the scripts to post to the designated channel!
1. Navigate to the "Stream Ending" event, and find the "Send Discord Message" effect. (Custom Effect List > Conditional Effects > Send Discord Message)
2. Under the "Discord Channel" section, set it to the webhook you created.
3. The bot should now be automatically set up to post to your selected Discord channel!

### 4. Overlay Setup
If you don't have it set up already, you'll likely want multiple overlay instances enabled. The task overlay is made of three conponents, so it might be a wise idea to keep them on a seperate instance of the overlay.
Simply navigate to Settings > Overlay Instances, and toggle it on.

## Available commands
|Command |Function  |
| :----- | :------- |
| `!task`| View a specific task. |
| `!task add <text>`| Add a task to the list. |
| `!task <number> edit <text>` | Edit the text of a specific task. |
| `!task <number> delete` | Delete a specific task. |
| `!task <number>` | View a specific task. |
| `!task <number> done` | Mark a task as completed. |
| `!task <number> undo` | Mark a task as incomplete. |
| `!task clear` | Clears the entire task list. |
| `!task show` | Shows the task overlay until toggled off.|
| `!task hide` | Hides the task overlay. |
| `!task filepath <filepath>` | Sets the filepath for the .txt document used. |
| `!task help` | Displays a list of all available commands (excluding the filepath one) |

## Disclaimer
Absolutely zero generative AI was used in ANY stage of the project, whether it be for the code or the art. This is simply a passion project coded for the fun of it.

## Special Thanks
- l337f00l (Windows tester)
- alhuno (Linux tester)
- iamtheratio (light feedback)
