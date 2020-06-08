# commitver

Derive a [semver](https://semver.org) version from the commit history in any repo.

## Installation

Copy the `commitver` script anywhere in your path and ensure it is executable by running `chmod +x commitver`.

## Usage

Run the `commitver` script from any git repo. e.g.

```
$ cd repos/my-git-repo
$ commitver
1.0.2
```

Commits to the repo automatically increment the `patch` release version. If you add `[major]` or `[minor]` to a commit message in the repo, the corresponding version will be bumped instead.

You can override the current version at any time (e.g. to `1.2.3`) by adding a `.commitver.yaml` file to the root of your repo. Any subsequent commits will continue to increment, starting from the version number in the file. `.commitver.yaml` should have the following contents:

```yaml
version-at-commit: 1.2.3
```

## Committers

 * Nathan Essex ([@Nessex](https://github.com/Nessex))

## Contribution

Please read the CLA below carefully before submitting your contribution.

https://www.mercari.com/cla/

## License

Copyright 2020 Mercari, Inc.

Licensed under the MIT License.
