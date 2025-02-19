# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [6.0.2] - 2022-08-03

- Upgrade junit-report-builder to fix a deprecation warning when installing the package.

## [6.0.1] - 2022-07-23

- Fix an issue where the tool crashes if installed globally.

## [6.0.0] - 2022-07-23

- Use `pkg-dir` instead of `app-root-path` to find a Spellchecker CLI config file. `pkg-dir` looks for the root directory of a Node.js project by searching up from the current working directory for a directory containing a `package.json` file. This is simpler than `app-root-path`'s strategy.

## [5.0.1] - 2022-07-21

- Rebuild package with LF line endings instead of CRLF.

## [5.0.0] - 2022-07-15

- Spellchecker now uses ES modules instead of CommonJS modules. This means that the tool will fail to import personal dictionaries from `.js` files that use CommonJS module syntax. To fix this, change the personal dictionary file's extension from `.js` to `.cjs`.
- Fix an issue where the `:gear:` Gemoji would show up as a spelling mistake.

## [4.11.0] - 2022-05-21

- Allow specifying a path to write the generated dictionary to.

## [4.10.1] - 2022-05-16

- Rebuild package with LF line endings instead of CRLF.

## [4.10.0] - 2022-04-23

- Add built-in dictionaries for Next.js and React.

## [4.9.1] - 2022-03-30

- Upgrade dependencies.

## [4.9.0] - 2022-03-30

