# Reproduction of the Glob misbehavior

1. Run the tests using script

```bash
./test.sh
```

Only `src/usecases/tar.e2e.js` will be executed

2. Move `src/usecases/tar.e2e.js` to `src/usecases/far/tar/tar.e2e.js`

```bash
mv ./src/usecases/tar.e2e.js ./src/usecases/far/tar
```

3. Run tests again using script

```bash
./test.sh
```

As a result all test files (`bar.e2e.js`, `tar.e2e.js`, `far.e2e.js`) will be executed

# Expected behavior

In the step `1.` all tests should be executed (`bar.e2e.js`, `tar.e2e.js`, `far.e2e.js`)

## Side note

If we move `tar.e2e.js` to to the `src` folder then all tests will run as well, e.g.

```bash
mv ./src/usecases/tar.e2e.js ./src/tar
```
