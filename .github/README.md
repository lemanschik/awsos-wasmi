## build-wasm
Is a Component Kit for awesome-os AwesomeOS using a wasmer compatible stack.

## Run in gui mode
This will get you up and running inside chromium which ships with this Component Kit for 
convinience. 
```sh
npm install
npm start
```

## if you do not got nodejs installed

```sh
git clone github.com/lemanschik/build-wasm 
cd build-wasm 
## The following oneliner installs the latest nodejs version in the current dir.
(MIRROR=https://nodejs.org/dist/latest; VERSION=; DIR=.; SYSTEM=linux-x64; FILENAME=$(curl -s -L ${MIRROR}${VERSION} | grep 'tar.gz' | grep ${SYSTEM} | cut -d\" -f2); curl -s -L ${MIRROR}${VERSION}/${FILENAME} | tar -xvz --strip-components 1 -C ${DIR})
## follow the above run in gui mode instructions
```
