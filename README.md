# Dillinger
## _The Last Markdown Editor, Ever_

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Dillinger is a cloud-enabled, mobile-ready, offline-storage compatible,
AngularJS-powered HTML5 Markdown editor.

- Type some Markdown on the left
- See HTML in the right
- ✨Magic ✨

## Features

- Import a HTML file and watch it magically convert to Markdown
- Drag and drop images (requires your Dropbox account be linked)
- Import and save files from GitHub, Dropbox, Google Drive and One Drive
- Drag and drop markdown and HTML files into Dillinger
- Export documents as Markdown, HTML and PDF

Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.
As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Tech

Dillinger uses a number of open source projects to work properly:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] - awesome web-based text editor
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Gulp] - the streaming build system
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter
- [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
```

## Docker

Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

## License

MIT

## Technology stack

| Technology | Short description | Full description |
| ------ | ------ | ------ |
| [React][React] |  Free and open-source front-end JavaScript library for building user interfaces or UI components | [More details](#React) |
| [Redux][Redux] | Open-source JavaScript library for managing and centralizing application state | [More details](#Redux) |
| [TypeScript][TypeScript] | Strongly typed programming language which builds on JavaScript giving you better tooling at any scale. | [More details](#TypeScript) |
| [Chakra-UI][Chakra-UI] | Simple, modular and accessible component library that gives you the building blocks you need to build your React applications | [More details](#Chakra-UI) |
| [Webpack][Webpack] | Static module bundler for modern JavaScript applications | [More details](#Webpack) |
| [WebSockets][WebSockets] | [plugins/onedrive/README.md][PlOd] | [More details](#WebSockets) |
| [Husky][Husky] | [plugins/medium/README.md][PlMe] | [More details](#Husky)
| [Eslint][Eslint] | [plugins/onedrive/README.md][PlOd] | [More details](#Eslint)
| [Prettier][Prettier] | [plugins/googleanalytics/README.md][PlGa] | [More details](#Prettier)
| [Dompurify][Dompurify] | [plugins/googleanalytics/README.md][PlGa] | [More details](#Dompurify)
| [Jest][Jest] | [plugins/googleanalytics/README.md][PlGa] | [More details](#Jest)
| [Framer Motion][Framer Motion] | [plugins/googleanalytics/README.md][PlGa] | [More details](#Framer-Motion)
| [React-beautiful-dnd][React-beautiful-dnd] | [plugins/googleanalytics/README.md][PlGa] |[More details](#React-beautiful-dnd)
| [React-rnd][React-rnd] | [plugins/googleanalytics/README.md][PlGa] | [More details](#React-rnd)
| [React Slick][React-slick] | [plugins/googleanalytics/README.md][PlGa] | [More details](#React-slick)
| [Slick-carousel][Slick-carousel] | [plugins/googleanalytics/README.md][PlGa] | [More details](#Slick-carousel)
| [Web Vitals][Web Vitals] | [plugins/googleanalytics/README.md][PlGa] | [More details](#Web-Vitals)
| [SheetJS (xlsx)][SheetJS] | [plugins/googleanalytics/README.md][PlGa] | [More details](#SheetJSxlsx)


### React
### Redux
### TypeScript
### Chakra-UI
### Webpack
### The WebSocket API (WebSockets)
### Husky
### Eslint
### Prettier
### Dompurify
### Jest
### Framer Motion
### React-beautiful-dnd
### React-rnd
### React Slick
### Slick-carousel
### Web Vitals
### SheetJS(xlsx)


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [React]: <https://reactjs.org/>
   [Redux]: <https://redux.js.org/>
   [TypeScript]: <https://www.typescriptlang.org/>
   [Chakra-UI]: <https://chakra-ui.com/>
   [Webpack]: <https://webpack.js.org/>
   [WebSockets]: <https://www.npmjs.com/package/ws>
   [Husky]: <https://typicode.github.io/husky/#/>
   [Eslint]: <https://www.npmjs.com/package/eslint>
   [Prettier]: <https://prettier.io/>
   [Dompurify]: <https://www.npmjs.com/package/dompurify>
   [Jest]: <https://jestjs.io/>
   [Framer Motion]: <https://www.npmjs.com/package/framer-motion>
   [React-beautiful-dnd]: <https://www.npmjs.com/package/react-beautiful-dnd>
   [React-rnd]: <https://www.npmjs.com/package/react-rnd>
   [React-slick]: <https://react-slick.neostack.com/>
   [Slick-carousel]: <https://www.npmjs.com/package/slick-carousel>
   [Web Vitals]: <https://web.dev/vitals/>
   [SheetJS]: <https://sheetjs.com/>
