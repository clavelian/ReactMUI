Installation

Install Material UI, the world's most popular React UI framework.
Default installation

Run one of the following commands to add Material UI to your project:

npm install @mui/material @emotion/react @emotion/styled

Peer dependencies

Please note that react and react-dom are peer dependencies, meaning you should ensure they are installed before installing Material UI.

"peerDependencies": {
  "react": "^17.0.0 || ^18.0.0",
  "react-dom": "^17.0.0 || ^18.0.0"
},

With styled-components

Material UI uses Emotion as its default styling engine. If you want to use styled-components instead, run one of the following commands:

npm install @mui/material @mui/styled-engine-sc styled-components

Next, follow the styled-components how-to guide to properly configure your bundler to support @mui/styled-engine-sc.

As of late 2021, styled-components is not compatible with server-rendered Material UI projects. This is because babel-plugin-styled-components isn't able to work with the styled() utility inside @mui packages. See this GitHub issue for more details.

We strongly recommend using Emotion for SSR projects.
Roboto font

Material UI uses the Roboto font by default. Add it to your project via Fontsource, or with the Google Fonts CDN.

npm install @fontsource/roboto

Then you can import it in your entry point like this:

import '@fontsource/roboto/300.css';
import '@fontsource/roboto/400.css';
import '@fontsource/roboto/500.css';
import '@fontsource/roboto/700.css';

Fontsource can be configured to load specific subsets, weights and styles. Material UI's default typography configuration relies only on the 300, 400, 500, and 700 font weights.
Google Web Fonts

To install Roboto through the Google Web Fonts CDN, add the following code inside your project's tag:

<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  rel="stylesheet"
  href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap"
/>

Icons

To use the font Icon component or the prebuilt SVG Material Icons (such as those found in the icon demos), you must first install the Material Icons font. You can do so with npm, or with the Google Web Fonts CDN.

npm install @mui/icons-material

Google Web Fonts

To install the Material Icons font in your project using the Google Web Fonts CDN, add the following code snippet inside your project's <head /> tag:

To use the font Icon component, you must first add the Material Icons font. Here are some instructions on how to do so. For instance, via Google Web Fonts:

<link
  rel="stylesheet"
  href="https://fonts.googleapis.com/icon?family=Material+Icons"
/>

CDN

You can start using Material UI right away with minimal front-end infrastructure by installing it via CDN, which is a great option for rapid prototyping. Follow this CDN example to get started.

We do not recommend using this approach in production. It requires the client to download the entire library—regardless of which components are actually used—which negatively impacts performance and bandwidth utilization.

Two Universal Module Definition (UMD) files are provided:

    one for development: https://unpkg.com/@mui/material@latest/umd/material-ui.development.js
    one for production: https://unpkg.com/@mui/material@latest/umd/material-ui.production.min.js

The UMD links use the latest tag to point to the latest version of the library. This pointer is unstable and subject to change as we release new versions. You should consider pointing to a specific version, such as v5.0.0.
