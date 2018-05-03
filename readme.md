# Markdown Builder

This is a simple Markdown builder.

## Getting Started

### Required

[Node](https://nodejs.org/en/)

### Install

Clone this Repo

```
$ git clone https://github.com/reactivepixel/ColabCode.git
```

## Deploy

Go to the ColabCode Folder

```
$ cd ColabCode
```

checkout bhess-markdown

```
$ git checkout bhess-markdown
```

Run the app

```
$ npm start
```

## Functionality

Edit dataset in [markdown.js](/markdown.js)

```js
const dataSet = [
  { type: 'title', text: '## Headers H1-H6'},
  { type: 'h1', text: '# H1 Header'},
  { type: 'h2', text: '## H2 Header'},
  { type: 'h3', text: '### H3 Header'},
  { type: 'h4', text: '#### H4 Header'},
  { type: 'h5', text: '##### H5 Header'},
  { type: 'h6', text: '###### H6 Header'},
  { type: 'title', text: '## Lists'},
  { type: 'text', text: 'This is a ordered list'},
  { type: 'list', text: '1. One\n2. Two\n3. Three\n4. Four\n5. Five'},
  { type: 'text', text: 'This is a Unordered sub-list'},
  { type: 'list', text: '* One\n  * Two\n    * Three\n* four\n  * Six'},
  { type: 'text', text: 'This is a unordered list'},
  { type: 'list', text: '* Five\n* Four\n* Three\n* Two\n* One'},
  { type: 'title', text: '## Links'},
  { type: 'link', link: { text: 'Link One Google', url: 'google.com'} },
  { type: 'link', link: { text: 'Link Two Yahoo', url: 'yahoo.com'} },
  { type: 'link', link: { text: 'Link Three Reddit', url: 'reddit.com'} },
  { type: 'title', text: '## Code Blocks'},
  { type: 'code_js', code: 'js\n// js\nvar answer = 6 * 7;\nconsole.log(answer);\n'},
  { type: 'code_css', code: 'css\n/* css */\nh2 {\n  font-family: sans-serif;\n  color: #000;\n}\n'},
  { type: 'code_md', code: 'md\n<!-- md -->\n# H3 Title\n\nThis is a code block filler text number Three.\n'},
];
```

To edit where the markdown is created at change "./temp/readme.md" at the bottom of [markdown.js](/markdown.js)

```js
fs.writeFile("./temp/readme.md", builder(dataset), function(err)
```
