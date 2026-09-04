# File Manager

File Manager is a plugin for Sublime Text that is suppose to replace SideBarEnhancement and AdvancedNewFile.

Why? Because those to plugin basically do the same thing: *They manage files from sublime text*.

With this package, you can create, rename, move, duplicate and delete files or folders. You can also copy there relative/absolute path, or their name.

<!-- MarkdownTOC -->

- ["Spirit"](#spirit)
    - [The idea is to make you save time, not to propose you features you're never going to use.](#the-idea-is-to-make-you-save-time-not-to-propose-you-features-youre-never-going-to-use)
- [Docs](#docs)
- [Installation](#installation)
    - [Using package control](#using-package-control)
    - [Using the command line](#using-the-command-line)
- [How to open the `README`](#how-to-open-the-readme)
- [Contributing](#contributing)

<!-- /MarkdownTOC -->

## "Spirit"

#### The idea is to make you save time, not to propose you features you're never going to use.

> This package has as main goal to be 100% optimized.

So, for example, there is an **auto completion** system (based on the folders/files, both, you choose) on every input that is showed by FileManager. Just press <kbd>tab</kbd> to cycle through the auto completion.

> There shouldn't be 2 commands when 1 can do the job.

FileManager doesn't have a command `create_new_file` and `create_new_folder`. Just `fm_create`. It opens up an input, and the last character you type in is a `/` (or a `\`), it creates a folder instead of a file.

## Docs

Although they're a fair bit of information in there, the docs are still a work in progress. Here they are: [math2001.github.io/FileManager](https://math2001.github.io/FileManager). **Go have a quick look, you won't regret it** :smile:


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
    wait few seconds until the installation finishes up
1. Now,
    Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    input the following address and press <kbd>Enter</kbd>
    ```
    https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
    ```
1. Go to the menu **`Tools -> Command Palette...
    (Ctrl+Shift+P)`**
1. Type **`Preferences:
    Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    find the following setting on your **`Package Control.sublime-settings`** file:
    ```js
    "channels":
    [
        "https://packagecontrol.io/channel_v3.json",
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
    ],
    ```
1. And,
    change it to the following, i.e.,
    put the **`https://raw.githubusercontent...`** line as first:
    ```js
    "channels":
    [
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
        "https://packagecontrol.io/channel_v3.json",
    ],
    ```
    * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
      you will not install this forked version of the package,
      but the original available on the Package Control default channel **`https://packagecontrol.io...`**
    > [!WARNING]
    > Placing this custom channel before the default channel changes Package Control's resolution globally. Packages from this channel with the same name will override versions from the default channel.
    >
    > You can review the channel contents here:
    > https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
1. Now,
    go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    search for **`FileManager`** and press <kbd>Enter</kbd>

See also:

1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


## How to open the [`README`](https://github.com/math2001/FileManager/blob/master/README.md)

To open their README, some of the package add a command in the menus, others in the command palette, or other nowhere. None of those options are really good, especially the last one on ST3 because the packages are compressed. But, fortunately, there is plugin that exists and will **solve this problem for us** (and he has a really cute name, don't you think?): [ReadmePlease](https://packagecontrol.io/packages/ReadmePlease). :tada:

## Contributing

You want to contribute? Great! There's two different things you can contribute
to:

1. the package itself
2. the docs

If you want to contribute to the *package*, then you're at the right place.
Otherwise, please go have a look at [the contributing part of the docs][0]

First, whatever you want to do, please raise an issue. Then, if you feel in a
hacky mood, go ahead and code it:

- create a branch: `my-feature-name`
- don't hesitate to change stuff in the `.tasks` file.
- Push and PR

Note: This plugin is only working on Sublime Text 3.

[0]: https://math2001.github.io/FileManager/contributing/

## License
See the LICENSE file
