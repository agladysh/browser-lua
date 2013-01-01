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
 * nacl (http://code.google.com/p/nativeclient/)
 * emscripten (http://code.google.com/p/emscripten/)
 * jill (http://code.google.com/p/jillcode/), as Java applet (with some js-lua-like wrapper)
 * lua.js (https://github.com/mherkender/lua.js)
 * brozula (https://github.com/creationix/brozula)

API v1.0
--------

(To be implemented)

### JS

 * `BrowserLua.init([enabled_backends])`

 * `BrowserLua.doString(lua_code, [chunkname])`

 * `BrowserLua.callLua(functionName, args, ...) --> array of return values`

 * `BrowserLua.provideFile(path, file_contents_string)`

 * `BrowserLua.doFile(path)`

### Lua

 * `BrowserLua.callJS(functionName, args, ...) --> return value`

 * `BrowserLua.dofile(filename)`

 * `BrowserLua.loadfile(filename, chunkname)`

 * `BrowserLua.initWrapper()`

  Does the equivalent of this:

    getenv().dofile = BrowserLua.dofile
    getenv().loadfile = BrowserLua.loadfile

API v2.0
--------

(To be designed and implemented)

 * Data manipulation API just like lua-alchemy sugar.
  * For JS (to manipulate Lua data)
  * For Lua (to manipulate JS data)
 * Modules, native to backend
 * socket module (imitating luasocket.*)
