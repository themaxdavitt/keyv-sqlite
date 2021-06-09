# @keyv/sqlite [<img width="100" align="right" src="https://rawgit.com/lukechilds/keyv/master/media/logo.svg" alt="keyv">](https://github.com/lukechilds/keyv)

> SQLite storage adapter for Keyv

[![Build Status](https://github.com/themaxdavitt/keyv-sqlite/actions/workflows/node.js.yml/badge.svg)](https://github.com/themaxdavitt/keyv-sqlite/actions/workflows/node.js.yml)

Fork of [`@keyv/sqlite`](https://github.com/lukechilds/keyv-sqlite), a SQLite storage adapter for [Keyv](https://github.com/lukechilds/keyv).

## Install

```shell
npm install --save keyv themaxdavitt/keyv-sqlite
```

## Usage

```js
const Keyv = require('keyv');

const keyv = new Keyv('sqlite://path/to/database.sqlite');
keyv.on('error', handleConnectionError);
```

You can specify the `table` and [`busyTimeout`](https://sqlite.org/c3ref/busy_timeout.html) option.

e.g:

```js
const keyv = new Keyv('sqlite://path/to/database.sqlite', {
	table: 'cache',
	busyTimeout: 10000,
});
```

## License

MIT © Luke Childs
