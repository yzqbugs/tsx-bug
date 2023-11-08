# tsx-bug


run `yarn buld:cjs`,the script is ` gulp --require @esbuild-kit/cjs-loader`,there is no error.

while run `yarn buld:tsx`,the script is `gulp --require tsx/cjs`,there is a error. 

so i guess tsx causes this error.

```log
√ script to run » build:tsx
[19:28:19] Failed to load external module tsx/cjs
[19:28:19] Error: Cannot find module 'tsx/cjs' from 'E:\WebstormProjects\tsx-bug'
[19:28:19] Failed to load external module ts-node/register
[19:28:19] Error: Cannot find module 'ts-node/register' from 'E:\WebstormProjects\tsx-bug'
[19:28:19] Failed to load external module typescript-node/register
[19:28:19] Error: Cannot find module 'typescript-node/register' from 'E:\WebstormProjects\tsx-bug'
[19:28:19] Failed to load external module typescript-register
[19:28:19] Error: Cannot find module 'typescript-register' from 'E:\WebstormProjects\tsx-bug'
[19:28:19] Failed to load external module typescript-require
[19:28:19] Error: Cannot find module 'typescript-require' from 'E:\WebstormProjects\tsx-bug'
[19:28:19] Failed to load external module sucrase/register/ts
[19:28:19] Error: Cannot find module 'sucrase/register/ts' from 'E:\WebstormProjects\tsx-bug'
[19:28:19] Failed to load external module @babel/register
[19:28:19] Error: Cannot find module '@babel/register' from 'E:\WebstormProjects\tsx-bug'
E:\WebstormProjects\tsx-bug\gulpfile.ts:1
import gulp from "gulp";
^^^^^^

SyntaxError: Cannot use import statement outside a module
    at internalCompileFunction (node:internal/vm:73:18)
    at wrapSafe (node:internal/modules/cjs/loader:1178:20)
    at Module._compile (node:internal/modules/cjs/loader:1220:27)
    at Module._extensions..js (node:internal/modules/cjs/loader:1310:10)
    at Module.load (node:internal/modules/cjs/loader:1119:32)
    at Module._load (node:internal/modules/cjs/loader:960:12)
    at Module.require (node:internal/modules/cjs/loader:1143:19)
    at require (node:internal/modules/cjs/helpers:119:18)
    at requireOrImport (E:\WebstormProjects\tsx-bug\node_modules\gulp-cli\lib\shared\require-or-import.js:19:11)
    at execute (E:\WebstormProjects\tsx-bug\node_modules\gulp-cli\lib\versioned\^4.0.0\index.js:37:3)
```