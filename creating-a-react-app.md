---
icon: react
---

# Creating a React App

#### Step 1: Download Node.js from [here](https://nodejs.org/en/download/current)

```bash
# Download and install Homebrew
curl -o- https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh | bash

# Download and install Node.js:
brew install node@23

# Verify the Node.js version:
node -v # Should print "v23.6.0".


# Verify npm version:
npm -v # Should print "10.9.2".

```

* Verify the installation as below.

![](https://i.imgur.com/by9AYBU.jpeg)

#### Step 2: Create the React app

To create a react application, use the following command

```bash
npx create-react-app app-name
```

***

**Common Errors That You Might Encounter (first time users)**

1. **Permission Issues**

> \[!note] Encountered an error:
>
> ```bash
> ❯ npx create-react-app react-tutorial
> Need to install the following packages: create-react-app@5.0.1 Ok to proceed? (y) 
> npm error code EACCES
> npm error syscall mkdir
> npm error path /Users/rajendran/.npm/_cacache/index-v5/b0/05
> npm error errno EACCES npm error
> npm error Your cache folder contains root-owned files, due to a bug in npm error previous versions of npm which has since been addressed. npm error npm error To permanently fix this problem, please run: 
> npm error sudo chown -R 501:20 "/Users/rajendran/.npm" npm error A complete log of this run can be found in: /Users/rajendran/.npm/_logs/2025-01-16T13_31_04_443Z-debug-0.log
> ```
>
> The error occurs because some of the files in your npm cache folder (`/Users/rajendran/.npm`) are owned by `root`, which causes permission issues when you try to run npm commands.

> \[!solution] To fix it, Run the following command to change the ownership of the npm cache folder to your user account: `sudo chown -R $(whoami):$(id -gn) /Users/rajendran/.npm` This ensures you have proper permissions to access and modify the npm cache.

***

2. **Dependency Conflicts**

To resolve the dependency conflicts,

Why is this happening? Resolve it.

```bash

❯ npx create-react-app react-tutorial
Creating a new React app in /Users/rajendran/Desktop/ReactJS/react-tutorial.
Installing packages. This might take a couple of minutes.
Installing react, react-dom, and react-scripts with cra-template...
added 1323 packages in 39s
267 packages are looking for funding
  run `npm fund` for details
Installing template dependencies using npm...
npm error code ERESOLVE
npm error ERESOLVE unable to resolve dependency tree
npm error
npm error While resolving: react-tutorial@0.1.0
npm error Found: react@19.0.0
npm error node_modules/react
npm error   react@"^19.0.0" from the root project
npm error
npm error Could not resolve dependency:
npm error peer react@"^18.0.0" from @testing-library/react@13.4.0
npm error node_modules/@testing-library/react
npm error   @testing-library/react@"^13.0.0" from the root project
npm error
npm error Fix the upstream dependency conflict, or retry
npm error this command with --force or --legacy-peer-deps
npm error to accept an incorrect (and potentially broken) dependency resolution.
npm error
npm error
npm error For a full report see:
npm error /Users/rajendran/.npm/_logs/2025-01-16T13_42_04_366Z-eresolve-report.txt
npm error A complete log of this run can be found in: /Users/rajendran/.npm/_logs/2025-01-16T13_42_04_366Z-debug-0.log
`npm install --no-audit --save @testing-library/jest-dom@^5.14.1 @testing-library/react@^13.0.0 @testing-library/user-event@^13.2.1 web-vitals@^2.1.0` failed
~/Desktop/ReactJS master* 43s ❯                                                               07:12:05 PM
```

![](https://i.imgur.com/EUSIt1Z.png)

use the following commands in such case:

```shell

# First remove the current directory
rm -rf react-tutorial

# Create a new React project using Vite
npm create vite@latest react-tutorial -- --template react

# Navigate into the project directory
cd react-tutorial

# Install dependencies
npm install

# Start the development server
npm run dev

```

***

#### Running a react application

To run a react application, use the following commands.

```bash
npm start
```

(or)

```bash
npm run dev # if you're using along with vite
```

![](https://i.imgur.com/70EGbI6.png)

***

#### Project Structure

![](https://i.imgur.com/8NM1vfN.png)

```bash
.
└── react-tutorial
    ├── README.md
    ├── eslint.config.js
    ├── index.html
    ├── node_modules
    ├── package-lock.json
    ├── package.json
    ├── public
    ├── src
    └── vite.config.js

5 directories, 6 files
```

**Files in the Root**

* **`README.md`**
  * A markdown file that typically contains instructions or information about the project. It may describe how to set up, run, or contribute to the project.
* **`eslint.config.js`**
  * A configuration file for ESLint, a tool used to analyze and fix issues in JavaScript/React code. It defines coding standards and rules for the project.
* **`index.html`**
  * The main HTML file for the application. It's the entry point for the browser when the app runs. Typically, a single `<div>` (e.g., `id="root"`) is defined here for React to render components.
* **`package-lock.json`**
  * A file automatically generated by npm. It locks the exact versions of dependencies installed to ensure consistent behavior across environments.
* **`package.json`**
  * A configuration file for the project. It lists dependencies, scripts, project metadata, and other configurations. It's central to any Node.js project.
* **`vite.config.js`**
  * A configuration file for Vite, a fast modern bundler and build tool often used in modern React projects. It allows customization of how the app is built and served.

***

**Directories in the Root**

* **`node_modules/`**
  * A directory where npm stores all the project dependencies. These dependencies are installed based on the `package.json` file.
* **`public/`**
  * Contains static files that won't be processed by the bundler. Files here (e.g., images, fonts) are directly served as-is. Commonly includes:
    * `index.html`: The root HTML file for the app.
* **`src/`**
  * The main directory for your application's source code. Typically includes:
    * `main.jsx` or `index.js`: The main entry point for the React application.
    * Components, styles, and other assets.

***

> JSX - JavaScript XML
