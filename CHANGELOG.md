## [1.0.2](https://github.com/peers/peerjs-server/compare/v1.0.1...v1.0.2) (2023-12-05)


### Bug Fixes

* **deps:** update dependency @types/express to v4.17.18 ([f4bcc16](https://github.com/peers/peerjs-server/commit/f4bcc1651598f349626b67099c7a39b01b417f6c))
* **deps:** update dependency @types/express to v4.17.19 ([ebec5b0](https://github.com/peers/peerjs-server/commit/ebec5b07aa29e951058d64a5c98efa238ce0069a))
* **deps:** update dependency @types/express to v4.17.20 ([a6c01fd](https://github.com/peers/peerjs-server/commit/a6c01fd47bfd89fa74a716650a44643612a659aa))
* **deps:** update dependency @types/express to v4.17.21 ([80df87f](https://github.com/peers/peerjs-server/commit/80df87f3da63624e6c7107453f3789e76d688798))
* reduce unnecessary timeouts ([638af56](https://github.com/peers/peerjs-server/commit/638af56f679881194f60b29ae7f7bb7b5756662a)), closes [#431](https://github.com/peers/peerjs-server/issues/431)

## [1.0.1](https://github.com/peers/peerjs-server/compare/v1.0.0...v1.0.1) (2023-08-25)


### Bug Fixes

* **deps:** update dependency node-fetch to v3.3.1 ([2275ce3](https://github.com/peers/peerjs-server/commit/2275ce35eb3c44e0a22fd4a4e0d2dca66ebd1219))
* **deps:** update dependency node-fetch to v3.3.2 ([05a1833](https://github.com/peers/peerjs-server/commit/05a1833363b0592ee7941dd295c3ca9ac64d9d04))
* **deps:** update dependency yargs to v17.7.2 ([23b4e47](https://github.com/peers/peerjs-server/commit/23b4e47fb32a773d48027b0cdd0c10be7fad27cb))
* remove confusing version number ([f6314df](https://github.com/peers/peerjs-server/commit/f6314df40c37add66deac5dd8487ad54e4814237))


### Reverts

* Revert "build: deploy to fly.io" ([c3de627](https://github.com/peers/peerjs-server/commit/c3de627fad9ddd22230793fb3f6757d402a052a5))
* Revert "chore: Configure Mend Bolt for GitHub (#349)" ([fd00aef](https://github.com/peers/peerjs-server/commit/fd00aef9809dd60bb7e36b2fdc58e47a1e4b036c)), closes [#349](https://github.com/peers/peerjs-server/issues/349)

# [1.0.0](https://github.com/peers/peerjs-server/compare/v0.6.1...v1.0.0) (2023-03-07)


### Bug Fixes

* **deps:** update dependency ws to v8 ([1ecc94b](https://github.com/peers/peerjs-server/commit/1ecc94b887d23ac59b3622a2fefc9fdab24f170f))
* import from ESM only environments ([476299e](https://github.com/peers/peerjs-server/commit/476299ed08f73e41d175d61b4281736bf8df1ea6))
* more accurate types ([68f973a](https://github.com/peers/peerjs-server/commit/68f973afb44a1f71c9fd9a644602312d8ceda5cf)), closes [#182](https://github.com/peers/peerjs-server/issues/182)
* **npm audit:** Updates all dependencies that cause `npm audit` to issue a warning ([1aaafbc](https://github.com/peers/peerjs-server/commit/1aaafbc4504224f36287fd721f6edbc27a5b9eaa)), closes [#287](https://github.com/peers/peerjs-server/issues/287)
* the server could crash if a client sends invalid frames ([29394de](https://github.com/peers/peerjs-server/commit/29394dea5e1303cdf07337d39c2c93249fdd41db))


### Features

* drop Node {10,11,12,13} support ([b70ed79](https://github.com/peers/peerjs-server/commit/b70ed79d9a239593d128ea2914eea0c2107b03b2))
* ESM support ([2b73b5c](https://github.com/peers/peerjs-server/commit/2b73b5c97de4a366d6635719891b65d5f9878628))
* remove deprecated XHR fallback ([d900145](https://github.com/peers/peerjs-server/commit/d90014590160faf1d489a18ea489c28c43cd4690))
* set the PEERSERVER_PATH with an environment variable ([084fb8a](https://github.com/peers/peerjs-server/commit/084fb8a4bddfcb153a4cb861ba700c8352cd4b35)), closes [#213](https://github.com/peers/peerjs-server/issues/213)
* set the PORT with an environment variable ([68a3398](https://github.com/peers/peerjs-server/commit/68a3398f54b0f45bfe8c501c627f531980823ec1)), closes [#213](https://github.com/peers/peerjs-server/issues/213)
* specify cors options via cli or js ([05f12cd](https://github.com/peers/peerjs-server/commit/05f12cdc562b1a5eb9481f5116da7c001105793a)), closes [#196](https://github.com/peers/peerjs-server/issues/196) [#221](https://github.com/peers/peerjs-server/issues/221)


### Performance Improvements

* use the builtin UUID generator for Peer ids instead of the `uuid` module ([5d882dd](https://github.com/peers/peerjs-server/commit/5d882dd0c6af9bed8602e0507fdf5c1d284be075))


### BREAKING CHANGES

* Requires PeerJS >= 1.0
* Node >= 14 required

14 is the oldest currently supported version. See https://github.com/nodejs/release#release-schedule

# PeerServer Changelog

### vNEXT


### 0.6.1

* New: PeerJS Server in Docker capture ^C signal and terminate gracefully. #205
* Fix: SSL options in default config. #230

### 0.6.0

* New: `host` option (`--host`, `-H`). #197 Thanks @millette
* Fix: Allows SNICallback instead of hardcoded key/cert. #225 Thanks @brunobg
* Change: Upgrade TypeScript version to 4.1.2.

### 0.5.3

* PeerServer uses yargs instead of an outdated minimist. #190 Thanks @hobindar

### 0.5.2

* Fix: WebSocket server doesn't work  on Windows #170 Thanks @lqdchrm

### 0.5.1

* Fix: WebSocket server doesn't work  when use non "/" mount path with ExpressPeerServer #132

### 0.5.0

* Fix: http api not working - #163 Thanks riscoss63

* Change: use "/" instead of "/myapp" as a default value for config's `path` option

* New: typescript declaration file

* Update deps:
```diff
-  "cors": "2.8.4",
+  "cors": "^2.8.5",
-  "uuid": "3.3.3",
+  "uuid": "^3.4.0",
-  "ws": "7.1.2",
+  "ws": "^7.2.3"
```

### 0.4.0

* New: Allow passing in custom client ID generation function - #157 Thanks @ajmar

### 0.3.2

* Fixed: fix main field in package.json

### 0.3.1

* Fixed: no expire message in some cases

### 0.3.0

* Convert project to TypeScript 3.7.3.
* Use UUID when generate client id - #152
* Refactoring (add ESLint, split code into small unit) Thanks to @d07RiV @zhou-yg
* Update deps.

### 0.2.6

* Ensure 16 character IDs.

### 0.2.5

* Takes a `path` option, which the peer server will append PeerJS routes to.
* Add support for configurable server IP address.

### 0.2.1

* Added test suite.
* Locked node dependency for restify.
