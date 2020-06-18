<img src="./img/vscode.svg" height="150">

# VS Code Tricks and Tips

---

This is a bare-bones guide to using your favorite text editor. I hope to bring some tips and tricks that we can all utilize during our LA Cohort 37! If you have suggestions, please make a pull request and I'll try to figure out how to use git. **⚠️ I AM BY NO MEANS AN EXPERT! ⚠️** Everything on this guide is a collection of resources I've accumulated and filtered over the last few weeks.

## Table of Contents

---

- [My Motivation](#my-motivation)
- [Links](#links)
- [Personal Extension List](#personal-extension-list)
  - [Top 3](#top-3)
  - [Utility](#utility)
  - [UI](#ui)
- [File Locations](#file-locations)
- [First Steps](#first-steps)
- [Setup AirBnb](#setup-airbnb)
- [Curated Keyboard Shortcuts](#curated-keyboard-shortcuts)
  - [General](#general)
  - [Layouts](#layouts)
  - [Selection and Text Editing](#selection-and-text-editing)
  - [Extension Keyboard](#extension-keyboard)
- [Set your own keyboard bindings](#set-your-own-keyboard-bindings)
  - [Example](#example)
  - [Advanced: Using Snippets](#advanced--using-snippets)

## My Motivation

---

I suffer from moderate RSI that primarily resulted from a shoulder injury two years ago. Long story short, to make learning ~~to code~~ _software engineering_ feasible, I have to go to great lengths to keep my arms relatively pain free. Preparing for Codemsmith, I've fully committed to utilizing and learning as many hotkeys and shortcuts I can in the span of this week. Hopefully, you too will be able to put this resource to good use!

## Links

---

Microsoft's Visual Studio Code's **[official guide](https://code.visualstudio.com/docs/introvideos/basics)** will always be the canonical source. Stack Overflow and its subdirectory, such as [Super User](https://superuser.com/), have some serious power users in their ranks but they may be as a source too technical and erudite for fledglings like us.

| Links                                                                                                                     | Description                                                      |
| :------------------------------------------------------------------------------------------------------------------------ | :--------------------------------------------------------------- |
| [VS Code settings you should customize](https://dev.to/thegeoffstevens/vs-code-settings-you-should-customize-5e75)        | Miscellaneous setups, including fonts                            |
| [The 25 Best VS Code Extensions](https://medium.com/better-programming/how-to-use-vscode-like-a-pro-e120c428f45f)         | A good number of them are absolutely essential                   |
| [How to Get to the JSON settings in Newer Versions of VS Code](https://stackoverflow.com/a/57960147/13544596)             | Simple stackoverflow answer for User Setting JSON                |
| [VS Code Can Do That?](https://www.vscodecandothat.com/)                                                                  | Advanced videos that I need to check out                         |
| [Windows PDF](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)                                     | Official PDF of shortcuts                                        |
| [macOS PDF](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)                                         | PDF                                                              |
| [Linux PDF](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf)                                         | PDF                                                              |
| [Microsoft's Setting up Node JS](https://code.visualstudio.com/docs/nodejs/nodejs-tutorial)                               | Step-by-step setting up terminal, node and running your JS files |
| [Installing VS Code CLI to path](https://code.visualstudio.com/docs/setup/mac)                                            | Making sure to access `code` in your terminal                    |
| [VS Code shortcuts you should know](https://medium.com/swlh/15-visual-studio-code-shortcuts-you-should-know-ea1b4166f69f) | Some good ones you may find useful                               |

## Personal Extension List

---

There are too many extensions to list, but I've narrowed down to the absolute essentials, plus a few that I always end up using.

### Top 3

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) - Needed for Airbnb config
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) - Format on save 😍
- [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner) - press a hotkey to check your code

### Utility

- [Git Lens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) - I haven't touched git, but from the looks of it, it's the industry standard
- [Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare) - for browser rendering
- [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) - needed for remote programming
- [Quick and Simple Text Selection](https://marketplace.visualstudio.com/items?itemName=dbankier.vscode-quick-select) - powerful ways to select without using the mouse
  - [Bracket Select](https://marketplace.visualstudio.com/items?itemName=chunsen.bracket-select) - this may be a sub-section of Quick Select, but I like it because it does one thing well: select inside brackets

### UI

- [Bracket Colorizer 2](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2) - visual rendering of your scopes
- [Babel Javascript](https://marketplace.visualstudio.com/items?itemName=mgmcdermott.vscode-language-babel) - alternative highlighting syntax (pair this with a recommended theme)
- [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme) - popular colorful icons to visually distinguish

## File Locations

---

This is more of a reference for me, as I was a life long Windows user before switching to macOS. You can search around to tweak with your extension files and some default ones. Unless you know what you're doing, it's best to modify settings from the VS Code program.

**npm global packages**: downloaded `npm` modules with the `-g` flag:

- if you downloaded `node` with `nvm`, `~/.nvm/versions/node/{installed version}/lib/node_modules/`.
- Standard location should be: `/usr/local/lib/node_modules`.
- For Windows, should be `C:\Program Files\nodejs\node_modules\npm`.

I believe for CLI's, global installations are used to call the specified commands from any directory in your terminal.

**VS Code**: user settings and application defaults:

- `~/.vscode` for extensions and `Applications/Visual Studio Code.app/Contents/`
- `C:\users\{username}\AppData\Local\Programs\Microsoft VS Code`

## First Steps

---

Open up your VS Code, and press **⇧⌘P** to bring up the command palette. This is your most useful command: if you ever get lost, bring up the command palette and start typing. VS Code will match it and show you a list of results. Go to `User Settings`, and search for `workbench settings`, like shown below. You'll want to click `json` for `which settings editor to use by default` for more flexibility.
![alt](./img/editor-config1.png)
Click `Use Split JSON`.
![alt](./img/editor-config2.png)
Now, whenever you go to your User Settings, it will look like below. The left contains a list of all configurable settings in JSON. To overwrite a setting, simply copy it and paste it on the right. Make sure to change the value, otherwise you'd be simply overwriting with the same data.
![alt](./img/editor-config3.png)
For example, I edited `editor.fontLigature` to `true` from a default value of `false`. Try typing `fontfamily` in the search settings and bunch of options will pop up. Copy and paste `"editor.fontFamily": ...` to the right, making sure it's between the starting `{` and last `}`.

Now let's download code runner. If you haven't, **⌘O** (`Ctrl + O`) to a sample folder with basic Javascript file. Once you've successfully downloaded it, you can click the button on the top right (make sure you are in a js file). The default hotkey should pop up on hover (**⌃⌥N** or `Ctrl + Alt + N`).
img

## Setup AirBnb

---

Here's a **[relatively recent Medium Article](https://medium.com/javascript-in-plain-english/set-up-react-js-with-eslint-prettier-and-airbnb-cc015363a7c7)** and **[a Youtube video](https://www.youtube.com/watch?v=SydnKbGc7W8&t=3s)**. I'll be documenting the steps I have and will take as succintly and clearly as possible.

### First Step

1. Check: `which node`, `which npm`, `which eslint`. For Windows, `where.exe` should work in Powershell. If you don't have eslint installed, type `npm i eslint -g` and check again with `which`. Make sure you have node and npm installed to your path.
   ![ss](./img/which_ss.png)
2. `npm i -y` in your root directory. Mine is `~/dev/Codesmith/`. You should have this on your `pacage.json` file.

```{
  "name": "airBnb",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "Your Name",
  "license": "ISC",
  "description": ""
}
```

3.  type `npm i -D eslint-config-prettier eslint-plugin-prettier eslint-config-node eslint-plugin-node` into your terminal. If you inspect your `package.json`, you should notice this:

```
 "devDependencies": {
    "eslint-config-node": "^4.1.0",
    "eslint-config-prettier": "^6.11.0",
    "eslint-plugin-node": "^11.1.0",
    "eslint-plugin-prettier": "^3.1.4"
  }
```

4. type `npx install-peerdeps --dev eslint-config-airbnb` to install the AirBnb configuration file AND its peer dependencies. By default, React files are downloaded. For non-React projects, the AirBnb [docs](https://www.npmjs.com/package/eslint-config-airbnb) state that `eslint-config-airbnb-base` does not contain React files.

```
  "devDependencies": {
    "eslint-config-airbnb": "^18.1.0",
    "eslint-config-node": "^4.1.0",
    "eslint-config-prettier": "^6.11.0",
    "eslint-plugin-import": "^2.21.2",
    "eslint-plugin-jsx-a11y": "^6.2.3",
    "eslint-plugin-node": "^11.1.0",
    "eslint-plugin-prettier": "^3.1.4",
    "eslint-plugin-react-hooks": "^2.5.0",
    "eslint-plugin-react": "^7.20.0",
    "eslint": "^6.8.0"
  }
```

5. Create a `.prettierrc` file in your root directory. Here's my settings:

```
{
  "singleQuote": true,
  "tabWidth": 2,
  "printWidth": 100,
  "trailingComma": "none"
}
```

6. Type `eslint --init`. If not found, remember to `npm i eslint -g` which then you should be able to call the `eslint` command globally. You can follow along with the answers I've provided. Strangely, they told me to re-download the peer dependencies of the config file.

```
╰─ eslint --init                                           ─╯
? How would you like to use ESLint? To check syntax, find prob
lems, and enforce code style
? What type of modules does your project use? JavaScript modul
es (import/export)
? Which framework does your project use? React
? Does your project use TypeScript? No
? Where does your code run? Browser, Node
? How would you like to define a style for your project? Use a
 popular style guide
? Which style guide do you want to follow? Airbnb: https://git
hub.com/airbnb/javascript
? What format do you want your config file to be in? JSON
Checking peerDependencies of eslint-config-airbnb@latest
The config that you've selected requires the following dependencies:

eslint-plugin-react@^7.19.0 eslint-config-airbnb@latest eslint@^5.16.0 || ^6.8.0 eslint-plugin-import@^2.20.1 eslint-plugin-jsx-a11y@^6.2.3 eslint-plugin-react-hooks@^2.5.0 || ^1.7.0
? Would you like to install them now with npm? Yes
Installing eslint-plugin-react@^7.19.0, eslint-config-airbnb@latest, eslint@^5.16.0 || ^6.8.0, eslint-plugin-import@^2.20.1, eslint-plugin-jsx-a11y@^6.2.3, eslint-plugin-react-hooks@^2.5.0 || ^1.7.0
npm WARN eslint-plugin-prettier@3.1.4 requires a peer of prettier@>=1.13.0 but none is installed. You must install peer dependencies yourself.
npm WARN airBnb@1.0.0 No description
npm WARN airBnb@1.0.0 No repository field.

+ eslint-config-airbnb@18.1.0
+ eslint-plugin-react@7.20.0
+ eslint-plugin-react-hooks@2.5.1
+ eslint-plugin-import@2.21.2
+ eslint-plugin-jsx-a11y@6.2.3
+ eslint@6.8.0
updated 6 packages and audited 253 packages in 11.89s

5 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

Successfully created .eslintrc.json file in /Users/dev/Codesmith
```

7. Check your folder. There should be a `.eslintrc.json` in your root directory.
8. **MOST IMPORTANT STEP** I am not 100% sure of how this step works. If any of you can edit/add to this, it would be GREATLY appreciated! Look over your `.eslintrc.json` file. Then, modify it so it looks like this:

```
{
  "env": {
    "browser": true,
    "es2020": true,
    "node": true
  },
  "extends": ["plugin:node/recommended", "airbnb", "prettier", "prettier/react"],
  "parserOptions": {
    "ecmaFeatures": {
      "jsx": true
    },
    "ecmaVersion": 11,
    "sourceType": "module"
  },
  "plugins": ["react", "prettier"],
  "rules": {
    "no-console": "off"
  }
}
```

The `"extends"` key's value is an array which points to the (❓❓❓) configuration listed in your `package.json`. Note that `"prettier"` MUST come last in the array to make sure the conflicting rules between eslint and prettier works correctly.
Secondly, the `"rules"` determine which eslint configuration you can turn off, warn or on. For instance, I turned off `"no-console"` rule so that eslint would not mark console.logs as an warning (with the yellow squiggly).

## Curated Keyboard Shortcuts

---

Not to overwhelm you, but these are the commands that someone taught me to use when I first started using VS Code.

#### General

| Keyboard | Command            | Description                                                                            |
| -------- | ------------------ | -------------------------------------------------------------------------------------- |
| ⇧⌘P      | Command Palette    | Brings up a prompt to search for commands and settings                                 |
| ⌘P       | Quick Open         | Use this to switch between files instead of mouse click                                |
| ⌘⇧N      | New window         | Sometimes you may want to open a separate VS Code windows, useful for pair programming |
| ⌘,       | Open user setting  | If you set up split JSON, this is where you customize                                  |
| ⌘K ⌘S    | Keyboard shortcuts | Press ⌘K and then ⌘S -- you can search for commands and/or keyboards                   |

#### Layouts

| Keyboard   | Command           | Description                                                                                                                                      |
| ---------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| ⌘1/2/3     | Focus group       | When you split editor (⌘\\), helpful to move around                                                                                              |
| ⌃1/2/3/..9 | Switch to nth tab | Search `workbench.action.openEditorAtIndex1` in Keyboard shortcuts (⌘K ⌘S). I don't personally like how `⌃ Tab` switch between most recent tabs. |
| ⌘P         | Quick Open        | Use this to switch between files instead of mouse click                                                                                          |
| ⌘⇧N        | New window        | Sometimes you may want to open a separate VS Code windows, useful for pair programming                                                           |

#### Selection and Text Editing

| Keyboard           | Command                | Description                                                                                                                |
| ------------------ | ---------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| ⌘←/⌥← + ⇧          | Move by word/line      | Try to experiment and see how to move by word, move to ends of line. Holding down shift usually highlights your selection. |
| ⌘ Enter / ⇧⌘ Enter | Enter line below/above | You can have your cursor at the middle of the line and will insert new line and move your cursor. Super useful.            |
| ⌘⌥↓/↑              | Insert line below/up   |                                                                                                                            |
| ⌥↓↑                | Move line down/up      |                                                                                                                            |
| ⌘D                 | Add next selection     |
| ⌘L                 | Select line            |                                                                                                                            |
| F2                 | Rename Symbol          | Rename safely your function names and variables                                                                            |
| ⌃G                 | Go to line             |                                                                                                                            |
| ⌃⇧⌘→/←             | Expand Selection       | Quick way to select word or phrase                                                                                         |

#### Extension Keyboard

| Keyboard   | Command                         | Description                                                                         |
| ---------- | ------------------------------- | ----------------------------------------------------------------------------------- |
| ⌃⌥N        | `code-runner.run`               | Default hotkey binding to run your `js` files                                       |
| ⌘L ⌘O      | Open with Live Server           | I mapped it to ⌥L ⌥O so that I can use ⌘L for line select.                          |
| ⌘K + ( [ ' | Quick and Simple Text Selection | Consult the extension docs to select between matching brackets                      |
| ⌥A / ⌘⌥A   | `BraSel:Select`                 | Simply select inside `[], {}, ()`. Add ⌘ or Control to select the brackets as well. |

## Set your own keyboard bindings

- ⌘K ⌘S to open Keyboard Shortcuts (UI)
- Search command and double click on row. A prompt should open up and you can press your desired hotkey. If there are hotkey conflicts, it will tell you.

#### Example

- I unmapped the default command of ⌘G that was bound to `Find next/previous` by right clicking > Remove Keybinding.
- I searched "Go to line" in the Keyboard Shortcuts section, and overwrote the default ⌃G to ⌘G for my convenience.
- You can also do this by going to `Preferences: Open Keyboard Shorcuts (JSON)`. Search for this with your command palette.
- `keybindings.json`:

```
  {
    "key": "cmd+g",
    "command": "-editor.action.nextMatchFindAction",
    "when": "editorFocus"
  },
  {
    "key": "cmd+g",
    "command": "-workbench.action.terminal.findNext",
    "when": "terminalFindFocused || terminalFocus"
  },
```

## Using Snippets

#### Built-in snippets

To use built-in snippets more conveniently, go into your setting JSON. Paste `"editor.snippetSuggestions": "top",`. Now, open a js file and type "fo". A list should popup in your cursor. Just press enter, click or tab to expand the snippet. You can use tab to move around and quickly change variables.

#### Advanced Customization

To really take it to the next level, you can configure your own snippets and/or even modify the default ones.
Go to `Preferences > Configure User Snippets` and click `javascript.json` from the pull down menu.

## More to come...

This is just a small slice of how powerful VS Code is. I honestly spent more time on VS Code and tweaking with the settings than I would like. For me, it's imperative that I utilize all the shortcuts as much as possible, and keep my typing (and my mouse usage) as low as possible. For you, you may not need to go all-in, so just take whatever part you need to be more productive and stress-free.
