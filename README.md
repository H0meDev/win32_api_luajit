win32_api_luajit
================

Tracking of Cosmin's win32 api for luajit (with adjustments)

https://code.google.com/p/lua-files/wiki/winapi

Instructions for building a version of luajit with the library linked in:

1)Checkout files to the luajit src directory.

1.5)Ensure that luajit.exe is there.

2)Run build.bat

3)Rebuild luajit, but make sure that msvcbuild.bat doesn't delete the luajit.obj file.

4)Link .o files to lua executable, ala:

    link.exe /out:luajit.exe luajit.obj lua51.lib winapi_*.o glue.o stddef_h.o systypes_h.o unit.o


5)Run luajit.exe test.lua


Here is the screenshot of running luajit.exe test2.lua, which uses the HTMLayout control.

<img src=https://github.com/rmbishop/win32_api_luajit/shot1.png>
