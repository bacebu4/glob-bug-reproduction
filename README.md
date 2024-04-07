# Reproduction of the Glob misbehavior

1. Run the tests using script and node version `v21.7.2`

```bash
./test.sh
```

Only `far.e2e.js` is being run

2. Delete `far.e2e.js`

3. Run tests again

Now as a result `bar.e2.js` and `tar.e2e.js` are being run.

# Expected behavior

All tests are being run without deletion
