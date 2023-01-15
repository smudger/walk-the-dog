<h1 align="center">Walk The Dog</h1>

<div align="center">

<a href="https://github.com/smudger/walk-the-dog/actions/workflows/build.yml">![Build & Release](https://github.com/smudger/walk-the-dog/actions/workflows/build.yml/badge.svg?branch=main)</a>
<a href="https://app.netlify.com/sites/walk-the-dog-smudger/deploys">![Netlify Status](https://api.netlify.com/api/v1/badges/7135287c-8807-4aed-b528-78a8822573e5/deploy-status)</a>
<a href="https://badge.fury.io/js/@smudger%2Fwalk-the-dog">![npm version](https://badge.fury.io/js/@smudger%2Fwalk-the-dog.svg)</a>

</div>

___

An endless runner about a boy walking his dog. The game from the Rust Games with WebAssembly book.

## Getting Started

```sh
npm install

# Builds the project and opens it in a new browser tab. Auto-reloads when the project changes.
npm run start
```

## Testing

```sh
# Run unit tests
cargo test

# Run integration tests
wasm-pack test --headless --firefox

# Run all tests
npm run test
```

## Releasing

1. Ensure `package.json` version is correct.

2. Create a tag with the desired version. This should match whatever is in `package.json`.
```sh
# e.g. git tag v0.3.2-alpha
git tag <version>
```

3. Push tag to GitHub repo. This will trigger a release to be created and the package to be released to the [NPM registry](https://npmjs.com).
```sh
# e.g. git push origin v0.3.2-alpha
git push origin <version>
```

4. Ensure the release notes are correct on the [GitHub repo](https://github.com/smudger/walk-the-dog/releases).

## Troubleshooting

If you are struggling to run the integration tests and use Firefox Developer Edition, you will need to add Firefox Developer Edition's firefox-bin to the path by running the following command.

```sh
export PATH="$PATH:/Applications/Firefox Developer Edition.app/Contents/MacOS"
```

This ensures that geckodriver is able to find a valid Firefox binary to use to run the tests.
