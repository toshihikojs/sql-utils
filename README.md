# @toshihiko/sql-utils

[![Build Status](https://github.com/toshihikojs/sql-utils/actions/workflows/node.js.yml/badge.svg)](https://github.com/toshihikojs/sql-utils/actions/workflows/node.js.yml)
[![Coverage Status](https://coveralls.io/repos/github/toshihikojs/sql-utils/badge.svg?branch=master)](https://coveralls.io/github/toshihikojs/sql-utils?branch=master)

SQL string utils for Toshihiko.js.

## Description

This package provides utilities for processing SQL strings, including mapping SQL column names to new names using a provided map.

## Installation

To install this package, run:

```bash
npm install --save @toshihiko/sql-utils
```

## Usage

### Mapping SQL Column Names

You can use the `sqlNameToColumn` function to map SQL column names to new names using a provided map. Here is an example:

```typescript
import { sqlNameToColumn } from '@toshihiko/sql-utils';

const sql = 'SELECT aa FROM b WHERE cc = dd';
const map = {
  aa: 'a',
  cc: 'c',
  dd: 'd',
};

const newSql = sqlNameToColumn(sql, map);
console.log(newSql); // Output: SELECT a FROM b WHERE c = d
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
