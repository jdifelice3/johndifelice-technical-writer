# Installation

## Git Repository
Use one of the following GitHub remote URLs to clone the ZohoDataExplorer repository. You can clone two types of URL addresses:

|  Type | URL |
|----------|----------|
| HTTPS  | https://github.com/jdifelice3/ZohoDataExplorer.git  |
| SSH   | git@github.com:jdifelice3/ZohoDataExplorer.git  |

If you want to use HTTPS, the git command is:
```bash
clone https://github.com/jdifelice3/ZohoDataExplorer.git
```

## Node.js & Node Package Manager (npm)
Once you have cloned the repository, use **Node Package Manager** (npm) to install
application dependencies. The following table shows the versions of Node.js and npm you should use.
Some of the components in ZohoDataExplorer are picky about the version of Node.js installed, notably 
**AG-Grid**.

|          | Version |
|----------|----------|
| node.js  | v22.14.0  |
| npm      | 11.4.2  |

If you do not have npm installed, install it by following the instructions on the nodejs.org site for your operating system. Installing Node.js will also install npm.

<a href="https://nodejs.org/en/download/">Install Node.js</a>

Once Node.js is installed, open a bash or VS Code terminal and change the directory to where you cloned the ZohoDataExplorer source code.

Run the following command:
    ```bash
    npm install
    ```

This will download and install all dependencies in the package.json file (into the node_modules folder). It contains a json object that contains all packages, including their version numbers.

#### package.json
```json
{
  "name": "client",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite --config vite.config.js --mode=development",
    "build": "vite build --config vite.config.prod.js --mode=production",
    "lint": "eslint .",
    "preview": "vite preview",
    "testvite": "npx vite --version",
    "start": "node server.js"
  },
  "dependencies": {
    "ag-grid-community": "^28.2.1",
    "ag-grid-enterprise": "^28.2.1",
    "ag-grid-react": "^28.2.1",
    "axios": "^1.8.4",
    "body-parser": "^1.19.0",
    "express": "^4.17.1",
    "qs": "^6.14.0",
    "react": "^18.3.1",
    "react-dom": "^18.3.1",
    "react-querybuilder": "^8.5.0",
    "react-router-dom": "^7.5.0",
    "react-toastify": "^11.0.5",
    "sass": "^1.86.1"
  },
  "devDependencies": {
    "@eslint/js": "^9.21.0",
    "@types/react": "^19.0.10",
    "@types/react-dom": "^19.0.4",
    "@vitejs/plugin-react": "^4.3.4",
    "eslint": "^9.21.0",
    "eslint-plugin-react-hooks": "^5.1.0",
    "eslint-plugin-react-refresh": "^0.4.19",
    "globals": "^15.15.0",
    "nodemon": "^2.0.4",
    "sass-loader": "^8.0.2",
    "style-loader": "^1.3.0",
    "vite": "^6.3.4"
  },
  "packageManager": "pnpm@10.14.0+sha512.ad27a79641b49c3e481a16a805baa71817a04bbe06a38d17e60e2eaee83f6a146c6a688125f5792e48dd5ba30e7da52a5cda4c3992b9ccf333f9ce223af84748"
}

```

If you ever have problems with dependencies, you can simply delete the `node_modules` folder and rerun `npm install`.

Note that there are two elements with dependency information: `"dependencies"` and `"devDependencies"`. Packages in the 
`"dependencies"` element are those required to run the app. The ones in the `"devDependencies"` are only required for 
development and will not be deployed to higher environments like Production. `"devDepencies"` are install using the -D option, *e.g.*:
```bash
npm install -D eslint
```
<br>
# Vite Build Tool

The ZohoDataExplorer development environment uses Vite instead of the more traditional package bundler, Webpack. You can see it
in the "scripts" element of the package.json file:
```json
"dev": "vite --config vite.config.js --mode=development",
```
The command `npm run dev` runs Vite.

Vite made full-stack debugging much easier, which is a big reason it was chosen over Webpack.

Vite requires a config file, `vite.config.js`, which was downloaded when the project was cloned.

At the top of the project folder structure is a folder named `.vscode`. Within this folder are two files:

`launch.json`
:   a configuration file used to define how the debugger should run an application. It specifies settings such as the program to debug, environment variables, and other parameters needed for debugging sessions.  

`tasks.json`
:   a configuration file used to define and manage tasks that automate various operations, such as building, testing, or running scripts. It allows users to specify commands, arguments, and other settings for executing tasks directly from the editor.

These files configure the VS Code debugger.