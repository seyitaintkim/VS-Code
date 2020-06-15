[logo]: ./img/vscode.svg "VS Code Logo"

# VS Code Tricks and Tips

This is a bare-bones guide to using your favorite text editor. I have been digging deep into (reading individual settings, line by line) VS Code for a couple of weeks, and read too many articles to care for. I hope to bring some tips and tricks that we can all utilize during our cohort! If you have suggestions, please make a pull request (I'll figure git out soon).

#### My Motivation

I suffer from moderate RSI that primarily resulted from a freak shoulder injury. Initially, I was not able to use my hands at all for a couple of months. Long story short, June 2020 marks my 25th month of my battle with RSI. I have tried everything under the sun to limit the usage of my arms and to stay functional. Crazy how now I am in the midst of frantically preparing for Codesmith (LA Cohort 37). Despite my fear of hurting myself again, I've fully committed to utilizing and learning as many hotkeys and shortcuts I can. Hopefully, you too will be able to put this resource to good use!

## Resources

Microsoft's [official guide](https://code.visualstudio.com/docs/introvideos/basics) will always be the canonical source. Stackoverflow and its subdirectory, such as [superuser](https://superuser.com/), have some serious power users but may be too technical and erudite for fledglings like us.

| Links                                                                                                                     |                           Description                            |
| ------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------: |
| [VS Code settings you should customize](https://dev.to/thegeoffstevens/vs-code-settings-you-should-customize-5e75)        |              Miscellaneous setups, including fonts               |
| [The 25 Best VS Code Extensions](https://medium.com/better-programming/how-to-use-vscode-like-a-pro-e120c428f45f)         |          A good number of them are absolutely essential          |
| [How to Get to the JSON settings in Newer Versions of VS Code](https://stackoverflow.com/a/57960147/13544596)             |        Simple stackoverflow answer for User Setting JSON         |
| [VS Code Can Do That?](https://www.vscodecandothat.com/)                                                                  |             Advanced videos that I need to check out             |
| [Windows PDF](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)                                     |                 PDF, if you want to print it out                 |
| [macOS PDF](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)                                         |                               PDF                                |
| [Linux PDF](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf)                                         |                               PDF                                |
| [Microsoft's Setting up Node JS](https://code.visualstudio.com/docs/nodejs/nodejs-tutorial)                               | Step-by-step setting up terminal, node and running your JS files |
| [Installing VS Code CLI to path](https://code.visualstudio.com/docs/setup/mac)                                            |           I think Windows users don't need to do this            |
| [VS Code shortcuts you should know](https://medium.com/swlh/15-visual-studio-code-shortcuts-you-should-know-ea1b4166f69f) |                          Some good ones                          |

## 👍 Personal Extension List

###Top 3

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) - Needed for Airbnb config
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) - Format on save 😍
- [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner) - press a hotkey to check your code

###Utility

- [Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare) - for browser rendering
- [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) - needed for remote pairing
- [Bracket Colorizer 2](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2) - visual rendering of your scopes
- [Quick and Simple Text Selection](https://marketplace.visualstudio.com/items?itemName=dbankier.vscode-quick-select) - powerful ways to select without using the mouse
- [Bracket Select](https://marketplace.visualstudio.com/items?itemName=chunsen.bracket-select) - this does one thing well: select inside brackets

###UI

- [Babel Javascript](https://marketplace.visualstudio.com/items?itemName=mgmcdermott.vscode-language-babel) - alternative highlighting syntax
- [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme) - popular colorful icons to visually distinguish

## Ok, how do I really set up Airbnb Config?

Here's **[relatively recent Medium Article](https://medium.com/javascript-in-plain-english/set-up-react-js-with-eslint-prettier-and-airbnb-cc015363a7c7)** and **[a Youtube video](https://www.youtube.com/watch?v=SydnKbGc7W8&t=3s)**. You don't need to create react app (I've only ran the command a couple of times) to completely set up an airbnb linting config. I'll try to be as succint as possible, and hopefully, you'll have your perfect combination ready to go so you can focus on the code.
