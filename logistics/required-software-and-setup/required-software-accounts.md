# 👨🏫 Required Software - Coding

## 1. Google Chrome - Browser

Chrome is the most popular web browser for software engineers because of its mature developer tools, which we will soon see in course videos. Chrome also has the largest library of browser extensions, which further help developers build and maintain software.

#### **Installation:**

1. Download Chrome for your OS [here](https://www.google.com/intl/en\_sg/chrome/).

## 2. VSCode - Code Editor

VSCode is a very popular code editor. We will be writing all our code for Coding Basics using VSCode. \
Please download VSCode for your OS [here](https://code.visualstudio.com/download) and install it.

## 3. Git - Command Line Software

Command-line software is software primarily operated from the command line that may not have a graphical user interface we can interact with. This will be further explained in the course.

This software is typically used by software developers to write programs. Command-line software is not stored in a computer's Applications folder. We'll cover more about the command line in xxyyzz.

Git is a popular software version control system.&#x20;

Tech companies use version control to manage contributions to and releases of their software. We will be using basic Git during Coding Basics to download and upload copies of projects. We'll cover more about Git in xxyyzz.

{% tabs %}
{% tab title="Mac Installation" %}
#### Installing Git for Mac OS

1. Download and install Git for Mac OS by downloading it here: [https://sourceforge.net/projects/git-osx-installer/](https://sourceforge.net/projects/git-osx-installer/)
2. Verify Git is installed by running `git --version` in the [VSCode terminal](https://code.visualstudio.com/docs/editor/integrated-terminal). This should print out a version number on the next line, e.g., `git version 2.28.0`.
3. Download and install the [Git Credential Manager.](https://github.com/microsoft/Git-Credential-Manager-Core/releases/download/v2.0.498/gcmcore-osx-2.0.498.54650.pkg)

{% hint style="warning" %}
To install the Git Credential Manager you may need to allow "unidentified developer apps". (_But don't worry, Git Credential Manager is created by Microsoft_) from instructions [here:](https://support.apple.com/en-sg/guide/mac-help/mh40616/mac)

**To override your security settings and open the app, follow these steps:**

1. _In the Finder_ ![](https://help.apple.com/assets/605932B4A1B7A93F492858E8/605932C0A1B7A93F492858FF/en\_US/058e4af8e726290f491044219d2eee73.png) _on your Mac, locate the download file._
2. _Control-click the app icon, then choose Open from the shortcut menu._
3.  _Click Open._\
    \_\_

    _The app is saved as an exception to your security settings, and you use it in the future just as you can any registered app._\
    \_\_

Note: If you are using a company computer for this course you may not be able to override the security settings- you may need to [create a personal token as described here.](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token)
{% endhint %}
{% endtab %}

{% tab title="Windows Installation" %}
#### Installing Git for Windows

1. Navigate to the Git website download page and click the download link: [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Open the downloaded file.
3. The Git install dialog will open. We'll need to set a few options here. The rest will be the default options.
4. Follow command line setup instructions **in the video below** to set Bash as the terminal language.
5. Verify Git is installed by running `git --version` in the [VSCode terminal](https://code.visualstudio.com/docs/editor/integrated-terminal). This should print out a version number on the next line, e.g., `git version 2.28.0`.

{% embed url="https://www.youtube.com/watch?t=87s&v=7Dq_e90LqTU" %}
{% endtab %}
{% endtabs %}

## VSCode Setup

### VSCode Formatters

### Prettier

Prettier is a code formatter that will auto-format our code and make it more readable when we save our files.

1. Install the Prettier extension for VSCode [here](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode).
2. Restart VSCode to activate Prettier.

### VSCode Formatting Settings

1. Open VSCode and open the command prompt with `Ctrl+Shift+P` on Windows and `Cmd+Shift+P` on Mac.
2. Start typing `Preferences: Open Settings (JSON)` and select this option when you see it in the search dropdown. A JSON settings file should open in VSCode.
3. Replace everything on the screen (in the file) with the code below.
4. Save the settings file.
5. Restart VSCode to apply our settings.
6. Open and save the settings file again and verify that Prettier auto-formats it as our default formatter.

### VSCode Settings

{% tabs %}
{% tab title="Mac OS" %}
#### VSCode Settings - Mac OS

```
{
	"editor.formatOnSave": true,
	"editor.formatOnPaste": true,
	"editor.minimap.enabled": true,
	"editor.tabSize": 2,
	"editor.wordWrap": "on",
	"editor.defaultFormatter": "esbenp.prettier-vscode"
}
```
{% endtab %}

{% tab title="Windows" %}
#### VSCode Settings - **Windows**

{% hint style="warning" %}
Windows users: The following code assumes we installed our Git folder at **the root of our C drive (**which is the default installation path for Windows).&#x20;

However, some students' installers install the Git folder elsewhere, for example in `C:\\Program Files (x86).`&#x20;

Note the installation location of Git when you installed it, as per the instructions above.

If your installed Git folder is not in the location as listed below, please edit line 8 and 12 to the appropriate values when you copy these configurations.
{% endhint %}

```
{
	"editor.formatOnSave": true,
	"editor.formatOnPaste": true,
	"editor.minimap.enabled": true,
	"editor.tabSize": 2,
	"editor.wordWrap": "on",
	"editor.defaultFormatter": "esbenp.prettier-vscode",
	"terminal.integrated.defaultProfile.windows": "Git Bash",
	"terminal.integrated.profiles.windows": {
		"Git Bash": {
			"path": "C:\\Program Files\\Git\\bin\\bash.exe",
			"icon": "terminal-bash"
		}
	}
}
```
{% endtab %}
{% endtabs %}

## 4. GitHub - required internet account

GitHub is the a code-hosting platform. Developers use GitHub to share code and collaborate on projects. Rocket Academy's starter code and project templates are hosted on GitHub, and we will use GitHub in Coding Basics to download, host, and submit assignments. Each student will need a GitHub account to host and submit assignment code.

#### **Sign Up**

Go to [https://github.com/](https://github.com), click the Sign Up button and follow on-screen instructions.

#### **Git and GitHub Credential Configuration**

Add your GitHub account credentials to your computer through the command line. Please replace `<YOUR_GITHUB_USERNAME>` AND `<YOUR_GITHUB_EMAIL>` with your own GitHub user name and the email you used to sign up to GitHub with. _Note to replace the_ `<>` _characters and keep the_ `"` _characters in the commands._

```
git config --global user.name "<YOUR_GITHUB_USERNAME>"
```

```
git config --global user.email "<YOUR_GITHUB_EMAIL>"
```

#### Configuration Check

You will not get any feedback from the terminal after entering these commands.

Type the following command into the terminal to check your work. If you see a `:` at the bottom of the output, you may need to press `Enter` until you see the lines starting with `user.name` and `user.email`.

```
git config -l
```

You should see your username and email in the output, and possibly some other settings.

#### Git default branch configuration

Following the convention of all the other Rocket Academy Git repositories and GitHub, we'll change the default Git branch name by typing in the command shown in the code box.

```
git config --global init.defaultBranch main
```

###
