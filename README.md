# Fisherman Index

The Fisherman Index is a plain text flat database externally managed and independent from [Fisherman][fisherman].

A copy of the index is downloaded each time Fisherman queries the INDEX file. This keeps the index up to date and allows the database to be searched offline.

The index lists records, each consisting of the following fields:

* *name*, *url*, *info*, *author* and one or more *tags*.

Fields are separated by a new line **\n**. Tags are separated by one space. Here is a sample record:

```
shark
https://github.com/bucaran/shark
Sparklines for your Fish
graph spark data
bucaran
```

To submit a new plugin for registration install the [submit][fisher-submit] plugin:

```
fisher install submit
```

For usage see the bundled documentation `fisher help submit`.

You can also submit a new plugin manually and create a pull request.

```fish
git clone https://github.com/fisherman/fisher-index
cd index
echo "$name\n$url\n$info\n$author\n$tags\n\n" >> index
git push origin master
open http://github.com
```

## Disclaimer

All the plugins listed are property of their respective owners. Follow the provided URL and see the bundled LICENSE or COPYING file for copyright information.

<!-- Links -->

[fisherman]: https://github.com/fisherman/fisherman

[fisher-submit]: https://github.com/bucaran/fisher-submit
