Run

```
docker-compose up
```

Which results in:

```
Building app
[+] Building 59.3s (8/9)
 => [internal] load build definition from Dockerfile                                                                                                                                                 0.0s
 => => transferring dockerfile: 36B                                                                                                                                                                  0.0s
 => [internal] load .dockerignore                                                                                                                                                                    0.0s
 => => transferring context: 34B                                                                                                                                                                     0.0s
 => [internal] load metadata for docker.io/library/node:16-alpine                                                                                                                                    0.0s
 => [1/5] FROM docker.io/library/node:16-alpine                                                                                                                                                      0.0s
 => [internal] load build context                                                                                                                                                                    0.0s
 => => transferring context: 6.14kB                                                                                                                                                                  0.0s
 => CACHED [2/5] WORKDIR /app                                                                                                                                                                        0.0s
 => CACHED [3/5] COPY package.json yarn.lock ./                                                                                                                                                      0.0s
 => ERROR [4/5] RUN yarn                                                                                                                                                                            59.2s
------
 > [4/5] RUN yarn:
#8 0.356 yarn install v1.22.19
#8 0.500 [1/5] Validating package.json...
#8 0.504 [2/5] Resolving packages...
#8 1.119 [3/5] Fetching packages...
#8 37.85 [4/5] Linking dependencies...
#8 37.86 warning " > @keystone-6/auth@1.0.2" has unmet peer dependency "react@^17.0.2".
#8 37.86 warning "@keystone-6/auth > @keystone-ui/core@4.0.0" has unmet peer dependency "react@^17.0.2".
#8 37.86 warning "@keystone-6/auth > @keystone-ui/core@4.0.0" has unmet peer dependency "react-dom@^17.0.2".
#8 37.87 warning "@keystone-6/auth > @keystone-ui/core > @emotion/react@11.9.3" has unmet peer dependency "react@>=16.8.0".
#8 37.87 warning "@keystone-6/auth > @keystone-ui/fields > react-select@5.3.2" has unmet peer dependency "react-dom@^16.8.0 || ^17.0.0 || ^18.0.0".
#8 37.87 warning "@keystone-6/auth > @keystone-ui/core > @emotion/react > @emotion/babel-plugin@11.9.2" has unmet peer dependency "@babel/core@^7.0.0".
#8 37.87 warning "@keystone-6/auth > @keystone-ui/fields > @keystone-ui/popover > react-popper@2.3.0" has unmet peer dependency "react-dom@^16.8.0 || ^17 || ^18".
#8 37.87 warning "@keystone-6/auth > @keystone-ui/fields > react-day-picker > @reach/auto-id@0.16.0" has unmet peer dependency "react-dom@^16.8.0 || 17.x".
#8 37.87 warning "@keystone-6/auth > @keystone-ui/core > @emotion/react > @emotion/babel-plugin > @babel/plugin-syntax-jsx@7.17.12" has unmet peer dependency "@babel/core@^7.0.0-0".
#8 37.87 warning "@keystone-6/auth > @keystone-ui/fields > react-day-picker > @reach/auto-id > @reach/utils@0.16.0" has unmet peer dependency "react-dom@^16.8.0 || 17.x".
#8 37.87 warning "@keystone-6/core > @prisma/migrate@3.12.0" has unmet peer dependency "@prisma/generator-helper@*".
#8 37.88 warning "@keystone-6/fields-document > slate-react@0.69.0" has unmet peer dependency "react-dom@>=16.8.0".
#8 51.02 [5/5] Building fresh packages...
#8 57.40 $ keystone postinstall
#8 58.66 Error: Cannot find module '/app/keystone'
#8 58.66 Require stack:
#8 58.66 - /app/node_modules/@keystone-6/core/dist/requireSource-ff4e29c3.cjs.dev.js
#8 58.66 - /app/node_modules/@keystone-6/core/scripts/dist/keystone-6-core-scripts.cjs.dev.js
#8 58.66 - /app/node_modules/@keystone-6/core/scripts/dist/keystone-6-core-scripts.cjs.js
#8 58.66 - /app/node_modules/@keystone-6/core/bin/cli.js
#8 58.66     at Function.Module._resolveFilename (node:internal/modules/cjs/loader:933:15)
#8 58.66     at Function.Module._load (node:internal/modules/cjs/loader:778:27)
#8 58.66     at Module.require (node:internal/modules/cjs/loader:1005:19)
#8 58.66     at require (node:internal/modules/cjs/helpers:102:18)
#8 58.66     at Object.requireSource (/app/node_modules/@keystone-6/core/dist/requireSource-ff4e29c3.cjs.dev.js:93:18)
#8 58.66     at postinstall (/app/node_modules/@keystone-6/core/scripts/dist/keystone-6-core-scripts.cjs.dev.js:610:54)
#8 58.66     at cli (/app/node_modules/@keystone-6/core/scripts/dist/keystone-6-core-scripts.cjs.dev.js:671:12)
#8 58.66     at Object.<anonymous> (/app/node_modules/@keystone-6/core/scripts/dist/keystone-6-core-scripts.cjs.dev.js:683:1)
#8 58.66     at Module._compile (node:internal/modules/cjs/loader:1105:14)
#8 58.66     at Object.Module._extensions..js (node:internal/modules/cjs/loader:1159:10) {
#8 58.66   code: 'MODULE_NOT_FOUND',
#8 58.66   requireStack: [
#8 58.66     '/app/node_modules/@keystone-6/core/dist/requireSource-ff4e29c3.cjs.dev.js',
#8 58.66     '/app/node_modules/@keystone-6/core/scripts/dist/keystone-6-core-scripts.cjs.dev.js',
#8 58.66     '/app/node_modules/@keystone-6/core/scripts/dist/keystone-6-core-scripts.cjs.js',
#8 58.66     '/app/node_modules/@keystone-6/core/bin/cli.js'
#8 58.66   ]
#8 58.66 }
#8 58.68 error Command failed with exit code 1.
#8 58.68 info Visit https://yarnpkg.com/en/docs/cli/install for documentation about this command.
------
executor failed running [/bin/sh -c yarn]: exit code: 1
ERROR: Service 'app' failed to build : Build failed
```
