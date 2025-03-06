{
  "name": "temp-server-cli",
  "version": "1.0.0",
  "description": "أداة لإنشاء سيرفر مؤقت بمساحة محددة من القرص",
  "main": "index.js",
  "bin": {
    "temp-server": "./index.js"
  },
  "scripts": {
    "start": "node index.js"
  },
  "keywords": [
    "server",
    "temporary",
    "file-sharing",
    "web-server",
    "cli"
  ],
  "author": "",
  "license": "MIT",
  "dependencies": {
    "boxen": "^5.1.2",
    "chalk": "^4.1.2",
    "clear": "^0.1.0",
    "diskspace": "^2.0.0",
    "express": "^4.17.1",
    "figlet": "^1.5.2",
    "inquirer": "^8.2.0",
    "internal-ip": "^6.2.0",
    "ora": "^5.4.1",
    "qrcode-terminal": "^0.12.0"
  }
}
