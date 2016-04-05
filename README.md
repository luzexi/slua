#slua 3rd library.
Fastest Unity lua binding via static code generating.

Introduction slua [Document](slua_README.md)

###What's different
This fork integrate with 3rd Lua library.

We already have pbc , lpeg , cjson , lua-socket , sproto , sqlite librarys and more and more in the future.

The library is already been test in Mac , Iphone , Android , Windows.

Website: http://www.luzexi.com

Email: jesse_luzexi@163.com

[中文请看](http://www.luzexi.com/unity3d/%E6%B8%B8%E6%88%8F%E9%80%9A%E7%94%A8%E6%A8%A1%E5%9D%97/%E5%89%8D%E7%AB%AF%E6%8A%80%E6%9C%AF/2015/09/26/Unity3D%E4%B9%8Bslua%E9%9B%86%E6%88%90%E7%AC%AC%E4%B8%89%E6%96%B9%E5%BA%93.html)

###MinGW for windows build
MinGW , a contraction of "Minimalist GNU for Windows", is a minimalist development environment for native Microsoft Windows applications.

MinGW be a submodule in this repo and about 300 MB , If you have to build dll in windows you must init and update the submodule like : git submoudle update --init.

###About 3rd library
1.pbc (https://github.com/cloudwu/pbc) is a google protocol buffers library for C without code generation.

2.lpeg (http://www.inf.puc-rio.br/~roberto/lpeg/lpeg.html) is a new pattern-matching library for Lua, based on Parsing Expression Grammars (PEGs).

3.lua-cjson (http://www.kyne.com.au/~mark/software/lua-cjson.php) provides JSON support for Lua.

4.lua-socket (http://w3.impa.br/~diego/software/luasocket/home.html) is a Lua extension library that is composed by two parts: a C core that provides support for the TCP and UDP transport layers, and a set of Lua modules that add support for functionality commonly needed by applications that deal with the Internet.

5.sproto (https://github.com/cloudwu/sproto) is an efficient serialization library for C, and focuses on lua binding. It's like Google protocol buffers, but much faster.

6.sqlite (https://github.com/LuaDist/lsqlite3) is a software library that implements a self-contained, serverless, zero-configuration, transactional SQL database engine. 

##How to use slua in unity3d.
See inner demo for help or [Document](https://github.com/pangweiwei/slua/wiki/%E4%B8%AD%E6%96%87%E5%B8%AE%E5%8A%A9) (in chinese).

##How to use 3rd library in unity3d.
See inner demo for help.

* pbc example
> The path of pbc example is Assets/Slua/example/example-pbc/protoTest.unity.
> 
> To integrate pbc I add ByteArray class in slua. It works when you use byte[] between c# and Lua.

* lua-cjson example
> The path of lua-cjson example is Assets/Slua/example/example-cjson/cjson_test.unity.
> 
> Test scripts include cjson_test.cs , cjsonTest.txt , cjsonTest/test1.txt.

* lua-socket example
> The path of lua-socket example is Assets/Slua/example/example-luasocket/lua_socket.unity.
> 
> The test scripts is 'testclnt.txt'. The test file copy from lua-scoket. If you wana test, you need to run the 'luasrvr.lua' from the lua-scoket's test folder.

* sproto example
> The path of sproto example is Assets/Slua/example/example-sproto/sproto-test.unity.
> 
> The test contain 3 files sprotoTest/test.txt , sprotoTest/testall.txt , sprotoTest/pbc.txt , all of these files from sproto project.

* sqlite example
> The path of sproto example is Assets/Slua/example/example-sqlite/sqlite-test.unity.
> 
> The test contain 2 files sqliteTest/test.txt , sqliteTest/tests-sqlite3.txt , all of them from lsqlite project.


###How to build library by yourself.
It has sevral shell or bat in the build folder. If you have to choose some of theirs , you can modify the build scripts by yourself. It's simple I think if you really want.

The shell or bat in the build folder can build the library for specially platform:

1.make_ios.sh will build iphone library in osx.

2.make_osx.sh will build osx library in osx.

3.make_android.sh will build android library. You can execute it in osx or linux. But first , please reset the ndk path in the shell.

4.make-windows-32.cmd will build windows 32bit dll in windows 32-bit or 64-bit.

5.make-windows-64.cmd will build windows 64bit dll in windows 64-bit.


###TODO
1.Add lua-cjson library in slua. ( Finished )

2.Add lua-socket library in slua. ( Finished )

3.Merge slua v1.x  ( Finished )

4.Add sproto library in slua. ( Finished )

5.Add sqlite library in slua. ( Finished )

6.Add Int64 in slua.

7.Add curl library in slua.
