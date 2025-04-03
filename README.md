# pypi-search-rez-filter-browser-plugin

A Firefox and Chrome browser plugin that hides seemingly unmaintained PyPI packages from search results.

Searching for Python packages on [PyPI.org](https://pypi.org) can be frustrating as many packages aren't maintained. This browser plugin hides packages in the search result with a "(Hidden by PyPI Search Rez Filter browser plugin)" link. Clicking the link will show the original search result, so it's easy to undo this plugin's hiding feature.

Packages are hidden if:

1. Their description is less than 200 characters.
1. It never had a release 30 days or more after it's very first release.

Brand new packages (currently meaning released after 2025-02-28) are never hidden.

<img src="https://raw.githubusercontent.com/asweigart/pypi-search-rez-filter-browser-plugin/refs/heads/main/screenshot-rez-filter.png">

If your PyPI package doesn't meet these requirements but you feel it should be on the allow list anyway, contact [al@inventwithpython.com](mailto:al@inventwithpython.com).

This data was scrapped from PyPI and formed into a 3.5 MB allow list of 209,949 package names. This list will be updated every few months.

## Install on Firefox

This browser plugin is not yet listed in the Firefox Add-ons site. Here is how to manually install it once you've downloaded the files in this repo:

1. In Firefox's address bar, go to `about:debugging`
1. Click "This Firefox" in the left sidebar.
1. Click "Load Temporary Add-on..."
1. Navigate to the folder with the plugin files, and select the `manifest.json` file.

Note that temporary extensions are removed when you restart Firefox.

## Install on Chrome

This browser plugin is not yet listed in the Chrome Extensions site. Here is how to manuallu install it once you've downloaded the files in this repo:

1. In Chrome's address bar, go to `chrome://extensions/`
1. Enable the "Developer Mode" slide toggle in the top right.
1. Click "Load unpacked"
1. Navigate to the folder with the plugin files, and select that folder.

## About the Filtered Packages

The PyPI Search Rez Filter plugin makes no claims of quality or judgements about individual packages. There are mature, high-quality packages from reputable developers that may get filtered because of the metrics the plugin uses. Being filtered is not a guarantee of low-quality, nor is not being filtered an indicator of reliability. These are rough metrics for users of this optional browser plugin. If you want your package to be added to the allow list in the next plugin release, either send me an email [al@inventwithpython.com](mailto:al@inventwithpython.com) or publish a new release of your package with a description greater than 200 characters.
