Npm pack crash...
=================

See npm/npm#19222

## How To Reproduce

```bash
david@ubuntu:npm-issue-19222$ cd auth/
david@ubuntu:auth$ npm -v
5.5.1

┌─────────────────────────────────────────────────────────┐
│                 npm update check failed                 │
│           Try running with sudo or get access           │
│          to the local update config store via           │
│ sudo chown -R $USER:$(id -gn $USER) /home/david/.config │
└─────────────────────────────────────────────────────────┘
david@ubuntu:auth$ node -vv9.2.0
david@ubuntu:auth$ npm pack .
(node:10679) UnhandledPromiseRejectionWarning: Unhandled promise rejecti
on (rejection id: 1): Error: ENOENT: no such file or directory, stat '/h
ome/david/Projects/github/dherges/npm-issue-19222/auth/org/auth.es5.js'
(node:10679) [DEP0018] DeprecationWarning: Unhandled promise rejections
are deprecated. In the future, promise rejections that are not handled w
ill terminate the Node.js process with a non-zero exit code.
```
