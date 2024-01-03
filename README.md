# Use Last Visit Date (publish to npm)

[![npm version](https://badge.fury.io/js/use-last-visit-date.svg)](https://badge.fury.io/js/use-last-visit-date)
[![Build Status](https://travis-ci.com/tylim88/use-last-visit-date.svg?branch=master)](https://travis-ci.com/tylim88/use-last-visit-date)
[![Coverage Status](https://coveralls.io/repos/github/tylim88/use-last-visit-date/badge.svg?branch=master)](https://coveralls.io/github/tylim88/use-last-visit-date?branch=master)

## Install

```bash
npm install --save use-last-visit-date
```

## Usage

```jsx
import React, { Component } from 'react'

import useLastVisitDate from 'use-last-visit-date'

const LastVisitDate = () => {
  const lastVisitDate = useLastVisitDate({
    date: new Date(),
    key: 'last-visit-date',
    ttl: 60 * 60 * 24 * 7 * 1000, // 7 days
  })

  return <div>{lastVisitDate}</div>
}
```

## API

### `useLastVisitDate(options)`

#### `options`

##### `date`

Type: `Date`<br>
Default: `new Date()`

The date to be used when the last visit date is not found in the storage.

##### `key`

Type: `string`<br>
Default: `last-visit-date`

The key to be used when storing the last visit date in the storage.

##### `ttl`

Type: `number`<br>
Default: `Infinity`

The time to live of the last visit date in milliseconds. The last visit date will be cleared from the storage when the time to live is reached.

## License

MIT © [tylim88](