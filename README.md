﻿# Learn Coding with Open Source

[![Join the chat at https://gitter.im/zhuangbiaowei/learn-with-open-source](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/zhuangbiaowei/learn-with-open-source?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![GitHub stars](https://img.shields.io/github/stars/zhuangbiaowei/learn-with-open-source.svg?label=github%20stars)](https://github.com/zhuangbiaowei/learn-with-open-source)
[![Powered by Gitbook](https://img.shields.io/badge/Powered%20by-Gitbook-blue)](https://www.gitbook.com)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Actions Status](https://github.com/zhuangbiaowei/learn-with-open-source/workflows/Build%20learn-with-open-source%20PDF/badge.svg)](https://github.com/zhuangbiaowei/learn-with-open-source/actions)

This book uses [GitBook](https://www.gitbook.com) to build.

License: CC BY-NC-SA 4.0

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />All contents licensed under the <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"> Creative Commons Attribution Non Commercial Share Alike 4.0 license</a>.

Welcome! Join us to finish this book.

You can visit the online ebook: [Learn Coding With Open Source](https://zhuangbiaowei.gitbook.io/learn-with-open-source/)

You can also get the PDF on the release page.

##  for developers

### Build the book
Note: you will need Linux or MacOS. Windows is not yet supported.

1. install [node.js](https://nodejs.org)
2. install [ebook-convert from calibre](http://calibre-ebook.com/download)
  * for pdf,epub etc ebook generation.
  * go Calibre > Misc > Install Command Line Tool after installed
    * or ln -s /Applications/calibre.app/Contents/MacOS/ebook-convert /usr/local/bin
3. enter the git repository directory

    ```bash
    cd learn-with-open-source
    npm install
    ```
4. generate the ebook via:
   1. generate html pages:

    ```bash
    ./node_modules/.bin/gitbook build . _book
    ```
   2. run a local server to read html:

    ```bash
    ./node_modules/.bin/gitbook serve .
    ```
   3. generate the pdf:

    ```bash
    ./node_modules/.bin/gitbook pdf .
    ```

### Update contributions automatically

It will update contributions through git commits after a pull request or merge is executed.
If you want to update it manually:

This script will update the "Contributor.md" file and copy it to the "zh" folder.

```bash
cd learn-with-open-source
./.githooks/post-merge/update-contributors

```

The contributors configuration file is the ".contributors" file
on the root of the repository.

### Update TOC automatically

TODO: this is not finished.

The gitbook uses the SUMMARY.md to get the TOC.
The list in the SUMMARY.md will be the TOC.

```
1. [Topic](topic.md)
  1. [SubTopic](subtopic.md)
    1. TheSameFileTopicNoLinkAllowed
    1. TheSameFileTopicNoLinkAllowed
1. [Topic2]
```

**note:**

* the parent directory is not supported via gitbook.
* the topic in the same file could not be a link.

the workflow automation is:

* a text file to determine the markdown files order,
  or use the file name order in a directory.
* get toc of each markdown file.
* merge it into SUMMARY.md

---------
dsadasdsadsad
