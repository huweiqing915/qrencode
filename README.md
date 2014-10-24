# qrencode: qrencode is a wrapper of libqrencode with libpng for lua.

qrencode is a wrapper of [libqrencode](http://fukuchi.org/works/qrencode/) with libpng for lua.

## Install

qrencode is dependent on [libqrencode](http://fukuchi.org/works/qrencode/) 
and [libpng](http://www.libpng.org/pub/png/libpng.html), so make sure these are installed
before compile it.

## Example usage

```lua
qr = require "qrencode"

-- print PNG data stream to stdout.

-- print(qr.encode("is ok?"))
-- or pass a table :
print(qr.encode(
{
    text="is ok?",
    level="L",
    kanji=false,
    size=3,
    symversion=0,
    dpi=80,
    casesensitive=true,
    eightbit=false,
    foreground="#48AF6D",
    background="#3FAF6F"
}
)
)

```

when pass a table, "text" is required and other is optional.

## Author

vinoca <http://www.vinoca.org/>

## Copyright and license

Code and documentation copyright 2014-2015 vinoca. Code released under the MIT license.
Docs released under Creative commons.