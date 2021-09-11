## Sublime Text Turbo Mode

### How to install Sublime Text in Ubuntu
The easy way is follow the steps in [Sublime Text / Linux Repositories] and choose the stable version. Check the steps below:

1. Install the GPG key:

`wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -`

2. Ensure apt is set up to work with https sources:

`sudo apt-get install apt-transport-https`

3. Select the channel to use:

**Stable Version**
`echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list`

**Dev Version**
`echo "deb https://download.sublimetext.com/ apt/dev/" | sudo tee /etc/apt/sources.list.d/sublime-text.list`

4. Update apt sources and install Sublime Text

`sudo apt-get update`
`sudo apt-get install sublime-text`

### Installing from a tarball
1. Download the [Sublime Text tarball] that also available as a [x86-64](https://download.sublimetext.com/sublime_text_build_4113_x64.tar.xz) or [ARM64](https://download.sublimetext.com/sublime_text_build_4113_arm64.tar.xz)
2. The Sublime Text executable should be symlinked to subl, with a command such as:

```
sudo ln -s /opt/sublime_text/sublime_text /usr/local/bin/subl
```

3. Check if the path environment variable values should contain /usr/local/bin

### Working with terminal commands
- Check [Sublime Text] version: `subl --version`.
- Check if is possible run [Sublime Text] from terminal using the command `subl`.
- Check the help using the command `subl --help`:

```Bash
Sublime Text build 4113

Usage: subl [arguments] [files]         Edit the given files
   or: subl [arguments] [directories]   Open the given directories
   or: subl [arguments] -- [files]      Edit files that may start with '-'
   or: subl [arguments] -               Edit stdin
   or: subl [arguments] - >out          Edit stdin and write the edit to stdout

Arguments:
  --project <project>:    Load the given project
  --command <command>:    Run the given command
  -n or --new-window:     Open a new window
  --launch-or-new-window: Only open a new window if the application is open
  -a or --add:            Add folders to the current window
  -w or --wait:           Wait for the files to be closed before returning
  -b or --background:     Don't activate the application
  --safe-mode:            Launch using a sandboxed (clean) environment
  -h or --help:           Show help (this message) and exit
  -v or --version:        Show version and exit

Filenames may be given a :line or :line:column suffix to open at a specific
location.
```

### My favorite extensions and themes
The [Sublime Text] has a [Package Control] with all extensions and themes to be installed though [Command Palette] or menu:
#### Command Palette
1.  Open the command palette  
	- Win/Linux: `ctrl+shift+p` and Mac: `cmd+shift+p`
2.  Type `Install Package Control`, press enter.
3.  Type the extension or theme name.
Please, check the [Package Control documentation](https://packagecontrol.io/docs) to know more about it.

### Script to install Sublime Text Stable
A Bash script to install it from terminal, just run it as `bash sublime.sh`.
```Bash
#!/bin/bash
echo "Installing Sublime Text [Stable]. Press ENTER to start or CTRL+C to cancel:"

wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
sudo apt-get install apt-transport-https

echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list

echo "Updating..."
sudo apt-get update

echo "Installing Sublime Text..."
sudo apt-get install -y sublime-text
```

![sublime](https://cdn.hashnode.com/res/hashnode/image/upload/v1631387201775/GiH0AtLLP.jpeg)

### List of my favorites extensions:
- [Rainbow Brackets](https://packagecontrol.io/packages/RainbowBrackets) at different levels the brackets will be dyed with different colors according to the settings.
- [Emmet](https://packagecontrol.io/packages/Emmet) is a web-developer’s toolkit for boosting HTML & CSS code writing.
- [Image Preview](https://packagecontrol.io/packages/ImagePreview) to preview images that need conversion the plugin requires [Imagemagick](https://www.imagemagick.org/script/download.php) and that `magick` command is in your path.
- [Color Highlighter](https://packagecontrol.io/packages/Color%20Highlighter) previews color values by underlaying the selected hex codes in different styles.
- [Color Picker](https://packagecontrol.io/packages/ColorPicker) to insert or change a selected color on  Linux pressing the shortcut `ctrl+shift+c`.
- [Markdown Editing](https://packagecontrol.io/packages/MarkdownEditing) provides a decent Markdown color scheme (light and dark) with more robust syntax highlighting.
- [Markdown](https://packagecontrol.io/packages/MarkdownPreview) preview and build plugin for [Sublime Text](https://facelessuser.github.io/MarkdownPreview/).
- [LaTeXTools](https://packagecontrol.io/packages/LaTeXTools) a LaTeX plugin.
- [Terminal](https://packagecontrol.io/packages/Terminal) launch terminals from the current file or the root project folder.
- [Terminus](https://packagecontrol.io/packages/Terminus) a real terminal to Sublime Text.
- [Placehold.it Image Tag Generator](https://packagecontrol.io/packages/Placehold.it%20Image%20Tag%20Generator) using the features of [Placehold.it](http://placehold.it/) to insert an image tag with dummy image.
- [SVG Preview](https://packagecontrol.io/packages/SVG%20Preview)
- [QuickView](https://packagecontrol.io/packages/QuickView) image and color previews in Sublime Text.
- [Gitlab Integrate](https://packagecontrol.io/packages/GitlabIntegrate) integrates various Gitlab features.
- [Git](https://packagecontrol.io/packages/Git) plugin for some git integration into sublime text.
- [AutoFileName](https://packagecontrol.io/packages/AutoFileName) plugin that autocompletes filenames.	
- [BracketHighlighter](https://packagecontrol.io/packages/BracketHighlighter) bracket and tag highlighter for Sublime Text.
- [Auto Close HTML Tags](https://packagecontrol.io/packages/Auto%20Close%20HTML%20Tags) plugin that auto closes HTML tags right after '>'.


### Themes and Icons
- [FileIcons](https://packagecontrol.io/packages/FileIcons) adds specific, colored icons for most file types for the sidebar.
- [A File Icon](https://packagecontrol.io/packages/A%20File%20Icon) specific Icons for Improved Visual Grepping.
- [Theme Spacegray](https://packagecontrol.io/packages/Theme%20-%20Spacegray) a hyperminimal UI Theme for Sublime Text.
- [Ayu](https://packagecontrol.io/packages/ayu) modern Sublime Text theme.
- [Enki Theme](https://packagecontrol.io/packages/Enki%20Theme) a color scheme and UI theme for [Sublime Text] with clear, disparate colors to help differentiate between all syntactic aspects of code, including syntax highlighting for the console.
- [Brogrammer](https://packagecontrol.io/packages/Theme%20-%20Brogrammer) is a flat sexy theme. Pushups not included.


#### References:
[Command Palette], [Package Control], [Sublime Text tarball], [Sublime Text] and [Sublime Text / Linux Repositories].

[Command Palette]: https://packagecontrol.io/installation
[Package Control]: https://packagecontrol.io/
[Sublime Text tarball]: https://www.sublimetext.com/download
[Sublime Text]: https://www.sublimetext.com/
[Sublime Text / Linux Repositories]: https://www.sublimetext.com/docs/linux_repositories.html


**Please, share comment, subscribe and give me a thumbs up!!**


