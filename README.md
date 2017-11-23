Npm pack crash...
=================

See npm/npm#19222

## How To Reproduce

```bash
david@ubuntu:npm-issue-19222$ cd auth/
david@ubuntu:auth$ npm -v
5.5.1
david@ubuntu:auth$ node -v
v9.2.0
david@ubuntu:auth$ npm pack .
(node:10679) UnhandledPromiseRejectionWarning: Unhandled promise rejecti
on (rejection id: 1): Error: ENOENT: no such file or directory, stat '/h
ome/david/Projects/github/dherges/npm-issue-19222/auth/org/auth.es5.js'
(node:10679) [DEP0018] DeprecationWarning: Unhandled promise rejections
are deprecated. In the future, promise rejections that are not handled w
ill terminate the Node.js process with a non-zero exit code.

npm ERR! cb() never called!

npm ERR! This is an error with npm itself. Please report this error at:
npm ERR!     <https://github.com/npm/npm/issues>

npm ERR! A complete log of this run can be found in:
npm ERR!     /home/david/.npm/_logs/2017-11-23T06_39_03_849Z-debug.log
$ cat /home/david/.npm/_logs/2017-11-23T06_39_03_849Z-debug.log
0 info it worked if it ends with ok
1 verbose cli [ '/usr/bin/node', '/usr/bin/npm', 'pack', '.' ]
2 info using npm@5.5.1
3 info using node@v9.2.0
4 verbose npm-session 9003a1f766fb94c7
5 silly pacote directory manifest for undefined@file: fetched in 10ms
6 info lifecycle @org/auth@2.0.0-dev.21~prepublish: @org/auth@2.0.0-dev.
21
7 info lifecycle @org/auth@2.0.0-dev.21~prepare: @org/auth@2.0.0-dev.21
8 info lifecycle @org/auth@2.0.0-dev.21~prepack: @org/auth@2.0.0-dev.21
9 error cb() never called!
10 error This is an error with npm itself. Please report this error at:
11 error <https://github.com/npm/npm/issues>
```
