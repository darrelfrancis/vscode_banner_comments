# Banner Comments fix

```json
  ____
 | __ )  __ _ _ __  _ __   ___ _ __
 |  _ \ / _` | '_ \| '_ \ / _ \ '__|
 | |_) | (_| | | | | | | |  __/ |
 |____/ \__,_|_| |_|_| |_|\___|_|           _
  / ___|___  _ __ ___  _ __ ___   ___ _ __ | |_ ___
 | |   / _ \| '_ ` _ \| '_ ` _ \ / _ \ '_ \| __/ __|
 | |__| (_) | | | | | | | | | | |  __/ | | | |_\__ \
  \____\___/|_| |_| |_|_| |_| |_|\___|_| |_|\__|___/ fix
```

A 2023 update on an old favourite, to accommodate `.mjs`, `.spec.js` and `.cy.js`.

Select one or more lines of text you want to turn into a banner heading. Open the VS Code command palette with Ctrl-Shift-P or Cmd-Shift-P, and then use the following commands.

## Normal use: use 3 heading levels consistently

- **"Set <h1|h2|h3> font"**: Choose figlet fonts to use for 3 heading levels: h1, h2 and h3. You might try Univers, Standard and Mini.
  ![feature 'Set font'](images/banner-comments-set-font.gif)

- **"Apply <h1|h2|h3> font"**: Text is transformed into one of 3 fonts you have chosen for heading levels h1, h2 and h3.
  ![feature 'Apply'](images/banner-comments-apply.gif)

## Special use: select fonts individually

You can select from the full list of figlet fonts.

- **"Apply from list"**

Or you can make a short list of favorites and select from that.

- **"Add to favorites"**

- **"Apply from favorites"**

NOTE: Also supports multi-line selections:

![feature 'Multi-cursor'](images/banner-comments-multi-line.gif)

## Extension Settings

This extension contributes the following settings:

- `banner-comments.h1`: "\<figlet font name\>"
- `banner-comments.h2`: "\<figlet font name\>"
- `banner-comments.h3`: "\<figlet font name\>"
- `banner-comments.favorites`: [ \<figlet font name\>, ... ]
- `banner-comments.figlet.horizontalLayout`: "\<default | full | fitted | controlled smushing | universal smushing\>"
- `banner-comments.figlet.verticalLayout`: "\<default | full | fitted | controlled smushing | universal smushing\>"

## Known Issues

## Release Notes

### 1.0.2

- Set default fonts to h1=Univers, h2=Standard, h3=Mini
- Use `const` instead of `let` where possible
- Improved ReadMe

### 1.0.1

- Improved ReadMe

### 1.0.0

**Fixes**:

- Added support for Cypress test files: .spec.js
- Added support for ES6 modules: .mjs
  Forked from version by Daniel-Junior Dube and IMFUZZ

### 0.3.0

**Fixes**:

- Fixed the package.json so the extension keeps working on newer vscode engines
- Code refactoring/simplification

**Features**:

- **Apply from list**: Opens the list of all available figlet fonts and applies the selected one.
- **Add/Remove to favorites**: Choose a font to add to/remove from the list of favorite fonts.
- **Apply from favorites**: Opens the list of favorite fonts and applies the selected one.

**Settings**:

- **banner-comments.figlet.horizontalLayout**: Figlet configuration providing 5 differents layout affecting the width of the font. See more details here: <https://www.npmjs.com/package/figlet#user-content-horizontallayout>
- **banner-comments.figlet.verticalLayout**: Figlet configuration providing 5 differents layout affecting the height of the font. See more details here: <https://www.npmjs.com/package/figlet#verticallayout>
- **banner-comments.favorites**: List of favorited fonts.

### 0.2.0

- Fixed indentation issues where only the first line was indented correctly.
- Converted apply and set font to "apply h*font" and "set h* font" with h1, h2 and h3.
- Code cleaned and removed unused dependencies.

### 0.1.0

- Now detects and uses the file's comment tags to wrap the banner text! (Uses the blockComment to wrap the text or puts lineComments in front of each line)
- Auto-trims whitespaces from the end of each line of the banner.

### 0.0.1

Initial release of the 'Banner comments' extension.

---
