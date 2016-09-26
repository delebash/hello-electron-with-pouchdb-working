You have to build the leveldb module for electron

Instead of trying to build manually (which I never got to work) use electron-rebuild module
https://github.com/electron/electron-rebuild.

Remove "postinstall": "bash postinstall.sh" from you package.json as we are running this manually and won't need it

Commands to run

npm install electron-rebuild --save-dev

then paste into your terminal

./node_modules/.bin/electron-rebuild -w leveldown -p