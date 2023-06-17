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

## Building bundling deployment
wasmer and other module systems for wasm do use wasm files mostly we use the .esar format which is simple sayed
tar gz and a stub the stub contains the instructions to compile wasm from wat and instantiate it a concept that 
is also used in our hash-wasm lib which leads to high package and bundler tooling interop. And is so a better format
to ship wasm. 

Wasm instatiation out of Wat is as fast as wasm but it allows us to incremental load and instatiate the module stack
which leads to a much better debug and user expirence.
