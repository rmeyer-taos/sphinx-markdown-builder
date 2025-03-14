# sphinx-markdown-builder

[![PyPI](https://img.shields.io/pypi/v/sphinx-markdown-builder.svg?style=flat-square)](https://pypi.org/project/sphinx-markdown-builder)
[![PyPI - Downloads](https://img.shields.io/pypi/dm/sphinx-markdown-builder.svg?style=flat-square)](https://pypi.org/project/sphinx-markdown-builder)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/sphinx-markdown-builder.svg?style=flat-square)](https://pypi.org/project/sphinx-markdown-builder)
[![GitHub stars](https://img.shields.io/github/stars/codejamninja/sphinx-markdown-builder.svg?style=flat-square&label=Stars)](https://github.com/codejamninja/sphinx-markdown-builder)
[![Liberapay receiving](https://img.shields.io/liberapay/receives/codejamninja.svg?style=flat-square)](https://liberapay.com/codejamninja/donate)
[![Liberapay patrons](https://img.shields.io/liberapay/patrons/codejamninja.svg?style=flat-square)](https://liberapay.com/codejamninja/donate)

> sphinx builder that outputs markdown files

Please ★ this repo if you found it useful ★ ★ ★

If you want frontmatter support please use [sphinx-jekyll-builder](https://github.com/codejamninja/sphinx-jekyll-builder)


## Features

* Generates markdown


## Installation

```sh
pip3 install sphinx-markdown-builder
```


## Dependencies

* [Python 3](https://www.python.org)


## Usage

Load extension in configuration.

#### Sphinx >= 1.8
_conf.py_
```py
from sphinx_markdown_parser.markdown_builder import MarkdownBuilder

source_suffix = {
    '.rst': 'restructuredtext',
    '.md': 'markdown'
}

def setup(app):
    app.add_source_suffix('.md', 'markdown')
    app.add_source_parser(MarkdownParser)
```

#### Sphinx < 1.8
_conf.py_
```py
from sphinx_markdown_parser.markdown_builder import MarkdownBuilder

source_suffix = ['.rst', '.md']

source_parsers = {
    '.md': MarkdownBuilder
}
```

If using [recommonmark](https://github.com/rtfd/recommonmark), make sure you
explicitly ignore the build files as they will conflict with the system.

_conf.py_
```py
exclude_patterns = [
    'build/*'
]
```

Build markdown files with Makefile

```sh
make markdown
```

Build markdown files with `sphinx-build` command

```sh
cd docs
sphinx-build -M markdown ./ build
```


## Support

Submit an [issue](https://github.com/codejamninja/sphinx-markdown-builder/issues/new)


## Screenshots

[Contribute](https://github.com/codejamninja/sphinx-markdown-builder/blob/master/CONTRIBUTING.md) a screenshot


## Contributing

Review the [guidelines for contributing](https://github.com/codejamninja/sphinx-markdown-builder/blob/master/CONTRIBUTING.md)


## License

[MIT License](https://github.com/codejamninja/sphinx-markdown-builder/blob/master/LICENSE)

[Jam Risser](https://codejam.ninja) © 2018


## Changelog

Review the [changelog](https://github.com/codejamninja/sphinx-markdown-builder/blob/master/CHANGELOG.md)


## Credits

* [Jam Risser](https://codejam.ninja) - Author
* [Matthew Brett](https://github.com/matthew-brett/nb2plots/blob/master/nb2plots/doctree2md.py) - doctree2md


## Support on Liberapay

A ridiculous amount of coffee ☕ ☕ ☕ was consumed in the process of building this project.

[Add some fuel](https://liberapay.com/codejamninja/donate) if you'd like to keep me going!

[![Liberapay receiving](https://img.shields.io/liberapay/receives/codejamninja.svg?style=flat-square)](https://liberapay.com/codejamninja/donate)
[![Liberapay patrons](https://img.shields.io/liberapay/patrons/codejamninja.svg?style=flat-square)](https://liberapay.com/codejamninja/donate)
