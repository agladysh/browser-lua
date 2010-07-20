Browser-Lua: Run Lua in Browser
===============================

About
-----

Browser-Lua project is an abstract wrapper to several alternative backends
that allow to run Lua code in browser.

Browser-Lua allows user to call Lua code from JS and JS code from Lua.

Browser-Lua is still in its embryonic phase of development.
More detailed description would be added later.

See the copyright information in the file named `COPYRIGHT`.

Supported backends
------------------

(None so far)

Planned backends
----------------

 * lua-alchemy (http://code.google.com/p/lua-alchemy)
 * js-lua (http://github.com/agladysh/js-lua)
 * ljs (http://code.matthewwild.co.uk/ljs)

API v1.0
--------

(To be implemented)

### JS

 * `BrowserLua.init([enabled_backends])`

 * `BrowserLua.dostring(lua_code, [chunkname])`

 * `BrowserLua.provideFile(path, file_contents_string)`

 * `BrowserLua.doFile(path)`

### Lua

 * `BrowserLua.runJS(js_code_string)`

 * `BrowserLua.dofile(filename)`

 * `BrowserLua.loadfile(filename, chunkname)`

 * `BrowserLua.initWrapper()`

  Does the equivalent of this:

    getenv().dofile = BrowserLua.dofile
    getenv().loadfile = BrowserLua.loadfile

API v2.0
--------

(To be implemented)

### JS

 * `result = BrowserLua.lua.<lua-global-name>(args, ...)`

### Lua

 * `result = BrowserLua.js.<js-global-name>(args, ...)`
