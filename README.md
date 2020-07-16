# Alfred Workflows

This repository contains some of the workflows I created using AlfredApp. You can download and
import these into your own Alfred installation if they seem useful to you. 

## JH Dev Tools

Provides the following new keyword-driven workflows:

* `dec2hex <decimal value>` - Converts the specified decimal value to hexadecimal and places the result in the pasteboard
* `hex2dec <hexadecimal value>` - Converts the specified hexadecimal valut to decimal value and places the result in the pasteboard
* `color2hex <red> <green> <blue>` - Takes three decimal values and converts them to one CSS-style hexadecimal color value
* `remember [thing to remember]` - Allows you to remember a single thing, has three activations:
    * No modifiers - Writes the `thing to remember` to `~/.remember`
    * While holding Option - Displays the contents of `~/.remember` on screen
    * While holding Command - Clears the contents of `~/.remember`
* `.a` - Kills all instances of AnyBar (may only be useful when using my AnyBar-fork)

## JH Pomodoro Timer

Provides a workflow to manage pomodoro-intervals. It uses `slackcli` under the hood, so make sure you installed it through
`brew tap rockymadden/rockymadden && brew install rockymadden/rockymadden/slack-cli`

This workflow allows you to type `.pd start` to start a period of 25 minutes. It will set your Slack-status to do not disturb with
and end-time. This makes it possible for other people to see you are in a pomodoro and should not be disturbed. It also allows others
to see when your current pomodoro ends. 

Once a pomodoro is active, you can cancel it using `.pd stop`. This will clear all things that were going to notify you of the
completion of your pomodoro.


When the 25 minute block comes to an end, you should be greeted by both a Slack reminder and a MacOS notification, indicating your
time for relaxation has started. You can of course start another pomodoro once you are ready for it.
