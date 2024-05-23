Creation d'un app electron
mkdir my-electron-app && cd my-electron-app
npm init
npm install electron --save-dev

Adding a .gitignore
The .gitignore file specifies which files and directories to avoid tracking with Git. 
You should place a copy of GitHub's Node.js gitignore template into 
your project's root folder to avoid committing your project's node_modules folder.
https://github.com/github/gitignore/blob/main/Node.gitignore

*creer un main.js et un index.html*
main de base: 

const { app, BrowserWindow } = require('electron')

const createWindow = () => {
  const win = new BrowserWindow({
    width: 800,
    height: 600
  })

  win.loadFile('index.html')
}

app.whenReady().then(() => {
  createWindow()
})

npm run start
