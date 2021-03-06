# jest-with-esmodules-example

jest で ESModules の import/export する例

[ここ](https://sbfl.net/blog/2019/01/20/javascript-unittest/)を写経

# jest 導入
```
$ npm init
$ npm install --save-dev jest babel-jest babel-core @babel/core @babel/preset-env
$ npm install --save-dev @babel/plugin-transform-modules-commonjs
```

# フォルダ構成
```
.
|-- README.md
|-- __tests__
|   `-- mylib.test.js
|-- mylib.js
|-- package-lock.json
`-- package.json
```

# テスト実施
```
$ npx jest
 PASS  __tests__/mylib.test.js
  ✓ add 1 + 2 (2 ms)

Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   0 total
Time:        0.736 s, estimated 1 s
Ran all test suites.
```

# カバレッジ表示
```
$ npx jest --coverage
 PASS  __tests__/mylib.test.js
  ✓ add 1 + 2 (3 ms)

----------|---------|----------|---------|---------|-------------------
File      | % Stmts | % Branch | % Funcs | % Lines | Uncovered Line #s
----------|---------|----------|---------|---------|-------------------
All files |     100 |      100 |     100 |     100 |
 mylib.js |     100 |      100 |     100 |     100 |
----------|---------|----------|---------|---------|-------------------
Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   0 total
Time:        0.873 s, estimated 1 s
Ran all test suites.
```
