# Development Notes

## Initial setup

```shell
$ git clone git@github.com:SkygearIO/skycli.git
$ cd skycli
$ npm install
$ npm link
```

Verify the initial setup by running `skycli`.

```shell
$ skycli version
```

## Build source

This command will watch the source directory for changes and automatically
update the built files.

```shell
$ npm start
```

Alternatively, you can run `npm run skycli` to build source and then run
`skycli`.

## Options for development

The command line interface has a developer mode that shows additional
information when running `skycli help`. This can be achieved by running
the program with `SKYCLI_DEVELOPER_MODE` environment variable set to `1`.

```shell
$ SKYCLI_DEVELOPER_MODE=1 skycli help
```

You can also run `skycli` with debug option to print debug information.

```shell
$ skycli --debug help
$ SKYCLI_DEBUG=true skycli help  # Alternative usage
```

## Publish

Bump version number to next version:

```shell
$ npm version minor  # 0.1.0 > 0.2.0
$ npm version patch  # 0.1.0 > 0.1.1
```

Publish to npm. This will also create a pull request on SkygearIO/homebrew-tap.

```shell
$ npm publish
```

Accepted the pull request to update homebrew tap.
