# Reproduction of the Glob misbehavior

1. Run the tests using script and node version `v21.7.2`

```bash
./test.sh
```

Only `far.e2e.js` is being run

2. Delete `far.e2e.js`

3. Run tests again

```bash
./test.sh
```

Now as a result `bar.e2.js` and `tar.e2e.js` are being run.

# Expected behavior

All tests are being run without deletion

# Node@20

In node@v20.12.1 in the third step nothing happens and I see the following log in the terminal

```
Could not find '/Users/bacebu4/dev/test-runner-test/src/**/*.e2e.js'
```
