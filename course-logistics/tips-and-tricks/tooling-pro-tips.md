---
description: Tips for using programming tools
---

# 🛠 Tooling Pro Tips

## Using VSCode Effectively

### Comment Out Multiple Lines at Once

Sometimes we wish to enable or disable certain segments of our code for quick testing. The easiest way to do this is to "comment out" the code we want to disable by turning it into comments, making our JavaScript runtime ignore those lines of code.

Rather than adding `//` to the start of each line manually, VSCode has a shortcut that allows us to comment out multiple lines simultaneously. To do this, select all lines we wish to comment out, then use the keyboard shortcut `Ctrl+/` on Windows, or `Cmd+/` on Mac.

### Editing a Variable Name in Multiple Places Concurrently

Sometimes we want to change the name of a variable in our code, a common practice in [refactoring](https://en.wikipedia.org/wiki/Code\_refactoring). If that variable is used in multiple places, we may be tempted to edit each instance individually. Luckily VSCode has a convenient feature that allows us to edit all instances of the same variable simultaneously, saving time and our fingers.

#### Within a Single File

1. Move your cursor to the first instance of the variable
2. Press/hold `Ctrl+D` on Windows or `Cmd+D` on Mac until all instances of that variable are selected
3. Use left or right arrow keys to enable cursors on each instance of that variable and edit them simultaneously

#### Across Multiple Files

VSCode has a [search and replace feature](https://code.visualstudio.com/docs/editor/codebasics#\_search-across-files) that allows us to edit all instances of a given string in multiple files at once.

### Hide Minimap

The [VSCode minimap](https://code.visualstudio.com/docs/getstarted/userinterface#\_minimap) is displayed by default in VSCode to show one's vertical position within a file. This may not be necessary in Coding Basics and we can hide the minimap for more space in VSCode. Hide the minimap by toggling View > Show Minimap in the menu bar.

## Troubleshooting the Terminal Editor

> Hi everyone, in the event you accidentally type `git commit` without the ‘-m’ option, you’ll notice that your terminal changes slightly and you realise you can’t type anymore. That is because a commit message is compulsory. So, by default, your terminal will open something called VIM - its a type of text editor that is not exactly user friendly, and expects you to type your commit message.

1. How to get out of VIM:
2. You have to enter something called a command mode simply by pressing the escape key
3. type the following:  `:q!`
4. the above characters should appear at the bottom of your terminal as you are typing
5. Then hit enter

2\. How to change the default editor to VSCode instead

1. run the following command on your terminal (you can run this command regardless of what folder you may be in): `git config --global core.editor "code --wait"`
2. This basically configures git to make VSCode your default editor should you ever forgot to use the ‘-m’ flag when committing.
3. If you ever do forget to use the ‘-m’ flag, a normal text file will open automatically on VSCode and you can simply type your message in that file and then close it.

> Don’t worry if this doesn’t make sense now(: But feel free to use this as a reference if you ever face that issue!

## Watching YouTube Videos at Different Speeds

If the course videos are too fast or too slow for you, you can watch them at slower or faster speeds by [toggling a speed setting in YouTube](https://support.google.com/youtube/answer/7509567?co=GENIE.Platform%3DDesktop\&hl=en) or you can use the [Video Speed Controller Extension](https://chrome.google.com/webstore/detail/video-speed-controller/nffaoalbilbmmfgbnbgppjihopabppdk?hl=en)

##
