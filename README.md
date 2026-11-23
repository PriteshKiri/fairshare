# Fairshare

Fairshare splits a shared trip bill to the cent and prints who should pay whom. The CI pipeline installs dependencies, lints the source, and runs the test suite.

```bash
npm ci
npm run lint
npm test
node src/cli.js examples/weekend-trip.json
```

`npm test` writes JUnit results to `junit.xml` so Harness can show them on the build.

Each expense names who paid, the dollar amount, and who shares the cost. The splitter turns dollars into cents, divides leftover cents fairly, and prints the fewest payments that bring the group back to zero.
