# Live-Down

Live-Down allows you to edit a Markdown file in your preferred editor and
have an in browser preview stay in sync every time you update. No more reloads,
no need to use a <textarea> to compose your file, do things your way.

Live-Down uses [Guard](https://github.com/guard/guard) along with
[Guard-Markdown](https://github.com/darwalenator/guard-markdown) and
[Guard-Livereload](https://github.com/guard/guard-livereload) in order to
render the markdown and push updates to the browser.

In addition, you will need the LiveReload [Chrome extension](https://chrome.google.com/webstore/detail/jnihajbhpnppcggbcgedagnkighmdlei), [Firefox addon](https://addons.mozilla.org/en-US/firefox/addon/livereload/), or the [Safari extension](http://help.livereload.com/kb/general-use/browser-extensions).

## Installation

git clone https://github.com/christoomey/live-down.git

## Usage

In order to use **live-down**, symlink the desired markdown file into the
src directory of the live-down repo, then fire up `guard` to render the
markdown into html on save, and to push changes to the browser.

``` shell
guard
# In alternate shell / tab
cd public ln -s <path_to_orig>/file.md ./
```

## LiveReload For File Protocol

In some cases your browser may prevent live reloading of files. In this case
you can either run a local file server or configure your browser / extension
to allow reloading of file extensions.

If you want to go the server route and you have python installed (there by
default on OS X), then it is as simple as running

``` python
python -m SimpleHTTPServer 8000
```