- Add support for MDX files([@davemooreuws](https://github.com/davemooreuws)).

## [4.8.1] - 2021-10-31

Happy Halloween!

- Fix a bug where the tool wouldn't respect the `--plugins` command line option or the `plugins` key in config files.

## [4.8.0] - 2021-06-13

- Convert project to TypeScript.

## [4.7.0] - 2021-06-12

- Add support for JSON and JSONC configuration files ([@gadhagod](https://github.com/gadhagod)).

## [4.6.0] - 2021-06-10

- Added support for reading configuration from a YAML file.

## [4.5.0] - 2021-06-04

- Add Vietnamese support
- Use Yarn for package management

## [4.4.1] - 2021-05-22

### Fixed

- Fixed a bug where the tool would print output in quiet mode, even if it found no errors.
- Upgraded dependencies.

## [4.4.0] - 2020-06-06

### Added

- Added support for inline HTML comments `spellchecker-enable/spellchecker-disable` to exclude blocks from spellchecking (@xoxys).

## [4.3.0] - 2020-05-30

### Added

- Added support for TOML frontmatter (@bryanfriedman)

## [4.2.0] - 2020-04-02

### Added

- Added flag to allow spellchecking of files that are ignored by git.

## [4.1.1] - 2020-03-15

### Fixed

- Upgraded packages that contained security vulnerabilities.

## [4.1.0] - 2020-02-11

### Added

- Added functionality to output JSON and JUnit reports, for better integration with automation and CI/CD tools.

## [4.0.2] - 2020-01-15

### Fixed

- Upgraded several packages that contained security vulnerabilities

## [4.0.1] - 2018-11-09

### Fixed

- Fix spelling errors appearing on Unicode emoji variation selectors by removing these characters before spellchecking.

## [4.0.0] - 2018-07-29

### Added

- Add support for programmatic dictionaries.
- Add support for parsing and spellchecking frontmatter with the `frontmatter` plugin and `--frontmatter-keys` command-line option.

### Changed

- Allow specification of more than one file to combine into a personal dictionary.
- Treat plaintext dictionaries as lists of regexes.

## [3.1.0] - 2018-06-12

### Added

- Added a `--no-suggestions` option, which allows users to disable the generation of spelling suggestions when errors are detected.

## [3.0.3] - 2018-04-24

### Fixed

- Fixed a bug where the spell checking was skipped after 30 found misspell errors, even if they are matched by one of `--ignore` patterns.

## [3.0.2] - 2018-04-14

### Fixed

- Updated [`retext-indefinite-article`](https://github.com/retextjs/retext-indefinite-article) to 1.1.3 in order to properly expect "a" in front of words like "1-to-1" and "1:00".
- Added a `--ignore` option. This option takes a list of regexes. Spelling mistakes that match any of the regexes, after wrapping each regex in `^` and `$`, will be ignored.

## [3.0.1] - 2017-12-30

### Fixed

- Fixed a bug where messages of type `overflow` generated by `retext-spell` were included in the generated dictionary, causing "undefined" to be added to the end of the dictionary.

## [3.0.0] - 2017-12-29

### Added

- Log a count of the files to be spellchecked.
- Add a large number of unit and end-to-end tests.
- Add development instructions to [README.md](./README.md).
- Add support for the following [retext](https://github.com/retextjs/retext) plugins:
  - [`retext-indefinite-article`](https://github.com/retextjs/retext-indefinite-article)
  - [`retext-repeated-words`](https://github.com/retextjs/retext-repeated-words)
  - [`retext-syntax-mentions`](https://github.com/retextjs/retext-syntax-mentions)
  - [`retext-syntax-urls`](https://github.com/retextjs/retext-syntax-urls)
- Apply all of the above plugins, as well as [`retext-spell`](https://github.com/retextjs/retext-spell), by default.
- Add a newline to the end of the generated dictionary.

## [2.0.0] - 2017-12-28

### Changed

- Skip checking the personal dictionary (if one is provided).

## [1.0.1] - 2017-12-28

### Fixed

- Added a shebang to [index.js](./index.js).

[unreleased]: https://github.com/tbroadley/spellchecker-cli/compare/v6.0.1...HEAD
[6.0.2]: https://github.com/tbroadley/spellchecker-cli/compare/v6.0.1...v6.0.2
[6.0.1]: https://github.com/tbroadley/spellchecker-cli/compare/v6.0.0...v6.0.1
[6.0.0]: https://github.com/tbroadley/spellchecker-cli/compare/v5.0.1...v6.0.0
[5.0.1]: https://github.com/tbroadley/spellchecker-cli/compare/v5.0.0...v5.0.1
[5.0.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.11.0...v5.0.0
[4.11.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.10.1...v4.11.0
[4.10.1]: https://github.com/tbroadley/spellchecker-cli/compare/v4.10.0...v4.10.1
[4.10.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.9.1...v4.10.0
[4.9.1]: https://github.com/tbroadley/spellchecker-cli/compare/v4.9.0...v4.9.1
[4.9.1]: https://github.com/tbroadley/spellchecker-cli/compare/v4.9.0...v4.9.1
[4.9.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.8.1...v4.9.0
[4.8.1]: https://github.com/tbroadley/spellchecker-cli/compare/v4.8.0...v4.8.1
[4.8.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.7.0...v4.8.0
[4.7.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.6.0...v4.7.0
[4.6.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.5.0...v4.6.0
[4.5.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.4.1...v4.5.0
[4.4.1]: https://github.com/tbroadley/spellchecker-cli/compare/v4.4.0...v4.4.1
[4.4.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.3.0...v4.4.0
[4.3.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.2.0...v4.3.0
[4.2.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.1.1...v4.2.0
[4.1.1]: https://github.com/tbroadley/spellchecker-cli/compare/v4.1.0...v4.1.1
[4.1.0]: https://github.com/tbroadley/spellchecker-cli/compare/v4.0.2...v4.1.0
[4.0.2]: https://github.com/tbroadley/spellchecker-cli/compare/v4.0.1...v4.0.2
[4.0.1]: https://github.com/tbroadley/spellchecker-cli/compare/v4.0.0...v4.0.1
[4.0.0]: https://github.com/tbroadley/spellchecker-cli/compare/v3.1.0...v4.0.0
[3.1.0]: https://github.com/tbroadley/spellchecker-cli/compare/v3.0.3...v3.1.0
[3.0.3]: https://github.com/tbroadley/spellchecker-cli/compare/v3.0.2...v3.0.3
[3.0.2]: https://github.com/tbroadley/spellchecker-cli/compare/v3.0.1...v3.0.2
[3.0.1]: https://github.com/tbroadley/spellchecker-cli/compare/v3.0.0...v3.0.1
[3.0.0]: https://github.com/tbroadley/spellchecker-cli/compare/v2.0.0...v3.0.0
[2.0.0]: https://github.com/tbroadley/spellchecker-cli/compare/v1.0.1...v2.0.0
[1.0.1]: https://github.com/tbroadley/spellchecker-cli/compare/v1.0.0...v1.0.1
